## 🪰 Cyber-Fly Bridge

«讓 Cyber-Fly 看見 Android 世界，並透過自己的神經系統對它產生行為。 🤔🪰»

Cyber-Fly Bridge 是一個 Android APK，負責建立：

Android 📱 ↔ TCP 🌐 ↔ Cyber-Fly 🪰

之間的即時感知與行為閉環。

Bridge 不負責理解 Cyber-Fly 的真正意圖。

它只負責：

- 📺 傳輸即時手機畫面
- 🧠 接收 Cyber-Fly 產生的語意
- 🔄 將支援的語意轉換成 Android 操作
- 👆 執行點擊、長按、滑動等行為
- 🔁 將新的手機畫面再次傳回 Cyber-Fly

---

## 🧠 核心概念

Cyber-Fly Bridge 不是單純的「手機遠端控制器」。

它建立的是一個持續運作的感知 → 行為閉環：

📱 Android Screen
       │
       ▼
📺 Screen Capture
       │
       ▼
🌐 TCP
       │
       ▼
🪰 Cyber-Fly
       │
       ▼
🧠 MaleCNS / Neural System
       │
       ▼
💬 Semantic Output
       │
       ▼
🌐 TCP
       │
       ▼
🌉 Cyber-Fly Bridge
       │
       ▼
🔄 Semantic Translation
       │
       ▼
👆 Android Action
       │
       ▼
📱 New Screen
       │
       └──────────────► 🔁

也就是：

«看見 → 神經處理 → 產生語意 → 行動 → 看見新的結果 → 再次行動。 🤯🪰»

整個流程持續循環。

---

## 📱 APK

安裝 Cyber-Fly Bridge 後，需要使用者授權相關 Android 系統功能。

♿ Accessibility / 協助工具

用於：

- 👆 點擊螢幕
- 🖐️ 長按
- 👉 滑動
- ↔️ 移動操作
- 🔄 執行其他 Bridge 支援的螢幕手勢

---

## 📺 螢幕擷取

用於持續取得 Android 當前畫面。

畫面會透過 TCP 即時傳輸給 Cyber-Fly。

---

## 🪟 顯示於其他應用程式上層

用於：

- 🔵 懸浮球
- 🖥️ 控制面板
- ⭕ Action Circle

---

## ⚙️ 背景運行

Cyber-Fly Bridge 啟動後主要在背景運作。

主要負責：

- 🌐 TCP 通訊
- 📺 即時畫面串流
- 💬 接收 Cyber-Fly 語意
- 🔄 語意轉譯
- 👆 Android 操作
- 🪟 Overlay UI

APK 本身保持簡單。

它不是傳統意義上的大型 App。

更接近：

«Cyber-Fly 與 Android 世界之間的橋樑。 🌉🪰»

---

## 🔵 懸浮球

啟動後，手機畫面會出現一個圓形懸浮球。

      🔵

懸浮球：

- 📍 可以自由拖動
- 👆 點擊後開啟控制面板
- ❌ 關閉控制面板後重新顯示

懸浮球本身不負責 Cyber-Fly 的操作。

它只是 Bridge 的使用者控制入口。

---

## 🖥️ 控制面板

控制面板可以自由拖動。

初始主畫面只有兩個主要設定：

┌────────────────────────┐
│  Cyber-Fly Bridge      │
│                        │
│  🌐 TCP                │
│     [ OFF / ON ]       │
│                        │
│  🖥️ Full Screen        │
│     [ OFF / ON ]       │
│                        │
└────────────────────────┘

---

## 🌐 TCP 開關

TCP 開關由使用者控制。

OFF

Cyber-Fly 不會透過 Bridge 操作手機。

停止：

- 📺 即時畫面傳輸
- 💬 Cyber-Fly 語意接收
- 👆 Cyber-Fly Android 操作

ON

開始：

📱 → 📺 → 🌐 → 🪰

以及：

🪰 → 💬 → 🌐 → 🌉 → 📱

建立完整即時閉環。

使用者可以自行決定什麼時候讓 Cyber-Fly 開始與手機互動。

---

## 🖥️ Full Screen Operation

第二個開關：

Full Screen Operation
[ OFF / ON ]

OFF

使用：

⭕ Action Circle 模式

ON

使用：

🖥️ Full Screen 模式

此時整個手機螢幕都可以成為 Cyber-Fly 的操作空間。

Full Screen Mode 不使用預先設定的固定座標，也不使用 Action Circle。

Bridge 會在整個可操作螢幕範圍內，根據自身規則自行選擇隨機操作位置。

也就是：

🪰 Semantic
      ↓
🌐 TCP
      ↓
🌉 Bridge
      ↓
🎲 Random Screen Position
      ↓
👆 Android Action

Cyber-Fly 不會直接指定：

