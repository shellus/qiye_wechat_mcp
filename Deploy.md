# 发布新版本指南

## 1. 更新版本号

编辑 `setup.py` 文件，修改版本号：
```python
version="0.1.2",
```

## 2. 构建新版本

```bash
# 构建源码包和wheel包
python setup.py sdist bdist_wheel
```

## 3. 发布到PyPI

```bash
# 安装twine（如果还没安装）
pip install twine

# 上传到PyPI
twine upload dist/*
```

就这么简单！