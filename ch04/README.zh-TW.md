# 第 4 章：從零開始實作 GPT 模型以產生文字

&nbsp;
## 主要章節程式碼

- [01_main-chapter-code](01_main-chapter-code) 包含主要章節程式碼。

&nbsp;
## 額外資料

- [02_performance-analysis](02_performance-analysis) 包含可選程式碼，分析主要章節中實作的 GPT 模型的效能
- [03_kv-cache](03_kv-cache) 實作 KV 快取以加速推論期間的文字生成
- [07_moe](07_moe) 專家混合（MoE）的解釋和實作
- [ch05/07_gpt_to_llama](../ch05/07_gpt_to_llama) 包含將 GPT 架構實作轉換為 Llama 3.2 並從 Meta AI 載入預訓練權重的逐步指南（在完成第 4 章後查看替代架構可能會很有趣，但您也可以在閱讀第 5 章後再看）

&nbsp;
## 注意力替代方案

&nbsp;

<img src="https://sebastianraschka.com/images/LLMs-from-scratch-images/bonus/attention-alternatives/attention-alternatives.webp">

&nbsp;

- [04_gqa](04_gqa) 包含分組查詢注意力（GQA）的介紹，大多數現代 LLM（Llama 4、gpt-oss、Qwen3、Gemma 3 等）使用它作為常規多頭注意力（MHA）的替代方案
- [05_mla](05_mla) 包含多頭潛在注意力（MLA）的介紹，DeepSeek V3 使用它作為常規多頭注意力（MHA）的替代方案
- [06_swa](06_swa) 包含滑動視窗注意力（SWA）的介紹，Gemma 3 等使用它
- [08_deltanet](08_deltanet) 閘控 DeltaNet 作為流行的線性注意力變體的解釋（用於 Qwen3-Next 和 Kimi Linear）

&nbsp;
## 更多資料

在下面的影片中，我提供了一個程式碼實作課程，涵蓋了一些章節內容作為補充資料。

<br>
<br>

[![連結到影片](https://img.youtube.com/vi/YSAkgEarBGE/0.jpg)](https://www.youtube.com/watch?v=YSAkgEarBGE)
