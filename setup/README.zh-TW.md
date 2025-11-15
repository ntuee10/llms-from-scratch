# 可選設定說明

本文件列出了設定您的機器和使用本儲存庫程式碼的不同方法。建議您從頭到尾瀏覽各個章節，然後決定哪種方法最適合您的需求。

&nbsp;

## 快速開始

如果您的機器上已經安裝了 Python，最快的入門方法是從本程式碼儲存庫的根目錄執行以下 pip 安裝命令，安裝 [../requirements.txt](../requirements.txt) 檔案中的套件需求：

```bash
pip install -r requirements.txt
```

<br>

> **注意：** 如果您在 Google Colab 上執行任何筆記本並想安裝相依套件，只需在筆記本頂部的新儲存格中執行以下程式碼：
> `pip install uv && uv pip install --system -r https://raw.githubusercontent.com/rasbt/LLMs-from-scratch/refs/heads/main/requirements.txt`
> 或者，在複製儲存庫後，您可以從專案根目錄使用 `uv pip install --group bonus` 安裝所有額外資料的相依套件。如果您不想在之後查看可選額外資料時單獨安裝，這會很有用。

在下面的影片中，我分享了我在電腦上設定 Python 環境的個人方法：

<br>
<br>

[![連結到影片](https://img.youtube.com/vi/yAcWnfsZhzo/0.jpg)](https://www.youtube.com/watch?v=yAcWnfsZhzo)

&nbsp;
# 本地設定

本節提供在本地執行本書程式碼的建議。請注意，本書主要章節中的程式碼設計為可在一般筆記型電腦上於合理時間內執行，不需要特殊硬體。我在 M3 MacBook Air 筆記型電腦上測試了所有主要章節。此外，如果您的筆記型電腦或桌上型電腦有 NVIDIA GPU，程式碼將自動使用它。

&nbsp;
## 設定 Python

如果您的機器上尚未設定 Python，我已在以下目錄中撰寫了我的個人 Python 設定偏好：

- [01_optional-python-setup-preferences](./01_optional-python-setup-preferences)
- [02_installing-python-libraries](./02_installing-python-libraries)

下面的*使用 DevContainers* 章節概述了在您的機器上安裝專案相依套件的替代方法。

&nbsp;

## 使用 Docker DevContainers

作為上述*設定 Python* 章節的替代方案，如果您偏好隔離專案相依套件和配置的開發設定，使用 Docker 是一個非常有效的解決方案。這種方法消除了手動安裝軟體套件和函式庫的需要，並確保一致的開發環境。您可以在以下位置找到更多關於設定 Docker 和使用 DevContainer 的說明：

- [03_optional-docker-environment](03_optional-docker-environment)

&nbsp;

## Visual Studio Code 編輯器

程式碼編輯器有很多不錯的選擇。我偏好的選擇是流行的開源 [Visual Studio Code (VSCode)](https://code.visualstudio.com) 編輯器，它可以透過許多有用的外掛和擴充功能輕鬆增強（有關更多資訊，請參閱下面的 *VSCode 擴充功能* 章節）。macOS、Linux 和 Windows 的下載說明可以在 [VSCode 主要網站](https://code.visualstudio.com)上找到。

&nbsp;

## VSCode 擴充功能

如果您使用 Visual Studio Code (VSCode) 作為主要程式碼編輯器，您可以在 `.vscode` 子資料夾中找到建議的擴充功能。這些擴充功能為本儲存庫提供了增強功能和有用的工具。

要安裝這些擴充功能，請在 VSCode 中開啟此「setup」資料夾（檔案 -> 開啟資料夾...），然後點擊右下角彈出選單中的「安裝」按鈕。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/setup/README/vs-code-extensions.webp?1" alt="1" width="700">

或者，您可以將 `.vscode` 擴充功能資料夾移動到此 GitHub 儲存庫的根目錄：

```bash
mv setup/.vscode ./
```

然後，每次您開啟 `LLMs-from-scratch` 主要資料夾時，VSCode 會自動檢查系統上是否已安裝建議的擴充功能。

&nbsp;

# 雲端資源

本節描述了執行本書程式碼的雲端替代方案。

雖然程式碼可以在沒有專用 GPU 的一般筆記型電腦和桌上型電腦上執行，但配備 NVIDIA GPU 的雲端平台可以大幅改善程式碼的執行時間，尤其是在第 5 到第 7 章。

&nbsp;

## 使用 Lightning Studio

為了在雲端獲得流暢的開發體驗，我推薦 [Lightning AI Studio](https://lightning.ai/) 平台，它允許使用者設定持久環境，並在雲端 CPU 和 GPU 上使用 VSCode 和 Jupyter Lab。

啟動新 Studio 後，您可以開啟終端機並執行以下設定步驟來複製儲存庫並安裝相依套件：

```bash
git clone https://github.com/rasbt/LLMs-from-scratch.git
cd LLMs-from-scratch
pip install -r requirements.txt
```

（與 Google Colab 相比，這些步驟只需執行一次，因為 Lightning AI Studio 環境是持久的，即使您在 CPU 和 GPU 機器之間切換也是如此。）

然後，導航到您想執行的 Python 腳本或 Jupyter Notebook。或者，您還可以輕鬆連接 GPU 來加速程式碼的執行時間，例如，當您在第 5 章預訓練 LLM 或在第 6 和第 7 章微調它時。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/setup/README/studio.webp" alt="1" width="700">

&nbsp;

## 使用 Google Colab

要在雲端使用 Google Colab 環境，請前往 [https://colab.research.google.com/](https://colab.research.google.com/)，並從 GitHub 選單開啟相應的章節筆記本，或將筆記本拖曳到 *Upload* 欄位，如下圖所示。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/setup/README/colab_1.webp" alt="1" width="700">

還要確保您將相關檔案（資料集檔案和筆記本匯入的 .py 檔案）也上傳到 Colab 環境，如下所示。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/setup/README/colab_2.webp" alt="2" width="700">

您可以選擇在 GPU 上執行程式碼，方法是變更 *Runtime*，如下圖所示。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/setup/README/colab_3.webp" alt="3" width="700">

&nbsp;

# 有問題嗎？

如果您有任何問題，請不要猶豫透過本 GitHub 儲存庫中的 [Discussions](https://github.com/rasbt/LLMs-from-scratch/discussions) 論壇聯繫我們。
