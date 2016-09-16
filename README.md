# LyX template generator for ltjsclasses/BXjscls

## 概要
LuaTeX・XeTeXをLyXで使う場合、ltjsarticle・bxjsarticleなどのクラスを使いますが、これらはLyXのテンプレートとして用意されていません。このスクリプトはjsarticleなどからそれ用のテンプレートを生成するものです。

## 使い方
TeX・LyXをインストールしたあと、次のコマンドを実行するだけです。

``` bash
# sudoを使用する場合
curl -LsSf https://raw.githubusercontent.com/tats-u/ltbxjscls_lyxtmplt/master/install_lyxtemplate | sudo env PATH="$PATH" bash
# sudoを使用しない場合(TeX・LyXにパスが通っているか確認してください)
curl -LsSf https://raw.githubusercontent.com/tats-u/ltbxjscls_lyxtmplt/master/install_lyxtemplate | bash
```

その後、LyXを起動し、オプション→環境構成を行います。これでLyXを次回以降に起動して新規文書を作成して文書設定を行う際に、文書クラスからltjsarticle・bxjsarticleなどが選べるようになります。

なお、このスクリプトはWindowsにも対応していますが、**sudoを使用する代わりにGit Bashを管理者権限で開き、下側のコマンドを**実行してください。LyXにパスが通っている必要はありません。(ただしTeXにはパスが通っていなければなりません)

## オプション
このスクリプトにはいくつかのオプションがあります。オプションを使用する場合は、「`|`」の後を、

```bash
# sudoを使用する場合
sudo env PATH="$PATH" bash /dev/stdin [OPTIONS]
# sudoを使用しない場合
bash /dev/stdin [OPTIONS]
```

に変更して実行します。オプションは次の表の通りです。

|オプション         |意味                                    |
|--------------------|---------------------------------------|
|`-f`・`--force`    |既にファイルが存在している場合上書き    |
|`-j`・`--justforme`|現在のユーザだけにインストール(sudo不要)|
|`-h`・`--help`     |ヘルプの表示                            |
|`-v`・`--version`  |バージョンの表示                        |
