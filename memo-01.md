
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
