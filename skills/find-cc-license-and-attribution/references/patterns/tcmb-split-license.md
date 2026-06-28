# TCMB-Style Split License Pattern

## Use When

Use this pattern for cultural memory, archive, museum, or collection records where the page may separately license the digital object, description text, and metadata.

## Main Risk

The page may have several reusable objects. A photo, record description, metadata, and platform UI may not share the same license.

## Check

1. Identify the reusable object: image, document scan, audio/video, description text, metadata, or the whole record page.
2. Look for file-level license icons, rights labels, citation fields, and collection-holder fields.
3. Check whether the platform gives a required attribution statement.
4. Check whether `授權人`, `典藏者`, `建檔單位`, `原攝`, `原撰`, or `著作財產權人` appear as attribution candidates.
5. Separate non-CC or unclear materials into their own rows.

## Output Rows

| 使用對象 | Attribution / 應標示對象 | CC 授權名稱 |
|---|---|---|
| **數位物件／圖片：頁面代表圖像** | 依頁面數位物件引用資訊、典藏者、作者或建檔單位標示 | 依物件層級授權正規化 |
| **內容描述／文字：藏品頁描述文字** | 依頁面內容描述引用資訊、撰寫者、建檔單位或來源網站標示 | 依文字或平台授權正規化；不明時填 `未明確標示` |
| **平台 UI／Logo／商標** | 各商標或標誌權利人 | 非 CC：不在授權範圍內 |

## Notes

If rights holder and original creator differ, preserve both roles instead of flattening the attribution to one name.
