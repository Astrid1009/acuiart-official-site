# Acuí 官方品牌網站

以 Astro 靜態輸出，部署至 GitHub Pages。網站頁面可被一般搜尋引擎直接讀取；不在 GitHub Pages 儲存訂單或付款資料。

## 本機預覽

需要 Node.js 22 或更新版本：

```sh
npm install
npm run dev
```

## 頁面

- `/` 首頁
- `/products/` 商品總覽
- `/products/acui/` Acuí
- `/products/shadow-shadooo-wonderland/` Shadow Shadooo Wonderland
- `/collaboration/` 插畫合作
- `/stockists/` 產品銷售據點

## 上線前要補的內容

1. 在 `src/data/site.ts` 的 `shopLinks` 加入各系列實際綠界 ECShop 網址。空白時商品頁會顯示「線上商店連結準備中」。
2. 將 `public/images/` 的主視覺和 OG 分享圖換成品牌正式圖片，並依頁面調整圖片替代文字。
3. 在 `src/pages/stockists/index.astro` 填入已確認的實體銷售據點、地址與營業資訊。
4. 校對品牌正式名稱、商品名稱、合作範圍，以及退換貨、運送與隱私權資訊。
5. 確認 GitHub Repository 的 Pages Source 設定為 GitHub Actions。推送到 `main` 後，`.github/workflows/deploy.yml` 會建置並發布 `dist/`。
6. 確認 GitHub Pages 自訂網域與 DNS；正式切換 `acuiart.com` 前先安排舊站網址導向與搜尋引擎收錄轉移。
