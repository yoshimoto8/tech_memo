---
search:
  keywords: ["github", "commit", "etc."]
---

## 単語

| 単語                                                 | 意味                                                                                                       |
| ---------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| undesirable                                          | 好ましくない                                                                                               |
| avoid, circumvent                                    | 回避する                                                                                                   |
| retrieve                                             | 取りに行く(fetch / 「受け取る」よりもっと能動的に「取りに行く」ニュアンスを示す)                           |
| revise                                               | = fix                                                                                                      |
| tweak                                                | 微調整する                                                                                                 |
| in the sight of 〜                                   | 〜の視点で (point of view をわざと仰々しく言った感じ)                                                      |
| refer                                                | 参照する                                                                                                   |
| disambiguate                                         | 曖昧さをなくす                                                                                             |
| quite                                                | とても（very のかわりにつかえる                                                                            |
| literally                                            | 文字通り                                                                                                   |
| exactly                                              | まさに、確かに、イグザクトリー                                                                             |
| resurrect                                            | よみがえらせる                                                                                             |
| in favor of                                          | 〜に賛成して, 何かに沿って                                                                                 |
| get rid of                                           | 好ましくないものを取り除く                                                                                 |
| kick out                                             | get rid of の強いバージョン、腹立たしさある                                                                |
| introduce                                            | 導入する                                                                                                   |
| extract                                              | 抽出する                                                                                                   |
| no longer used                                       | もはや使われてない                                                                                         |
| R.I.P.                                               | 安らかに眠れ（もう使ってないコードを消す時などに。「Remove では語りきれない思いがあるんだ」 by @idesaku ） |
| defeat                                               | 倒す、打ち負かす                                                                                           |
| :put_litter_in_its_place:`:put_litter_in_its_place:` | ゴミはゴミ箱へ（不要なコメントや whitespace を消したときなど）                                             |
| cosmetic change, cosme                               | インデントを美しくした時など                                                                               |
| fruitful                                             | みのりの多い〜, fruitful discussion など                                                                   |
| :golf:`:golf:`                                       | コードをより短くした（code golf）                                                                          |
| Take a cup of coffee                                 | JS を CoffeeScript 化した, または Coffee をより Coffee らしく書いた                                        |
| kick in                                              | 効きはじめる, 適用される など（DHH が使っていたらしい。）                                                  |
| A in B out                                           | B の変わりに A を導入（サッカー的な感じ。Gem の差し替えなどに使う）                                        |
| enable to work                                       | 動くようにした                                                                                             |
| wipe out                                             | 拭い去る（get rid of, kick out の亜種）                                                                    |
| stop rendering 〜                                    | 〜を表示しない                                                                                             |
| aesthetic                                            | cosmetic の亜種（多分）                                                                                    |
| Ooops! :scream:                                      | しょうもないミスした時などに。 :scream_cat: `:scream_cat:` 使うとかわいみでる。                            |

# ChangeLog を支える英語

ChangeLog を書く際によく使われる英語をまとめました。

ほとんど引用です。

## 基本形

基本的な文法です。あとは単語を知っていれば大体なんとかなるそうです。

### 大文字で始める

    Fix possible memory leak
    Removed obsolete username_max_length

### ピリオドをつけない

    Changed A to B
    Upgraded A to version 1.0

### 動詞の過去形で始まる「～を…しました」形

    Fixed a performance regression
    （パフォーマンスが低下するバグを修正しました）

### 「～は…するようになります」形

now + 動詞の過去分詞。仕様変更などの際に使いましょう。

    Minimized pages are now hidden
    （最小化したページは今後は隠されるようになります）

### 名詞句のみ

「～（という）こと」的な。

    Many usability improvements
    （多くのユーザビリティの向上）

## ちょっと便利ないいまわし

慣れてきたら少々のエスプリをきかせましょう。

### ときどき（時々）

a possible を使う。

    a possible crash.
    （ときどきクラッシュする）

    a possible null pointer dereference.
    （ときどきヌルポする）

### 不具合

致命的ではない不具合には issue を使う。

    the stability issue.
    （不安定になる不具合）

## よく使う動詞

- 新規追加

  add, added

        Added support for bridgeless SLI with GeForce 8 GPUs

- 改善

  improve, improved

        Improved device handling

- 変更

  change, changed

        Changed A to B

- 修正

  modify, modified

        Modified IPv6 default listen address

- バグフィックス

  fix, fixed

        Fixed a bug in test.t

- 削除

  remove, removed

        Removed a dependency to Huge::Module

- 取り消し（巻き戻し）

  revert, reverted

        Revert the 'require' in command.cmd to do 'do'

