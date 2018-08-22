# flow の説明

flow は javascript のための静的タイプをチェックします。静的タイプチェックをすることによって、コードを書くことが早くなったりコードに対して信頼が高まるのであなたの生産性を上げてくれます。

flow は`静的タイプアノテーション`を通して、どのようにコードが振舞って欲しいかや以下のコードのように確認してくれます。

```javascript
// @flow
function square(n: number): number {
  return n * n;
}

square("2"); // Error!
```

flow は javascript のことをよく知っているので、多くの type を必要としません。最低限必要な flow のコードだけ済み、残りの部分を推論してくれます。flow はコードを全くなしで理解してくれます。

```javascript
// @flow
function square(n) {
  return n * n; // Error!
}

square("2");
```

また flow は少しずつ適用することもでき、いつでも取り除くことができます。なので flow がどのように動くのかを見て見ましょう。
