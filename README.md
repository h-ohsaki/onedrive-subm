# NAME

onedrive-subm - OneDrive で回収したレポートのファイル名を正規化する

# DESCRIPTION

**onedrive-subm** は Microsoft OneDrive の「ファイル提出」機能を利用し
た回収したレポートファイルを採点しやすい名前に変更するPython スクリプ
トです。

OneDrive で回収したファイルには、「姓　名_元のファイル名.拡張子」、
「名_姓_元のファイル名.拡張子」などのファイル名が付けられます。同じ提
出者から複数のファイルが提出された場合は、「姓　名_元のファイル名 1.拡
張子」、「名_姓_元のファイル名 1.拡張子」のように、拡張子の直前に通し
番号が振られます。

このプログラムは、レポートファイルを一括して「学籍番号-バージョン-姓
名-元ファイル名.拡張子」という名前に変更します※。

※ 本来は名前を変更 (リネーム) すべきですが、現在は安全のため元のファイルを残
したまま複製 (コピー) しています。不要な場合は元のファイルを手動で削除してくだ
さい。

# REQUIREMENTS

- Python 3
- perlcompat (https://pypi.org/project/perlcompat/)

# INSTALLATION

```sh
pip3 install perlcompat
python3 onedrive-subm
```
# USAGE

実行すると複製を保存するディレクトリ (出力ディレクトリ) の名前を聞かれ
ます。何も入力せずにOK を選択すると「renamed」 というディレクトリにコ
ピーが保存されます。

続いてファイル選択ダイアログが開きますので、OneDrive からダウンロード
したレポートファイル (PDF ファイルや Word ファイル等)を選択してくださ
い。複数のファイルを選択することが可能です。

作業完了を知らせるダイアログ等は何も表示されませんが、最初に指定した出
力ディレクトリに、「学籍番号-バージョン-姓 名-元ファイル名.拡張子」の
ような名前でレポートファイルがコピーされています。

# AVAILABILITY

最新版の **onedrive-subm** は https://github.com/h-ohsaki/onedrive-subm
から入手できます。

# AUTHOR

Hiroyuki Ohsaki (ohsaki[atmark]lsnl.jp)