- 更新

  update, updated

        Updated docs for new-features options

  > Win7 -> Win7-SP1

- 拡張（機能追加などをともなう）

  upgrade, upgraded

        upgraded to 1.0

  > Win7 -> Win8

- 有効／無効

  enable, enabled / disable, disabled

        Enabled type checking of the app in MyApp::sub

- 拡張

  extend, extended

- 強化、向上

  enhance, enhanced

- 実装

  implement, implemented

        Implemented app.streaming in all blocking servers

- リファクタ

  refactor, refactored

        Refactored MyApp

- 最適化

  optimize, optimized

        Optimized a process

- 削減、切り詰め

  reduce, reduced

        Reduced kernel virtual memory usage with some GeForce 8 GPUs

* 微調整

  tweak, tweaked

        Tweaked labels of graph metrics

* 対応

  suppor, supported

        Supported the new format.

## 冠詞(a, the, any, some)

- a, the

  それと別物を置き換えても文章が成り立つ場合。
  どれでもいいのが a

  それでないと文章が成り立たない場合。
  それじゃないと駄目なのが the

  > - だから乞食は"Would you give me a quarter."(25 セントくれ)と言うのに、取引では"Give me the money."(その金よこせ)と言うわけです....というのは半分冗談ですが、そういうことです。
  > - OOP(Object Oriented Programming)で言うと、a がクラス(class)で the がインスタンス(instance)だ。

- any, some

  any => a, some => the

  > ♪Help! I need somebody<br/>
  > ♪Help! Not just anybody

### 注意事項

- 固有名詞には the をつけない

  固有名詞: 人名や地名等、それ以外には存在しない特定の対象を表す名詞

  > Taro, Tokyo, Japan

- 作品紹介では a を使う

  > - Spirited Away' is a Miyazaki film. The movie won the Academy Award in 2001.
  > - It's a Sony

# 以下列挙

（例は実際の同僚や OSS 上でのコミットメッセージです.）

## Add *A to *B

*A を*B に加える

```tex:例
Add ambiences to admin_notify_organizer_new_event email.
```

## Remove *A from *B

*B から*A を取り除く

```tex:例
Remove config/database.yml from git index and add it to gitignore.
```

## Move *A from *B to \*C

*A を*B から\*C に動かす

```tex:例
Move admin_notify_venues_shortlisted email from LeadMailer to AdminMailer.
```

## Replace *A with *B

*A を*B に取り替える

```tex:例
Replace the elaborate reloading connection checking scheme, just fix the Ruby-based MySQL adapter, ye?
```

## Make *A *B

*A を*B にする、させる

```tex:例
Make javascript_include_tag :default behave correctly with application.js
```

```tex:例
Make counter_cache work with polymorphic belongs_to
```

## Change *A to *B

*A を*B に変更する.

```tex:例
Change a to an for HTML word [ci skip]
```

## Update *A to *B

*A を*B に更新する

```tex:例
Update edge to script.aculo.us to 1.7.1_beta3
```

## Ensure \*A

\*A である事を確実にする.

that 節とよく使うぽい.

```tex:例
Ensure that request.path never returns nil.
```

## Use \*A

\*A を使う.

単体で用いるよりも instead of や for の前置詞（下部で述べる）とよく使うっぽい

```tex:例
Use `Base.strict_decode64` instead of `Base.decode64` just as we do in encoding;
```

## Fix \*A

\*A を直す

```tex:例
Fix saving reject_reason when rejecting lead.
```

## その他比較的頻度の高かった動詞

上記が題意となる頻出動詞１０です.

以下はその他比較的頻度の高かった動詞です.

#### Refactor

```tex:例
Refactor RoutesReloader a bit to avoid creating extra hash objects
```

#### Improve

```tex:例
Improved the silence method on the logger to ensure restoring the old level
```

#### Extract

```tex:例
Extract InflectorTestCases so both inflector and string inflections tests can use them.
```

#### Deprecate

```tex:例
Deprecate using method_missing for attributes that are columns.
```

#### Avoid

```tex:例
Avoid empty transaction from setting has_one association on new record.
```

#### Simplify

```tex:例
Simplify Preloader#grouped_records code.
```

#### Define

```tex:例
Define the Duration#instance_of? method
```

#### Allow

```tex:例
Allow use of assert_template with the :file option.
```

#### Switch from *A to *B

```tex:例
Switch from SHA2 to BCrypt
```

#### Implement

```tex:例
Implement #== for column
```

#### Clean up

```tex:例
Clean up JobWrappers::ResqueWrapper.perform
```

#### Enable

```tex:例
Enable memcached service on travis for running cache tests.
```

