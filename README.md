# license-how-to-by-tw

你是否常常到了一個網站，看到它說自己有採用創用 CC 授權，卻不知道該從哪裡開始判讀、該怎麼標示，或哪些素材其實不在授權範圍內？

`license-how-to-by-tw` 把 Ian 過去查找網頁與作品授權的經驗、關鍵字、判斷方法與標示習慣整理成一個可分享的 Codex skill，幫助你正確標示並安心享受創用 CC 素材。

這個專案尤其適合處理網頁、作品、圖片、資料集、簡報、文件、文化典藏頁或其他線上素材的 CC 授權判讀，並產生可直接使用的繁中標示表。

真正的 skill 入口在：

```text
skills/find-cc-license-and-attribution/
```

## 目前做什麼

- 找出頁面或作品的 CC 授權證據。
- 判斷授權適用於文字、圖片、資料、程式碼、Logo、第三方素材或整體頁面。
- 正規化 CC 授權名稱，例如 `CC BY 4.0`、`CC BY-NC 3.0 TW +`、`CC0 1.0`。
- 產生固定三欄輸出：`使用對象`、`Attribution / 應標示對象`、`CC 授權名稱`。
- 在授權不明確時，保守標示 `未明確標示`，並提醒不要直接當成 CC 授權作品使用。

## 專案結構

```text
.
├── README.md
├── LICENSE
└── skills/
    └── find-cc-license-and-attribution/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── patterns/
            │   ├── INDEX.md
            │   ├── google-docs-footer.md
            │   ├── openmuseum-license-link.md
            │   ├── tcmb-split-license.md
            │   └── ocf-explicit-attribution.md
            └── templates/
                └── output-templates.md
```

## 設計原則

主 `SKILL.md` 保持短而可執行，放核心流程、輸出格式與保守判斷規則。平台或網站案例放在 `references/patterns/`，只在遇到相似情境時讀取，避免 skill 變成過長的案例百科。

## 安裝使用

若要讓 Codex 自動發現這個 skill，可以把 skill 資料夾複製或 symlink 到你的 Codex skills 目錄：

```bash
cp -R skills/find-cc-license-and-attribution ~/.codex/skills/
```

之後可用類似提示：

```text
Use $find-cc-license-and-attribution 判讀這個網頁的創用 CC 授權並產生繁中標示表。
```

## 授權

本專案的文字、skill 內容、patterns 與 templates 採用 `CC BY 4.0` 授權。若未來加入程式碼，可再另外加入程式碼授權檔。