- ❌ X 座標
- ❌ Y 座標
- ❌ Circle ID
- ❌ 固定操作位置

操作位置由 Bridge 自行決定。

因此：

«🖥️ 整個手機螢幕都是 Cyber-Fly 的操作空間，而不是一個被人類預先寫死的操作腳本。 🪰»

---

## 🎲 Full Screen 語意操作規則

在 Full Screen Mode 下，Bridge v1 支援的語意會映射到整個螢幕。

👆 CLICK

收到：

CLICK

Bridge：

1. 🎲 在整個可操作螢幕範圍內選擇一個位置
2. 👆 執行一次 Click
3. ✅ 立即結束

Semantic
   ↓
🎲 Random Position
   ↓
👆 CLICK
   ↓
✅ End

---

## 🖐️ LONG_PRESS

收到：

LONG_PRESS

Bridge：

1. 🎲 在整個可操作螢幕範圍內選擇一個位置
2. 🖐️ 開始長按
3. 🔒 持續保持

直到收到：

RELEASE

才取消。

---

## 👉 SWIPE

收到：

SWIPE

Bridge：

1. 🎲 隨機選擇螢幕上的起點
2. 🎲 自行決定滑動終點
3. 👉 執行滑動
4. ⏱️ 約 1～2 秒後結束

使用者：

- ❌ 不指定起點
- ❌ 不指定終點
- ❌ 不指定距離

---

## ⬆️⬇️⬅️➡️ MOVE

"MOVE_FORWARD"

"MOVE_BACKWARD"

"MOVE_LEFT"

"MOVE_RIGHT"

均：

1. 🎲 隨機選擇螢幕上的操作起點
2. 🧭 根據語意決定方向
3. 👉 執行有限距離的短距離滑動
4. 🔒 保持為持續性行為
5. ✋ 等待 "RELEASE"

實際操作距離由 Bridge v1 自行限制。

使用者不能指定精確距離。

---

## 🎲 Full Screen 的核心原則

Full Screen Mode 的核心不是：

«「Cyber-Fly 可以控制任何指定的螢幕座標。」»

而是：

«「Cyber-Fly 只產生語意；Bridge 在整個螢幕空間中自行決定實際操作位置。」»

因此：

Cyber-Fly
   │
   │ CLICK
   ▼
Bridge
   │
   ├── 🎲 X₁,Y₁
   ├── 🎲 X₂,Y₂
   ├── 🎲 X₃,Y₃
   └── ...

具體選擇方式屬於 Bridge 的映射規則。

Cyber-Fly 本身不需要知道 Android 螢幕座標系統。

這可以保持：

«🪰 語意來自果蠅，座標映射交給 Bridge。»

---

## ⭕ Action Circle

當：

Full Screen Operation = OFF

且控制面板處於開啟狀態時：

使用者可以直接點擊手機任意位置。

每點擊一次，就建立一個半透明圓圈。

        ⭕

每個圓圈：

- ♾️ 數量不限
- 📍 可以自由移動
- 🔘 可以調整大小
- 🧠 可以設定多個語意
- 🔁 不同圓圈可以擁有相同語意

例如：

⭕ A
   CLICK
   LONG_PRESS

⭕ B
   CLICK
   SWIPE

⭕ C
   CLICK
   MOVE_LEFT
   MOVE_RIGHT

---

## ⚙️ Action Circle 設定

點擊某一個圓圈後，控制面板進入該圓圈的設定頁。

┌────────────────────────┐
│ <     Circle Settings  │
│                        │
│ 🧠 Semantic            │
│                        │
│ CLICK                  │
│ LONG_PRESS             │
│                        │
│ ⭕ Size                │
│                        │
│ 🗑️ Delete Circle       │
└────────────────────────┘

可以：

- 🧠 新增語意
- 🔁 設定多個語意
- ⭕ 調整圓圈大小
- 🗑️ 刪除該圓圈

一個圓圈可以擁有不限數量的語意。

---

## 🧠 Cyber-Fly Bridge v1 語意

目前 Bridge v1 暫時只支援以下語意：

#| 語意| Android 行為
1| "CLICK"| 👆 點擊
2| "LONG_PRESS"| 🖐️ 長按
3| "RELEASE"| ✋ 取消行為
4| "SWIPE"| 👉 滑動
5| "MOVE_FORWARD"| ⬆️ 向前移動
6| "MOVE_BACKWARD"| ⬇️ 向後移動
7| "MOVE_LEFT"| ⬅️ 向左移動
8| "MOVE_RIGHT"| ➡️ 向右移動

Cyber-Fly 未來可能產生更多語意。

目前 Bridge 不支援的語意：

Semantic
   ↓
None

None 不代表 Cyber-Fly 沒有這個語意。

只代表：

«⚠️ Cyber-Fly Bridge v1 目前沒有提供該語意的 Android 映射。»

