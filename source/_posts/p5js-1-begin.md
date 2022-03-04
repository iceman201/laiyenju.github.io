---
title: p5.js - 基本樣式
date: 2020-10-11
tag:
- [p5.js]
- [creative technology]
---

學習 p5.js 的第一次作業
1. setup 與 draw 有什麼不一樣，個別執行的時機跟作用是什麼？
2. 要如何改變視窗的大小呢？
3. background() 裡面可以使用哪些參數，試著從文件中找找看
4. 希望有按下滑鼠的時候，才根據滑鼠的位置改變顏色要怎麼做到呢？
5. 如果我想要改變先前軌跡變淡的速度，要怎麼做呢？
6. 從 openprocessing, pinterest, 或是 codepen 之類的平台找幾個覺得有趣的作品，並試著分析ㄧ下如何達成

## 1. setup 與 draw 有什麼不一樣，個別執行的時機跟作用是什麼？

setup 比較像是初始值，通常會在這裡設定畫布尺寸、畫布的背景顏色等，程式會先執行 setup 的設定；程式執行完 setup 後，就會循環執行 draw 的內容，因此我們能將希望動態呈現的物件放在 draw 內，產生動畫效果。

## 2. 要如何改變視窗的大小呢？

改變 setup 中的 `createCanvas(w, h）` 數值，w 數值代表寬度，h 數值代表高度。

![](https://i.imgur.com/kHsYep9.jpg)


```javascript

//w=500, h=500

function setup() {
	createCanvas(500, 500);
	background(255);
}

function draw() {
	
}


// w=800. h=500

function setup() {
	createCanvas(800, 500);
	background(255);
}

function draw() {
	
}

```


## 3. background() 裡面可以使用哪些參數，試著從文件中找找看

* background(color)
* background(colorstring, [a])
* background(gray, [a])
* background(v1, v2, v3, [a])
* background(values)
* background(image, [a])

> - [a] 代表透明度
> - background(image, [a]) 要搭配 `loadImage()` 或 `createImage()` 使用

```javascript

// color value and object
background(51);  // grayscale
background(255, 204, 0);  // RGB
background(color(0, 0, 255));  // color object

// HSB 數值
colorMode(HSB);
background(255, 204, 100);

// colorstring
background('red');  // color-name
background('#fae');  // 3-digit Hex
background('#222222');  // 6-digit Hex
background('rgb(0,255,0)');  // RGB
background('rgba(0,255,0, 0.25)');  // RGB with opacity
background('rgb(100%,0%,10%)');  // RGB by percentage
background('rgba(100%,0%,100%,0.5)');  // RGB with opacity by percentage


```


## 4. 希望有按下滑鼠的時候，才根據滑鼠的位置改變顏色要怎麼做到呢？

<iframe src="https://www.openprocessing.org/sketch/877927/embed/" width="700" height="700"></iframe>


## 5. 如果我想要改變先前軌跡變淡的速度，要怎麼做呢？

改變背景透明度，越透明則軌跡變淡的速度越慢，越不透明則軌跡變淡的速度越快。

<iframe src="https://www.openprocessing.org/sketch/877944/embed/" width="700" height="700"></iframe>


## 6. 從 openprocessing, pinterest, 或是 codepen 之類的平台找幾個覺得有趣的作品，並試著分析ㄧ下他是怎麼做的吧

在 OpenProcessing 找到 [Type_ABCDe Studios](https://www.openprocessing.org/sketch/831208) 作品，覺得像是廣告看板，有點可愛。裡面運用了以下元素，搭配 for 迴圈讓字體重複出現，並在固定的範圍內移動。

- 製作立面方塊：`box()`
- 在立體面放入圖樣：`createGraphics()`
- 旋轉：`rotateX()`、`rotateY()`
- 使用字體：載入字體檔`loadFont()`、調整字體的`text()`與`textSize()`、渲染字體`texture()`

因為原作品寫 for 迴圈的方式用了 `sin()`，這部分的寫法我還沒搞懂，在嘗試製作後，改讓旋轉的立面方塊內文字跟著設定好範圍的 X 軸與 Y 軸隨機變動位置與大小，成為喧鬧的方塊XD

<iframe src="https://www.openprocessing.org/sketch/877949/embed/" width="700" height="700"></iframe>