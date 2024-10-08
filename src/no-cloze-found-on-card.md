# カードに穴埋め問題が見つかりません

<h2>単一の空のカード</h2>

穴埋め問題を作成する際、各穴埋め問題の番号は別々のカードに変換されます。例えば、次の例では3枚のカードが作成されます：

```
{{c1::これは}} {{c2::サンプル}}の{{c3::文}}です。
```

テキストを後で編集し、穴埋め問題の番号を削除または変更すると、以前に作成されたカードが空白になることがあります。例えば：

```
{{c1::これは}} {{c2::サンプル}}です
```

および

```
{{c1::これは}} {{c2::サンプル}}の{{c1::文}}です。
```

これらの変更はどちらもカード3を空白にします。カード3を表示すると、カードが空白であることを示すメッセージが表示され、空のカード機能でクリーンアップできます。この機能には、コンピュータ版のメインウィンドウのツールメニューからアクセスでき、空のカードを削除するために使用します。報告された空のカードをまず確認し、疑わしい場合は、ファイル>エクスポートメニュー項目でバックアップを作成してから進めてください。

<h2>すべての穴埋め問題のカードが空白</h2>

カードテンプレートを誤って変更すると、穴埋め問題が表示されなくなることがあります。その場合は、その問題のあるカードを編集し、最初のフィールドの名前をメモしてください。通常は「テキスト」と呼ばれています。その後、以下の手順を行ってください：

- 「カード...」ボタンをクリックします
- 表面のテキストを次のように置き換えます

  ```
  {{cloze:テキスト}}
  ```

- 裏面のテキストも同様に置き換えます。

フィールドが「テキスト」以外の名前の場合は、「テキスト」をそのフィールドの名前に置き換えてください。