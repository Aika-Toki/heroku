>Class命名ルール  
>>それぞれの意味、役割

***Block***  
```text
この要素は独立しており、ページのどこに配置しても機能しなくてはならない。
つまり、この要素の位置をずらした場合でも他の要素に干渉することなく表示されなければならない。
```

***Element***
```text
Elementは必ずBlockの中に存在する。
つまり、Elementが単独で存在してはならない。
```

***Modifier***
```html
ブロック、エレメントの装飾のバリエーションを持たせるためのパターンを設定するための概念。
Modifierが二つ連続することもある。

Block__Element-list(M)-active(M)
```
***

>>BlockとElement

***Blockになるタグ***
```html
<header> <footer> <main> <section> <article> <nav> <aside> <div>
上記以外はBlockになってはいけない。
```

***Elementになるタグ***
```html
<div>を除くBlock以外
なお、divは極力Elementとして扱う。
```
***

>>セクションについて
```html
<div>以外のタグでh1~h6を挟んではいけない。
必ずh1~h6からセクションが始まり、h1~h6のないセクションは存在しない。
```
***

>>命名ルール

***Block***
```text
header
footer
main
gnav
etc...
```
***__Element***
```html
基本的にタグに対して固定のElementを使用する。

タグに対して固定のclass名
<p>
__text
__title
__button
__logo
__data

<h1>,<h2>...<h6>
__title

<table>
__table

<ul>
__list

<li>
__item
```

***-Modifire***
```text
-color
-list
-active
-hover
-button
```