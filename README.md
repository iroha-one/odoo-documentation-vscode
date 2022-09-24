# odoo-documentation-vscode
odooドキュメンテーションをVSCodeでメンテナンスします。

# ビルド方法

VSCodeで、コンテナを開き、ターミナルで次のコマンドを実行してビルドします。

```
cd /home/vscode/ws/repos
git clone https://github.com/odoo/documentation.git
cd documentation
pip install -r requirements.txt
make
```

# 参考
https://github.com/microsoft/vscode-remote-try-python.git

