- 画面遷移

ボタンを押して、遷移する一つの例
これが基本らしい
```
child: RaisedButton(
          child: Text('次へのボタン'),
          onPressed: () {
            // ここにActionを書いていく
            Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) => NextPage(),
              ),
            );
          },
),
```

遷移先の画面で、元の画面に戻るのはこれ
ボタンを押して、元の画面に戻る


```
child: RaisedButton(
            child: Text('戻る'),
            onPressed: () {
              // ここにActionを書いていく
              Navigator.pop(context);
            },
),
```


- 遷移画面の値渡し

元の画面
```
child: RaisedButton(
          child: Text('次へのボタン'),
          onPressed: () {
            // ここにActionを書いていく
            final result = Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) => NextPage('KBOY'), // イニシャライザで渡す方法
              ),
            );
            print(result);
          },
```

次の画面
```
class NextPage extends StatelessWidget {
  NextPage(this.name); // ここでイニシャライザに宣言する
  final String name;　// 受け取る変数を宣言

  @override
  Widget build(BuildContext context) {
    return Scaffold(
```

- 遷移先の画面から元の画面に値を戻す

遷移先の画面
```
child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(name),
            Center(
              child: RaisedButton(
                child: Text('戻る'),
                onPressed: () {
                  // ここにActionを書いていく
                  Navigator.pop(context, 'KBOYさん');　// ここに変数を入れる
                },
              ),
            ),
          ],
        ),
```

元の画面
```
body: Center(
        child: RaisedButton(
          child: Text('次へのボタン'),
          onPressed: () async {　// 非同期処理なので、asyncが必要
            // ここにActionを書いていく
            final result = await Navigator.push( // ここで値を受け取る　非同期処理から値をもらうのでawaitが必要
              context,
              MaterialPageRoute(
                builder: (context) => NextPage('KBOY'),
              ),
            );
            print(result);
          },
        ),
      ),
```



