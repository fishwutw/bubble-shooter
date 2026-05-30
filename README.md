# 氣泡消除測試版 Stage 1 - iPhone Safari 修正版

修正重點：

1. 不再依賴 `100dvh`，改用 JavaScript 讀取 `visualViewport.height` 後寫入 `--app-height`。
2. `resize()` 不再在每次 iPhone Safari 網址列變動時重置整個遊戲，只重新校正位置。
3. 泡泡繪製改成穩定的純色、陰影、反光，不使用可能在部分 Safari 狀態下出問題的複雜 radialGradient。
4. 事件處理改成 PointerEvent 優先，沒有 PointerEvent 才使用 touch/mouse，避免 iPhone 觸控被重複觸發。

請把這個 `index.html` 覆蓋 GitHub Pages repository 裡原本的 `index.html`。
