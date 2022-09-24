# ビルド環境の構築

VSCodeで、コンテナを開き、ターミナルで次のコマンドを実行してビルド環境を構築します(`odoo-doc-16.0`の例)。

```
cd /home/vscode/ws/repos
git clone -b 16.0 https://github.com/odoo/documentation.git odoo-doc-16.0
cd odoo-doc-16.0
pip install -r requirements.txt
```

# poファイルの再作成

`odoo-doc-16.0`の`poファイル`を再作成する例(`./locale/sources/`)

```
cd /home/vscode/ws/repos
cd odoo-doc-16.0

make gettext
```

# poファイルのマージ

`odoo-doc-16.0`の`potファイル`(sources)と`poファイル`(Japanese)とをマージする例

```
cd /home/vscode/ws/repos
cd odoo-doc-16.0
cd locale/sources
mkdir po

msgcat --no-location --no-wrap index.pot index-ja.po -o ./po/index.po
msgcat --no-location --no-wrap developer.pot developer-ja.po -o ./po/developer.po
msgcat --no-location --no-wrap general.pot general-ja.po -o ./po/general.po
```

# ビルド方法

`odoo-doc-16.0`をビルドする例(`CURRENT_LNAG=ja`)

```
cd /home/vscode/ws/repos
cd odoo-doc-16.0

export CURRENT_LANG=ja
make
```
