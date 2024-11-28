# hcx_documentation

## usage

```bash
python -m venv .shpinx --copies  # 创建虚拟环境
source .shpinx/bin/activate      # 激活虚拟环境
pip install sphinx-rtd-theme     # 安装 sphinx read the docs主题
sphinx-build -M html ./source/ ./build/  # 生成html
make html
```

## make pdf
```bash
chmod +x install.sh
./build.sh
make latexpdf
```

## reference

- [sphinx](https://www.sphinx-doc.org/zh-cn/master/tutorial/)
- [sphinx_rtd_theme](https://sphinx-rtd-theme.readthedocs.io/en/stable/)