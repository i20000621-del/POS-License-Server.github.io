POS License Server V1

Render 部署：
1. 建立新的 GitHub Repository，例如 POS-License-Server。
2. 將本資料夾內所有檔案上傳到 Repository 根目錄。
3. Render → New → Blueprint，選擇該 Repository。
4. 建立完成後，在 Render Environment 設定 ADMIN_PASSWORD。
5. 開啟 Render 網址 /login 登入。
6. 新增客戶、選方案與效期、按「產生金鑰」。
7. 金鑰第一次由 POS 呼叫 POST /api/v1/activate 時才開始計算效期。
8. POS 日後使用 POST /api/v1/verify 驗證。

重要：
- 正式環境務必修改 ADMIN_PASSWORD。
- SECRET_KEY 由 Render 自動產生。
- License Server 與客戶 POS 請分開部署。
