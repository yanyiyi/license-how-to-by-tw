---
name: find-cc-license-and-attribution
description: Find and interpret Creative Commons licensing information for webpages, images, articles, datasets, slide decks, videos, documentation pages, cultural heritage records, and other online works, then produce attribution-ready Traditional Chinese output. Use when Codex needs to decide whether a work is CC licensed, what object or part the license applies to, who should be attributed, how to normalize the license name, how to handle unclear or conflicting license signals, or how to prepare attribution tables for Taiwan-facing reuse.
---

# Find CC License and Attribution

## Purpose

Use this skill to locate visible Creative Commons license evidence, interpret what the license applies to, and produce a practical attribution table in Traditional Chinese.

This skill is for license and attribution triage, not legal advice. Do not say a work is CC licensed unless explicit evidence connects the license to the work or object being reused.

## Output Contract

Prefer a concise table over a long explanation:

| 使用對象 | Attribution / 應標示對象 | CC 授權名稱 |
|---|---|---|
| 明確指稱頁面中的物件或內容類型 | 授權人要求標示的作者、創作者、機構、作品名稱、來源或指定標示文字 | 正規化後的 CC 授權名稱 |

Make `使用對象` specific. Prefer labels such as:

- `文字內容：頁面主要文件說明`
- `圖像／數位檔案：頁面主圖`
- `內容描述／文字：藏品頁描述文字`
- `程式碼範例：文件中的 code block`
- `頁面整體內容：footer 所指稱的 this page and its contents`
- `Logo／商標／品牌特徵`

Avoid vague labels such as `本頁`, `內容`, `資料`, or `素材` unless the source itself clearly uses that scope.

After the table, add only the notes needed to prevent misuse: uncertainty, excluded objects, evidence to preserve, or next steps.

## Core Rules

- Do not assume a work is open or CC licensed because it is free to read, publicly accessible, open access, or hosted on a familiar platform.
- Prefer the most specific license statement closest to the object being reused.
- Separate rows when a page distinguishes text, image, metadata, code, dataset, embedded media, logo, trademark, third-party material, or fair-use material.
- Treat citation text as attribution guidance, not automatically as license evidence.
- Use the source's explicit attribution instruction first when it exists.
- If the result is unclear, write `未明確標示` instead of guessing.
- If the user needs reuse in a public, institutional, commercial, or high-visibility context, recommend preserving license evidence.

## License Name Normalization

Normalize Creative Commons licenses into compact standard names:

- `CC BY 4.0`
- `CC BY-SA 4.0`
- `CC BY-NC 3.0 TW +`
- `CC BY-NC-SA 3.0 TW +`
- `CC BY-NC-ND 3.0 TW`
- `CC0 1.0`
- `Public Domain Mark 1.0`

If the item is not CC, write a clear non-CC status:

- `非 CC：Apache 2.0`
- `非 CC：不在授權範圍內`
- `非 CC：合理使用／未納入整體授權`
- `未明確標示`

## Search Workflow

1. Check the current page for footer text, article footer, image caption, metadata, citation fields, license fields, copyright notices, rights statements, reuse instructions, and credit lines.
2. Search page text for `Creative Commons`, `CC`, `CC BY`, `CC-BY`, `CC BY-SA`, `CC BY-NC`, `CC BY-NC-SA`, `CC BY-NC-ND`, `CC0`, `Public Domain`, `創用 CC`, `姓名標示`, `非商業`, `相同方式分享`, `禁止改作`, `授權`, `著作權`, `版權`, `權利標示`, `引用資訊`, `unless otherwise noted`, `except where otherwise noted`, `this work is licensed under`, `credit line`, and `cite as`.
3. Check homepage, site-wide footer, About, Terms of Use, Copyright, License, FAQ, repository README, or dataset license files only when the current page has no object-level license.
4. Inspect license links and icons. Useful URL patterns include `creativecommons.org/licenses/`, `creativecommons.org/publicdomain/zero/`, `creativecommons.org/publicdomain/mark/`, and `rightsstatements.org/`.
5. Infer a license from a URL only when the link is attached to the licensed object, footer statement, or license declaration. Do not treat a general educational link about CC as a license declaration.
6. If the current source has no clear license, search alternative sources by work title, image filename, caption, author, photographer, distinctive text excerpt, or platform-specific result. Prefer the source where the same work has the clearest credible license evidence.

## Attribution Priority

Use this order when deciding the attribution text:

1. Explicit attribution instruction, such as `請標示以下文字`, `使用時請標示`, `please include the following attribution`, `credit line`, or `attribution`.
2. Platform-generated citation or `引用資訊`, after verifying it is attribution guidance and not the license itself.
3. Work-level metadata: title, creator, photographer, writer, rights holder, publisher, collection holder, data provider, contributor, or maintaining institution.
4. Page title plus organization or platform name.

Do not simplify a complete required attribution sentence into only one person's name.

## Attribution May Include More Than Creator

CC attribution should follow the information supplied or reasonably requested by the licensor. Attribution may include:

- 原創作者 / creator
- 攝影者 / photographer
- 撰寫者 / writer
- 著作財產權利人 / rights holder
- 發行者 / publisher
- 典藏者 / collection holder
- 建檔單位 / maintaining institution
- 資助者 / funder
- 協力者 / collaborator
- 授權人指定之其他應標示者 / others designated to receive attribution

The designated person or organization should have a reasonable relationship to the work's authorship, production, preservation, publication, funding, or release context.

## Split-License Handling

When a page contains mixed materials, split rows instead of collapsing everything into one license.

For `unless otherwise noted` or `除另有註明外` statements, still check whether code samples, images, logos, trademarks, third-party materials, or embedded media are excluded.

For multi-source documents, slide decks, issue packages, educational materials, exhibition panels, or reports, recommend wording like:

> 除另有標示及註記者外，本作品內容採 CC BY-NC 3.0 TW + 授權釋出。

For rights-holder and creator separation, use wording that avoids confusion:

> © 國立臺灣歷史博物館，原攝 XXX，採 CC BY 3.0 TW + 發布。

## Pattern Library

Keep the main workflow first. If the source resembles a known case, read `references/patterns/INDEX.md` and then the closest pattern file.

Use patterns as checklists, not mechanical rules. Priority remains:

1. object-specific license on the current page;
2. explicit attribution instruction;
3. license link URL attached to the object;
4. footer or site-wide statement;
5. platform pattern;
6. alternative licensed source.

For reusable output snippets, read `references/templates/output-templates.md`.

## Evidence To Preserve

When a clear CC license is found, recommend preserving evidence when the reuse matters. Preserve source URL, page title, author or rights holder, license name, license link URL, screenshot of the license statement, access date, and downloaded metadata if available.

## Unclear License

If no clear license is found, output:

| 使用對象 | Attribution / 應標示對象 | CC 授權名稱 |
|---|---|---|
| 頁面內容／作品本身 | 未明確標示 | 未明確標示 |

Then say:

> 目前不建議把它當作 CC 授權作品使用。若要引用，可考慮合理引用、取得授權，或尋找其他明確採用開放授權的來源。
