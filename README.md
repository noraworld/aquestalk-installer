# AquesTalk Installer
AquesTalk Installer は、[AquesTalk](https://www.a-quest.com/products/index.html) (通称、ゆっくりボイス、または、棒読みちゃん) を簡単にインストールするためのインストーラである。

[オンラインデモ](https://www.a-quest.com/demo/index.html)

## AquesTalk10
未実装

## AquesTalk2
未実装

## AquesTalk1
未実装

## AquesTalk Pi (Raspberry Pi)
### 事前準備
AquesTalk Pi のインストールおよび利用時に以下のコマンドが必要なため、インストールしていない場合は事前にインストールする。

* [zcat](https://command-not-found.com/zcat)
* [aplay](https://command-not-found.com/aplay)

### インストール方法
AquesTalk Pi をインストールしたい任意のディレクトリで以下のコマンドを実行する。

```shell
wget -qO- https://raw.githubusercontent.com/noraworld/aquestalk-installer/master/bin/pi | sh
```

### 使い方
出力結果を `aplay` コマンドに渡すことで発声させることができる。

```shell
aquestalkpi/AquesTalkPi 漢字も読めます。 | aplay
```

`echo` コマンドで発声させる文字列を指定する場合は以下のようにする。

```shell
echo ゆっくりしていってね？ | aquestalkpi/AquesTalkPi -b -f - | aplay
```

ファイルに出力する場合は `-o` オプションを使用する。

```shell
aquestalkpi/AquesTalkPi -s 150 -v f2 -k -o out.wav "ファイルニ、シュツ'リョクシマ_ス。"
aplay out.wav
```

より詳しい使い方は [AquesTalk Pi の使い方まとめ](http://blog-yama.a-quest.com/?eid=970157) を参照すること。
