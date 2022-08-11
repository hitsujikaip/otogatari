# 音語（おとがたり）

このリポジトリでは[人工言語「音語」](https://youtu.be/qzh0EjgbCWc)（のうち、特に変種「星」第一版）を使いやすくするプログラムを公開しています。音語や「星」についての作品を公開する場合は、「羊飼いP([@hitsujikaip](https://twitter.com/hitsujikaip))」のクレジットをどこかに入れてください。連絡があれば喜んで見に行きたいと思います。

`dict.csv`はコンマ区切りの辞書ファイルです。空欄は未割当です。

```
category,token,display,text
...
prefix-3,_HRH,楽しい,楽しい
prefix-3,_HRL,寂しい,寂しい
prefix-3,_HRR,空しい,空しい
...
```

`input.txt`には、楽句をスペースで区切って書いてください。改行は無視されますが、楽句の途中では改行できません。

```
L_HL HRHR RHHH HF__
```

`dict.csv`と`input.txt`を実行ファイルと同じディレクトリに入れておいてください。

`translate.exe`は`input.txt`に書かれた文を楽句ごとに`dict.csv`を用いて逐語訳します。

```
>translate.exe
ただ 願う こと で
>
```

`midi_gen.exe`は`input.txt`に書かれた文をMIDIファイル`output_melody.mid`に変換します。

```
>midi_gen.exe

>
```

`chord_gen.exe`は引数のコード進行(TDStdsの表記、4文字)をMIDIファイル`output_chord.mid`に変換します。

```
>chord_gen.exe TSsD

>
```
