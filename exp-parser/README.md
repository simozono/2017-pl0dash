### 構文解析器の作成方法
以下のようにして構文解析器を作成できます。
````console
$ cd exp-parser
$ make
いろいろ画面に出力される
$
````

### 簡単な文法G4

第20回授業(後期第05回)p.247 で示した文法に対応する構文解析器等です。

#### 1. 第20回授業(後期第05回) p. 250～の構文解析器のプログラム
* ファイルの説明
  * [LL(1)構文解析器本体: (exp-ll-parser01.c)](exp-ll-parser01.c)
  * [サンプルファイル: (../sample/exp01.txt)](../sample/exp01.txt)
* 実行方法と実行結果
````console
$ ./exp-ll-parser01 ../sample/exp01.txt
LOAD A, 3
PUSH A
LOAD A, 2
PUSH A
POP B
POP A
...
````

### 簡単な文法G4の拡張版

第20回授業(後期第05回)p.247 で示した文法で、さらに引き算と割り算ができ
るようにした物です。

#### 1. 第20回授業(後期第05回) p. 250～の構文解析器の拡張
* ファイルの説明
  * [LL(1)構文解析器本体: (exp-ll-parser02.c)](exp-ll-parser02.c)
  * [サンプルファイル: (../sample/exp02.txt)](../sample/exp02.txt)
* 実行方法と実行結果
````console
$ ./exp-ll-parser02 ../sample/exp02.txt
LOAD A, 8
PUSH A
LOAD A, 5
PUSH A
POP B
...
````
### 上記に対する共通ファイル
* ファイルの説明
  * [字句解析用サブルーチン(lex版) (exp-scanner.l)](exp-scanner.l)
