# テキスト読み上げサポート

<h1>Anki 2.1.20以降の場合</h1>

<https://shigeyukey.github.io/anki-manual-jp/templates/fields.html#個別フィールドのテキスト読み上げ> をご覧ください。

<h1>AnkiMobile 2.0.56以降の場合</h1>

<https://docs.ankimobile.net/tts.html> をご覧ください。

<h1>AnkiDroidの場合</h1>

AnkiDroidマニュアルでTTSを検索してください。

<h1>古いAnkiバージョンの場合</h1>

AwesomeTTSという人気のアドオンがあり、多くのテキスト読み上げプログラムやサービスをサポートしています。詳細はこちらをご覧ください：

<https://ankiweb.net/shared/info/814349176>

このアドオンはオーディオをコレクションにダウンロードすることで機能します。したがって、AnkiWebと同期すると、他のデバイスでもオーディオにアクセスできるようになります。

生成されたファイルをコンピュータ版以外で使用したい場合は、「オンザフライ」ではなく「保存されたファイル」モードを使用してください。

AnkiMobile <2.0.56 にはデバイス上でのTTSの公式サポートはありませんが、AppleはiOS7でTTSサポートを導入しており、アクセスすることが可能です。以下はユーザーが提供したソリューションに基づいています。

```html
<span id="word">{{Word}}</span>

<script>
  var w = document.getElementById("word");
  window.setTimeout("speak(w.innerHTML)", 500);

  function speak(word) {
    var speech = new SpeechSynthesisUtterance();
    speech.text = word;
    speech.volume = 1; // 0 to 1
    speech.rate = 1; // 0.1 to 9
    speech.pitch = 1; // 0 to 2, 1=normal
    speech.voice = window.speechSynthesis
      .getVoices()
      .filter((v) => v.lang == "en-GB")[0];
    speechSynthesis.cancel();
    speechSynthesis.speak(speech);
  }
</script>
```

`en-GB`を`en-US`、`de-DE`、`ja-JP`、`zh-HK`などの他の言語に変更できます。以下のページの例のセクションを使用して、すべての異なる言語を確認できます。<https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis/getVoices>

再生したい言語の拡張オーディオファイルをインストールする必要があるかもしれません。これは、設定アプリの「一般」、「アクセシビリティ」、「スピーチ」と「声」から行うことができます。