# 見通しが悪いコールバック

Viewに表示させたい情報が多くなってしまった時、コントローラのコールバックが増えがちになってしまうことがある。

```ruby
class UserController < ApplicationController
  before_action :load_user, only: [:show, :edit, :update, :destroy]
  before_action :load_users, only: [:index]
  before_action :load_roles, only: [:new, :edit]
  before_action :load_user_form, only: [:new, :create, :edit, :update]

  def show
    @recommendation_items = user.recommendation_items
    @cart_items = user.cart_items
    # ...
  end
end
```

管理できる数ならいいが、数が多くなってしまった場合コールバックをやめるタイミングかもしれない。

その時の対策として`ViewModel`クラスを作って対応するといいかもしれない。

```ruby
class UserController < ApplicationController
  def show
    @view_model = UserShowViewModel.new()
  end
end

class UserShowViewModel
  include Virtus.model

  attribute :user, Integer

  def recommendation_items
    @recommendation_items ||= user.recommendation_items
  end

  def cart_items
    @cart_items ||= user.cart_items
  end

end
```

このようにViewに渡すためのデータを管理するクラスを一つ作ることによって、そのクラスを見ればそのビューがどのようにデータを暑かつているかもわかりますし、Viewやcontrollerにロジックを書くことも防ぐことができる。



