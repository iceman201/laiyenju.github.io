---
title: 人與人的互動：溝通
date: 2020-02-11
---

> **摘要**
> 人機互動等於「人與系統的溝通」，因此可參考溝通心理學人與人溝通的模式：
> - 要先了解使用者（目標使用者）
> - 不能只了解字面意義，要讓使用者能推測意義（設計意向）
> - 要提供使用者在互動之間的期待、修正回饋機制
> - 通常人的溝通內容有一個隱含的焦點，人機互動也要有「焦點」
> - given-before-new 考慮介面呈現的邏輯，想想要如何讓使用者在互動過程中順利累積 common ground
> - 不在每個溝通階段做太多事、提供太多選擇

## 本課程涉及的領域
- 心理學和傳播
- 研究法
- 作業分析／資訊架構
- 設計的實作和測驗

## 什麼是介面

- 若以人體的神經傳導系統當作比喻，介面就像是神經軸突與樹突間的接口：突觸。當動作電位刺激軸突末端，會迫使鈣離子通道打開，原本位在軸突內的傳導物質會通過鈣離子通道，進入突觸間隙（軸突與樹突間的空間），與受體結合，引發下個神經元反應，傳遞動作反應，做用完的傳導物質會再被攝取泵吸回軸突。
- 若從程式設計來看，介面就像是 API（Application Programming Interface），能從客戶端向公司資料庫請求需要的資料。

### 介面的定義
- 一個會發生事件的地方或方法
- 能讓兩個個體或系統互動
- 功能：溝通或傳遞

從上述定義可歸納出介面具備的元素：
- 傳送
- 接收
- 效果（啟動某功能，滿足互動條件）
- 遵循某規範
    - 傳送者對接收者有期待
    - 接收者對傳送者與訊息／行動／行動的結果有期待
    - 傳送的內容
    - 事件發生的順序
    - 介面的啟動與結束

👉**介面是協助人機互動的必要物件**，至少現階段對人機互動的設計與想像，都無法脫離「介面」，例如：觸控面板、螢幕、穿戴裝置都是。

## 人機互動要考慮的問題
- 使用者：
    - 外在：能力、年齡、人體結構
    - 內在：動機、目的、背景
- 小環境：照明、溫度、網路速度、硬體軟體、使用情境
- 大環境：文化、社會氛圍

### 溝通
溝通是傳遞什麼訊息？或者說，是有意識地還是無意識地傳遞某些訊息？


| 人類溝通的類別 | Sign 徵兆              | Symbol 符號                     |
| -------------- | ---------------------- | ------------------------------- |
| 定義           | 反映內心狀態、反射動作 | 傳送資訊與意圖                  |
| 由來           | intrinsic              | social convention               |
| 發生           | involuntary            | intentional                     |
| 理解           | self-relate            | interpret through symbol system |
| 能力           | innate                 | learned and practiced           |
| 指涉           | n/a                    | signify-signified               |

微笑是 sign 還是 symbol？事實上 sign 與 symbol 有時無法完全分辨，同樣的行為可能反映內心情緒，也有可能是有社會意義。[^1]

[^1]: Kraut, R. (2006). Why bowlers smile. APS Observer, 19(6).


## 與溝通有關的理論

### **Aristotle's model of communication**
- 線性溝通模型：Speaker → Speech → Audience → Effect
- 有效溝通的三個要件
    1. Ethos 傳播者的可信度
    2. Pathos 情感的影響
    3. Logos 內容的邏輯

### **Encode-Decode Model**

