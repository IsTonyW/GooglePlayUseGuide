# IAB驗證帳戶與權限設置辦法
適用對象：Google Play Developer Console帳戶擁有者(最高權限)

操作步驟說明：

*[Step1.~3.：於Google Play Developer Console 進行操作]* 

Step1. 左側選單點擊「設定」 > 「API存取權」 

Step 2. 選擇並連結你要查詢的專案(完成後會建立在「已連結的專案」底下，如果已經連結了就略過此步驟) 

Step 3. 啟用Oauth用戶端 

*[Step4.：於Google Developer Console 進行操作]* 

Step 4. 取得用戶端ID(service account client ID) 

Step 4.1. 到API管理員 > 資訊主頁 > 啟用 Google Play Android Developer API 

Step 4.2. 到API管理員 > 憑證 > 建立憑證，建立一個新的Oauth用戶端 ID > 網路應用程式 > 建立。 

Step 4.3. 將建立的用戶端ID記下，步驟5.會用到。 

Step 4.4. 到API管理員 > 憑證 > 建立憑證，建立一個新的服務帳戶金鑰 > 服務帳戶選「compute engine default service account」，金鑰類型選「JSON」> 建立。 

Step 4.5. 儲存JSON檔案，密碼為notasecret。 

Step 4.6. 點一下「管理服務帳戶」，將剛剛建立的服務帳戶ID記下，步驟7.會用到。 

*[Step5.~10.：於Google Play Developer Console 進行操作]* 

Step5. 剛剛在步驟4.3.所記下的用戶端ID這時應該會顯示在「OAUTH用戶端」底下，若未出現請按F5重新整理網頁，若仍然未出現請回到步驟4.。 

Step6. 啟用用戶端ID。 

Step7. 增加1個服務帳戶：設定 > 使用者帳戶與權限 > 邀請新使用者。 

Step8. 在電子郵件的欄位填入步驟4.6.所記下的服務帳戶ID，並勾選給予此使用者「查看財務資料」(View financial reports)的權限 > 點擊「寄送邀請」。

Step9. 到此已完成Google Play開發後台與Google API開發後台的帳戶與權限設定。 

Step10. 將以下參數交給負責介接Google IAB金流驗證 API的開發人員。

*需交給開發人員的參數* 

Clientid：步驟4.3.的用戶端ID 

Service account name：步驟4.6.的服務帳戶ID

JSON：步驟4.5.儲存的JSON金鑰檔 

JSON密碼：notasecret
