# 第 5 章：使用未標記資料進行預訓練

&nbsp;
## 主要章節程式碼

- [01_main-chapter-code](01_main-chapter-code) 包含主要章節程式碼

&nbsp;
## 額外資料

- [02_alternative_weight_loading](02_alternative_weight_loading) 包含從替代位置載入 GPT 模型權重的程式碼，以防模型權重無法從 OpenAI 取得
- [03_bonus_pretraining_on_gutenberg](03_bonus_pretraining_on_gutenberg) 包含在古騰堡計畫的整個書籍語料庫上對 LLM 進行更長時間預訓練的程式碼
- [04_learning_rate_schedulers](04_learning_rate_schedulers) 包含實作更複雜的訓練函數的程式碼，包括學習率調度器和梯度裁剪
- [05_bonus_hparam_tuning](05_bonus_hparam_tuning) 包含可選的超參數調整腳本
- [06_user_interface](06_user_interface) 實作與預訓練 LLM 互動的互動式使用者介面
- [07_gpt_to_llama](07_gpt_to_llama) 包含將 GPT 架構實作轉換為 Llama 3.2 並從 Meta AI 載入預訓練權重的逐步指南
- [08_memory_efficient_weight_loading](08_memory_efficient_weight_loading) 包含額外筆記本，展示如何透過 PyTorch 的 `load_state_dict` 方法更有效地載入模型權重
- [09_extending-tokenizers](09_extending-tokenizers) 包含從零開始實作 GPT-2 BPE 分詞器
- [10_llm-training-speed](10_llm-training-speed) 展示提升 LLM 訓練速度的 PyTorch 效能技巧
- [11_qwen3](11_qwen3) 從零開始實作 Qwen3 0.6B 和 Qwen3 30B-A3B（專家混合），包括載入基礎、推理和編碼模型變體的預訓練權重的程式碼
- [12_gemma3](12_gemma3) 從零開始實作 Gemma 3 270M 和具有 KV 快取的替代方案，包括載入預訓練權重的程式碼

<br>
<br>

[![連結到影片](https://img.youtube.com/vi/Zar2TJv-sE0/0.jpg)](https://www.youtube.com/watch?v=Zar2TJv-sE0)
