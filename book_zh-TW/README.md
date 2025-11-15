# 繁體中文版書籍建置系統

本目錄包含《從零開始打造大型語言模型》繁體中文（台灣）版本的 LaTeX 原始檔和建置系統。

## 目錄結構

```
book_zh-TW/
├── main.tex                 # 主 LaTeX 檔案
├── Makefile                 # 建置腳本
├── README.md                # 本檔案
├── references.bib           # 參考文獻資料庫
├── metadata.xml             # EPUB 元資料
├── epub-style.css           # EPUB 樣式
├── cover.jpg                # 封面圖片
├── chapters/                # 章節目錄
│   ├── ch01.tex            # 第 1 章
│   ├── ch02.tex            # 第 2 章
│   ├── ch03.tex            # 第 3 章
│   ├── ch04.tex            # 第 4 章
│   ├── ch05.tex            # 第 5 章
│   ├── ch06.tex            # 第 6 章
│   ├── ch07.tex            # 第 7 章
│   ├── appendix-A.tex      # 附錄 A
│   ├── appendix-B.tex      # 附錄 B
│   ├── appendix-C.tex      # 附錄 C
│   ├── appendix-D.tex      # 附錄 D
│   └── appendix-E.tex      # 附錄 E
├── figures/                 # 圖片目錄
│   ├── ch01/               # 第 1 章圖片
│   ├── ch02/               # 第 2 章圖片
│   └── ...
└── code/                    # 程式碼片段
    ├── ch02/
    ├── ch03/
    └── ...
```

## 系統需求

### 必要工具

1. **XeLaTeX**: 支援中文的 LaTeX 編譯器
2. **biber**: 參考文獻管理工具
3. **makeindex**: 索引生成工具
4. **Pygments**: Python 程式碼高亮庫
5. **中文字型**: Noto Serif/Sans CJK TC

### 可選工具

1. **pandoc**: 用於生成 EPUB 格式
2. **inotify-tools**: 用於檔案監看模式（Linux）

## 安裝依賴

### Ubuntu/Debian

```bash
make install-deps-ubuntu
```

或手動安裝：

```bash
sudo apt-get update
sudo apt-get install -y texlive-xetex texlive-latex-extra texlive-fonts-recommended
sudo apt-get install -y texlive-bibtex-extra biber
sudo apt-get install -y python3-pygments
sudo apt-get install -y pandoc
sudo apt-get install -y fonts-noto-cjk fonts-noto-cjk-extra
```

### macOS

```bash
make install-deps-macos
```

或手動安裝：

```bash
brew install --cask mactex
brew install pandoc
pip3 install pygments
```

然後手動安裝 Noto CJK 字型。

### Windows

1. 安裝 [MiKTeX](https://miktex.org/) 或 [TeX Live](https://www.tug.org/texlive/)
2. 安裝 [Python](https://www.python.org/) 並執行 `pip install pygments`
3. 安裝 [pandoc](https://pandoc.org/)
4. 安裝 Noto CJK 字型

## 建置說明

### 檢查依賴

```bash
make check-deps
```

### 建立 PDF

```bash
make pdf
```

或使用預設目標：

```bash
make
```

### 快速編譯（測試用）

僅編譯一次，不處理參考文獻和索引：

```bash
make quick
```

### 建立 EPUB

```bash
make epub
```

### 建立所有格式

```bash
make all-formats
```

### 清理輔助檔案

```bash
make clean
```

### 完全清理（包含輸出檔案）

```bash
make cleanall
```

### 監看模式（自動重新編譯）

```bash
make watch
```

### 顯示幫助

```bash
make help
```

## 程式碼高亮

本書使用 `minted` 套件進行程式碼高亮，支援多種程式語言：

### Python 程式碼區塊

```latex
\begin{minted}{python}
import torch
print("Hello, LLM!")
\end{minted}
```

### 行內程式碼

```latex
使用 \pyinline{torch.nn.Module} 來定義模型。
```

### 包含外部程式碼檔案

```latex
\inputminted[linenos,frame=lines]{python}{code/ch02/example.py}
```

## 圖片處理

### 插入圖片

```latex
\begin{figure}[H]
    \centering
    \includegraphics[width=0.8\textwidth]{ch01/mental-model.jpg}
    \caption{LLM 開發的心智模型}
    \label{fig:ch01-mental-model}
\end{figure}
```

### 引用圖片

```latex
如圖 \ref{fig:ch01-mental-model} 所示...
```

## 數學公式

### 行內公式

```latex
損失函數 $L = -\sum_{i} y_i \log(\hat{y}_i)$ 用於...
```

### 獨立公式

```latex
\begin{equation}
    \text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
    \label{eq:attention}
\end{equation}
```

## 術語標註

首次出現專業術語時，使用 `\term` 命令標註英文：

```latex
\term{注意力機制}{Attention Mechanism} 是 Transformer 的核心...
```

## 自訂環境

### 定理

```latex
\begin{theorem}
    注意力機制的時間複雜度為 $O(n^2 \cdot d)$。
\end{theorem}
```

### 範例

```latex
\begin{example}
    以下是一個簡單的 GPT 模型實作...
\end{example}
```

### 註記

```latex
\begin{remark}
    注意：此處省略了梯度裁剪的實作。
\end{remark}
```

## 品質控制

### 拼字檢查

```bash
aspell -t -c main.tex
```

### 字數統計

```bash
make wordcount
```

### LaTeX 語法檢查

```bash
lacheck main.tex
```

## 貢獻指南

### 新增章節

1. 在 `chapters/` 目錄下建立新的 `.tex` 檔案
2. 在 `main.tex` 中使用 `\include{chapters/新章節}` 包含
3. 遵循現有的格式和術語標準

### 新增圖片

1. 將圖片放在 `figures/` 對應章節的子目錄中
2. 使用描述性的檔名（英文）
3. 建議使用 PNG 或 PDF 格式
4. 確保圖片解析度足夠（至少 300 DPI）

### 翻譯術語

1. 參考 `../TERMINOLOGY_GLOSSARY.zh-TW.md`
2. 保持術語一致性
3. 新術語需要在術語表中新增

## 常見問題

### Q: 編譯時出現字型錯誤

**A**: 確認已安裝 Noto CJK 字型。如果使用不同的字型，請修改 `main.tex` 中的字型設定。

### Q: 程式碼高亮不顯示

**A**: 確認已安裝 Pygments 並使用 `-shell-escape` 選項編譯。

### Q: 編譯很慢

**A**:
- 使用 `make quick` 進行快速測試
- 註解掉不需要的章節
- 使用 SSD 硬碟

### Q: EPUB 轉換失敗

**A**: 確認已安裝 pandoc，並檢查 LaTeX 原始碼是否有不相容的命令。

## 輸出檔案

成功建置後會產生：

- `main.pdf`: PDF 版本（高品質印刷）
- `main.epub`: EPUB 版本（電子書閱讀器）

## 版本資訊

- **LaTeX 版本**: XeLaTeX
- **文件類別**: book
- **紙張大小**: A4
- **字型**: Noto CJK, Libertinus
- **程式碼高亮**: minted + Pygments

## 授權

本翻譯遵循原著的 Apache-2.0 授權。

## 聯絡資訊

如有問題或建議，請參閱 `../TRANSLATION_GUIDELINES.zh-TW.md`。

---

**最後更新**: 2025-11-15
