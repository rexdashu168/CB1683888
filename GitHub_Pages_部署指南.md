# Rex大叔CB系統 GitHub Pages 部署完整指南

**目標**: 將Rex_CB_v6.0_Ultimate.html部署到GitHub Pages,讓網頁可以正常使用

**更新日期**: 2025-11-17

---

## 📋 目錄
1. [前置準備](#前置準備)
2. [檔案準備](#檔案準備)
3. [GitHub倉庫設定](#github倉庫設定)
4. [上傳檔案](#上傳檔案)
5. [啟用GitHub Pages](#啟用github-pages)
6. [常見問題排除](#常見問題排除)
7. [進階設定](#進階設定)

---

## 1️⃣ 前置準備

### 需要的東西
- ✅ GitHub帳號 (如果沒有請先註冊: https://github.com)
- ✅ Rex_CB_v6.0_Ultimate.html檔案
- ✅ 瀏覽器 (Chrome/Edge/Firefox)

### 確認檔案狀態
**當前檔案**: `Rex_CB_v6.0_Ultimate.html`
- 檔案大小: 26KB ✅ (適合GitHub)
- 包含內容: HTML+CSS+JavaScript+資料庫
- 單一檔案: ✅ (不需要外部依賴)

---

## 2️⃣ 檔案準備

### 步驟1: 重新命名檔案 ⭐ 重要!

**為什麼要重新命名?**
GitHub Pages預設會尋找`index.html`作為首頁

**操作步驟**:
```
原檔名: Rex_CB_v6.0_Ultimate.html
改成:   index.html
```

**Windows操作**:
1. 找到檔案 `Rex_CB_v6.0_Ultimate.html`
2. 右鍵 → 重新命名
3. 改成 `index.html`
4. 確認

**Mac操作**:
1. 找到檔案 `Rex_CB_v6.0_Ultimate.html`
2. 點擊檔案名稱
3. 改成 `index.html`
4. Enter確認

---

## 3️⃣ GitHub倉庫設定

### 步驟1: 登入GitHub
前往: https://github.com
輸入帳號密碼登入

### 步驟2: 建立新倉庫 (Repository)

**方法A: 使用特殊倉庫名稱 (推薦)**
```
倉庫名稱: [您的GitHub用戶名].github.io

範例:
如果您的用戶名是 rexdashu168
那倉庫名稱就是: rexdashu168.github.io

網址會是: https://rexdashu168.github.io/
```

**方法B: 使用一般倉庫名稱**
```
倉庫名稱: CB-System (或任何您喜歡的名稱)

網址會是: https://[用戶名].github.io/CB-System/
```

### 步驟3: 倉庫設定選項

填寫以下資訊:
```
Repository name: [選擇上面的方法A或B]
Description: Rex大叔168 CB智能查詢系統
Public: ✅ 選這個 (公開)
Add a README file: ☐ 不要勾選
```

然後點擊 **"Create repository"** 綠色按鈕

---

## 4️⃣ 上傳檔案

### 方法A: 網頁上傳 (最簡單) ⭐ 推薦

**步驟1: 進入上傳頁面**
建立倉庫後,您會看到:
```
Quick setup — if you've done this kind of thing before
```

找到並點擊: **"uploading an existing file"**

**步驟2: 上傳index.html**
1. 點擊 **"choose your files"** 或直接拖曳檔案
2. 選擇剛剛重新命名的 `index.html`
3. 等待上傳完成 (26KB很快)

**步驟3: Commit變更**
在頁面下方:
```
Commit message: 上傳CB查詢系統v6.0
```
點擊綠色按鈕 **"Commit changes"**

✅ 完成!

### 方法B: 使用Git命令 (進階)

如果您熟悉Git:
```bash
git clone https://github.com/[用戶名]/[倉庫名].git
cd [倉庫名]
# 將index.html複製到這個資料夾
git add index.html
git commit -m "上傳CB查詢系統v6.0"
git push origin main
```

---

## 5️⃣ 啟用GitHub Pages

### 步驟1: 進入Settings
在您的倉庫頁面:
1. 點擊上方選單的 **"Settings"** (⚙️齒輪圖示)

### 步驟2: 找到Pages設定
在左側選單:
1. 往下捲動
2. 找到並點擊 **"Pages"**

### 步驟3: 設定來源
在"Build and deployment"區塊:

**Source**: 
- 選擇 **"Deploy from a branch"**

**Branch**:
- 第一個下拉選單選 **"main"** (或 "master")
- 第二個下拉選單選 **"/ (root)"**
- 點擊 **"Save"** 按鈕

### 步驟4: 等待部署
⏰ **重要**: 第一次部署需要1-5分鐘

您會看到:
```
✅ Your site is live at https://[用戶名].github.io/[倉庫名]/
```

---

## 6️⃣ 常見問題排除

### ❌ 問題1: 404 Not Found

**可能原因**:
1. 檔案沒有命名為 `index.html`
2. Pages還在部署中(等1-5分鐘)
3. Branch設定錯誤

**解決方案**:
```
1. 確認檔案名稱是 index.html (不是 Index.html 或其他)
2. 重新檢查Settings → Pages → Branch設定
3. 清除瀏覽器快取 (Ctrl+F5)
4. 等待5分鐘後再試
```

### ❌ 問題2: 網頁顯示但功能不正常

**可能原因**:
1. 檔案上傳不完整
2. 瀏覽器快取問題
3. JavaScript載入失敗

**解決方案**:
```
1. 重新上傳檔案(覆蓋舊的)
2. 開無痕視窗測試
3. 按F12檢查Console有無錯誤
4. 確認檔案大小正確(26KB)
```

### ❌ 問題3: 網址太長或不好記

**解決方案**: 使用自訂網域 (需付費購買網域)

或使用縮網址:
```
原網址: https://rexdashu168.github.io/CB-System/
縮網址服務: 
- https://bit.ly
- https://reurl.cc
```

### ❌ 問題4: 圖表不顯示

**可能原因**: ECharts CDN載入失敗

**解決方案**:
檔案中已使用可靠的CDN,如果還是有問題:
```
打開F12 Console
看是否有 "Failed to load resource" 錯誤
如果有,可能是網路問題,換個時間或網路再試
```

### ❌ 問題5: 搜尋功能不能用

**可能原因**: 資料庫定義錯誤

**解決方案**:
```
1. 確認上傳的是最新版本(11/17的檔案)
2. F12 Console檢查是否有 "fullCBDatabase is not defined" 錯誤
3. 如果有,請重新下載修正後的檔案
```

---

## 7️⃣ 進階設定

### 選項1: 自訂網域

**步驟**:
1. 購買網域 (如: cbsystem.com)
2. 在DNS設定中加入CNAME記錄
3. 在GitHub Pages設定中輸入自訂網域
4. 等待DNS生效(24-48小時)

### 選項2: HTTPS強制啟用

**步驟**:
Settings → Pages → 勾選 "Enforce HTTPS"

### 選項3: 加入README

在倉庫中新增 `README.md`:
```markdown
# Rex大叔168 CB智能查詢系統 v6.0

專注風險 • 數據驅動 • 智能分析

## 功能特色
- 2,232檔完整CB資料庫
- 智能搜尋(CB代號/股票代號/公司名稱)
- 雙圖表系統(CB走勢+CBAS走勢)
- 競拍資料完整呈現

## 使用方式
直接訪問: https://[您的網址]

## 聯絡方式
Rex大叔168投資教室
```

---

## 📋 完整檢查清單

上線前確認:
- [ ] 檔案已重新命名為 index.html
- [ ] 檔案大小確認為 26KB
- [ ] GitHub倉庫已建立
- [ ] index.html已上傳
- [ ] GitHub Pages已啟用
- [ ] Branch設定為 main / (root)
- [ ] 等待5分鐘讓部署完成
- [ ] 測試網址可以開啟
- [ ] 測試搜尋功能正常
- [ ] 測試10檔CB都能查詢
- [ ] 測試圖表可以顯示

---

## 🎯 快速部署步驟 (濃縮版)

```
1. 將 Rex_CB_v6.0_Ultimate.html 改名為 index.html
2. 登入 GitHub
3. 建立新倉庫 (名稱: [用戶名].github.io)
4. 上傳 index.html
5. Settings → Pages → Branch選main → Save
6. 等待5分鐘
7. 訪問 https://[用戶名].github.io/
8. 完成! ✅
```

---

## 📞 如果還是有問題

**檢查順序**:
1. ✅ 檔案名稱是 `index.html` 嗎?
2. ✅ Settings → Pages 設定正確嗎?
3. ✅ 等待至少5分鐘了嗎?
4. ✅ 用無痕視窗測試過嗎?
5. ✅ F12 Console有錯誤訊息嗎?

**Debug技巧**:
```
1. 打開瀏覽器F12
2. 切換到Console標籤
3. 重新整理頁面
4. 看紅色錯誤訊息
5. 截圖錯誤訊息
6. 回報給Claude或技術支援
```

---

## 🎉 成功指標

您的網站成功部署如果:
- ✅ 網址可以正常開啟
- ✅ 首頁顯示完整(統計方塊+搜尋框)
- ✅ 輸入11011可以查到台泥一永
- ✅ 基本資料有23項完整資訊
- ✅ CB走勢圖可以顯示
- ✅ 競拍CB(13166)有完整競拍資料

**恭喜您!系統已成功上線!** 🎊

---

## 📚 參考資源

- GitHub Pages官方文件: https://pages.github.com/
- GitHub使用教學: https://guides.github.com/
- HTML基礎知識: https://developer.mozilla.org/zh-TW/docs/Web/HTML

---

**最後更新**: 2025-11-17
**版本**: v6.0部署指南
**作者**: Claude AI for Rex大叔168

祝部署順利! 🚀
