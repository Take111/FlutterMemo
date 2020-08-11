
- Android StudioでSimulatorがLoadingのまま止まってしまう時

  検索で、Flutter Restart Deamonを検索して、実行すると解決

  https://github.com/flutter/flutter-intellij/issues/3892#issuecomment-647024484

- Dart Formatに変換
  
  ```
  runApp(MaterialApp(home: Center(Text: ""),),);
  ```
  こんな感じで1文で書いた場合
  ()の後に,つけておくと、右クリック->Reformat with dartfmt
  これを行うことで、ネストしたコードに自動で変換してくれる
  こうなる
  ```
  runApp(
    MaterialApp(
      home: Center(
        child: Text("Hello"),
      ),
    ),
  );
  ```

- DebugのBannerを隠す
  
  Flutter inspector -> More Actions -> Hide Debug Mode Banner
  
- Option + Enter
  
  Option + Enterをクリックすると、Center widgetとか色々出てくる

- ColumnとRow
  
  Columnが縦に並べるときに使う
  
  Rowが横に並べるときに使う

- 次の画面への遷移

```
body: Center(
        child: RaisedButton(
          child: Text('次へのボタン'),
          onPressed: () {
            // ここにActionを書いていく
            Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) => NextPage(), // NextPage()は新しく用意した
              ),
            );
          },
        ),
      ),
```

- Flutterのドキュメント

ここにサンプルコード付きで、いろいろな動きが紹介されている

https://flutter.dev/docs/cookbook