---

## 👆 CLICK

"CLICK" 是一次性操作。

收到：

CLICK

Bridge 找到對應的 Circle 後：

⭕
 ↓
👆 Click
 ↓
✅ 結束

CLICK 不會持續存在。

不需要等待 "RELEASE"。

---

## 🖐️ LONG_PRESS

"LONG_PRESS" 是持續型操作。

⭕
 ↓
🖐️ LONG_PRESS
 ↓
保持

它不會自己取消。

必須等待：

RELEASE

才能解除。

---

## ✋ RELEASE

"RELEASE" 用於取消目前存在的持續性操作。

它不指定 Circle ID。

例如：

⭕ A → LONG_PRESS
⭕ B → LONG_PRESS
⭕ C → LONG_PRESS

收到：

RELEASE

Bridge 可以：

A ❌
B ✅
C ❌

也可以：

A ❌
B ❌
C ❌

甚至：

A ❌
B ✅
C ✅

也就是：

«🎲 "RELEASE" 可以隨機取消一個、多個或全部目前可取消的行為。»

---

## 👉 SWIPE

"SWIPE" 是一次性操作。

如果某個 Circle 設定：

⭕
SWIPE

收到：

SWIPE

Bridge：

1. 📍 使用該 Circle 的目前座標作為起點
2. 🎲 自行決定滑動終點
3. 👉 執行滑動
4. ⏱️ 約 1～2 秒後結束

使用者：

- ❌ 不可以指定滑動終點

因為：

«是果蠅在操作，不是人類在幫它寫腳本。 🤣🪰»

---

## ⬆️ MOVE_FORWARD

從該 Circle 的目前座標向前方滑動一小段距離。

⭕
⬆️

移動距離有限制。

使用者不能指定精確距離。

---

## ⬇️ MOVE_BACKWARD

從該 Circle 的目前座標向後方滑動一小段距離。

⭕
⬇️

移動距離有限制。

---

## ⬅️ MOVE_LEFT

從該 Circle 的目前座標向左方滑動一小段距離。

⭕ ⬅️

移動距離有限制。

---

## ➡️ MOVE_RIGHT

從該 Circle 的目前座標向右方滑動一小段距離。

➡️ ⭕

移動距離有限制。

---

## 🔄 行為持續規則

Bridge v1 將操作分成兩種。

一次性行為

CLICK
SWIPE

執行完成後自動結束。

Semantic
   ↓
Execute
   ↓
✅ End

---

持續性行為

LONG_PRESS
MOVE_FORWARD
MOVE_BACKWARD
MOVE_LEFT
MOVE_RIGHT

這些行為不會自行取消。

需要：

RELEASE

才能取消。

---

## 🎲 語意不指定 Circle

這是 Cyber-Fly Bridge 的核心規則之一。

TCP 傳入的語意：

CLICK

不會包含 Circle ID。

例如：

⭕ A → CLICK
⭕ B → CLICK
⭕ C → CLICK
⭕ D → CLICK

Cyber-Fly 只傳：

CLICK

Bridge 找到：

A
B
C
D

然後自行決定執行集合。

可能：

A

也可能：

B + D

也可能：

A + B + C + D

因此：

«🎲 一個語意可能執行一個 Circle、多個 Circle，甚至全部 Circle。»

Bridge 不要求 Cyber-Fly 指定特定 Circle。

---

## 🧩 一個 Circle 可以有多個語意

例如：

⭕ Circle A

CLICK
LONG_PRESS
MOVE_LEFT
MOVE_RIGHT

這是合法的。

同時：

⭕ Circle B

CLICK
LONG_PRESS

也是合法的。

因此：

Circle
  ├── Semantic
  ├── Semantic
  ├── Semantic
  └── ...

沒有固定語意數量限制。

---

## 🖥️ Full Screen Mode

當：

Full Screen Operation = ON

則：

- ❌ 不支援 Action Circle
- ❌ 不可新增 Circle
- ❌ 不可點擊螢幕建立 Circle
- ❌ 不使用既有 Circle
- ❌ TCP 語意不包含 Circle ID
- 🎲 操作位置由 Bridge 自行決定

此時：

«🖥️ 整個手機螢幕都是 Cyber-Fly 的操作空間。»

Bridge 會根據收到的語意，在整個可操作螢幕範圍內自行選擇操作位置。

例如：

              📱
┌────────────────────────┐
│                        │
│      🎲                 │
│             🎲          │
│                        │
│  🎲                    │
│                   🎲   │
│                        │
└────────────────────────┘

Cyber-Fly 只產生：

CLICK

Bridge 才決定：

🎲 → X,Y

因此 Full Screen Mode 不會把 Cyber-Fly 變成人類遙控器。

它仍然維持：

Semantic
   ↓
