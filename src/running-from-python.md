# Pythonからの実行

パッケージ化されたAnkiのビルドで起動問題やクラッシュが発生し、それを解決できない場合、最終手段としてPythonから直接実行することを試みることができます。

以下の手順は、これらの問題がWindowsで最も多く発生するため、Windowsユーザー向けに提供されていますが、他のプラットフォームでも同様のアプローチを取ることができます。

1. <https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe> をインストールします。インストール場所をカスタマイズし、`c:\python` を選択します。
2. スタートメニューを開き、コマンドプロンプトを開きます。
3. 次のコマンドを入力してEnterキーを押します：

```
\python\python -m venv \anki-venv
```

4. 次に、以下のコマンドを入力します。これにはしばらく時間がかかります：

```
\anki-venv\scripts\pip install aqt orjson pyqt6-webengine
```

5. 最後に：

```
\anki-venv\scripts\anki
```

これで問題が解決した場合、今後Ankiを再起動するには、手順2と5を繰り返してください。

それでも問題が解決しない場合は、Qtのバージョンを変更してみてください：

```
\anki-venv\scripts\pip install pyqt5==5.15 pyqtwebengine==5.15.0
```

それでも解決しない場合、そして[問題が発生した場合](./when-problems-occur.md)の手順をすべて実行した場合は、残念ながら運が悪いかもしれません。