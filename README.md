# esp32s3-watch-gemini-live-directconn

這裡提供下載的韌體檔案 是專門build給Waveshare ESP32-S3-Touch-AMOLED-1.75 or ESP32-S3 2.06寸 AMOLED 
https://www.waveshare.net/shop/ESP32-S3-Touch-AMOLED-1.75.htm </p>
https://www.waveshare.net/shop/ESP32-S3-Touch-AMOLED-2.06-EN.htm </p>

這韌體 提供 直接透過WiFi 連上Gemini Live 進行具有情緒感知的語音對話
不需要中間架設伺服器轉接
<img width="441" height="461" alt="image" src="https://github.com/user-attachments/assets/cc4784ab-1fff-4057-b44d-a70daf7a0d6e" /> <BR>

底下是DEMO影片 (via facebook or youtube) 
https://www.facebook.com/share/v/1aFy7rsWeZ/ or
https://youtube.com/shorts/7TGrHV79h8U?feature=share </p>

系統一開始 為了要取得能連上Internet的 WiFi account/password , 會先開起一個名為ESP-WATCH的WIFI基地台. <BR>
請用手機選擇連上這個基地台後, 掃描QRCODE開啟瀏覽器進行設定. <BR>
在手機瀏覽器上會看到底下畫面, 等他幾秒鐘下載完成, 太快點會沒反應</p>
<img width="717" height="566" alt="image" src="https://github.com/user-attachments/assets/fc5a5e89-70e1-4be8-b6b5-a3c8617cc8f3" /><BR>
等他幾秒鐘下載完成, 點選WiFi存取點設定, 會看到底下畫面, 接著打入你的WiFi帳號密碼, 可以多組 然後按送出WiFi設定 <BR>
<img width="701" height="804" alt="image" src="https://github.com/user-attachments/assets/fdf5a362-2c57-43e9-8b7a-d0bbefa21639" /><BR>

成功後會得到提示, 但畫面依舊留在這頁. <BR>
<img width="456" height="140" alt="image" src="https://github.com/user-attachments/assets/66e552e2-4da0-4d1d-95e4-72a1de9503f2" /> <BR>

不過這時手表會自動重開機, 並使用你提供的WIFI開始對時.<BR>
<img width="436" height="553" alt="image" src="https://github.com/user-attachments/assets/20098ddb-4377-4864-a829-51795f494017" />

目前使用的Gemini Live 是免費的測試版本model: models/gemini-2.5-flash-native-audio-preview-12-2025 <BR>
儘管免費, 為了進行Gemini Live, 你得在gemini studio申請一把key. 
https://aistudio.google.com/api-keys <BR>
手把手申請API教學文件可以參考: https://lifecheatslab.com/freegeminiapi/ <BR>
為了安心你可以設定他所屬的project有預算限制, 例如設定一塊美金. 如果真的發生收費也不會超支。
事實上google提供每個新帳號300美金的有限時間試用 根本用不掉 就到期了. </p>

anyway, 在你拿到key之後, 一樣透過手錶提供的網頁 輸入KEY。 <BR>
請滑動你的手表 來找QRCODE, 先從時間頁開始 <BR>
<img width="436" height="553" alt="image" src="https://github.com/user-attachments/assets/20098ddb-4377-4864-a829-51795f494017" /> <BR>
把畫面往右方拖拉滑過去 會看到 <BR>
<img width="427" height="412" alt="image" src="https://github.com/user-attachments/assets/d3359efe-1d6c-46ae-afba-d6eccf316c01" /> <BR>
ps. 你要是看到底下這個 就是你拖拉反了, 請反方向拖拉回去 <BR>
<img width="444" height="508" alt="image" src="https://github.com/user-attachments/assets/c7c17d9a-00b7-4201-8d64-bbbb5cc519e9" /> <BR>

在剛剛那個有太陽調亮度的畫面, 把畫面往下拖拉會看到 <BR>
<img width="439" height="429" alt="image" src="https://github.com/user-attachments/assets/d3630661-14b8-4dec-8190-ecee173332c0" /> <BR>
再把畫面往下拖拉 就會看到條碼 <BR>
<img width="461" height="428" alt="image" src="https://github.com/user-attachments/assets/db9be663-2093-4d16-bf98-c1e2c8acf079" /> <BR>

滑到QR code設定頁. 等他一下 他會自動開啟WIFI連線. 如畫面顯示, 這次他開的網址 IP是在你的WifiAP管轄下(e.g. 我的WIFIAP是Wfoff), 就不是手錶自己的AP了。 
一般來說 你的手機 在手錶AP消失後, 會自動跳回你環境下本來的AP (也就是你剛給他的)。
確定你手機基地台(AP)選對了以後, 一樣透過掃描連上網站。

這次點選API KEYS設定 看到底下畫面. 先輸入GEMINI_API_KEY那把KEY, 輸入完記得按下儲存API KEY. 一樣會有彈出一個成功的提示, 畫面一樣會留在這邊不用管。 <BR>
至於其他的可以先不用, 你想要再去申請. <BR>
openai的部分目前我關閉了沒支援. <BR>
TWMOE_API_KEY 是要連到中央氣象局用的 https://data.moenv.gov.tw/paradigm <BR>
TDX_CLIENT_ID 與 TDX_CLIENT_SECRET 是要連到 及時公路客運狀況的 https://tdx.transportdata.tw/ <BR>
<img width="706" height="715" alt="image" src="https://github.com/user-attachments/assets/a729afa4-751f-4272-b639-236b8cc001fd" /> <BR>

設定完 請反向 滑回時間頁
然後再把畫面往上托拉兩回. 
第一回 會看到 <BR>
<img width="410" height="481" alt="image" src="https://github.com/user-attachments/assets/c7f29bf5-44a6-4139-acf6-0b9d547e982e" />
第二回就會看到 <BR>
<img width="450" height="513" alt="image" src="https://github.com/user-attachments/assets/da3be03d-c102-4661-91fb-f67a3572bb3c" />

按下CALL鍵 就會企圖連上Gemini Live
(Wifi用完會30秒後為了省電會自動關閉, 所以如果WIFI斷線, 在這邊會預先花點時間連上WIFI)  <BR>
<img width="431" height="500" alt="image" src="https://github.com/user-attachments/assets/baccca12-09f5-452d-a707-e8a6b52c0dc7" /> <BR>
<img width="435" height="505" alt="image" src="https://github.com/user-attachments/assets/1e39c74f-c864-4852-9d5e-9a4fbba20990" /> <BR>
<img width="441" height="461" alt="image" src="https://github.com/user-attachments/assets/cc4784ab-1fff-4057-b44d-a70daf7a0d6e" /> <BR>
不講話44秒後會斷線. 自己按下HangUp也會掛上 (要是不幸當機 三秒後會自動重開.)




























