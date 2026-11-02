# 幾A幾B（1A2B 猜數字遊戲）

單一 HTML 檔的網頁小遊戲，不需要安裝、不需要後端，用瀏覽器開啟 `index.html` 就能玩。

## 規則

- 電腦隨機選出 **4 個不重複的數字**（0～9，可以 0 開頭）。
- 你每次猜一組 4 位數字，電腦回覆「幾A幾B」：
  - **A**：數字和位置都正確
  - **B**：數字正確，但位置不對
- 猜出 `4A0B` 就過關，並顯示猜了幾次。

範例：答案 `1234`，猜 `1357` → `1A1B`（1 位置對；3 數字對但位置錯）。

## 除錯模式

兩種開啟方式：

1. 勾選畫面下方的「除錯模式」。
2. 在網址後面加上 `?debug=1`，例如 `index.html?debug=1`。

開啟後會：

- 顯示目前這一局的答案。
- 顯示最近一次猜測的逐位判定（例如 `1→A，3→B，5→－，7→－`）。
- 在瀏覽器主控台（F12 → Console）輸出紀錄，前綴為 `[1A2B debug]`。

## 部署到 GitHub Pages

1. 把 `index.html` 與 `README.md` 放進 repository 的根目錄並推送到 `main` 分支。
2. 到 repository 的 **Settings → Pages**。
3. **Source** 選 *Deploy from a branch*，Branch 選 `main`、資料夾選 `/ (root)`，按 Save。
4. 約一兩分鐘後，網站會在 `https://<你的帳號>.github.io/<repository 名稱>/`。

## 檔案

| 檔案 | 說明 |
| --- | --- |
| `index.html` | 遊戲本體（HTML + CSS + JavaScript） |
| `README.md` | 本說明 |
