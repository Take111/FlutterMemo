- テキストのFontを変える方法

Textの下に、styleを設けて、TextStyleで宣言していく
```
Text(
  'KBOYさん',
  style: TextStyle(
    fontSize: 20,
    color: Colors.blue,
    fontWeight: FontWeight.bold,
    fontStyle: FontStyle.italic,
    decoration: TextDecoration.underline,
  ),
),
```
- デフォルトのText Fontを設定する

```
DefaultTextStyle(
  // ここにデフォルトで設定したいFontを書いていく
)
```
