# Gitの初期設定

## Gitのインストール

インストール手順は[こちら](https://www.curict.com/item/60/60bfe0e.html)を参照

## SourceTreeのインストール

SourceTreeとは、Gitを操作するためのGUIアプリケーション。Gitの基本はコマンドラインでの操作だが、学習コストが高いため直感的に操作できるSourceTreeを用いる

インストール手順は[こちら](https://sukkiri.jp/technologies/devtools/git/sourcetree_win.html)を参照

※ツールを選択で「Git」を選択すること

## Gitの初期設定

下記のコマンドをそれぞれ実行する。※名前やアドレスは変更すること

```powershell
> git config --global user.name "FirstName LastName "
> git config --global user.email "your.email@example.com"
> git config --global http.proxy "http://127.0.0.1:17200"
> git config --global https.proxy "http://127.0.0.1:17200"
```

下記コマンドで設定が反映されているか確認

```bash
> git config --global -l
# 期待される出力
user.name=FirstName LastName
user.email=your.email@example.com
http.proxy=http://127.0.0.1:17200
http.sslVerify=http://127.0.0.1:17200
https.proxy=http://127.0.0.1:17200
```
