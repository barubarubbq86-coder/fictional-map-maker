# 架空マップメーカー PWA v24

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

## v23 変更点
- 実在地図リストに「南極」を確実に表示
- 南極を一覧の先頭に固定
- 国・地域リストを80件制限から全件スクロール表示へ変更

## v24 変更点
- 完成画面に「🌐 地球儀風表示」を追加
- 通常地図 / 地球儀風表示を切替可能
- 地球儀を左右ドラッグして回転
- 地球儀表示のままフレームアニメーション再生に対応
- 球面陰影・緯線・経線を追加