#### Sorting *A by *B

```tex:例
Sort migrations by the migration ID.
```

#### Rewrite

```tex:例
Rewrite Account Setting page from ERB to HAML.
```

#### Support

```tex:例
Support multiple config.after_initialize blocks so plugins and apps can more easily cooperate.
```

#### Stop, Prevent

```tex:例
Stop relying on columns in sqlite quoting tests
```

#### Drop

```tex:例
Drop variable assignment in validations
```

## 前置詞（上記の動詞に情報を付加するもの）

## with \*P

\*P と一緒に、伴って

```tex:例
Fixed error with 'rails generate new plugin'.
```

## for \*P

\*P のために

```tex:例
Add a simple API for fetching a list of entries from the cache
```

## instead of \*P

\*P の代わりに

```tex:例
Use `Base.strict_decode64` instead of `Base.decode64` just as we do in encoding;
```

## in \*P

\*P の、で

```tex:例
Use strong_params in example
```

## at \*P

\*P の、で

```tex:例
Revert "log at debug level what line caused the redirect_to"
```

## as \*P

\*P として

```tex:例
Stop messing up with instance variables, use protected as it was meant for
```

## 頻出動詞 TOP20

| 順位 | 英単語          | 意味         | 出現回数           |
| :--- | :-------------- | :----------- | :----------------- |
| 1    | fix/fixed/fixes | 修正する     | 165084/35773/19813 |
| 2    | add/added       | 追加する     | 141711/35282       |
| 3    | remove/removed  | 取り除く     | 81124/12528        |
| 4    | use             | 用いる       | 75767              |
| 5    | update/updated  | 更新する     | 57004/11761        |
| 6    | support         | サポートする | 43808              |
| 7    | merge           | マージする   | 34762              |
| 8    | make            | 作成する     | 31425              |
| 9    | move            | 移動させる   | 22208              |
| 10   | don't           | しない       | 21431              |
| 11   | check           | チェックする | 16882              |
| 12   | change          | 変更する     | 14594              |
| 13   | allow           | 許す         | 14352              |
| 14   | cleanup/clean   | 一掃する     | 12217/8405         |
| 15   | set             | セットする   | 13132              |
| 16   | convert         | 変換する     | 11633              |
| 17   | rename          | リネームする | 10703              |
| 18   | do              | する         | 10028              |
| 19   | revert          | リバートする | 9268               |
| 20   | avoid           | 避ける       | 8822               |

シンプルな単語が多いようです。
modify が入っていないのは意外でした。20 位以降は、improve や、handle、replace などの動詞が続きます。

しかし、動詞が分かっただけでは、英語でコメント書けませんよね。
これらの動詞とセットでよく用いられる単語を分析してみます。

## 頻出動詞とセットでよく用いられている単語とコメント集

頻出動詞とセットで用いられた単語、それぞれ TOP10 を解析し、
その中から、有用な組み合わせと実際のコメントを列挙していきます。

### 1 位.fix

| 単語のセット | 代表例     | 意味                | 実際のコメント          |
| :----------- | :--------- | :------------------ | :---------------------- |
| fix,in       | Fix A in B | B の箇所の A を修正 | Fix typo in docs        |
| fix,for      | Fix for A  | A に対する修正      | fix for #4183           |
| fix,to       | Fix A to B | B への A を修正     | Fix link to the spec    |
| fix,of       | Fix A of B | B の A を修正       | fix location of favicon |

fix は、いろいろな前置詞と用いられています。
fix だけではないのですが、for の後には、issue の ID などがよく用いられています。

### 2 位.add

| 単語のセット | 代表例      | 意味            | 実際のコメント         |
| :----------- | :---------- | :-------------- | :--------------------- |
| add,to       | Add A to B  | B に A を追加   | add .js to import      |
| add,for      | Add A for B | B 用に A を追加 | Add test for bug #3116 |

add は、to がよく用いられています。

### 3 位.remove

| 単語のセット  | 代表例          | 意味                | 実際のコメント                        |
| :------------ | :-------------- | :------------------ | :------------------------------------ |
| remove,from   | Remove A from B | B から A を除去     | Remove Debug from tests               |
| remove,in     | Remove A in B   | B の箇所の A を除去 | Remove duplication in render function |
| remove,unused | Remove unused A | 不必要な A を除去   | Remove unused code                    |

unused は remove に限らず使えそうです。

### 4 位.use

