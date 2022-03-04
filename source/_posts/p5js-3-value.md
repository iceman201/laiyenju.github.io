
---
title: p5.js - 變數與資料
date: 2020-10-25
tag:
- [p5.js]
- [creative technology]
---

目標：學習如何產生更複雜、有規律的連續圖示。


## 為什麼要使用變數？

1. 減少重複
2. 暫存手邊資料
3. 為複雜運算解構概念
4. 留下上一刻的狀態

## 數字的操作

> 想法：
> 因為 draw function 本身就會一直循環，所以製作有序、不斷生成的圖像時，可以善用這點。

- `%` 取餘數，可以處理間隔式規律，例如：每隔三個方塊，就要有一個方塊是白色的。
- `abs` 取絕對值

## 轉換數值範圍的應用

- map/ constrain，map 是把一個數字從舊範圍對應到新範圍。
- lerp 逼近，會有種逐漸靠近的感覺
- min/max

```javascript
//讓滑鼠 x 軸位置的範圍是在 0, 255 之間
var colorR = map(mouseX, 0, width, 0, 255, true); 

//map(mouseX, 實際最小值, 實際最大值, 要對應的最小值, 要對應的最大值, [true])，true 讓最小值與最大值是乾淨的
```

## Questions

1. 使用 var 跟 let 在 p5.js 的使用有差別嗎？
3. 第二個範例的 brightness 放在 function 外面會更清楚、更好管理嗎？為何有時定義變數在 function 外，有時在裡面？

自己的想法：
`map()` 如果寫在 function 外，會被系統報錯，要求寫在 setup() 內，當改寫到 setup() 內，卻沒有畫面。如果跟老師一樣，寫在 draw 才會出現理想效果。


## 作業

1. 畫個蝸牛型，由內慢慢畫元到外，且顏色會變
2. 時鐘表面（番茄時鐘）
3. 嘗試物理模擬


<iframe src="https://editor.p5js.org/laiyenju/embed/bDppjKFI3" height="500" width="700" frameborder="0"></iframe>