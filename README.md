# MS ARCHIVE — 宇宙世紀機動戰士檔案館

使用純粹 **HTML5 + CSS3 + Vanilla JavaScript** 打造的宇宙世紀機動戰士機械圖鑑網站，無須任何後端或前端框架即可直接部署至 **GitHub Pages**。

## 檔案結構

- `index.html` — 語意化 HTML5 頁面結構
- `style.css` — 純 CSS3 響應式樣式與印刷排版系統
- `script.js` — 原生 ES6+ JavaScript（機體篩選、排序、技術詳情視窗、Canvas 2D 五軸雷達圖、雙機規格對比與宇宙世紀年表）
- `src/assets/images/` — 機體靜態高畫質展示圖檔
- `.github/workflows/deploy.yml` — GitHub Actions 自動部署設定檔

## 部署至 GitHub Pages

### 方法一：直接靜態分支部署（最簡單）

1. 在 GitHub 建立新的 Repository（例如 `gundam-archive`）。
2. 將專案推送至 `main` 分支：
   ```bash
   git init
   git add index.html style.css script.js src/assets README.md
   git commit -m "Initial commit: Gundam MS Archive"
   git branch -M main
   git remote add origin https://github.com/<你的帳號>/<倉庫名稱>.git
   git push -u origin main
   ```
3. 前往 GitHub 倉庫的 **Settings → Pages**。
4. 在 **Build and deployment → Source** 選擇 **Deploy from a branch**，Branch 選 `main`、`/(root)`，點擊 **Save**。
5. 等待約 1 分鐘即可於 `https://<你的帳號>.github.io/<倉庫名稱>/` 查看網站。

### 方法二：使用 GitHub Actions 自動部署

本專案已附帶 `.github/workflows/deploy.yml`：
1. 前往 **Settings → Pages**，將 Source 改為 **GitHub Actions**。
2. 每次推送至 `main` 分支時，GitHub 將自動完成靜態網站部署。
