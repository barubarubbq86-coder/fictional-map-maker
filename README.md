# 架空マップメーカー PWA v18

GitHub Pages 更新用の正式版です。

## アップロードするファイル

ZIPを展開し、リポジトリの一番上（root）へ次の6ファイルをアップロードしてください。

- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png
- README.md

保存した地図JSONや「架空マップメーカー_保存データ」フォルダはGitHubへアップロードしないでください。

## GitHub Pages設定

Settings → Pages → Build and deployment

- Source: Deploy from a branch
- Branch: main
- Folder: /(root)

既にこの設定が済んでいる場合、更新時に設定し直す必要はありません。

## 保存データ

作成した地図はGitHubへ送信せず、各端末のPWA内部領域と、ユーザーが許可した
「架空マップメーカー_保存データ」
に保存します。

v14正式版と同じ保存フォルダ名・IndexedDB名を使用し、v18はv14のlocalStorageデータも読み込めるようにしています。