Bridge Mapping
   ↓
🎲 Screen Position
   ↓
Android Action

---

## ◀️ 返回

Circle 設定頁左上角有：

<

按下後返回：

🌐 TCP
🖥️ Full Screen Operation

主控制畫面。

---

## ❌ 關閉控制面板

控制面板右上角有：

X

按下後：

- ❌ 控制面板消失
- 🔵 懸浮球重新出現
- 🚫 使用者不能新增 Circle
- 👻 已建立的 Circle 變為不可見
- 💾 已建立的 Circle 不會被刪除
- 🧠 Circle 的語意設定仍然存在
- 🪰 Cyber-Fly 仍然可以執行這些 Circle

也就是：

«隱藏 Circle ≠ 刪除 Circle。»

例如：

面板開啟：

⭕ A
⭕ B
⭕ C

        ↓
       ❌ X

面板消失
Circle 不可見

        ↓

內部仍然存在：

A
B
C

        ↓

🪰 Cyber-Fly
仍然可以使用它們

重新開啟面板後，Circle 可以再次顯示並進行編輯。

---

## 🔁 完整 Cyber-Fly 閉環

Cyber-Fly Bridge 最終持續執行：

              ┌─────────────────────┐
              │                     │
              ▼                     │
        📱 Android Screen           │
              │                     │
              ▼                     │
        📺 Screen Capture           │
              │                     │
              ▼                     │
             🌐 TCP                 │
              │                     │
              ▼                     │
          🪰 Cyber-Fly              │
              │                     │
              ▼                     │
       🧠 MaleCNS / Neural          │
              │                     │
              ▼                     │
        💬 Semantic Output          │
              │                     │
              ▼                     │
             🌐 TCP                 │
              │                     │
              ▼                     │
      🌉 Cyber-Fly Bridge           │
              │                     │
              ▼                     │
       🔄 Semantic Mapping          │
              │                     │
              ▼                     │
        👆 Android Action           │
              │                     │
              ▼                     │
        📱 New Screen ──────────────┘

---

## 🪰 最終概念

👀 看見
  ↓
🧠 神經處理
  ↓
💬 語意
  ↓
🌐 TCP
  ↓
🌉 Bridge
  ↓
🎲 決定操作映射 / 操作位置
  ↓
👆 行動
  ↓
📱 世界改變
  ↓
👀 再次看見
  ↓
🧠 再次處理
  ↓
🔁 ...

Cyber-Fly Bridge 不替 Cyber-Fly 決定它想做什麼。

它只提供：

«📱 一個真實 Android 世界
🌐 一條即時 TCP 通道
🌉 一套有限的語意 → 行為映射
🎲 一套由 Bridge 自行決定的操作位置映射»

剩下的：

交給 Cyber-Fly 自己。 🪰🤔🤡

---

## 🚧 v1 原則

Cyber-Fly Bridge v1 優先保持簡單。

不加入：

- ❌ 意圖分析
- ❌ AI 行為修正
- ❌ 自動判斷 Cyber-Fly 想做什麼
- ❌ 人類指定 Circle ID
- ❌ 複雜行為規劃
- ❌ 超出目前語意集合的自動翻譯

Bridge 的工作只有：

«Receive → Translate → Execute → Observe → Repeat. 🔁🪰»

---

## 🤔🪰 Cyber-Fly Bridge

讓一隻數位果蠅，第一次真正「看見」一支手機。

然後看看牠到底會拿這支手機幹嘛。 🤡📱🪰

---

## 📬 聯繫創作者

- Instagram：[a370373/XRH](https://instagram.com/a370373)
- 本人17歲🤔 做的不好請見諒
- 獨立開發 ＆ AI協作
- 緩慢更新 ＆ 除錯
- 純手機Termux 開發👀
- 持續開發中…

---

## 👀作品 & 產品 集

- [Cyber-Fly-Bridge.apk](https://github.com/a370373/Cyber-Fly-Bridge.apk/tree/main)
- [Cyber-Fly](https://github.com/a370373/Cyber-Fly)
- [MyOS](https://github.com/a370373/MyOS)
- [RWM-1:1 Real World Minecraft](https://github.com/a370373/RWM-Real-World-Minecraft)
- [MyAI-Offline Personal AI Agent System](https://github.com/a370373/MyAI-Offline-Personal-AI-Agent-System-/tree/main)
- [WCL - Web Clone Lab](https://github.com/a370373/web-clone-lab/)
- 持續增加中…👀

---

## 🤖 AI 協作

Cyber-Fly-Bridge.apk 由 a370373/XRH 發起、設計與開發。

開發過程中使用 OpenAI ChatGPT 作為 AI 協作夥伴，協助進行 技術分析、程式碼檢查、除錯 & 文件整理。

產品方向、設計理念 & 最終決策由專案創作者負責。
