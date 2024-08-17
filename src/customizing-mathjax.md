# MathJaxのカスタマイズ

AnkiにバンドルされているMathJaxサポートはカードの内容の前に読み込まれるため、MathJaxをカスタマイズする場合は特定の方法で行う必要があります。

最近のAnkiバージョンでは、次のようにします：

```html
<script>
MathJax.config.tex['macros'] = {
    R: '{\\mathbb {R}}',
};
if (typeof is_already_run == 'undefined') {
  is_already_run = true
  MathJax.startup.getComponents();
}
</script>
```

古いバージョンのAnkiの場合：

```html
<script>
  MathJax.Hub.Config({
  ...
  });
  MathJax.Hub.Configured();
</script>
```

注意：

- 標準の開閉タグ（`\(` と `\[`）を `$` や `$$` のようなものに変更しないでください。Ankiにはクロース削除のための特別なロジックがあり、デリミタを変更すると機能しなくなります。
