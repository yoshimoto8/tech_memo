## インストールしたパッケージに新しいバージョンが存在するかどうか、確認する。コマンド

```
$ npm outdated
```

[参照](https://dackdive.hateblo.jp/entry/2016/10/10/095800)

## npm-check-updates を使う

#### versionを調べる

`ncu`でバージョンの一覧を見ることができる

```
 ncu
```
#### package.jsonのversionsをすべて最新にする

-u でpackage.jsonのパッケージを一括あげる

```
ncu -u
```

#### パッケージを選択する

１つ選択してバージョンをあげることが可能。

```
ncu -u [パッケージ名]
```