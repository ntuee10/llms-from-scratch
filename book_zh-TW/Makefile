# Makefile for building "Build a Large Language Model (From Scratch)" Traditional Chinese Edition
# 《從零開始打造大型語言模型》繁體中文版建置腳本

# 編譯器設定
LATEX = xelatex
BIBTEX = biber
MAKEINDEX = makeindex

# 主檔案
MAIN = main
MAINTEX = $(MAIN).tex
MAINPDF = $(MAIN).pdf

# 目錄
CHAPTERSDIR = chapters
FIGURESDIR = figures
BUILDDIR = build

# Shell 命令
SHELL = /bin/bash
RM = rm -f
MKDIR = mkdir -p

# Minted 需要 shell-escape
LATEXFLAGS = -shell-escape -interaction=nonstopmode -file-line-error

# 預設目標
.PHONY: all
all: pdf

# 建立 PDF
.PHONY: pdf
pdf: $(MAINPDF)

$(MAINPDF): $(MAINTEX) $(wildcard $(CHAPTERSDIR)/*.tex)
	@echo "正在編譯 PDF..."
	@$(MKDIR) $(BUILDDIR)
	@$(LATEX) $(LATEXFLAGS) $(MAINTEX)
	@$(BIBTEX) $(MAIN)
	@$(MAKEINDEX) $(MAIN).idx
	@$(LATEX) $(LATEXFLAGS) $(MAINTEX)
	@$(LATEX) $(LATEXFLAGS) $(MAINTEX)
	@echo "PDF 編譯完成：$(MAINPDF)"

# 快速編譯（僅編譯一次，用於測試）
.PHONY: quick
quick:
	@echo "快速編譯中..."
	@$(LATEX) $(LATEXFLAGS) $(MAINTEX)
	@echo "快速編譯完成"

# 建立 EPUB（使用 pandoc）
.PHONY: epub
epub: $(MAINTEX)
	@echo "正在轉換為 EPUB..."
	@pandoc $(MAINTEX) -o $(MAIN).epub \
		--from=latex \
		--to=epub3 \
		--toc \
		--toc-depth=2 \
		--epub-cover-image=cover.jpg \
		--epub-metadata=metadata.xml \
		--css=epub-style.css
	@echo "EPUB 轉換完成：$(MAIN).epub"

# 清理輔助檔案
.PHONY: clean
clean:
	@echo "清理輔助檔案..."
	@$(RM) *.aux *.log *.out *.toc *.lof *.lot *.bbl *.blg *.idx *.ilg *.ind
	@$(RM) *.fls *.fdb_latexmk *.synctex.gz *.bcf *.run.xml
	@$(RM) $(CHAPTERSDIR)/*.aux
	@$(RM) -r _minted-$(MAIN)
	@echo "清理完成"

# 完全清理（包含 PDF 和 EPUB）
.PHONY: cleanall
cleanall: clean
	@echo "完全清理中..."
	@$(RM) $(MAINPDF) $(MAIN).epub
	@$(RM) -r $(BUILDDIR)
	@echo "完全清理完成"

# 檢查依賴
.PHONY: check-deps
check-deps:
	@echo "檢查必要的工具..."
	@which $(LATEX) > /dev/null || (echo "錯誤：找不到 xelatex" && exit 1)
	@which $(BIBTEX) > /dev/null || (echo "錯誤：找不到 biber" && exit 1)
	@which $(MAKEINDEX) > /dev/null || (echo "錯誤：找不到 makeindex" && exit 1)
	@which pandoc > /dev/null || echo "警告：找不到 pandoc（EPUB 轉換需要）"
	@python3 -c "import pygments" 2>/dev/null || echo "警告：找不到 pygments（程式碼高亮需要）"
	@echo "依賴檢查完成"

# 顯示幫助
.PHONY: help
help:
	@echo "《從零開始打造大型語言模型》繁體中文版建置系統"
	@echo ""
	@echo "可用目標："
	@echo "  make pdf        - 建立 PDF 版本（預設）"
	@echo "  make quick      - 快速編譯（僅編譯一次，用於測試）"
	@echo "  make epub       - 建立 EPUB 版本"
	@echo "  make all        - 建立所有格式"
	@echo "  make clean      - 清理輔助檔案"
	@echo "  make cleanall   - 完全清理（包含輸出檔案）"
	@echo "  make check-deps - 檢查必要的工具"
	@echo "  make help       - 顯示此幫助訊息"
	@echo ""
	@echo "需求："
	@echo "  - XeLaTeX（支援中文）"
	@echo "  - biber（參考文獻管理）"
	@echo "  - makeindex（索引生成）"
	@echo "  - Pygments（程式碼高亮）"
	@echo "  - pandoc（EPUB 轉換）"
	@echo "  - 中文字型：Noto Serif/Sans CJK TC"

# 安裝依賴（Ubuntu/Debian）
.PHONY: install-deps-ubuntu
install-deps-ubuntu:
	@echo "安裝 LaTeX 相關套件..."
	@sudo apt-get update
	@sudo apt-get install -y texlive-xetex texlive-latex-extra texlive-fonts-recommended
	@sudo apt-get install -y texlive-bibtex-extra biber
	@sudo apt-get install -y python3-pygments
	@sudo apt-get install -y pandoc
	@sudo apt-get install -y fonts-noto-cjk fonts-noto-cjk-extra
	@echo "依賴安裝完成"

# 安裝依賴（macOS）
.PHONY: install-deps-macos
install-deps-macos:
	@echo "安裝 LaTeX 相關套件..."
	@brew install --cask mactex
	@brew install pandoc
	@pip3 install pygments
	@echo "請手動安裝 Noto CJK 字型"
	@echo "依賴安裝完成"

# 觀察模式（自動重新編譯）
.PHONY: watch
watch:
	@echo "監看檔案變更並自動重新編譯..."
	@while true; do \
		inotifywait -e modify $(MAINTEX) $(CHAPTERSDIR)/*.tex 2>/dev/null && \
		make quick; \
	done

# 計算字數
.PHONY: wordcount
wordcount:
	@echo "統計字數..."
	@texcount -chinese $(MAINTEX) -inc

.PHONY: all-formats
all-formats: pdf epub
	@echo "所有格式建立完成"
