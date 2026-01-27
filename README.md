# esp32s3-watch-gemini-live-directconn

這裡提供下載的韌體檔案 是專門build給Waveshare ESP32-S3-Touch-AMOLED-1.75 or ESP32-S3 2.06寸 AMOLED <BR>
The firmware file available for download here is specifically built for the Waveshare ESP32-S3-Touch-AMOLED-1.75 or ESP32-S3 2.06-inch AMOLED displays.<BR>
https://www.waveshare.net/shop/ESP32-S3-Touch-AMOLED-1.75.htm </p>
https://www.waveshare.net/shop/ESP32-S3-Touch-AMOLED-2.06-EN.htm </p>
<H1>功能簡介</H1>
這韌體 提供 直接透過WiFi 連上Gemini Live 進行具有情緒感知的語音對話, 不需要中間架設伺服器轉接<BR>

This firmware allows for direct WiFi connection to Gemini Live for emotion-aware voice conversations without the need for an intermediary server. <BR>
<img width="441" height="461" alt="image" src="https://github.com/user-attachments/assets/cc4784ab-1fff-4057-b44d-a70daf7a0d6e" /> <BR>

底下是DEMO影片 (via facebook or youtube) 
https://www.facebook.com/share/v/1aFy7rsWeZ/ or
https://youtube.com/shorts/7TGrHV79h8U?feature=share or 
https://portaly.cc/Timemate </p>

AI外的實用功能:

1. 提供載具條碼或會員QRCODE甚至於是 數位禮卷QRCODE顯示 方便平常購物掃描
   (請在掃描的WEB網頁畫面點選 標籤與序號設定, 載具建議選code39編碼, 大全聯紙本會員固定卡號選 code128, 其他大部分都可以用QRCODE) <BR>
   <img width="449" height="494" alt="image" src="https://github.com/user-attachments/assets/eb6144ac-52a1-4ca6-82e5-0cefe39c8cb7" /> <BR>

2. 及時新竹客運從台北新竹的車號, 以及站點追蹤 (如果你GEMINI AI設定成功, 這邊會同步發出聲音報告車況). 或 往台北在馬偕站上車的等待時間<BR>
   <img width="441" height="462" alt="image" src="https://github.com/user-attachments/assets/ab8fe93c-1c4f-4e10-b289-424015eb5d82" /><BR>
<img width="454" height="469" alt="image" src="https://github.com/user-attachments/assets/2b212dc8-d23b-48a1-8913-e3d4b3bba932" /><BR>

3. 基於個人五行, 所反映的當下時間的五行十神曆 . 以及當天及當月 由五行生剋所計算的分數 (需要在WEB畫面點選個人基本資料 輸入生日 及時間)<BR>
<img width="444" height="508" alt="image" src="https://github.com/user-attachments/assets/c7c17d9a-00b7-4201-8d64-bbbb5cc519e9" /> <BR>

4. 天氣查詢 (需要填入TWMOE_API_KEY)<BR>
 <img width="435" height="413" alt="image" src="https://github.com/user-attachments/assets/6851ea9e-6801-4583-a5d3-6a6975730e1a" /><BR>

5. 隨著手錶角度 移動眼珠的無聊喵喵<BR>
<img width="340" height="388" alt="image" src="https://github.com/user-attachments/assets/af74aba9-f738-4bac-8a34-6a16c75e6cfb" /><BR>

6. 手機如果有裝特定APP可以把訊息 整5分鐘倍數時 轉發到手錶. (手錶整5分鐘時 也會醒來啟動藍芽然後再休眠)<BR>

<H1>開關機, 電源相關重要訊息</H1>

