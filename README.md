# audience-finder｜受眾分析 Skill

協助你找出核心受眾，整理需求、痛點與疑慮，也能依分析製作「頭像＋重點資料」人物卡。

## 安裝到 Codex（學生適用）

這個 Skill 的必要檔案只有 `SKILL.md`，本身不需要 Python、Git、Xcode 或 API 金鑰。某些通用安裝程式會用到 Python；如果它無法啟動，可以改用直接下載檔案的方式。

將下面整段貼到 Codex：

```text
請安裝或更新 https://github.com/stw80418-hue/audience-finder 的 audience-finder Skill。
先閱讀儲存庫 README.md，使用直接下載 Markdown 檔案的方式，不使用 Python 安裝腳本或 git clone。

必要來源檔案：
https://raw.githubusercontent.com/stw80418-hue/audience-finder/main/SKILL.md

先確認目前 Codex 支援的個人 Skill 目錄與是否已有 audience-finder。
若已有可辨識的版本，備份後原地更新，避免在不同目錄建立同名副本。
新安裝依目前官方文件放入 ~/.agents/skills/audience-finder/SKILL.md；
Windows 的 ~ 是使用者家目錄。若目前版本使用其他 Skill 路徑，依實際設定處理。

使用環境已有的下載或檔案工具；macOS 可用 curl，Windows 可用 PowerShell。
先下載到暫存檔，確認下載成功、不是 HTML 錯誤頁，且 YAML 開頭包含
name: audience-finder 與 description，再放入目的地；失敗時保留舊版。
不需要為這個純文字 Skill 安裝 Python、Git 或 Xcode Command Line Tools。
若受網路或檔案權限限制，說明實際錯誤，改提供手動下載方式。

完成後回報檔案位置，確認能否辨識 Skill；若尚未出現，提醒我重新啟動 Codex。
不要把檔案已下載當成已確認載入，也不要宣稱安裝 Skill 就會開通生圖功能。
```

## Mac 出現 Command Line Tools 安裝視窗怎麼辦？

如果只是為了安裝這個 Skill，可以取消該視窗，再貼上面的安裝指令，改走直接下載流程。這不代表電腦上的其他開發工作也不需要 Command Line Tools。

如果 Codex 仍無法代為下載，可手動安裝：

1. 開啟 [SKILL.md 原始檔](https://raw.githubusercontent.com/stw80418-hue/audience-finder/main/SKILL.md)，儲存為 `SKILL.md`，不要存成 HTML 或 `SKILL.md.txt`。
2. 在 Finder 按 `Command + Shift + G`，前往 `~`（你的使用者家目錄）。按 `Command + Shift + .` 顯示隱藏檔案。
3. 若尚未安裝此 Skill，建立 `.agents/skills/audience-finder` 資料夾，將檔案放入。已有舊版時，請先由 Codex 確認舊版位置、備份並原地更新，避免重複安裝。
4. 回到 Codex，請它確認是否能找到 audience-finder。若沒有出現，重新啟動 Codex。

個人 Skill 目錄與手動安裝方式依據：[OpenAI 官方文件](https://learn.chatgpt.com/docs/build-skills)。不同版本的目錄設定可能不同。

## 開始使用

安裝完成後，可以直接說：

> 請使用 audience-finder。我是蝦皮電商小老闆，主要販售便宜的桌面收納盒。我想經營社群，但不知道應該優先服務誰，請幫我找出目標受眾。

確認受眾後，再說：

> 請把剛才的分析做成一張「頭像＋重點資料」的受眾人物卡，加入核心受眾一句話。

Skill 會先整理受眾，不自動跳到貼文題目發想；沒有證據的年齡、職業等推估會標示「待驗證」。

## 人物卡與生圖

優先使用當前 Codex 可用的內建生圖工具，不主動要求設定 `OPENAI_API_KEY`。Skill 是操作指引，不能安裝或開通平台未提供的工具。

若當前環境無法生圖，會提供完整人物卡文案、排版規格與生圖提示詞。只有你明確選擇 API 方式時，才另外處理金鑰與費用。
