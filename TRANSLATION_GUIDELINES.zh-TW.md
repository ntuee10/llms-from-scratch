# 繁體中文翻譯指南

## 關於本翻譯

本儲存庫包含 Sebastian Raschka 所著《Build a Large Language Model (From Scratch)》一書的繁體中文（台灣）翻譯版本。

### 原作資訊

- **原作者**: Sebastian Raschka
- **出版社**: Manning Publications
- **ISBN**: 978-1633437166
- **出版日期**: 2024年9月12日
- **原始儲存庫**: https://github.com/rasbt/LLMs-from-scratch
- **授權**: Apache-2.0

### 翻譯資訊

- **翻譯版本**: 繁體中文（台灣）
- **翻譯輔助工具**: Claude Code（Anthropic）
- **翻譯分支**: `claude/translate-book-traditional-chinese-012af33C5mQwAgkDsfVpSDLb`
- **翻譯日期**: 2025年11月

### 致謝

本翻譯專案特別感謝：
- **Sebastian Raschka**: 原作者，提供如此優質的技術書籍
- **Manning Publications**: 授權和出版原著
- **Claude Code**: Anthropic 開發的 AI 輔助工具，協助進行高品質翻譯

## 翻譯原則

### 1. 準確性優先
- 忠實於原文內容，不添加或刪減原意
- 保持技術術語的準確性
- 確保程式碼範例和註解的正確性

### 2. 台灣繁體中文標準
- 使用台灣地區的技術術語和慣用語
- 遵循台灣教育部《重編國語辭典修訂本》和《國語辭典簡編本》的用字標準
- 使用台灣資訊工程界通用的專業術語

### 3. 術語一致性
- 維護統一的術語表，確保全書用詞一致
- 專有名詞首次出現時提供英文原文對照

### 4. 可讀性
- 採用符合中文閱讀習慣的表達方式
- 保持語句流暢自然
- 適當使用標點符號和排版

## 台灣技術術語對照表

以下是本翻譯採用的台灣技術術語標準：

### 核心概念
- Large Language Model → 大型語言模型
- Deep Learning → 深度學習
- Neural Network → 神經網路
- Artificial Intelligence → 人工智慧
- Machine Learning → 機器學習
- Training → 訓練
- Pretraining → 預訓練
- Fine-tuning → 微調
- Inference → 推論

### 模型架構
- Transformer → Transformer（保留原文）
- Attention Mechanism → 注意力機制
- Self-Attention → 自注意力
- Multi-Head Attention → 多頭注意力
- Feed-Forward Network → 前饋網路
- Layer Normalization → 層正規化
- Embedding → 嵌入/嵌入層
- Token → 標記/語元

### 訓練相關
- Dataset → 資料集
- Batch → 批次
- Epoch → 訓練輪次/週期
- Learning Rate → 學習率
- Optimizer → 最佳化器
- Loss Function → 損失函數
- Gradient Descent → 梯度下降
- Backpropagation → 反向傳播
- Overfitting → 過度擬合
- Underfitting → 擬合不足

### 資料處理
- Tokenization → 分詞/標記化
- Vocabulary → 詞彙表
- Preprocessing → 前處理
- Data Augmentation → 資料擴增
- Normalization → 正規化

### 技術工具
- PyTorch → PyTorch（保留原文）
- GPU (Graphics Processing Unit) → 圖形處理器
- CPU (Central Processing Unit) → 中央處理器
- Framework → 框架
- Library → 函式庫
- Repository → 儲存庫
- Notebook → 筆記本（Jupyter Notebook）

### 評估指標
- Accuracy → 準確率
- Precision → 精確率
- Recall → 召回率
- F1 Score → F1 分數
- Perplexity → 困惑度

## 翻譯檔案結構

繁體中文翻譯檔案與原始英文檔案並存：

```
/
├── README.md              # 英文版
├── README.zh-TW.md        # 繁體中文版（台灣）
├── ch01/
│   ├── README.md          # 英文版
│   └── README.zh-TW.md    # 繁體中文版
├── ch02/
│   ├── 01_main-chapter-code/
│   │   ├── ch02.ipynb             # 英文版
│   │   └── ch02.zh-TW.ipynb       # 繁體中文版
│   ├── README.md
│   └── README.zh-TW.md
└── ...
```

## 翻譯流程

1. **準備階段**: 建立術語表和翻譯指南
2. **翻譯階段**: 按章節順序進行翻譯
3. **審閱階段**: 檢查術語一致性和翻譯品質
4. **測試階段**: 確保程式碼範例可正常執行
5. **發布階段**: 提交至指定分支

## 品質標準

### 高標準要求
- **準確性**: 技術內容必須 100% 準確
- **一致性**: 術語使用必須全書統一
- **可信度**: 不杜撰原文未提及的內容
- **完整性**: 保留所有原文資訊
- **可讀性**: 符合台灣讀者的閱讀習慣

### 檢查清單
- [ ] 所有技術術語符合台灣標準
- [ ] 程式碼註解已翻譯且正確
- [ ] 圖表說明已翻譯
- [ ] 連結和參考資料保持有效
- [ ] 排版格式正確
- [ ] 無繁簡混用情況
- [ ] 標點符號使用正確

## 維護與更新

本翻譯將隨原著更新而維護。如發現翻譯錯誤或建議改進，請：

1. 查閱術語表確認標準用法
2. 參考台灣資訊工程界慣用語
3. 保持與原文的一致性
4. 提交問題或建議至儲存庫

## 著作權聲明

- 原著內容版權歸 Sebastian Raschka 和 Manning Publications 所有
- 翻譯內容遵循原著的 Apache-2.0 授權
- 翻譯過程使用 Claude Code 輔助，但最終內容忠實於原著

---

**翻譯品質承諾**: 本翻譯堅持高標準，確保技術準確性和可讀性，為台灣讀者提供優質的學習資源。