| 単語のセット | 代表例             | 意味                    | 　実際のコメント                |
| :----------- | :----------------- | :---------------------- | :------------------------------ |
| use,to       | to use A           | A を用いるために        | Change syntax to use dots       |
| use,of       | Use A instead of B | B の代わりに A を用いる | Use ++ instead of += 1          |
| use,in       | Use A in B         | B の箇所の A を用いる   | Use stub in testing.            |
| use,for      | Use A for B        | B のために A を用いる   | use Ruby for mocking            |
| use,remove   | Remove use of B    | B を用いるのを除去      | Remove use of deprecated method |

use は、不定詞として用いられていていました。
また、名詞としても用いられていますね。instead of は、use に限らず使えそうです。

### 5 位.update

| 単語のセット | 代表例                         | 意味                                      | 　実際のコメント                                    |
| :----------- | :----------------------------- | :---------------------------------------- | :-------------------------------------------------- |
| update,to    | Update to A <br> Update A to B | A にアップデート<br>A を B にアップデート | Update to Unicode 6.3.0<br>Update Modernizr to v1.6 |
| update,for   | Update A for B                 | B に対して A をアップデート               | update History.md for #1563                         |

### 6 位.support

| 単語のセット | 代表例                             | 意味                                         | 　実際のコメント                                   |
| :----------- | :--------------------------------- | :------------------------------------------- | :------------------------------------------------- |
| support,add  | Add A support<br>Add support for A | A サポートを追加<br>A に対するサポートを追加 | Add Travis CI Support<br>Add support for callbacks |

support は、名詞的にも使われていることが多いようです。

### 8 位.make

| 単語のセット | 代表例                               | 意味                                                                   | 　実際のコメント                                                                                                                                    |
| :----------- | :----------------------------------- | :--------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| make,of      | Make use of A                        | A を使用する                                                           | make use of Ember.isNone explicit in Ember.isEmpty                                                                                                  |
| make,it      | Make it A<br>Make it A の比較級      | A にする<br>より A にする<br>(A には、possible,simple,easy,clear など) | Make it possible to have IDs per request <br>Make it easy to check platform requirements in a command<br>Make it easier to debug the release script |
| make,sure    | Make sure to A<br>Make sure (that) A | 必ず A するようにする                                                  | Make sure to reset default_url_options<br>Make sure all packages rebuild.                                                                           |

make 単体では、Make A B といった、A を B にするという形式がよく用いられますが、
他の単語との組み合わせで見てみると、Make it possible,Make it easier などの使い方がされています。

### 9 位.move

| 単語のセット | 代表例        | 意味                  | 　実際のコメント             |
| :----------- | :------------ | :-------------------- | :--------------------------- |
| move,from    | Move A from B | B から A を移動させる | Move fix_fname from buffer.c |
| move,to      | Move A to B   | A を B に移動させる   | Move strings to strings.js   |
| move,in      | Move A in B   | B 内の A を移動させる | Move quotes in nav-main.html |

### 10 位.don't

| 単語のセット | 代表例      | 意味         | 　実際のコメント           |
| :----------- | :---------- | :----------- | :------------------------- |
| don't,use    | Don't use A | A を用いない | Don't use "assert_not_nil" |

don't は、様々な動詞と用いられますが、use が多く用いれていました。

### 11 位.check

| 単語のセット | 代表例         | 意味                | 　実際のコメント                     |
| :----------- | :------------- | :------------------ | :----------------------------------- |
| check,for    | Check for A    | A に対するチェック  | Check for weak dependency correctly. |
| check,in     | Check A in B   | B 内の A をチェック | check ID in os-release instead       |
| chcek,fix    | Fix A check    | A チェックを修正    | Fix html extension check             |
| check,add    | Add A check    | A チェックを追加    | Add null check                       |
| remove,check | Remove A check | A チェックを除去    | remove useless nil check             |

check は、結構名詞的な使われ方もしていて、if 文の修正によく使われているようです。

### 12 位.change

| 単語のセット | 代表例                       | 意味                      | 　実際のコメント                                   |
| :----------- | :--------------------------- | :------------------------ | :------------------------------------------------- |
| change,to    | Change A to B<br>Change to B | A を B に変更<br>B に変更 | Change copyright to 2013<br>change to lazy Unmount |
| change,for   | Chage A for B                | B に対して A を変更       | Change API for sending handles                     |
| change,in    | Change A in B                | B 中の A を変更           | change rm usage in docs                            |

### 13 位.allow

| 単語のセット | 代表例       | 意味                | 　実際のコメント              |
| :----------- | :----------- | :------------------ | :---------------------------- |
| allow,to     | Allow A to B | A が B するのを許す | Allow the user to drag faster |

### 15 位.set

