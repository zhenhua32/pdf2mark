# Example Package

This is a simple example package. You can use
[GitHub-flavored Markdown](https://guides.github.com/features/mastering-markdown/)
to write your content.

# 安装后的结构

```bash
C:\ANACONDA3\ENVS\TORCH\LIB\SITE-PACKAGES\PDF2MARK
│  main.py
│  __init__.py
│
└─__pycache__
        main.cpython-310.pyc
        __init__.cpython-310.pyc
```

# 上传到 pypi 的流程

配置好 api token 到 `~/.pypirc` 文件中

```ini
[pypi]
  username = __token__
  password = api_token
```

执行构建和上传命令

```bash
python -m build
python -m twine upload --repository pypi dist/* --verbose

# 指定 index-url, 才能实时装上, 国内的代理同步没这么快
pip install pdf2mark --index-url https://pypi.org/simple/ 
```
