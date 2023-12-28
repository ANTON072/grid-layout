# grid-template-areas を使用した、1 ～ 3 列の流動的なレスポンシブレイアウト

[サンプルページ](https://grid-layout-euh.pages.dev/08/)

## 1. まず領域に名前を付ける

```css
.main-head {
  grid-area: header;
}

.content {
  grid-area: content;
}

...
```

レイアウトは作成されないが、アイテムに名前がついたので、それを使ってレイアウトを作成することができる。

## 2. grid-template-areas

`grid-template-areas` で表示順に並べる。
