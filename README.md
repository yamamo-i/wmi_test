# wmi_test

* windowsのリソース監視情報で何が取得できるかみてみる

## wmi_exporter

### is 何?

* WMIを利用してWindows機から監視メトリクスを取得するexporter  
https://github.com/martinlindhe/wmi_exporter
* go言語で書かれているのでbinaryを落としてwin機で実行するだけ
* 主要なメトリクスは取得できる  
https://github.com/martinlindhe/wmi_exporter#collectors

### wmi_exporterの使い方

* buildしたbinary(zip)をダウンロードする(中身はexe)  
https://github.com/martinlindhe/wmi_exporter/releases
* Windows上でexeファイルを起動する
    * コマンドプロンプトを「管理者として実行」する
    * exeファイルを実行する  
    ex) `$ ./wmi_exporter.exe --collectors.enabled "cpu,cs,logical_disk,net,os,tcp,system"`
* Windows機に向けてhttpリクエスト `http://[hoge]/metrics` を発行する

## local環境構築

* `env` 配下にdocker-composeで構築できるように用意した