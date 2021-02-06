scrsavwr
========

Windows用スクリーンセーバのラッパープログラム


Table of Contents
-----------------

* [Description](#description)
* [Usage](#usage)
* [Environment](#environment)
* [License](#license)
* [Author](#author)


Description
-----------

Windows上でスクリーンセーバが起動する際に、
iniファイルに記述されたプログラムを起動して、そのまま終了するスクリーンセーバです。

Windows用のスクリーンセーバプログラムは、
与えられたコマンドライン引数によって動作を変えなければいけないので、
作成するのが少々面倒です。

しかし、このラッパーを使うことで、
フルスクリーン表示(かつ、キー入力等で終了)するプログラムさえ作ってしまえば、
スクリーンセーバとして利用することができます。
スクリーンセーバの制作が多少は楽になるかもしれません。


Usage
-----

1. scrsavwr.ini の内容を書き換えて、呼び出したいフルスクリーン表示プログラムのパスを記述します。
2. C:\Windows\System32\、もしくは C:\Windows\SysWOW64\ 以下に、scrsavwr.scr と scrsavwr.ini をコピーします。
   * 32bit版Windowsの場合、C:\Windows\System32\ 以下にコピーします。
   * 64bit版Windowsの場合、C:\Windows\SysWOW64\ 以下にコピーします。

必要であれば、scrsavwr.scr と scrsavwr.ini を任意のファイル名にリネームしてください。
例えば、hoge.scr と hoge.ini にリネームすれば、hoge.scr が呼び出された際、hoge.ini を読み込んで処理をします。

scrsavwr.ini の内容は、以下のようになっています。

```
fullscreen_bin=D:\home\prg\hsp\scrsavwr\fullscrn_sample\boundball.exe
config_bin=D:\home\prg\hsp\scrsavwr\fullscrn_sample\boundball_about.exe
preview_img=D:\home\prg\hsp\scrsavwr\fullscrn_sample\boundball.bmp
```

fullscreen_bin= には、フルスクリーン表示するプログラムのパスを書いてください。

config_bin= には、設定画面用プログラムのパスを書いてください。
用意してなければ、行頭に「;」をつけてコメントアウトしていいです。

preview_img= には、Windows上でスクリーンセーバを選択する際の、小さい画面に表示するbmp画像のパスを指定してください。
Windows10上では、152 x 112ドットのbmp画像なら、ちょうどよいサイズになるようです。
用意してなければ、行頭に「;」をつけてコメントアウトしていいです。


Environment
-----------

* Windows10 x64 20H2
* HSP 3.6 beta4


License
-------

「あるがーまんスクリーンセーバー for HSP3」のライセンスに従います。


Author
------

[mieki256](https://github.com/mieki256)


