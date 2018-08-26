# Viewを知りすぎたDecoratorクラス

ControllerからViewにModelを渡すような場面で、Viewで加工したり結合したりして使っている場合があると思います。デコレーターを使うことによって、その見せ方の責任をデコレータに任せることができます。

そうすることで見せ方を変更したい場合、デコレータークラスを変更するだけでよくなり保守性が上がります。またViewにロジックを書くようなことも抑えることができます。


ちなみにRailsで開発している場合 draper というGemを使うとDecoratorを簡単に実現できます。

[draper](https://github.com/drapergem/draper)

```ruby
class UserDecorator < Draper::Decorator
  delegate_all

  def fullname
    [object.sei, object.mei].join(' ')
  end
end

class UserController < ApplicationController
  def show
    @user = User.find(params[:id]).decorate
  end
end
```

```ruby
<%= @user.fullname %>
```

適切に利用すると、保守性をあげることができるのですが、デコレータをビューに依存させてしまうことがあります。開発者はビューで特定の表示がしたいときにデコレータを活用しようとします。なので、気をつけていないと、そのビューに依存しすぎた作りにしてしまうことがあります。

↓そのケース

```ruby
class UserDecorator < Draper::Decorator
  delegate_all

  def profile
    "#{object.sei} #{object.mei} (#{object.age}) <br /> #{object.company_name}"
  end
end

class UserController < ApplicationController
  def show
    @user = User.find(params[:id]).decorate
  end
end
```

```ruby
<%== @user.profile %>
```