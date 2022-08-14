# Python組み込み関数アウトプット


## len()
オブジェクトの長さ (要素の数) を返します。引数は文字列、バイト列、タプル、リスト、range、辞書型配列

```python
 #条件判定に使用できる
 if len(item_num) != 0:
 
 #文字数の長さでバリデーションにもできる
 if len(str_len) == 10:
 
 #string型の引数の存在判定に使用できる
 def x(str=""):
  if len(str) != 0: #引数に値が入っている場合
   print(str)
  else: #初期値の場合
   print("値が入っていません。")
```

## open()
file を開き、対応する ファイルオブジェクト を返します。ファイルを開くことができなければ、OSError が送出されます。
withを使用することによりwith内の処理が終了するたびにf.close()を自動でおこなってくれるため、おすすめの書き方。
下記の例の場合、fはファイルポインタである。
```python
 with open('log.txt') as f:
  f.read()
```

## print()
複数の引数を受け取れる。sepで区切り文字を指定できる。endは最後に出力
```python
 print('あ', 'い', 'う', sep=',', end=' end\n')
 あ,い,う end
```

## filter()
リストやタプルなどから条件を満たす要素を抽出したり削除したりできる。Python3のfilter()はイテレータを返す
```python
#偶数のときTrueを返すlambda（ラムダ式、無名関数）下記の場合、filter()の第一引数は無名関数、第二引数は1である
 for i in filter(lambda x: x % 2 == 0, l):
    print(i)
    
#結果をリストに変換したい場合はlist()を使う。
print(list(filter(lambda x: x % 2 == 0, l)))
# [-2, 0, 2]
```

## lambda式（超絶便利）
無名関数を定義できる。（普通の関数はdef）。引数に関数を取るときに使うと便利でコンパクトになる
現在、無名引数に名前をつける（値として受けとる）のは非推奨。（そりゃそう）
```python
#偶数のときTrueを返すlambda（ラムダ式、無名関数）。引数はx１つ。コロンの後ろが式
 for i in filter(lambda x: x % 2 == 0, l):
    print(i)
```

