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

## AI 轉初稿與授權

第一次使用「AI 轉初稿」時，程式會從 Hugging Face 下載模型（預設是 Taiwan-Tongues 客語＋國語模型，約 3.2 GB，下載後會在本機轉成約 1.1 GB）。下載完成並核對檔案後，之後就可以完全離線使用。華語模型（Whisper turbo）也在選單裡，可另外下載。

Taiwan-Tongues 模型採用 [TRAIL–TWM](https://huggingface.co/adi-gov-tw/Taiwan-Tongues-ASR-CE-v1.0) 授權。程式會附上授權全文，AI 轉初稿視窗也有「授權」連結，並註明「初稿由 AI 產生，請人工校對」。匯出的字幕檔不會加上註記。請把 AI 輸出當作初稿，務必人工校對後再使用。

## 更新

從 V5.6 起，桌面版開啟時會自動檢查這個頁面有沒有新版本。有新版時會提醒你，也可從選單按「檢查更新…」。網頁版沒有自動檢查，請自行到 Releases 下載最新的檔案。
