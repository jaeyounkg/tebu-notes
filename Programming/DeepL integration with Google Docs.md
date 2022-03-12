```
function DEEPL(text, sourceLang, targetLang) {
  if (text == "") {
    return "";
  } else if (targetLang == "tr") {
    // Fall back to Google Translate if the language is not supported
    return LanguageApp.translate(text, "en", "tr");
  }

  var response = UrlFetchApp.fetch(
    "https://api-free.deepl.com/v2/translate?auth_key=REPLACE_ME_WITH_KEY" +
    "&text=" + encodeURIComponent(text) +
    "&target_lang=" + targetLang +
    "&source_lang=" + sourceLang
  );
  var json = response.getContentText();
  var data = JSON.parse(json);
  return data["translations"][0]["text"];
}
```

To use the script:
1.  Open Google sheets
2.  Click on 'Extensions'
3.  Click on 'Apps Script'
4.  Paste the code
5.  Use for example this code in a cell `=DEEPL($A1; "en"; "de")`
