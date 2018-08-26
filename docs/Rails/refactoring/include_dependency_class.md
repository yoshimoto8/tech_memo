# 依存を含んだクラス

疎結合なコードを書くためには可能な限り依存を少なくする、隔離する努力が必要

↓依存しまくっているケース

```ruby
class Image
  def create
    url = Amazon::S3::Uploader.new(image, name).upload
    Image.create({url: url, name: name})
  end

  def update
    url = Amazon::S3::Uploader.new(image, name).upload
    Image.find(id).update({url: url, name: name})
  end
end
```

上のコードはAmazon::S3::Uploaderクラス、Imageクラスに依存しています。UploadeするのをS3から別のクラウドストレージにする場合には複数の箇所を変更しなければならなくなります。２つとかならまだいいですが、その数が大きくなればなるほど変更が大きくなります。結局のところcreateでもupdateでもuploaderはuploadメソッドを持っていることを期待しているので以下のように変更することで、依存範囲を限定することができます。

↓依存を少なくしたコード

```ruby
class Image
  def create
    url = uploader.upload
    image.create({url: url, name: name})
  end

  def update
    url = uploader.upload
    image.update({url: url, name: name})
  end

  def uploader
    @uploader ||= Amazon::S3::Uploader.new(image, name)
  end

  def image
    @image ||= Image.find(id)
  end
end
```

↓さらにリファクタリングしたコード

```ruby
class Image
  def create
    url = upload
    image.create({url: url, name: name})
  end

  def update
    url = upload
    image.update({url: url, name: name})
  end

  def upload
    uploader.upload
  end

  def uploader
    @uploader ||= Amazon::S3::Uploader.new(image, name)
  end

  def image
    @image ||= Image.find(id)
  end
end
```

このように依存の範囲を限定することで、変更に対して修正箇所を少なくすることができます。

`（全てに対してこのようにすると見通しが悪くなることにもつながるので、そこら辺は臨機応変に）`

### 引数の順番に関する依存

```ruby
class Image
  def self.resize(image_path, output_path, x, y)
  end
end

Image.resize('./sample.png', './sample-2.png', 300, 400)
```

メッセージを送る側をパッと見て引数のうち何が何を表していることがわからないことです。

引数の順番が変わった時にそれを使っているところをすべて定義し直さないといけない。

そのような場合にはキーワード引数を使うことで回避することができます。

```ruby
class Image
  def self.resize(image_path:, output_path:, x:, y:)
  end
end

Image.resize(image_path: './sample.png', output_path: './sample-2.png', x: 300, y: 400)
```

## 参照

https://qiita.com/shunhikita/items/7fdb5d95c883e38c63fc