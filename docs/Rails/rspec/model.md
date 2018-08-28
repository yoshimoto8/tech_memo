# モデルスペック

```ruby
describe Contact do
# 姓と名とメールがあれば有効な状態であること
it "is valid with a firstname, lastname and email" # 名がなければ無効な状態であること
it "is invalid without a firstname"
# 姓がなければ無効な状態であること
it "is invalid without a lastname"
# メールアドレスがなければ無効な状態であること
it "is invalid without an email address"
# 重複したメールアドレスなら無効な状態であること
it "is invalid with a duplicate email address"
# 連絡先のフルネームを文字列として返すこと
it "returns a contact's full name as a string"
end
```

- describe: 期待する結果をまとめて記述する
このケースでは`Contact`がどんなモデルまたは、どんな振る舞いをするかを記述している。

- it: 結果を１つだけ記述している。
細かく分けることによって、もしエラーが発生した場合そこまで細かくみる必要がなくなる。


予測するときは`expect()`を使う。

```ruby
# 2 と 1 を足すと 3 になること it "adds 2 and 1 to make 3" do
expect(2 + 1).to eq 3 end
```

### モデルが有効かどうかを判断するテスト

```ruby
require'rails_helper'
describeContactdo
# 姓と名とメールがあれば有効な状態であること
it "is valid with a firstname, lastname and email" do
    contact = Contact.new(
      firstname: 'Aaron',
      lastname: 'Sumner',
      email: 'tester@example.com')
      expect(contact).to be_valid
end
```

`be_valid`を使ってモデルが有効かどうかを判断している。

## モデルテストに参考になりそうな記事

https://qiita.com/shizuma/items/c7b8d7b91e8f325f8ad9