| 単語のセット | 代表例      | 意味                  | 　実際のコメント                |
| :----------- | :---------- | :-------------------- | :------------------------------ |
| set,to       | Set A to B  | A を B にセット       | Set default kernel to Gaussian. |
| set,for      | Set A for B | B に対して A をセット | Set release date for 0.10.1     |

### 16 位.convert

| 単語のセット | 代表例                         | 意味                      | 　実際のコメント                             |
| :----------- | :----------------------------- | :------------------------ | :------------------------------------------- |
| convert,to   | Convert A to B<br>Convert to B | A を B に変換<br>B に変換 | convert time to string<br>convert to boolean |

### 17 位.rename

| 単語のセット | 代表例        | 意味              | 　実際のコメント                   |
| :----------- | :------------ | :---------------- | :--------------------------------- |
| rename,to    | Rename A to B | A を B にリネーム | Rename hero.html to jumbotron.html |

### 20 位.avoid

| 単語のセット | 代表例                     | 意味                                        | 　実際のコメント                                                  |
| :----------- | :------------------------- | :------------------------------------------ | :---------------------------------------------------------------- |
| avoid,to     | Avoid A to B<br>to avoid A | B するために A を避ける<br>A を避けるために | avoid method call to compact<br>Remove methods to avoid warnings. |

動詞単体では, Avoid A や、Avoid ~ing でよく用いられています。

18 位の do は、主に do not で用いられていたため省略しています。
7 位の merge、13 位の cleanup、19 位の revert はセットでよく使われている単語はあまり出てきませんでした。

# 解析方法

## データの収集

github 上のリポジトリから、一括でコミットメッセージを取得するのには以下のプログラムを参考にしました。
**参考 URL**
https://github.com/minamijoyo/commit-crawler

github API のアクセストークンを登録するだけで、一括でコミットメッセージを取得することができます。

## 解析と可視化

英語のコミットメッセージなので、日本語とは違いスペースで区切るだけで簡単に単語ごとに分解できます。
分解した単語の出現頻度をカウントするプログラムを python で書きました。
ただ単純に頻度の多い単語を分析していっても、a や the などの意味のない単語が多いので、ある程度絞る必要があります。自然言語処理のライブラリである nltk を用いて、品詞の分析をし、名詞と動詞の抽出しました。抽出した結果のワードクラウド表示は、以下の参考 URL で簡単にできました。

