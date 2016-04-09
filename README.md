# LyX template generator for ltjsclasses/BXjscls

## 概要
LuaTeX・XeTeXをLyXで使う場合、ltjsarticle・bxjsarticleなどのクラスを使いますが、これらはLyXのテンプレートとして用意されていません。このスクリプトはjsarticleなどからそれ用のテンプレートを生成するものです。

## 使い方
TeX・LyXをインストールしたあと、次のコマンドを実行するだけです。

``` bash
sudo ./install_lyxtemplate
```

その後、LyXを起動し、オプション→環境構成を行います。これでLyXを次回以降に起動して新規文書を作成して文書設定を行う際に、文書クラスからltjsarticle・bxjsarticleなどが選べるようになります。

## オプション
このスクリプトにはいくつかのオプションがあります。

|オプション         |意味                                    |
|--------------------|---------------------------------------|
|`-f`・`--force`    |既にファイルが存在している場合上書き    |
|`-j`・`--justforme`|現在のユーザだけにインストール(sudo不要)|
|`-h`・`--help`     |ヘルプの表示                            |
|`-v`・`--version`  |バージョンの表示                        |
