---
kind: deck
deck_id: hh-os-light
category: brand
summary: 鴻海 OS Light 原始 PowerPoint 範本的 Mirror；保留 8 張來源投影片及其順序、來源主題與投影片實際使用的 Master/Layout 結構。
keywords: [鴻海, Hon Hai, OS Light, 企業簡報]
primary_color: "#083C63"
replication_mode: mirror
native_structure_mode: structured
canvas_format: ppt169
canvas_width: 1280
canvas_height: 720
canvas_viewbox: "0 0 1280 720"
source_viewbox: "0 0 1280 720"
page_count: 8
---

# Hon Hai OS Light — Mirror Template Design Spec

## I. Template Overview

此範本以 `projects/HH_Template_OS_Light.pptx` 為唯一原稿，保留 8 張投影片的頁面順序、畫面內容、來源 Master、Layout、placeholder 身分與匯入後可承載的原生屬性。用途、受眾與交付情境未由原稿明確限定；套用時依當前簡報材料決定。

Mirror 僅發布原始投影片引用的結構：本範本保留 1 個 Master 與 6 個 Layout。來源另有 7 個未被這 8 張投影片引用的 Layout，因此不在 Mirror 發布名冊中；若需使用這些版型，應以來源檔另行建立涵蓋未使用 Layout 的 fidelity 範本。

## II. Color Scheme

| Role | Color | Application |
| --- | --- | --- |
| 深藍 | `#083C63` | 標題、頁碼、文字與結構線 |
| 藍色 | `#0052A3` | 章節與流程重點 |
| 珊瑚紅 | `#FA574F` | 項目符號及局部強調 |
| 白色 | `#FFFFFF` | 內容頁底色與深色圖形上的文字 |

顏色依匯入 SVG 中可見的來源色值記錄；沒有另行建立色彩變體。

## III. Typography

| Role | Source font declaration | Application |
| --- | --- | --- |
| 標題與內文 | `Arial`, `Microsoft YaHei`, sans-serif | 中文與英文標題、內文及清單 |
| 頁碼與頁尾 | `Microsoft YaHei`, `Tahoma`, sans-serif；部分頁尾使用 `Arial`, `Microsoft JhengHei`, sans-serif | 頁碼、版權文字與小型標籤 |

字型名稱照來源 SVG 記錄；實際顯示依使用端已安裝字型及 PowerPoint 字型替代行為而定。

## IV. Signature Design Elements

- 淺色內容頁使用白底、深藍文字與留白；`#FA574F` 用於項目層級或局部提示。
- 保留原稿頁首標題、頁碼、頁尾及內容區的既有位置與比例；頁碼與頁尾沿用來源 placeholder。
- 原生 clipArt placeholder 以 `clipart` 語意槽輸出，映射回 OOXML `clipArt` 類型，不降級為一般圖片 placeholder。
- 本範本為來源頁面 Mirror；不重排頁面、不補造來源未使用的 Layout prototype，也不將來源內容重繪成另一套設計。

## V. Page Roster

| File | Master | Layout key | PowerPoint picker name | Slots |
| --- | --- | --- | --- | --- |
| `001_cover.svg` | master_01 | layout_01 | 1_cover | slot-layout_01-15: slide-number, slot-layout_01-16: footer |
| `002_toc.svg` | master_01 | layout_02 | 1_agenda | slot-layout_02-5: slide-number, slot-layout_02-6: footer, slot-layout_02-2: title, slot-layout_02-8: body |
| `003_content.svg` | master_01 | layout_03 | 1_new category | slot-layout_03-5: title, slot-layout_03-6: slide-number, slot-layout_03-7: footer |
| `004_toc.svg` | master_01 | layout_07 | 1_content page | slot-layout_07-9: title, slot-layout_07-3: slide-number, slot-layout_07-7: footer, slot-layout_07-4: object, slot-layout_07-5: clipart |
| `005_content.svg` | master_01 | layout_07 | 1_content page | slot-layout_07-9: title, slot-layout_07-3: slide-number, slot-layout_07-7: footer, slot-layout_07-4: object, slot-layout_07-5: clipart |
| `006_chapter.svg` | master_01 | layout_13 | 7_ending page | slot-layout_13-15: slide-number, slot-layout_13-16: footer |
| `007_toc.svg` | master_01 | layout_12 | 6_reference page | slot-layout_12-3: slide-number, slot-layout_12-12: title, slot-layout_12-13: object |
| `008_ending.svg` | master_01 | layout_12 | 6_reference page | slot-layout_12-3: slide-number, slot-layout_12-12: title, slot-layout_12-13: object |

Slots `none` means the source package declared no PowerPoint placeholder; editable text targets are listed in `template_execution/<prototype>.text-slots.json`.

### Source Preservation Map

Source package SHA-256: `08d66df08c9f7010e51caa2491ebf9020f0eae7d1e4cfba49c3047b16a13ad18`

| Source slide | Template | Master | Layout |
| --- | --- | --- | --- |
| 1 | `001_cover.svg` | master_01 | layout_01 |
| 2 | `002_toc.svg` | master_01 | layout_02 |
| 3 | `003_content.svg` | master_01 | layout_03 |
| 4 | `004_toc.svg` | master_01 | layout_07 |
| 5 | `005_content.svg` | master_01 | layout_07 |
| 6 | `006_chapter.svg` | master_01 | layout_13 |
| 7 | `007_toc.svg` | master_01 | layout_12 |
| 8 | `008_ending.svg` | master_01 | layout_12 |

Only source-slide-reachable Masters and Layouts are retained. The seven omitted source Layouts are `layout_04`, `layout_05`, `layout_06`, `layout_08`, `layout_09`, `layout_10`, and `layout_11`.

## VI. Assets

隨範本封裝的圖片與向量資產均由原稿匯入，不另行補圖或改繪。來源匯入報告記錄 14 項 recovery warnings；查看 `projects/HH_Template_OS_Light.pptx` 的原始檔作為精確視覺基準，尤其注意匯入器無法完整重建的線條斜接、外陰影屬性與轉場資訊。Mirror 不保證這些資訊在 SVG/PPTX 預覽中與 PowerPoint 原稿完全一致。
