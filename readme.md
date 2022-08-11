# 目次
1. [Class命名ルール](#anchor1)  
   1-1. [それぞれの意味、役割](#anchor1-1)  
   1-2. [BlockとElement](#anchor1-2)  
   1-3. [セクションについて](#anchor1-3)  
   1-4. [命名ルール](#anchor1-4)
   
2. [mediaファイル設計](#anchor2)  
   2-1. [画像タイプ](#anchor2-1)  
   2-2. []()  
   2-3. []()  
***
<a id="anchor1"></a>
>Class命名ルール

<a id="anchor1-1"></a>
* **それぞれの意味、役割**
  
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
<a id="anchor1-2"></a>
* **BlockとElement**

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
<a id="anchor1-3"></a>
* **セクションについて**
```html
<div>以外のタグでh1~h6を挟んではいけない。
必ずh1~h6からセクションが始まり、h1~h6のないセクションは存在しない。
```
***

<a id="anchor1-4"></a>
* **命名ルール**

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

***-Modifier***
```text
-color
-list
-active
-hover
-button
```
***
<a id="anchor2"></a>
> mediaファイル設計

<a id="anchor2-1"></a>
* **画像タイプ(これ以外の画像タイプは使用しない)**
```text
アイコン    icon
写真        pic
背景        bg
テキスト    txt
ボタン      btn
動画        mov
```
***
<a id="anchor2-2"></a>
* **ファイル管理**
```text
media
>img
    >page
    >page
>video
    >page
    >page
```
***
<a id="anchor2-3"></a>
* **命名規則**

***サイト共通***
```text
画像タイプ_文字列
例
icon_twitter.png
icon_facebook.png
```

***サイト共通モジュール***
```text
Block_Element

例
header_item1.png
header_item2.png
footer_logo.svg

or

Block_Element_画像タイプ

例
header_item_icon1.png
header_item_icon2.png

or

Block_Element_Modifier

例
header_item_active.png
main_form_button.png
```