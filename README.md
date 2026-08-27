# 架空マップメーカー PWA v22

既存の本番リポジトリ `fictional-map-maker` へ上書き更新するための正式版です。

## 更新方法

ZIPを展開し、リポジトリの root に次の6ファイルをアップロードして上書きしてください。

- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png
- README.md

ZIPそのものはアップロードしません。

## GitHub Pages

既に GitHub Pages が
- Source: Deploy from a branch
- Branch: main
- Folder: /(root)

で公開されているなら、設定変更は不要です。

## 保存データ

本番版と同じ保存領域を使います。

- visible folder: `架空マップメーカー_保存データ`
- IndexedDB: `fictional-map-maker-pwa`
- current map key: `fictional-map-maker-current-name`

v18 / v14 の production localStorage からの移行も残しています。

## 安全性

ユーザーの地図・フレーム・名前を外部へ送信する処理はありません。
ページ本体は `connect-src 'none'`。
Service Worker は同じ GitHub Pages オリジンのアプリ本体だけをキャッシュします。
