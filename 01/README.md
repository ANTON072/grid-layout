# 横並びのメニュー

![スクリーンショット](./screen.png)

[サンプルページ](https://grid-layout-euh.pages.dev/01/)

- ウインドウ幅を縮めたとき、ロゴの大きさは変えず、メニューの領域を狭めていく。
- メニューリンクはすべて同じ幅で配置
- リンクの文字は上下左右中央揃え

## gap

`gap` でよく指定していたが、横方向と縦方向に分けてそれぞれ指定できるのは知らなかった。  
縦方向は `column-gap`、横方向は `row-gap` でそれぞれ指定可能。

## 横に並べる `grid-auto-flow: column;`

Grid レイアウトはデフォルトでは子要素が縦に配置される（`grid-auto-flow: row;`）。  
`grid-auto-flow: column` を設定すると横並びになる。  
flex の `flex-direction` 的なもの。

## 全部同じ幅にする `grid-auto-columns: 1fr`

要素に対して自動的に割り当たる大きさを指定する。  
1fr を指定することで、領域を均等に割り当てるので、すべての要素が同じ大きさで並ぶ。  
ちなみに auto でも同じ挙動だった。

## 配置指定

`align-items` や `justify-content` の挙動は flex と同じ。  
メニューリストのみ右揃えにしたいので、親が配置指定することはできない。  
そういう場合は、子要素が配置指定することができる。  
横位置は `justify-self`、縦位置は `align-self` で指定が可能。
