# GitHub Pages 上傳說明

本資料夾已整理為可直接放到 GitHub Pages 的靜態網站結構。

## 上傳方式

1. 將本 ZIP 解壓縮。
2. 把解壓縮後的 `index.html`、`assets/`、`docs/` 上傳到 GitHub repository 的根目錄。
3. 在 GitHub repository 的 Settings → Pages，選擇要發布的 branch 與 root 目錄。
4. 發布後首頁會讀取 `index.html`。

## 檔案結構

```text
index.html
assets/
  maps/
    population-factor-score-5class.png
    population-density-5class.png
    conflict-heat-5class.png
    factor-score-2to10.png
    high-conflict-top20-mask.png
    population-conflict-overlay-code.png
  counties/
    09020.png
    10002.png
    ...
docs/
  image_paths.csv
  README_GitHubPages.md
```

## HTML 使用中的圖片路徑

目前 `index.html` 主要使用下列圖片路徑：

### 全臺圖

- `assets/maps/population-factor-score-5class.png`
- `assets/maps/population-density-5class.png`
- `assets/maps/conflict-heat-5class.png`

### 縣市圖

縣市分圖統一使用：

```text
assets/counties/{COUNTYCODE}.png
```

例如：

- 臺北市：`assets/counties/63000.png`
- 新北市：`assets/counties/65000.png`
- 桃園市：`assets/counties/68000.png`
- 澎湖縣：`assets/counties/10016.png`
- 金門縣：`assets/counties/09020.png`

完整對照請看：`docs/image_paths.csv`。

## 注意事項

- 本包已將原始 ZIP 中較長、含特殊字碼的檔名整理為適合 GitHub Pages 使用的簡短路徑。
- `index.html` 已改名並放在根目錄，可作為 GitHub Pages 首頁。
- 本包僅整理網站展示所需 PNG 圖片；GeoTIFF 未放入網站包，避免 GitHub Pages 載入與儲存負擔過大。
