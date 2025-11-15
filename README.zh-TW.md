# 從零開始打造大型語言模型

本儲存庫包含開發、預訓練和微調類 GPT 大型語言模型的程式碼，是《從零開始打造大型語言模型》（[Build a Large Language Model (From Scratch)](https://amzn.to/4fqvn0D)）一書的官方程式碼儲存庫。

<br>
<br>

<a href="https://amzn.to/4fqvn0D"><img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/cover.jpg?123" width="250px"></a>

<br>

在《從零開始打造大型語言模型》（[*Build a Large Language Model (From Scratch)*](http://mng.bz/orYv)）一書中，您將透過逐步編寫程式碼，從內部徹底學習和理解大型語言模型（LLMs）的運作原理。在本書中，我將引導您建立自己的 LLM，並透過清晰的文字、圖表和範例來解釋每個階段。

本書所描述的訓練和開發小型但功能完整的教育用模型的方法，反映了建立大規模基礎模型（例如 ChatGPT 背後的模型）所使用的方法。此外，本書還包含載入大型預訓練模型權重以進行微調的程式碼。

- 官方[原始碼儲存庫](https://github.com/rasbt/LLMs-from-scratch)連結
- [Manning（出版社網站）的書籍連結](http://mng.bz/orYv)
- [Amazon.com 的書籍頁面連結](https://www.amazon.com/gp/product/1633437167)
- ISBN 9781633437166

<a href="http://mng.bz/orYv#reviews"><img src="https://sebastianraschka.com//images/LLMs-from-scratch-images/other/reviews.png" width="220px"></a>

<br>
<br>

若要下載本儲存庫的副本，請點擊 [Download ZIP](https://github.com/rasbt/LLMs-from-scratch/archive/refs/heads/main.zip) 按鈕，或在您的終端機中執行以下命令：

```bash
git clone --depth 1 https://github.com/rasbt/LLMs-from-scratch.git
```

<br>

（如果您從 Manning 網站下載了程式碼套件，請考慮造訪 GitHub 上的官方程式碼儲存庫 [https://github.com/rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch) 以取得最新更新。）

<br>
<br>

# 目錄

請注意，此 `README.md` 檔案是 Markdown（`.md`）檔案。如果您從 Manning 網站下載了此程式碼套件並在本地電腦上查看，建議使用 Markdown 編輯器或預覽器以正確顯示。如果您尚未安裝 Markdown 編輯器，[Ghostwriter](https://ghostwriter.kde.org) 是一個不錯的免費選擇。

您也可以在瀏覽器中於 GitHub 上查看此檔案和其他檔案：[https://github.com/rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)，GitHub 會自動渲染 Markdown。

<br>
<br>

> **提示：**
> 如果您需要有關安裝 Python 和 Python 套件以及設定程式碼環境的指引，建議閱讀位於 [setup](setup) 目錄中的 [README.md](setup/README.md) 檔案。

<br>
<br>

[![Code tests Linux](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-linux-uv.yml/badge.svg)](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-linux-uv.yml)
[![Code tests Windows](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-windows-uv-pip.yml/badge.svg)](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-windows-uv-pip.yml)
[![Code tests macOS](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-macos-uv.yml/badge.svg)](https://github.com/rasbt/LLMs-from-scratch/actions/workflows/basic-tests-macos-uv.yml)

| 章節標題                                              | 主要程式碼（快速存取）                                                                                                    | 所有程式碼 + 補充資料      |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| [設定建議](setup) <br/>[如何最佳閱讀本書](https://sebastianraschka.com/blog/2025/reading-books.html)                            | -                                                                                                                               | -                             |
| 第 1 章：理解大型語言模型                  | 無程式碼                                                                                                                         | -                             |
| 第 2 章：處理文字資料                               | - [ch02.ipynb](ch02/01_main-chapter-code/ch02.ipynb)<br/>- [dataloader.ipynb](ch02/01_main-chapter-code/dataloader.ipynb)（摘要）<br/>- [exercise-solutions.ipynb](ch02/01_main-chapter-code/exercise-solutions.ipynb)               | [./ch02](./ch02)            |
| 第 3 章：編寫注意力機制                          | - [ch03.ipynb](ch03/01_main-chapter-code/ch03.ipynb)<br/>- [multihead-attention.ipynb](ch03/01_main-chapter-code/multihead-attention.ipynb)（摘要）<br/>- [exercise-solutions.ipynb](ch03/01_main-chapter-code/exercise-solutions.ipynb)| [./ch03](./ch03)             |
| 第 4 章：從零開始實作 GPT 模型                | - [ch04.ipynb](ch04/01_main-chapter-code/ch04.ipynb)<br/>- [gpt.py](ch04/01_main-chapter-code/gpt.py)（摘要）<br/>- [exercise-solutions.ipynb](ch04/01_main-chapter-code/exercise-solutions.ipynb) | [./ch04](./ch04)           |
| 第 5 章：使用未標記資料進行預訓練                        | - [ch05.ipynb](ch05/01_main-chapter-code/ch05.ipynb)<br/>- [gpt_train.py](ch05/01_main-chapter-code/gpt_train.py)（摘要）<br/>- [gpt_generate.py](ch05/01_main-chapter-code/gpt_generate.py)（摘要）<br/>- [exercise-solutions.ipynb](ch05/01_main-chapter-code/exercise-solutions.ipynb) | [./ch05](./ch05)              |
| 第 6 章：針對文字分類進行微調                   | - [ch06.ipynb](ch06/01_main-chapter-code/ch06.ipynb)<br/>- [gpt_class_finetune.py](ch06/01_main-chapter-code/gpt_class_finetune.py)<br/>- [exercise-solutions.ipynb](ch06/01_main-chapter-code/exercise-solutions.ipynb) | [./ch06](./ch06)              |
| 第 7 章：針對遵循指令進行微調                    | - [ch07.ipynb](ch07/01_main-chapter-code/ch07.ipynb)<br/>- [gpt_instruction_finetuning.py](ch07/01_main-chapter-code/gpt_instruction_finetuning.py)（摘要）<br/>- [ollama_evaluate.py](ch07/01_main-chapter-code/ollama_evaluate.py)（摘要）<br/>- [exercise-solutions.ipynb](ch07/01_main-chapter-code/exercise-solutions.ipynb) | [./ch07](./ch07)  |
| 附錄 A：PyTorch 入門                        | - [code-part1.ipynb](appendix-A/01_main-chapter-code/code-part1.ipynb)<br/>- [code-part2.ipynb](appendix-A/01_main-chapter-code/code-part2.ipynb)<br/>- [DDP-script.py](appendix-A/01_main-chapter-code/DDP-script.py)<br/>- [exercise-solutions.ipynb](appendix-A/01_main-chapter-code/exercise-solutions.ipynb) | [./appendix-A](./appendix-A) |
| 附錄 B：參考資料與延伸閱讀                 | 無程式碼                                                                                                                         | [./appendix-B](./appendix-B) |
| 附錄 C：習題解答                             | - [習題解答清單](appendix-C)                                                                 | [./appendix-C](./appendix-C) |
| 附錄 D：為訓練迴圈增加功能與改進 | - [appendix-D.ipynb](appendix-D/01_main-chapter-code/appendix-D.ipynb)                                                          | [./appendix-D](./appendix-D)  |
| 附錄 E：使用 LoRA 進行參數高效微調       | - [appendix-E.ipynb](appendix-E/01_main-chapter-code/appendix-E.ipynb)                                                          | [./appendix-E](./appendix-E) |

<br>
&nbsp;

下面的心智模型總結了本書涵蓋的內容。

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/mental-model.jpg" width="650px">

<br>
&nbsp;

## 先備知識

最重要的先備知識是紮實的 Python 程式設計基礎。
具備這些知識，您將能夠充分準備探索 LLM 的迷人世界，
並理解本書中呈現的概念和程式碼範例。

如果您有一些深度神經網路的經驗，您可能會發現某些概念更為熟悉，因為 LLM 是建立在這些架構之上的。

本書使用 PyTorch 從零開始實作程式碼，不使用任何外部 LLM 函式庫。雖然精通 PyTorch 不是先決條件，但熟悉 PyTorch 基礎知識肯定會有所幫助。如果您是 PyTorch 的新手，附錄 A 提供了 PyTorch 的簡潔介紹。或者，您可能會發現我的書籍《一小時學會 PyTorch：從張量到在多 GPU 上訓練神經網路》（[PyTorch in One Hour: From Tensors to Training Neural Networks on Multiple GPUs](https://sebastianraschka.com/teaching/pytorch-1h/)）對學習基本知識很有幫助。

<br>
&nbsp;

## 硬體需求

本書主要章節中的程式碼設計為可在一般筆記型電腦上於合理時間內執行，不需要特殊硬體。這種方法確保廣大讀者都能參與學習。此外，如果有 GPU 可用，程式碼會自動使用。（請參閱[設定](https://github.com/rasbt/LLMs-from-scratch/blob/main/setup/README.md)文件以獲取其他建議。）

&nbsp;
## 影片課程

[17 小時 15 分鐘的配套影片課程](https://www.manning.com/livevideo/master-and-build-large-language-models)，我在其中逐章編寫程式碼。該課程的組織結構與本書的章節和小節一一對應，因此可以作為獨立的替代方案，或作為互補的程式碼實作資源。

<a href="https://www.manning.com/livevideo/master-and-build-large-language-models"><img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/video-screenshot.webp?123" width="350px"></a>

&nbsp;

## 配套書籍 / 續集

《從零開始打造推理模型》（[*Build A Reasoning Model (From Scratch)*](https://mng.bz/lZ5B)）雖然是一本獨立的書籍，但可以被視為《從零開始打造大型語言模型》的續集。

它從一個預訓練模型開始，實作不同的推理方法，包括推論時擴展、強化學習和蒸餾，以提升模型的推理能力。

與《從零開始打造大型語言模型》類似，《從零開始打造推理模型》（[*Build A Reasoning Model (From Scratch)*](https://mng.bz/lZ5B)）採用實作方法，從零開始實作這些方法。

<a href="https://mng.bz/lZ5B"><img src="https://sebastianraschka.com/images/reasoning-from-scratch-images/cover.webp?123" width="120px"></a>

- Amazon 連結（待定）
- [Manning 連結](https://mng.bz/lZ5B)
- [GitHub 儲存庫](https://github.com/rasbt/reasoning-from-scratch)

<br>

&nbsp;
## 習題

本書的每一章都包含若干習題。解答總結於附錄 C，相應的程式碼筆記本可在本儲存庫的主要章節資料夾中找到（例如，[./ch02/01_main-chapter-code/exercise-solutions.ipynb](./ch02/01_main-chapter-code/exercise-solutions.ipynb)）。

除了程式碼習題外，您還可以從 Manning 網站下載免費的 170 頁 PDF《測試您對從零開始打造大型語言模型的理解》（[Test Yourself On Build a Large Language Model (From Scratch)](https://www.manning.com/books/test-yourself-on-build-a-large-language-model-from-scratch)）。其中包含每章約 30 個測驗問題和解答，幫助您測試理解程度。

<a href="https://www.manning.com/books/test-yourself-on-build-a-large-language-model-from-scratch"><img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/test-yourself-cover.jpg?123" width="150px"></a>

&nbsp;
## 額外資料

多個資料夾包含可選的額外資料，供有興趣的讀者參考：
- **設定**
  - [Python 設定技巧](setup/01_optional-python-setup-preferences)
  - [安裝本書使用的 Python 套件和函式庫](setup/02_installing-python-libraries)
  - [Docker 環境設定指南](setup/03_optional-docker-environment)

- **第 2 章：處理文字資料**
  - [從零開始實作位元組對編碼（BPE）分詞器](ch02/05_bpe-from-scratch/bpe-from-scratch-simple.ipynb)
  - [比較各種位元組對編碼（BPE）實作](ch02/02_bonus_bytepair-encoder)
  - [理解嵌入層和線性層之間的差異](ch02/03_bonus_embedding-vs-matmul)
  - [使用簡單數字理解資料載入器](ch02/04_bonus_dataloader-intuition)

- **第 3 章：編寫注意力機制**
  - [比較高效多頭注意力實作](ch03/02_bonus_efficient-multihead-attention/mha-implementations.ipynb)
  - [理解 PyTorch 緩衝區](ch03/03_understanding-buffers/understanding-buffers.ipynb)

- **第 4 章：從零開始實作 GPT 模型**
  - [FLOPs 分析](ch04/02_performance-analysis/flops-analysis.ipynb)
  - [KV 快取](ch04/03_kv-cache)
  - [注意力替代方案](ch04/#attention-alternatives)
    - [分組查詢注意力](ch04/04_gqa)
    - [多頭潛在注意力](ch04/05_mla)
    - [滑動視窗注意力](ch04/06_swa)
    - [閘控 DeltaNet](ch04/08_deltanet)
  - [專家混合（MoE）](ch04/07_moe)

- **第 5 章：使用未標記資料進行預訓練**
  - [替代權重載入方法](ch05/02_alternative_weight_loading/)
  - [在古騰堡計畫資料集上預訓練 GPT](ch05/03_bonus_pretraining_on_gutenberg)
  - [為訓練迴圈增加功能與改進](ch05/04_learning_rate_schedulers)
  - [最佳化預訓練超參數](ch05/05_bonus_hparam_tuning)
  - [建立使用者介面與預訓練 LLM 互動](ch05/06_user_interface)
  - [將 GPT 轉換為 Llama](ch05/07_gpt_to_llama)
  - [從零開始實作 Llama 3.2](ch05/07_gpt_to_llama/standalone-llama32.ipynb)
  - [從零開始實作 Qwen3 密集和專家混合（MoE）模型](ch05/11_qwen3/)
  - [從零開始實作 Gemma 3](ch05/12_gemma3/)
  - [記憶體高效的模型權重載入](ch05/08_memory_efficient_weight_loading/memory-efficient-state-dict.ipynb)
  - [使用新標記擴展 Tiktoken BPE 分詞器](ch05/09_extending-tokenizers/extend-tiktoken.ipynb)
  - [PyTorch 效能技巧以加快 LLM 訓練](ch05/10_llm-training-speed)

- **第 6 章：針對分類進行微調**
  - [微調不同層和使用更大模型的額外實驗](ch06/02_bonus_additional-experiments)
  - [在 50k IMDb 電影評論資料集上微調不同模型](ch06/03_bonus_imdb-classification)
  - [建立使用者介面與基於 GPT 的垃圾郵件分類器互動](ch06/04_user_interface)

- **第 7 章：針對遵循指令進行微調**
  - [資料集工具：尋找近似重複項和建立被動語態條目](ch07/02_dataset-utilities)
  - [使用 OpenAI API 和 Ollama 評估指令回應](ch07/03_model-evaluation)
  - [產生指令微調資料集](ch07/05_dataset-generation/llama3-ollama.ipynb)
  - [改進指令微調資料集](ch07/05_dataset-generation/reflection-gpt4.ipynb)
  - [使用 Llama 3.1 70B 和 Ollama 產生偏好資料集](ch07/04_preference-tuning-with-dpo/create-preference-data-ollama.ipynb)
  - [用於 LLM 對齊的直接偏好最佳化（DPO）](ch07/04_preference-tuning-with-dpo/dpo-from-scratch.ipynb)
  - [建立使用者介面與經指令微調的 GPT 模型互動](ch07/06_user_interface)

來自[從零開始推理](https://github.com/rasbt/reasoning-from-scratch)儲存庫的更多額外資料：

- **Qwen3（從零開始）基礎**
  - [Qwen3 原始碼逐步解說](https://github.com/rasbt/reasoning-from-scratch/blob/main/chC/01_main-chapter-code/chC_main.ipynb)
  - [最佳化 Qwen3](https://github.com/rasbt/reasoning-from-scratch/tree/main/ch02/03_optimized-LLM)

- **評估**
  - [基於驗證器的評估（MATH-500）](https://github.com/rasbt/reasoning-from-scratch/tree/main/ch03)
  - [多選題評估（MMLU）](https://github.com/rasbt/reasoning-from-scratch/blob/main/chF/02_mmlu)
  - [LLM 排行榜評估](https://github.com/rasbt/reasoning-from-scratch/blob/main/chF/03_leaderboards)
  - [LLM 作為評審的評估](https://github.com/rasbt/reasoning-from-scratch/blob/main/chF/04_llm-judge)

<br>
&nbsp;

## 問題、回饋與貢獻本儲存庫

我歡迎各種回饋，最好透過 [Manning 論壇](https://livebook.manning.com/forum?product=raschka&page=1)或 [GitHub Discussions](https://github.com/rasbt/LLMs-from-scratch/discussions) 分享。同樣地，如果您有任何問題或只是想與其他人交流想法，也請不要猶豫在論壇上發表。

請注意，由於本儲存庫包含與實體書相對應的程式碼，我目前無法接受會擴展主要章節程式碼內容的貢獻，因為這會導致與實體書的偏差。保持一致有助於確保每個人都有流暢的體驗。

&nbsp;
## 引用

如果您發現本書或程式碼對您的研究有用，請考慮引用。

芝加哥風格引用：

> Raschka, Sebastian. *Build A Large Language Model (From Scratch)*. Manning, 2024. ISBN: 978-1633437166.

BibTeX 條目：

```
@book{build-llms-from-scratch-book,
  author       = {Sebastian Raschka},
  title        = {Build A Large Language Model (From Scratch)},
  publisher    = {Manning},
  year         = {2024},
  isbn         = {978-1633437166},
  url          = {https://www.manning.com/books/build-a-large-language-model-from-scratch},
  github       = {https://github.com/rasbt/LLMs-from-scratch}
}
```

---

## 關於本繁體中文翻譯

本繁體中文（台灣）翻譯版本由 Claude Code（Anthropic）輔助完成，遵循台灣技術術語標準，旨在為台灣讀者提供高品質的學習資源。

**原作者**: Sebastian Raschka
**出版社**: Manning Publications
**翻譯輔助**: Claude Code
**翻譯指南**: 請參閱 [TRANSLATION_GUIDELINES.zh-TW.md](TRANSLATION_GUIDELINES.zh-TW.md)

所有版權歸原作者和出版社所有。本翻譯遵循原著的 Apache-2.0 授權。
