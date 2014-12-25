enotify-slack
=============

This is a tool to get event information and send the information to a channel in [Slack](https://slack.com/).
The event information is provided by event support sites such as [Connpass](http://connpass.com/).
Currently this tool only gets event information provided by Japanese event support sites.
Although the following part of this document is written in Japanese, Godoc and comments in the source code are written in English.


## 概要

イベント支援サイトから勉強会の情報を取得してSlackに通知するためのツールです。
イベントのタイトルか説明にキーワードが含まれている場合、または指定したユーザが開催(または参加)しているイベントの情報をSlackの指定のチャネルに通知します。

![キャプチャ](https://raw.github.com/wiki/daikikohara/enotify-slack/images/capture01.png)

## 使い方

現在ソースしか用意していません。
依存性の解決には[godep](https://github.com/tools/godep)を使ってます。
需要があればバイナリも用意するかもしれません。

* 取得
```
go get github.com/daikikohara/enotify-slack
cd /path/to/enotify-slack
godep get
go build
```
* 設定
conf.ymlを必要に応じて編集して下さい。
設定方法はconf.ymlのコメントを参照して下さい。
* 起動
nohupを付けるかscreen/tmuxのセッションの中で起動して下さい。
```
nohup ./enotify-slack &
```

## Thanks

以下のAPIを利用させて頂いております。
ありがとうございます。

* イベント情報サイト
 * [ATND](http://api.atnd.org/)
 * [Connpass](http://connpass.com/about/api/)
 * [Doorkeeper](http://www.doorkeeperhq.com/developer/api)
 * [Partake](https://github.com/partakein/partake/wiki/PARTAKE-Web-API)
 * [Zusaar](http://www.zusaar.com/doc/api.html)
* Slack通知
 * [Slack](https://api.slack.com/)

## License

enotify-slack is under the Apache 2.0 license. See the [LICENSE](LICENSE) file for details.
