# hcx_documentation

## usage (in Ubuntu)

```
python -m venv .shpinx --copies  # 创建虚拟环境
source .shpinx/bin/activate      # 激活虚拟环境

pip install -r requirements.txt  # 安装依赖 sphinx read the docs主题
```

## #build make only once
```
chmod +x install.sh              # 添加执行权限
./build.sh                       # 编译生成 html, docx, pdf
```

### make html

```bash
make html
```

### view html
```bash
sensible-browser build/html/index.html
```

will open the html file in the default web browser if you run this command in the terminal.

### make docx
```bash
make docx
```

you can find the docx file in the `build/docx` folder if you run this command in the terminal.

open it with Microsoft Word or other word processors.

### make pdf
```bash
make latexpdf
```

then, you can find the pdf file in the `build/latex` folder. open it with Adobe Reader or other pdf readers.

## reference

- [sphinx](https://www.sphinx-doc.org/zh-cn/master/tutorial/)
- [sphinx_rtd_theme](https://sphinx-rtd-theme.readthedocs.io/en/stable/)