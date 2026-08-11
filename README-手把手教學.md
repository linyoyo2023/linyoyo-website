# 林友友網站｜手把手教學

這套網站使用三種最容易理解的技術：

- `index.html`：網站文字與各個區塊
- `assets/css/main.css`：顏色、版面與手機版
- `assets/js/ui.js`：手機選單和按鈕互動

正式網域已設定為 `linyoyo.com`，註冊商是中華電信。現在先在電腦預覽，不要先修改 DNS。

## 專案結構

```text
lin-youyou-site/
├── index.html
├── README-手把手教學.md
├── assets/
│   ├── css/
│   │   └── main.css
│   └── js/
│       └── ui.js
└── images/
    └── 請把候選人照片放在這裡.txt
```

## 第一課：用 VS Code 打開網站

1. 解壓縮完整專案。
2. 開啟 VS Code。
3. 點選 `File` → `Open Folder…`。
4. 選擇解壓縮後的 `lin-youyou-site` 資料夾。
5. 左側應該會看到 `index.html`、`assets` 和 `images`。

## 第二課：安裝預覽工具

1. 點 VS Code 左側的 Extensions 圖示。
2. 搜尋 `Live Server`。
3. 安裝作者 Ritwick Dey 的 Live Server。
4. 回到檔案區，點開 `index.html`。
5. 在 `index.html` 上按滑鼠右鍵，選 `Open with Live Server`。
6. 瀏覽器會自動打開網站。

如果沒有自動打開，看 VS Code 右下角是否出現 `Go Live`，點一下即可。

## 第三課：修改網站文字

1. 在 VS Code 打開 `index.html`。
2. 按 `Command + F` 搜尋想修改的文字，例如 `用心傾聽`。
3. 直接修改標籤中間的中文。
4. 按 `Command + S` 儲存。
5. 回到瀏覽器，畫面會自動更新。

請只修改 `>` 與 `<` 之間的中文，先不要刪除角括號和英文標籤。

## 第四課：放入林友友照片

1. 準備一張直式照片，命名為 `candidate.jpg`。
2. 把照片放進 `images` 資料夾。
3. 打開 `index.html`。
4. 搜尋 `候選人照片放置區`。
5. 刪除這一段：

```html
<div class="portrait-placeholder">
  <span class="portrait-name">林友友</span>
  <span class="portrait-note">候選人照片放置區</span>
</div>
```

6. 在原本位置貼上：

```html
<img class="candidate-photo" src="images/candidate.jpg" alt="林友友候選人照片">
```

7. 儲存後回到瀏覽器確認照片。

## 第五課：設定官方 LINE

1. 在 `index.html` 搜尋 `加入官方 LINE`。
2. 找到該按鈕前面的 `href="#"`。
3. 把 `#` 換成真正的 LINE 網址。
4. 同一行刪除 `placeholder-link`。
5. 加上 `target="_blank" rel="noopener noreferrer"`。

完成後會像這樣：

```html
<a href="https://lin.ee/你的代碼" target="_blank" rel="noopener noreferrer" class="button button-primary">
  加入官方 LINE
</a>
```

志工加入按鈕也是相同做法，可以換成 Google 表單網址。

## 第六課：修改五大政見

1. 在 `index.html` 搜尋 `五大政見`。
2. 每一個 `<article class="policy-card">` 就是一張政見卡片。
3. `<h3>` 中間是標題，`<p>` 中間是說明。
4. 每修改一張就先儲存並確認，避免一次改太多而找不到錯誤。

## 第七課：修改網站顏色

在 `assets/css/main.css` 最上方可以看到：

```css
:root {
  --ink: #102c24;
  --forest: #185b47;
  --cream: #f6f2e9;
  --orange: #ee6645;
}
```

這些是網站主要顏色。更換 `#` 後面的色碼，整個網站會一起改變。

## 第八課：檢查手機版

1. 用 Chrome 打開網站。
2. 按 `Command + Option + I` 開啟開發者工具。
3. 點擊工具列的手機／平板圖示。
4. 分別查看 iPhone 和桌機尺寸。
5. 測試右上角選單、導覽連結及「加入支持」按鈕。

## 正式上線前必須補齊

- 林友友正式照片
- 官方 LINE 網址
- 志工表單網址
- 正式競選團隊聯絡資料
- 最終確認的政見文字
- Facebook／LINE 分享圖片

以上內容確認完成後，再進行上線與 `linyoyo.com` DNS 連接。
