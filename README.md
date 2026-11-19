# 聽打小幫手

聽打小幫手是給電台聽打與字幕對時使用的單機工具。你可以在波形上拉字幕、邊聽邊打文稿，再匯出 SRT 或 TXT。程式不必安裝，也不必一直連網；第一次使用「AI 轉初稿」時，才會下載語音辨識模型。

這個儲存庫只放安裝檔與版本說明，不含原始碼。

## 下載

請到 [Releases](https://github.com/j2020533-star/tingda-helper-releases/releases) 下載最新版本，依你的電腦選對檔案：

| 電腦 | 下載檔案 |
| --- | --- |
| Windows（64 位元） | `TingdaHelper-x.y.z-win-x64-portable.exe` |
| Mac（Apple 晶片，M 系列） | `TingdaHelper-x.y.z-mac-arm64.tar.xz` |
| Mac（Intel） | `TingdaHelper-x.y.z-mac-x64.tar.xz` |

不確定自己的 Mac 是哪一種時：左上角蘋果選單 →「關於這台 Mac」。如果晶片寫 Apple M1、M2、M3、M4，請選 Apple 晶片版；寫 Intel 就選 Intel 版。

## 贊助開發者

聽打小幫手免費提供，若覺得好用，歡迎自願贊助開發者持續維護。贊助屬自願性質，不會解鎖任何功能，也不代表取得商業使用授權。

[前往綠界贊助頁](https://p.ecpay.com.tw/BFBDAF1)（支援信用卡、ATM、超商代碼）

<img src="assets/ecpay-qr.png" alt="手機掃描 QR Code 贊助" width="200">

手機掃描 QR Code 贊助

## Windows 第一次開啟

這份程式尚未做程式簽章，Windows 可能會出現 SmartScreen「Windows 已保護你的電腦」。請按「更多資訊」，再按「仍要執行」。

這是免安裝版本，下載後直接開啟即可，不必安裝。

## Mac 第一次開啟

這份程式尚未通過 Apple 簽章與公證，第一次開啟可能會看到「無法打開，因為無法確認開發者」。請依下列方式打開：

1. 先把 `.tar.xz` 解壓縮（可雙擊，或在「終端機」執行 `tar -xJf 檔名.tar.xz`），會得到「聽打小幫手.app」。建議把它拖到「應用程式」資料夾。
2. 按住 Control 鍵再點一下「聽打小幫手.app」（或按右鍵），選「打開」，接著在提示視窗再按一次「打開」。
3. 如果還是被擋下來，請打開「終端機」，執行：

```bash
xattr -cr /Applications/聽打小幫手.app
```

然後再從「應用程式」打開一次。也可以到「系統設定」→「隱私權與安全性」，在被擋下的提示旁按「仍要打開」。

如果出現「“聽打小幫手”已損毀，無法打開。你應該將它丟到垃圾桶」（英文是 “聽打小幫手” is damaged and can’t be opened），不是檔案壞掉，而是程式尚未經過 Apple 簽章，被 macOS 擋下來。請先把 .app 拖到「應用程式」資料夾，再用上面的 `xattr -cr /Applications/聽打小幫手.app` 指令處理，然後重新打開。每次下載新版後都要再執行一次。

## AI 轉初稿

第一次使用「AI 轉初稿」時，程式會從 Hugging Face 下載模型（預設是 Taiwan-Tongues 客語＋國語模型，約 3.2 GB，下載後會在本機轉成約 1.1 GB）。下載完成並核對檔案後，之後就可以完全離線使用。華語模型（Whisper turbo）也在選單裡，可另外下載。

程式會附上授權全文，AI 轉初稿視窗也有「授權」連結，並註明「初稿由 AI 產生，請人工校對」。匯出的字幕檔不會加上註記。授權與使用限制見下方說明。

## 授權與使用限制

聽打小幫手免費提供，但不得做商業用途。

程式中使用的 AI 模型，其使用方式請參考各模型的授權條款：

- Taiwan-Tongues-ASR-CE-v1.0 採用 [TRAIL – TWM Responsible AI License](https://huggingface.co/adi-gov-tw/Taiwan-Tongues-ASR-CE-v1.0/blob/main/LICENSE)（[模型頁](https://huggingface.co/adi-gov-tw/Taiwan-Tongues-ASR-CE-v1.0)）。
- whisper.cpp 與 OpenAI Whisper 模型採用 MIT 授權，詳見 [whisper.cpp LICENSE](https://github.com/ggml-org/whisper.cpp/blob/master/LICENSE) 與 [OpenAI Whisper LICENSE](https://github.com/openai/whisper/blob/main/LICENSE)。
- 以「選擇本機模型檔」自行載入的其他模型（例如 FormoSpeech，採用 [CC BY-NC](https://creativecommons.org/licenses/by-nc/4.0/) 非商業授權），須由使用者自行取得，並遵守該模型自己的授權條款。

AI 產生的初稿僅供參考，須人工校對。

本軟體依現況提供，不提供任何保證。

## 更新

從 V5.6 起，桌面版開啟時會自動檢查這個頁面有沒有新版本。有新版時會提醒你，也可從選單按「檢查更新…」。網頁版沒有自動檢查，請自行到 Releases 下載最新的檔案。
