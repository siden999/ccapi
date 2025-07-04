# AI Post Automator 隱私權政策

## 資料來源與蒐集方式
1. 本應用程式會定期抓取您設定的公開 RSS Feed，取得文章標題、連結與摘要內容。
2. 抓取到的內容將送往 Google Gemini 服務產生貼文文字，並與原始資料一併存入我們的 Supabase 資料庫 `posts` 資料表（包含 `source_url`、`title`、`original_content`、`ai_generated_text` 等欄位）。
3. 程式需要您的 Facebook Page ID 與 Page Access Token 才能將貼文發布到指定粉絲專頁；這些憑證僅在 Edge Function 執行時讀取，不會寫入資料庫。

## 資料使用
- 蒐集到的 RSS 文章內容與 AI 生成的貼文僅用於發佈至您的 Facebook Page，或在前端介面上供您瀏覽、修改與手動發布。
- 我們不會將上述資料出售或提供給第三方。

## 第三方服務
- **Google Gemini API**：用於生成貼文內容，傳送的文字資料僅用於貼文生成，並依照 Google 的隱私條款處理。
- **Supabase**：用於存放貼文資料與執行 Edge Functions，資料會依 Supabase 的安全機制保存。
- **Facebook Graph API**：僅用於將貼文發送到指定的 Facebook Page。

## 資料保存與刪除
- 已發布或尚未發布的貼文記錄將保留在 Supabase 資料庫中，除非您透過前端介面手動刪除。
- 如需刪除所有資料，可聯絡專案維護者協助清除。

## 聯絡方式
若您對本隱私權政策有任何疑問，或欲行使相關權利，請透過本專案 README 中提供的聯絡方式與我們聯繫。