# 秀丸エディタでPythonを動かすマクロ

## 概要
秀丸エディタで編集中のソースコードをPythonで実行します。

### スクリーンショット（その１）
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161934.gif "Python 秀丸エディタ")
### スクリーンショット（その２）
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161912.gif "Python 秀丸エディタ")
### スクリーンショット（その３）
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161852.gif "Python 秀丸エディタ")
### スクリーンショット（その４）
- ![python hidemaru](http://cdn-ak.f.st-hatena.com/images/fotolife/o/ohtorii/20120414/20120414161838.gif "Python 秀丸エディタ")

### インストール方法
- 秀丸のマクロディレクトリへコピーしたらキーアサインして下さい。

## 動作環境
- 秀丸エディタ ver8.20 b14 で動作を確認、ver8以降なら動くはず。

### Pythonバージョン
- どのバージョンでも動くはずです、動作検証はPython ver2.7/ver3系で行っています。
- 切り替えはマクロ冒頭の$g_exe 変数を編集して下さい。

### 特徴
スクリーンショットを見てもらえば分かるかと思いますが、利便性のため「エンコード指定」を補っています。
エンコード指定を行わなくても日本語(utf8/cp932とか)が使えます。

リダイレクトするとPythonがエラー出力するので、正しく動くようにリダイレクトも補っています。
>UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-3: ordinal not in range(128)


なので、このマクロではコード冒頭で色々補っています。

 
    （オリジナル）
    print u"にほんご"
     
    （実行されるコード）
    # -*- coding:utf8 -*-
    import sys, codecs
    sys.stdout = codecs.getwriter('cp932')(sys.stdout)
    del sys, codecs
    print u"にほんご"

エラー行数がずれてしまう副作用がありますが、いいコードを思いついたときすぐ試せるように便利さを優先しています。