1.手錶在 有USB供電時, 如果熄滅 可以藉由碰觸螢幕喚醒<BR>
2. 單純電池供電時, 螢幕五秒會熄滅<BR>
3A. 使用鋰電池請多加小心. 本軟體不負鋰電池或設備使用造成損失的賠償責任 . 此設備由硬體電源管理晶片控制充電 . 在醒著或輕度睡眠下, UI電源控制畫面 可以選擇強制關閉充電或開啟充電. 
在完全關機下 也可以充電, 但充電節奏完全由電源控制晶片控制<BR>
3B. 充電時可能會到40多度, 螢幕超過37度就會顯示紅色的字. 停止充電後, 如果溫度還高, 會自動重開機. 一兩次後溫度就會降回30度左右.<Br>
4. 充電允許開啟狀態下, 電源到70%下會啟動自動充電. 也可以按"!"強制啟動.<BR>
5. 充到100%, 電源晶片會自動停止充電. 但如果看到畫面顯示一下充一下不充, 請按強制關閉充電. 表示你電池已經老舊. 目前參數設定是預設的充到4.2V and 100mA電流以下, 電源晶片會停止充電.<BR>
6. 螢幕熄滅15秒後, 會lightsleep, 要藉由模擬手碗舉起扭轉晃動 喚醒<BR>
7. 每5分鐘手表會自動醒來與手機APP的藍芽同步 如果手錶APP有攔截到訊息 會從手機發送到手錶 (需安裝特定手機APP)<BR>
8. 如果擺著不動 超過45分鐘. 為了省電會自動關機. <BR>
9. 這時要輕按一下外殼右側 SD插槽 上方按鈕. 放開後會開機,不過螢幕大約三秒內才會亮起, <BR>
10. 同樣的按鍵 長按六秒 硬體電源管理晶片 會關機 (任何緊急情況 都可以使用)<BR>
11. 插著USB當時中用的時候, 到了晚上9:30~06:00 螢幕會熄滅, 但系統還開著 碰一下會亮起, 三四秒後會熄掉<BR>
12. 整點會發出咚一聲..<BR>

<H1>起始設定</H1>

系統一開始 為了要取得能連上Internet的 WiFi account/password , 會先開起一個名為WATCH的WIFI基地台. <BR>
<img width="392" height="376" alt="image" src="https://github.com/user-attachments/assets/fdef8a69-5512-441c-939a-68400822096f" />
請用手機選擇連上這個基地台後, 掃描手錶螢幕上的QRCODE開啟瀏覽器進行後續設定. <BR>
在手機瀏覽器上會看到底下畫面, 等他幾秒鐘下載完成, 太快點會沒反應</p>
<img width="717" height="566" alt="image" src="https://github.com/user-attachments/assets/fc5a5e89-70e1-4be8-b6b5-a3c8617cc8f3" /><BR>
等他幾秒鐘下載完成, 點選WiFi存取點設定, 會看到底下畫面, 接著打入你的WiFi帳號密碼, 可以多組 然後按送出WiFi設定 <BR>
<img width="701" height="804" alt="image" src="https://github.com/user-attachments/assets/fdf5a362-2c57-43e9-8b7a-d0bbefa21639" /><BR>

成功後會得到提示, 但畫面依舊留在這頁. <BR>
<img width="456" height="140" alt="image" src="https://github.com/user-attachments/assets/66e552e2-4da0-4d1d-95e4-72a1de9503f2" /> <BR>

另一方面, 手表會自動重開機, 並透過你提供的WIFI,連上internet ntp進行自動對時.<BR>
<img width="436" height="553" alt="image" src="https://github.com/user-attachments/assets/20098ddb-4377-4864-a829-51795f494017" />

<H1>Gemini AI KEY取得與輸入</H1>
目前使用的Gemini Live 是免費的測試版本model: models/gemini-2.5-flash-native-audio-preview-12-2025 <BR>
儘管免費, 為了進行Gemini Live, 你得在gemini studio申請一把key. 
https://aistudio.google.com/api-keys <BR>
手把手申請API教學文件可以參考: https://lifecheatslab.com/freegeminiapi/ <BR>
為了安心你可以設定他所屬的project有預算限制, 例如設定一塊美金. 如果真的發生收費也不會超支。
事實上google提供每個新帳號300美金的有限時間試用 根本用不掉 就到期了. </p>

anyway, 在你拿到key之後, 一樣透過手錶提供的網頁 輸入KEY。 <BR>
請滑動你的手表 來找QRCODE. 手錶的UI展開是一個如下的圖案, 起始點是時間頁 範例時間是15:41
<img width="887" height="704" alt="image" src="https://github.com/user-attachments/assets/5097362e-1a7c-4de8-a9d7-6823f6755307" />

先從時間頁, 範例中時間是15:41 開始 <BR>
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
(Wifi用完會30秒後為了省電會自動關閉, 所以如果WIFI斷線, 在這邊會預先花點時間連上WIFI) <BR>
畫面出現轉轉時 會暫時限制滑動 因為在連線網路 最好不要動它... <BR>
<img width="431" height="500" alt="image" src="https://github.com/user-attachments/assets/baccca12-09f5-452d-a707-e8a6b52c0dc7" /> <BR>

<img width="435" height="505" alt="image" src="https://github.com/user-attachments/assets/1e39c74f-c864-4852-9d5e-9a4fbba20990" /> <BR>
<img width="441" height="461" alt="image" src="https://github.com/user-attachments/assets/cc4784ab-1fff-4057-b44d-a70daf7a0d6e" /> <BR>
不講話44秒後會斷線. 自己按下HangUp也會掛上 (要是不幸當機 三秒後會自動重開.)


   




























