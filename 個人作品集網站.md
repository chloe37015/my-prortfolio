# 個人作品集網站

一個簡約優雅的個人作品集網站，使用 HTML5 和 Tailwind CSS 構建。支持動態新增作品、編輯自我介紹、管理技能標籤，以及上傳 PDF 和圖片檔案。

## 🎯 功能特性

- ✨ **簡約白色調設計** - 專業、現代的視覺風格
- 📱 **完全響應式** - 完美適配桌面、平板和手機設備
- 🎨 **作品展示 Grid 佈局** - 優雅的卡片式作品展示
- 📝 **動態內容管理** - 隨時新增、編輯、刪除作品
- 🏷️ **技能標籤系統** - 展示專業技能和專長
- 📄 **PDF 和圖片支持** - 上傳作品相關檔案
- 💬 **聯絡表單** - 內置聯絡表單功能
- 💾 **本地存儲** - 使用瀏覽器 LocalStorage 保存數據
- 🚀 **單文件部署** - 無需後端，直接在任何服務器上運行

## 📋 包含內容

### 頁面區域

1. **導航欄** - 固定導航，快速訪問各個區域
2. **首頁 Hero 區域** - 吸引人的開場，大型標題和行動按鈕
3. **作品展示區** - 3 列 Grid 佈局，展示精選作品
4. **技能標籤區** - 展示所有專業技能和技術棧
5. **關於我** - 個人介紹和背景信息
6. **聯絡資訊** - 郵件、LinkedIn、GitHub 等聯絡方式
7. **聯絡表單** - 訪客可直接發送訊息

### 交互功能

- 新增作品 Modal
- 編輯自我介紹 Modal
- 編輯技能標籤 Modal
- 文件上傳預覽
- 表單驗證
- 成功提示訊息

## 🚀 快速開始

### 方法 1：直接在瀏覽器中打開

1. 下載 `portfolio.html` 文件
2. 用瀏覽器打開該文件
3. 開始編輯和自定義內容

### 方法 2：本地服務器運行

```bash
# 使用 Python 3
python3 -m http.server 8000

# 或使用 Python 2
python -m SimpleHTTPServer 8000

# 或使用 Node.js (如已安裝)
npx http-server
```

然後在瀏覽器中訪問 `http://localhost:8000/portfolio.html`

### 方法 3：部署到 GitHub Pages

1. 創建 GitHub 倉庫
2. 上傳 `portfolio.html` 文件
3. 在倉庫設置中啟用 GitHub Pages
4. 訪問 `https://yourusername.github.io/portfolio.html`

## 📝 使用指南

### 新增作品

1. 點擊導航欄的「+ 新增作品」按鈕
2. 填寫作品標題、描述和技能標籤
3. 上傳作品圖片或 PDF 檔案（可選）
4. 點擊「新增作品」按鈕

### 編輯自我介紹

1. 在「關於我」區域點擊「編輯自我介紹」按鈕
2. 修改自我介紹文本
3. 點擊「保存」按鈕

### 編輯技能標籤

1. 在「技能與專長」區域點擊「編輯技能」按鈕
2. 每行輸入一個技能標籤
3. 點擊「保存」按鈕

### 修改聯絡資訊

編輯 HTML 文件中的以下部分：

```html
<a href="mailto:hello@example.com">hello@example.com</a>
<a href="https://linkedin.com" target="_blank">查看我的檔案</a>
<a href="https://github.com" target="_blank">查看我的代碼</a>
```

## 🎨 自定義指南

### 修改顏色方案

在 `<style>` 標籤中修改以下 CSS 變量：

```css
/* 主要文本顏色 */
color: #333333;

/* 背景顏色 */
background-color: #ffffff;

/* 按鈕顏色 */
background-color: #000;
```

### 修改字體

在 `<style>` 標籤中修改：

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
```

### 修改 Hero 區域

編輯 `.hero-section` 中的 HTML 內容：

```html
<h1 class="text-5xl font-bold mb-6 text-black">歡迎來到我的作品集</h1>
<p class="text-xl text-gray-600 mb-8 leading-relaxed">自定義描述文本</p>
```

### 修改預設作品

在 `initializeStorage()` 函數中修改預設作品數據。

## 💾 數據存儲

所有數據都存儲在瀏覽器的 LocalStorage 中：

- `projects` - 作品列表
- `about` - 自我介紹
- `skills` - 技能標籤

**注意**：數據僅在本地瀏覽器中保存。如果清除瀏覽器緩存，數據將被刪除。

### 備份數據

要備份數據，在瀏覽器控制台中運行：

```javascript
// 導出數據
const backup = {
    projects: localStorage.getItem('projects'),
    about: localStorage.getItem('about'),
    skills: localStorage.getItem('skills')
};
console.log(JSON.stringify(backup));

// 恢復數據
const backup = { /* 之前導出的數據 */ };
localStorage.setItem('projects', backup.projects);
localStorage.setItem('about', backup.about);
localStorage.setItem('skills', backup.skills);
location.reload();
```

## 📱 響應式設計

網站使用 Tailwind CSS 的響應式網格系統：

- **桌面版** - 3 列網格
- **平板版** - 2 列網格
- **手機版** - 1 列網格

## 🔧 技術棧

- **HTML5** - 語義化標記
- **CSS3** - 現代樣式和動畫
- **Tailwind CSS** - 實用優先的 CSS 框架
- **Vanilla JavaScript** - 無依賴的交互功能
- **LocalStorage API** - 客戶端數據存儲

## 📦 文件結構

```
portfolio.html          # 單一 HTML 文件，包含所有代碼
README.md              # 本文件
```

## 🌐 部署選項

### 1. GitHub Pages（推薦）

```bash
git init
git add portfolio.html README.md
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/portfolio.git
git push -u origin main
```

然後在 GitHub 倉庫設置中啟用 Pages。

### 2. Netlify

1. 訪問 [Netlify](https://netlify.com)
2. 拖拽 `portfolio.html` 文件到 Netlify
3. 自動部署完成

### 3. Vercel

1. 訪問 [Vercel](https://vercel.com)
2. 導入 GitHub 倉庫
3. 自動部署完成

### 4. 自托管服務器

直接將 `portfolio.html` 上傳到任何支持靜態文件的服務器。

## 🎯 下一步改進

- [ ] 添加暗黑模式切換
- [ ] 集成後端 API 用於郵件發送
- [ ] 添加圖片懶加載
- [ ] 添加動畫效果
- [ ] 添加多語言支持
- [ ] 集成分析工具
- [ ] 添加博客功能
- [ ] 集成 CMS 系統

## 📄 許可證

此項目採用 MIT 許可證。詳見 LICENSE 文件。

## 💡 提示

- 定期備份您的數據
- 使用不同瀏覽器測試響應式設計
- 在部署前在本地測試所有功能
- 考慮添加 Google Analytics 追蹤訪客

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

## 📧 聯絡

如有問題或建議，請提交 Issue 或直接聯絡。

---

**祝您使用愉快！** 🚀
