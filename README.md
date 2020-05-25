<<<<<<< HEAD
# BCDice-API

BCDiceを提供するWebAPIサーバー

[![Build Status](https://travis-ci.org/ysakasin/bcdice-api.svg?branch=master)](https://travis-ci.org/ysakasin/bcdice-api)

## Demo

https://bcdice.herokuapp.com

## What is BCDice

BCDiceは日本のTRPGセッションツールにおいて、デファクトスタンダードとも言えるダイスロールエンジンです。
初めは、Faceless氏によってPerlを用いて作成されました。後に、たいたい竹流氏によってRubyへの移植され、現在までメンテナンスされています。

BCDiceは[どどんとふ](http://www.dodontof.com)をはじめとして、[TRPGオンラインセッションSNS](https://trpgsession.click)や[Onset!](https://github.com/kiridaruma/Onset)においてダイスロールエンジンとして使われています。

## Setup

```
$ git clone https://github.com/ysakasin/bcdice-api.git
$ cd bcdice-api
$ git checkout `git describe --abbrev=0` #直近のリリースに移動
$ git submodule init
$ git submodule update
$ bundle install
```

## Run

### Development

```
$ bundle exec rackup
```

### Production

```
$ APP_ENV=production bundle exec rackup -E deployment
```

実際に運用する場合には、[Puma](https://puma.io/)の利用をお勧めします。
- [Configuration](https://github.com/puma/puma#configuration)
- [設定例](https://devcenter.heroku.com/articles/deploying-rails-applications-with-the-puma-web-server#config)

公開サーバーとして運用する場合、 `/v1/admin` の情報を設定するようにしてください。
- [/v1/admin 設定方法](/docs/api.md#admin)

## API

Method                           | Description
-------------------------------- | -----
[/v1/version](/docs/api.md#version)   | BCDiceとAPIサーバーのバージョン
[/v1/admin](/docs/api.md#admin)       | APIサーバ提供者の名前と連絡先
[/v1/systems](/docs/api.md#systems)   | ダイスボットのシステムID一覧
[/v1/names](/docs/api.md#names)       | ダイスボットのシステムIDとシステム名前の一覧
[/v1/systeminfo](/docs/api.md#systeminfo)   | ダイスボットのシステム情報取得
[/v1/diceroll](/docs/api.md#diceroll) | ダイスボットのコマンドを実行

## Plugin

`plugins/` ディレクトリにダイスボットのコードを入れておくと、サーバー起動時にロードし、使うことができます。
既存のダイスボットを上書きすることもできます。

## Documents

- [無料で独自ダイスボット入りのBCDice-APIサーバーを立てる](docs/heroku.md) (中級者向け)

## Cases

- [discord-bcdicebot](https://shunshun94.github.io/discord-bcdicebot/)
- [Line botでダイスを振る - Qiita](http://qiita.com/violet2525/items/85607f2cc466a76cca07)
- [HTTPS版BCDice-API | 大ちゃんのいろいろ雑記](https://www.taruki.com/wp/?p=6610) : どどんとふ公式鯖による公開サーバー
- [オンラインセッションツール – Hotch Potch .](https://aimsot.net/tool-info/) : えいむ氏による公開サーバー

## Donate

- [Amazonほしい物リスト](http://amzn.asia/gK5kW6A)
- [Amazonギフト券](https://www.amazon.co.jp/dp/B004N3APGO/) 宛先: ysakasin@gmail.com

## The Auther

酒田　シンジ (@ysakasin)
=======
# BCDice

[![Build Status](https://travis-ci.org/bcdice/BCDice.svg?branch=master)](https://travis-ci.org/bcdice/BCDice)
[![codecov](https://codecov.io/gh/bcdice/BCDice/branch/master/graph/badge.svg)](https://codecov.io/gh/bcdice/BCDice)
[![Discord](https://img.shields.io/discord/597133335243784192.svg?color=7289DA&logo=discord&logoColor=fff)][invite discord]

様々なTRPGシステムの判定に対応したIRC用ダイスボット兼オンセツール用ダイスエンジン

## Documents

- [ロードマップ](ROADMAP.md)
- [ChangeLog](CHANGELOG.md)
- [旧README](docs/README.txt)

## バグ報告や機能要望

BCDiceの問題を発見したり、機能の要望がある時に起こすアクションの一例は以下のようなものがあります。
上位の例ほど歓迎します。

1. バグ修正や機能追加のコードを書いて、Pull Requestを作成する
2. issueを作成する
3. Discordの [BCDice Offcial Chat][invite discord] にある各種チャンネルへ投稿する
4. Twitterで [@ysakasin](https://twitter.com/ysakasin) にメンションを送る

## LICENSE

[BSD 3-Clause License](LICENSE)


[invite discord]:https://discord.gg/x5MMKWA
>>>>>>> origin/master