1. Shannon-Weaver Model
    - [Claude Elwood Shannon](https://spectrum.ieee.org/tech-history/cyberspace/claude-shannon-tinkerer-prankster-and-father-of-information-theory) 提出 
    - 來源 → 入碼 → 傳送 →（干擾）→ 媒介 → 接收 → 解碼 → 目的地
    - 中間的干擾是經過媒介的耗損，例如電話收訊不佳，但只要還能斷斷續續聽到聲音，大概能猜到意思，訊息仍能被成功解碼。
    - 溝通的雙方要有共同的入碼-解碼對應系統（類似對碼表的概念）
    - 缺陷：由於 Encode-Decode Model 認為訊息等於資訊，資訊包含在訊息內，所以只要解碼訊息就能得知資訊，資訊量是可估算的，這無法解釋缺乏相同知識背景、生活記憶的兩人，可能在對話中產生的混淆。

2. 擴充的 Encode-Decode Model
    - Wilbur Schramm[^2] 提出
    - 溝通的雙方之所以能成功地解碼與入碼，是因為媒介訊息屬於共同的經驗範疇。
    - 儘管 Wilbur Schramm 的補充，但 Encode-Decode Model 是個不完整的模型，因為除了「共同經驗範疇」會影響溝通的有效性外，溝通過程的人、訊息、情境都會因為 **context（情境／脈絡）** 而不同。


### **Intentionalist Model 意向理論模式**
- 要溝通的不是資訊，而是「意義 meaning」或「意向 intention」
- 因此人之間的問答，不會只看字面意義，而是「詮釋」出背後的意義（了解對方的意圖）才回覆。



| model              | Encode-decode                  | Intentionalist             |
| ------------------ | ------------------------------ | -------------------------- |
| 溝通的主體         | information 資訊               | intention 意向             |
| 獲得溝通主體的方式 | 意義 = information，由解碼而來 | 意義 = meaning，由詮釋而來 |
| 主體存在於         | 訊息本身包含所有資訊           | 詮釋（訊息＋情境）= 意義   |

[^2]: Schramm, W. (1954). How communication works. The process and effects of mass communication, 3-26.

👉語言是種介面，供人際溝通使用。

1. Paul Grice: Cooperative Principles[^3]
    1. Quantity
    2. Quality
    3. Relation
    4. Manner

    人在學習溝通時遵循上述原則，因此也會假設對方遵守原則，但這些原則常被違反，所以我們會以「歸因」的方式理解對方的意向。（會在心裡以自己對世界的理解與觀點，不斷推敲對方到底表達的是什麼意思）

[^3]: Grice, H. P. (1975). Logic and conversation. In Speech acts (pp. 41-58). Br

2. Speech Act 理論
    補充說話者背後的幾個意向種類
    - lucutionary act 字面意義
    - illucutionary act 表達意向
    - perlocutionary act 使役，要求反應

    同一個訊息能被詮釋出三種不同的 speech act；不同訊息也可以被詮釋為同一種 speech act[^4]

[^4]: 禮貌原則／面子保全論 Levinson, Stephen. (1983). Pragmaics. Cambridge, U. K.: Cambridge
University Press.

3. Saliency and Interpretation in Context[^5]
    
    突出某項目與情境詮釋間的關係。
    
### Perspective-taking Model
- 以對方的觀點、因素決定溝通行為。
- perspective 指的是
    - inferred knowledge about the **person**
        - background, identity
        - plans, goals. attitudes
    - inferred knowledge about the **situation**
        - social context
        - physical context
- **Commmon Ground 共同認知**
- **Inferred Knowledge** 例如：口音
- **Referential Paradigm**[^6]
- **Back Channel**[^7]

👉溝通是動態的過程，會不斷調整，累積 common ground，使用在短時間內建立的 local convention，提升溝通效率。[^8]

👉**Scripts（腳本）**，一種社會心理學概念，一組有順序的行為與事件，在特定場景中進行規範的社會互動：遞名片、看診、到餐廳點餐。我們在社會化的過程中不斷習得各種場合的腳本。

## 溝通是複雜的心理歷程
1. 根據對對方的了解 → 決定如何溝通（溝通的方式）
2. 根據對情境的了解與期待 → 知道下一步將發生什麼
3. 在互動中累積共同認知 → 能知道 scripts 進行到哪個階段
4. 對共同認知的修正 → 若出錯或不確定，就確認並不斷修正

## 人機互動的溝通方式

- 將溝通模式套用在人機互動：設計產品 → 做出產品 → 介面 → 接觸介面 → 使用產品。
    - 設計者會在心中模擬使用情境，根據對使用者的了解設計產品。
    - 使用者設計產品的了解，因為系統印象而改變，會自己去詮釋介面，而詮釋介面會受到介面以外的因素（文化背景、年齡、身體結構等）影響。
    - 在使用產品中還有一連串過程：使用者會如何使用這個產品，中間也有溝通歷程。

- 人機互動的 Speech Act 與意向詮釋

|                              | 設計產品             | 使用者                                   |
| ---------------------------- | -------------------- | ---------------------------------------- |
| locution meaning 字面意義    | （產品長得像一顆球） | 對介面做情感性的反應：可愛               |
| illocution meaning 意向意義  | 這個設計是為了...... | 對意向意義的詮釋：這可以用來做......     |
| perlocution meaning 使役意義 | 我期待你這樣用...... | 對使役意義的詮釋：（嘗試用各種使用方式） |

- 人機介面的溝通方式取決於
    - 對使用者的了解
    - 對使用情境的了解與期待
    - 互動中，使用者對系統狀態的理解（知道系統在做什麼）
    - **設計的困難點：如果出錯或不清楚，對互動過程修補**

|            | 溝通行為               | 人機介面的溝通方式     |
| ---------- | ---------------------- | ---------------------- |
| 取決於     | 傳訊息者對對方的了解   | 設計師對使用者的了解   |
| 預期       | 根據對情境的了解與期待 | 對使用情境的了解與期待 |
| 互動過程中 | 在互動中累積共同認知   | 使用者對系統狀態的理解 |
| 若出錯了   | 不斷修正共同認知       | ？？？                 |


👉 若在人機介面的互動遇到錯誤，通常是跳出錯誤訊息，中止互動，沒有邊進行、編修正的機會，很多時候無法判斷使用者感覺困惑，在操作錯誤前提供說明；有時使用者也不知道自己詮釋錯誤。**設計的目標：幫助使用者形成正確的解釋。**



[^5]: Clark, H. H., Schreuder, R., & Buttrick, S. (1983). Common ground at the understanding of demonstrative reference. Journal of verbal learning and verbal behavior, 22(2), 245-258.

[^6]: Fussell, S. R., & Krauss, R. M. (1989). The effects of intended audience on message production and comprehension: Reference in a common ground framework. Journal of experimental social psychology, 25(3), 203-219.

[^7]: Chen, Y. (1990). The functionality of back channel responses in face-to-face interaction. Unpublished Masters Thesis, Department of Psychology, Columbia University.

[^8]: Krauss, R. M., & Weinheimer, S. (1964). Changes in reference phrases as a function of frequency of usage in social interaction: A preliminary study. Psychonomic Science, 1(1-12), 113-114.