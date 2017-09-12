# htmlcss
 ## learnfront

# CSS関連
セレクタ

|書き方|意味|
|:--|:--|
|a, b|a要素と b要素　に適用のスタイル|
|a b|a要素したにあるすべての要素ｂに適用のスタイル|
|a > b|　　　要素a直下したの要素bに適用のスタイル|
|a + b|　　　要素a後ろの要素ｂに適用のスタイル|
|a.b|     要素aのクラスbのスタイル|
|a[title] {color: skyblue;}|属性セレクタ|


>>属性セレクタ

a[title] {
    color: skyblue;
}

a[class~="search"] {
    color: violet;
}

a[href="http://google.co.jp"] {
    color: orange;
}

>>擬似セレクタ

ul li:first-child {
    color: skyblue;
}

a:link {
    color: violet;
}

a:visited {
    color: orange;
}

a:hover {
    color: pink;
}

a:active {
    color: rebeccapurple;
}

input:focus {
    background-color: yellowgreen;
}

p::first-line {
    color: lightgreen;
}

p::before {
    content: "--> ";
}

p::after {
    content: " <--";
}

>>セレクタ詳細度　優先度
[!important] >a>b>c>d

(a)style =""

(b)id

(c)属性・似クラス

(d)要素・似要素

--- css

a{color : skyblue;}

a.link{color : pink;}

a.search{color : orangle;}

a#site{color : blue;}

 ---html

<a href="http://google.co.jp" class="link search" id="site" style"color:green;">to google<'/a>

---

>>ディバイス幅HTML中の書き方

```
<link rel="stylesheet" href="desktop.css" media="(min-width:769px)">

<link rel="stylesheet" href="tablet.css"  media="(max-width:768px) and (min-width: 321px)">

<link rel="stylesheet" href="mobile.css"  media="(max-width:320px)"> 

@import url(style.css) screen and (min-width: 769px);
@import url(tablet.css) screen and (max-width: 768px);
@import url(smart.css) screen and (max-width: 640px);

//pc用のcssを記述
@media screen and (min-width:961px) {}

//tablet用のcssを記述
@media only screen and (min-width:376px) and (max-width:960px) {
}

//スマホ用のcssを記述
@media screen and (max-width:375px) {
}
```


>--
```
<div class="sp_contents"><img src="/img/example_01.gif"></div>
<div class="pc_contents"><img src="/img/example_02.gif"></div>

@media screen and (min-width:376px) {
.sp_contents {display:none;} //横幅376px以上では表示しない
}
  
@media screen and (max-width:375px) {
.pc_contents {display:none;} //横幅375px以下では表示しない
} 
```