**参考 URL**
[英語前処理サーベイ](http://yusuke0h.hatenablog.com/entry/2013/10/15/123832)
[nltk と pytagcloud で英語のワードクラウド](http://moguranosenshi.hatenablog.com/entry/2014/09/14/nltk%E3%81%A8pytagcloud%E3%81%A7%E8%8B%B1%E8%AA%9E%E3%81%AE%E3%83%AF%E3%83%BC%E3%83%89%E3%82%AF%E3%83%A9%E3%82%A6%E3%83%89)

# 感想

github 上のコメントは解析してみると、シンプルな単語が用いられており、
小難しい単語はあまり見受けられません。
中学校で習う単語と文法ばかりですし、書くときは考えすぎずに書いてよさそうです。
ちなみに、「Yes」や、「Oops」だけのコメントもあったりします。笑

## 分析に関して

Merge Branch や Merge pull request などの github が自動で生成するようなコメントは除いています。しかし、リポジトリごとに特有のコミットメッセージが存在
また、use や、support などは名詞としても用いられるため、動詞の用法としての順位は変わってくる可能性が大いにあります。
今回は行いませんでしたが、形容詞や副詞に関して分析するのも面白そうです。
ということで、番外編に結果を載せたいと思います。

## (番外編 1)頻出形容詞 TOP20

| 順位 | 英単語   | 意味                        | 実際のコメント                          |
| :--- | :------- | :-------------------------- | :-------------------------------------- |
| 1    | new      | 新しい                      | New URL.                                |
| 2    | unused   | 使用されていない            | Remove unused $$                        |
| 3    | static   | 静的な                      | Build static executable.                |
| 4    | empty    | 空の                        | Add empty line                          |
| 5    | old      | 古い                        | Fix old links                           |
| 6    | small    | 小さな                      | Small typo                              |
| 7    | initial  | 最初の                      | Initial commit                          |
| 8    | local    | ローカルの                  | Updates local dev guide                 |
| 9    | wrong    | 間違った                    | Fix wrong id                            |
| 10   | common   | 共通の                      | Optimize the most common resolver case. |
| 11   | other    | 他の                        | Change other example fields             |
| 12   | dead     | 死んだ                      | Remove dead link                        |
| 13   | rid      | (get rid of で)<br>取り除く | get rid of EmptyComponent               |
| 14   | possible | 可能性のある                | possible regression fix                 |
| 15   | unneeded | 不必要な                    | Remove unneeded @                       |
| 16   | same     | 同じ                        | Use same colors for disabled buttons    |
| 17   | global   | グローバルの                | Fix global leaks                        |
| 18   | invalid  | 不正な                      | Fix invalid timer test                  |
| 19   | specific | 特定の                      | Remove linux specific calls             |
| 20   | extra    | 余分な                      | Remove extra whitespace                 |

簡単な英単語ばかりですね。
rid は、**get rid of**でよく使われるようです(形容詞ではないですが)。
また、**possible**は 「possible + (何か悪いこと、例えば crash や memory leak など)を修正する」という文脈で使われていました。他にも、**if possible** (文末に付けて: 可能なら)や、**as early as possible**(できるだけ早く)、**make it possible**(可能にする)などで使われていました。

ちなみに、enable,variable,disable,clear,separate も入っていましたが、形容詞以外の使われ方の方が多いようなので除いています。

## (番外編 2)頻出名詞 TOP20

名詞も並べてみます。タイポ多いですね。笑

| 順位 | 英単語             | 意味           | 出現回数    |
| :--- | :----------------- | :------------- | :---------- |
| 1    | test/tests         | テスト         | 30306/20073 |
| 2    | code               | コード         | 25839       |
| 3    | error              | エラー         | 22700       |
| 4    | function/functions | ファンクション | 14464/9640  |
| 5    | driver             | ドライバー     | 14386       |
| 6    | version            | バージョン     | 13231       |
| 7    | typo               | タイポ         | 12167       |
| 8    | docs               | ドキュメント   | 11865       |
| 9    | bug                | バグ           | 11518       |
| 10   | return             | リターン       | 11296       |
| 11   | tag                | タグ           | 14352       |
| 12   | default            | デフォルト     | 10556       |
| 13   | device             | デバイス       | 10381       |
| 14   | handling           | ハンドリング   | 10147       |
| 15   | files              | ファイル       | 9195        |
| 16   | type               | タイプ         | 9166        |
| 17   | auto               | オート         | 9268        |
| 18   | name               | 名前           | 8765        |
| 19   | data               | データ         | 8511        |
| 20   | warning            | 警告           | 8448        |

| 略語                                   | 元の語                                                            | 意味                                                                                                                         |
| -------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| AFAICT                                 | As far as I can tell                                              | 分かる限りでは ○○                                                                                                            |
| AFAIK                                  | As far as I know                                                  | 知る限りでは ○○                                                                                                              |
| AKA, aka, a.k.a.                       | Also known as                                                     | ○○ としても知られる                                                                                                          |
| ASAP                                   | As soon as possible                                               | できる限り早く                                                                                                               |
| BTW                                    | By the way                                                        | ところで                                                                                                                     |
| c.f., cf.                              | ラテン語 confer / 英語 compare                                    | ○○ を参照                                                                                                                    |
| e.g., E.g.                             | ラテン語 exempli gratia / 英語 for example                        | たとえば                                                                                                                     |
| ETA                                    | Estimated time of arrival                                         | （作業の）完了予定時刻　（用例は[コメントを参照](http://qiita.com/items/86c3a09d17792ab62dfe#comment-54f3d7872ba953941e7d)） |
| FTW                                    | For the win                                                       | 〔何か良い案を挙げて〕これで決まり；これでよし                                                                               |
| FWIW                                   | For what it's worth                                               | 役に立つかどうかは分からないが                                                                                               |
| FYA                                    | For your action                                                   | 要対応；要返信                                                                                                               |
| FYI                                    | For your information                                              | 参考；ご参考までに                                                                                                           |
| HTH                                    | Happy to help                                                     | （用例は[コメントを参照](http://qiita.com/items/86c3a09d17792ab62dfe#comment-54f3d7872ba953941e7d)）                         |
| idk, IDK                               | I don't know                                                      | 知らない；分からない                                                                                                         |
| i.e., I.e.                             | ラテン語 id est / 英語 that is                                    | すなわち                                                                                                                     |
| IIRC                                   | If I remember [recall] correctly                                  | 記憶が正しければ ○○                                                                                                          |
| IIUC                                   | If I understand correctly                                         | 〔相手の発言を受けて〕私の理解が正しければ                                                                                   |
| IMO, IMHO                              | In my (humble) opinion                                            | 〔ていねいに〕○○ だと思います                                                                                                |
| LGTM                                   | Looks good to me                                                  | 〔提案に対して〕いいと思う；問題ないと思う；〔コードレビュアーが、問題ないコードに対して〕レビュー終了；（コードの）承認     |
| LOL, lol                               | Laugh out loud                                                    | 〔くだけて〕www；（笑）                                                                                                      |
| NA, N/A                                | Not applicable; not available                                     | 〔表などで、項目の組み合わせが無効な欄に記載して〕該当なし；〔表などで、まだ値がない欄に記載して〕該当値なし                 |
| NB, N.B.                               | ラテン語 nota bene / 英語 note well                               | 〔通例コメントの先頭で〕特に注意せよ                                                                                         |
| NP, np                                 | No problem                                                        | 〔依頼・謝罪などに対してくだけて〕（問題ないから）気にしないで；大丈夫〔感謝に対してくだけて〕どういたしまして               |
| OTOH                                   | On the other hand                                                 | もう一方では、これに反して                                                                                                   |
| PTAL                                   | Please take another look                                          | 〔再レビューの要求などで〕再度ご確認ください                                                                                 |
| PR                                     | Pull request                                                      | プルリクエスト                                                                                                               |
| RFC                                    | Request for comments                                              | 〔おもに issue のタグとして〕意見募集                                                                                        |
| ROFL, rofl                             | Rolling on the floor laughing                                     | 〔くだけて〕www；（笑）                                                                                                      |
| RTFM                                   | Read the fucking manual                                           | 〔乱暴に〕マニュアルを読め                                                                                                   |
| TBA                                    | To be advised                                                     | あとで連絡する                                                                                                               |
| TBA                                    | To be announced                                                   | あとで発表する                                                                                                               |
| TBD                                    | To be determined                                                  | あとで決める                                                                                                                 |
| TBW                                    | To be written                                                     | あとで書く                                                                                                                   |
| TLDR, tldr, TL;DR, tl;dr, TL/DR, tl/dr | Too long, didn't read                                             | 長すぎるので読んでいない；（長い文を読みたくない人向けの）要約                                                               |
| UTSL                                   | Use the source, Luke                                              | 〔くだけて〕ソースを読め（スター・ウォーズのセリフとかけた言葉遊び）                                                         |
| w/                                     | with                                                              | （with の省略形）                                                                                                            |
| w/o                                    | without                                                           | （without の省略形）                                                                                                         |
| WIP                                    | Work in progress                                                  | 作業中                                                                                                                       |
| wrt, w.r.t., WRT                       | With regard [respect, reference] to                               | 〜に関して言えば                                                                                                             |
| WTF, wtf                               | What the fuck                                                     | 〔想定外の事・ものにくだけて〕なんてこった；どうすりゃいいんだ；マジかよ                                                     |
| XD                                     | 顔文字：90 度右に回すと、目をつぶって大きく口を開けた笑顔に見える | 〔くだけたコメントで〕(≧▽≦)                                                                                                  |

# おまけ

ソフトウェアのバージョン：

| 略語 | 元の語                 | 意味                                |
| ---- | ---------------------- | ----------------------------------- |
| LTS  | Long-term Support      | 長期サポート対象版                  |
| GA   | General availability   | 一般向け提供；正式リリース版        |
| GM   | Golden master          | （CD プレスの）原盤；正式リリース版 |
| RTM  | Ready to manufacturing | 量産可能；正式リリース版            |
| RC   | Release candidate      | リリース候補版                      |
| ES   | Engineering Sample     | 機能評価版                          |

慣用表現：

| 語                     | 直訳         | 意味                                                                                                                                                                                                                                                            |
| ---------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bikeshed, Bikeshedding | 自転車置き場 | 重要でない議論に時間を取られること（家のペンキを塗り終える前に自転車置き場を何色で塗るか揉めることから）                                                                                                                                                        |
| Yak shaving            | ヤクの毛刈り | ある大きな問題を解決するために、 一見無関係な小さい問題をいくつも片付けること。転じて、大きな問題を解決するつもりが、一見関係しているように見えて実は無用な小さい問題に気を取られること（長く固いヤクの毛を刈ってウールにするには多くの下準備が必要なことから） |

## コミットメッセージを書く

| Japanese                                         | English                           |
| :----------------------------------------------- | :-------------------------------- |
| A を実装しました                                 | Implement A                       |
| 機能(クラス)B に A を実装しました                | Add A to B                        |
| 機能(クラス)B の A をリファクタリングしました    | Refactor A in B                   |
| A を B から C に変更しました                     | Change A from B to C              |
| A でなく B を使うようにしました                  | Replace A with B                  |
| 機能(クラス)A のテストを追加しました             | Add test for A                    |
| 機能(クラス)A の失敗していたテストを修正しました | Fix broken A tests                |
| 依存ライブラリ A をバージョン x.y.z に上げました | Update A to x.y.z                 |
| ファイル A 中の誤字を修正しました                | Fix typo in A                     |
| 〜のとき〜するバグを修正しました                 | Fix the problem where 〜 when 〜  |
| 機能(クラス)A について、B にも対応しました       | Support B in A                    |
| ドキュメント A の B に関する記述を修正しました   | Improve B in A                    |
| A で発生するエラーメッセージを見直しました       | Improve error message thrown in A |
| バージョン x.y.z をリリースしました              | Release x.y.z                     |

### 本当は避けたほうが良いが、細かい修正をまとめてコミットするときのコメント用例

| Japanese                                             | English             |
| :--------------------------------------------------- | :------------------ |
| 依存ライブラリのバージョンを諸々更新しました         | Update dependencies |
| 雑多なコードフォーマット修正・可視性の修正をしました | Polish              |
| コンパイル・静的解析の警告を出ないように修正しました | Clean up            |

## 問い合わせる

| Japanese                                          | English                                |
| :------------------------------------------------ | :------------------------------------- |
| 〜する予定はありますか?                           | Do you have any plans to 〜 ?          |
| (このプロダクトを使って)〜することはできますか?   | Is there any way                       |
| 回避策ありませんか?                               | Is there a workaround?                 |
| ～してないのって、何か理由ありますか?             | What is the reason for not ～?         |
| 設定/実装例がほしいです                           | Could you provide an example please?   |
| どうぞよろしくお願いします                        | Thanks in advance.                     |
| 〜すると NullPointerException がでます            | We get NPE when 〜                     |
| このドキュメントを日本語に翻訳してもいいですか?   | Can I translate the docs to Japanese?  |
| クローズしちゃっていいですか?                     | Can I close this?                      |
| バージョン x.y.z でも、まだこのバグ潰れてないです | I still encounter this bug with x.y.z. |

## 問合せに答える

| Japanese                        | English                                                     |
| :------------------------------ | :---------------------------------------------------------- |
| 再現できないですねぇ…           | I'm afraid I can't reproduce the error you're seeing.       |
| もうちょっと情報ください        | You'll need to provide a little more information than that. |
| スタックトレースはありませんか? | Could you provide a stack trace?                            |
| そこがまさに問題なんです        | That's exactly the problem.                                 |

## お礼をいう

| Japanese                                     | English                                                                         |
| :------------------------------------------- | :------------------------------------------------------------------------------ |
| とても勉強になりました                       | I think I've learned a lot.                                                     |
| オッ、分かりました!                          | I see now.                                                                      |
| フィードバックありがとう                     | Thanks for the feedback.                                                        |
| 何か他にもありましたら、よろしくお願いします | You're more than welcome to contribute.                                         |
| もし解決できたら、プルリク送ってください     | If you are able to resolve this, we would encourage you to send a pull request. |
| ちゃんと動きました!                          | It's working as expected.                                                       |

## 引用元

- [Changelog のための英文テンプレート集 - ぴょぴょぴょ？ - Linux とかプログラミングの覚え書き -](http://d.hatena.ne.jp/pyopyopyo/20070920)
- [辞書で引けない技術英語 ChangeLog でよく使う表現](http://linuxenglish.blog83.fc2.com/blog-entry-115.html)
- [404 Blog Not Found:プログラマーでなくてもわかる a と the の違い](http://blog.livedoor.jp/dankogai/archives/50963216.html)
- [a と the の話: 極東ブログ](http://finalvent.cocolog-nifty.com/fareastblog/2004/02/athe.html)
- [英語でコミットを書こう](https://speakerdeck.com/pwim/ying-yu-dekomitutowoshu-kou)
- [コミットメッセージの書き方 - ククログ(2012-02-21)](http://www.clear-code.com/blog/2012/2/21.html)
- [わかりやすいコミットメッセージの書き方 - ククログ(2013-04-24)](http://www.clear-code.com/blog/2013/4/24.html)
- [なぜ太陽は Sun ではないか　固有名詞にも区別がある | ごきげんようチャンネル](http://soundsteps.jugem.jp/?eid=2387)
- [日本人ため「a」と「the」の違い | 外国語を学習するなら Lang-8](http://lang-8.com/300419/journals/63961979153871083784092209061940160075)

- [Awesome Commit English](https://github.com/azu/awesome-commit-english)
- [Abbreviations.com - Computing Abbreviations](http://www.abbreviations.com/category/COMPUTING)
- [Acronym Finder](http://www.acronymfinder.com)
- [GitHub English Challenge Cheat Sheet](https://qiita.com/kawasima/items/feac49a299213e2c8ba6)
