# カードテンプレートに問題があります

Ankiは最近、カードテンプレートのミスを報告する際に厳格になりました。以前は、一部の問題を黙って無視していましたが、予期しない方法でテンプレートを表示していました。この変更は、ミスをより簡単に見つけられるようにするために行われました。

自分でカードテンプレートを編集していない場合、共有デッキをダウンロードした可能性が高く、その場合、元のデッキの作成者がテンプレート作成時にミスをした可能性があります。

テンプレートのミスを修正するには、カードテンプレート画面を開きます：

- コンピュータ版では、問題のあるカードを編集し、「カード...」ボタンをクリックします
- AnkiMobileでは、復習画面で問題のあるカードを表示中に歯車アイコンをタップし、「カードテンプレート」を選択します

ミスを修正すると、そのタイプのすべてのカードが更新されます。同じテンプレートを使用するすべてのカードに対して同じ変更を行う必要はありません。

何を変更する必要があるかは、表示されているメッセージによります。

**「{{Field}} が見つかりましたが、『Field』という名前のフィールドは存在しません」**

これは、テンプレートに存在しないフィールドの名前が含まれていることを示しています。問題を修正するには、カードテンプレート内の {{Field}} を見つけて削除してください。

**「{{Field の中に }} がありません」**

このメッセージは、テンプレート内に {{ があり、それに対応する }} がない場合に表示されます。例えば、テンプレートに
```
{{Field
```

この場合、次のように変更する必要があります

```
{{Field}}
```

**{{/Field}} が見つかりません**

これは、カードテンプレート内に `{{#Field}}` または `{{^Field}}` があり、それに対応する `{{/Field}}` がないことを意味します。テンプレートから `{{#Field}}` または `{{^Field}}` を削除することでエラーを修正できます。

**{{/One}} が見つかりましたが、{{/Two}} が予期されました**

条件付き置換は、開いた順序で閉じる必要があります。例えば、次のテンプレートは正しくありません：

```
{{#One}}
  {{#Two}}
    {{Three}}
  {{/One}}
{{/Two}}
```

問題を修正するには、テンプレートを次のように変更する必要があります：

```
{{#One}}
  {{#Two}}
    {{Three}}
  {{/Two}}
{{/One}}
```
**{{/Field}} が見つかりましたが、{{#Field}} または {{^Field}} がありません**

終了タグは開始タグと一致する必要があります。例えば、次のようなテンプレートは無効です。なぜなら、最初に `{{#Two}}` または `{{^Two}}` がないからです：

```
  {{Field}}
{{/Two}}
```

終了タグを削除することで修正できます：

```
{{Field}}
```