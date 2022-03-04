---
title: p5.js - 基礎圖形繪製
date: 2020-10-18
tag:
- [p5.js]
- [creative technology]
---

## 定位點

圓形與方形的預設定位方式不同，圓形 `ellipse()` 是「圓心」為定位點，方形 `rect()` 是左上角為定位點。如果要統一使用一種定位點，可以使用 `rectMode()`。

- `rectMode(CENTER)` 以方形正中心為定位點
- `rectMode(CORNER)` 以方形左上角為定位點

## 基本幾何圖形的變化組合

- 圖形 
`rect()`, `ellipse()`, `triangle()`
- 影格
`framCount`
- 滑鼠位置 
`mouseX`, `mouseY`
- 填色 
`fill()`, `noFill()`
- 外框粗細與顏色 
`stroke()`, `strokeWeight()`, `noStroke()`
- 判斷式 
`strokeWeight(frameCount % 2==0? 5:1)` 如果 frameCount 是偶數，就粗外框，是奇數就細外框。

## 尋找位置的技巧

直接在頁面上印出滑鼠所在位置的座標點（x, y）。以下是能在頁面（50, 50）的位置印出滑鼠所在的座標點。

```javascript
function draw() {
    background(255)
    fill('black')
    text(int(mouseX) + ' , ' + int(mouseY), 50, 50)

}
```

## 自製圖形

```javascript
beginShape();
vertex(30, 20);
vertex(85, 20);
vertex(85, 75);
vertex(30, 75);
endShape(CLOSE);
```

## 課後問題

#### 1. ellipse() 跟 circle() 有什麼不一樣，有辦法用 ellipse() 繪製出 circle() 的圖形嗎？

- `ellipse(x, y, w, [h])`, `circle(x, y, d)`
- `ellipse()` 因為能控制長寬，所以可以畫出橢圓；`circle()` 只有控制 diameter，所以只能畫圓形。
- 兩者都能用`ellipseMode()`選擇定位模式：CENTER, CORNER, CORNERS, RADIUS

![](https://i.imgur.com/d0v2U7e.png)


```javascript
function setup() {
  createCanvas(380, 500);
}

function draw() {
  background(220);
  push();
  textSize(20);
  text('Circle Method', 25, 50);
  text('Ellipse Method', 25, 300);
  pop();  
  
  textSize(12);
  text('circle(80, 150, 100)', 25, 70);
  text('diameter = 100', 25, 90);
  circle(80, 150, 100);
  text('circle(250, 175, 150)', 200, 70);
  text('diameter = 150', 200, 90);
  circle(250, 175, 150);
  
  text('ellipse(80, 380, 100)', 25, 320);
  text('width = 100, height = 100', 25, 340);
  ellipse(80, 400, 100);
  text('ellipse(250, 380, 150, 100)', 200, 320);
  text('width = 150, height = 100', 200, 340);
  ellipse(250, 400, 150, 100);
  
}
```

#### 2. 我們如何繪製不規則的圖形？需要使用到哪些指令呢？

![](https://i.imgur.com/NXdBd93.png)

```javascript
function setup() {
  createCanvas(300, 300);
}

function draw() {
  background(220);
  beginShape();
  vertex(30, 20);
  vertex(85, 20);
  vertex(85, 75);
  vertex(30, 75);
  endShape(CLOSE);
  
  beginShape();
  vertex(100, 100);
  bezierVertex(20, 0, 80, 75, 30, 100);
  endShape(CLOSE);
  
  beginShape();
  curveVertex(130, 20);
  curveVertex(185, 20);
  curveVertex(185, 75);
  curveVertex(130, 75);
  endShape(CLOSE);
}
```

#### 3. 透過可以畫面的元素（如圖形、邊框顏色、粗細、大小、填色等）與各種參數（如 frameCount, mouseX, mouseY, mouseIsPressed 等）互相搭配，可以顯示出讓人驚艷的效果，也試試看隨意的搭配，看看會有什麼變化吧，像是 “隨著滑鼠位置變化邊框粗細，或是判斷是否透點擊滑鼠改變圖形的填色”

<iframe src="https://www.openprocessing.org/sketch/885229/embed/" width="600" height="700"></iframe>


#### 4. 如何用三元運算子表達這個判斷式的結果if(imHungry){return 'eatDinner'}else{return 'goToSleep'}
```javascript
imHungary ? console.log('eatDinner'):console.log('goToSleep');
```

#### 5. 如何讓繪製的圖形隨時間變形/變色呢？ 需要使用到什麼變數？

使用 `frameCount` 放到圖形的 x 或 y 變數中，可以讓圖形隨時間變形；放到 fill 內可以讓圖形隨時間變色。

<iframe src="https://editor.p5js.org/laiyenju/embed/DzkSTiNBp" width="300" height="300" frameborder="0"></iframe>

<iframe src="https://editor.p5js.org/laiyenju/embed/lLLmD710v" width="300" height="300" frameborder="0"></iframe>

```javascript

function draw() {
// 圖形的外框隨時間變形
  noFill();
  beginShape();
  vertex(30+frameCount*2, 20+frameCount*1.4);
  vertex(85+frameCount*8, 20);
  vertex(85, 75+frameCount*2);
  vertex(30, 75);
  endShape(CLOSE);
  
  beginShape();
  vertex(100, 100);
  bezierVertex(20+frameCount*0.3, 0, 80, 75, 30, 100+frameCount*1.1);
  endShape(CLOSE);
  
  ellipse(100, 200, 50, 50+frameCount*5);
}


function draw() {
//圖形由白色越變越黑
  fill(255-frameCount*0.4);  
  beginShape();
  vertex(30+frameCount*2, 20+frameCount*1.4);
  vertex(85+frameCount*8, 20);
  vertex(85, 75+frameCount*2);
  vertex(30, 75);
  endShape(CLOSE);
  
  beginShape();
  vertex(100, 100);
  bezierVertex(20+frameCount*0.3, 0, 80, 75, 30, 100+frameCount*1.1);
  endShape(CLOSE);
  
  ellipse(100, 200, 50, 50+frameCount*5);
}
```

#### 6. 曲線是不是不能應用在非封閉線段？


#### 7. 很想知道重複偏移要如何使用？

不確定此題的意思，如果是要在特定位置重複偏移，可以使用`random()` 或迴圈。

<iframe src="https://editor.p5js.org/laiyenju/embed/JU8ntIIhk" width="500" height="500" frameborder="0"></iframe>

<iframe src="https://editor.p5js.org/laiyenju/embed/21DHnJ7JS" width="500" height="500" frameborder="0"></iframe>