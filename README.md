# 架空マップメーカー PWA v14

GitHub Pages にそのまま置ける正式版です。

## GitHubへアップロードするファイル
このフォルダ内の次の6ファイルを、リポジトリの一番上（root）へ置いてください。

- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png
- README.md

地図のJSONファイルや「架空マップメーカー_保存データ」フォルダはGitHubへアップロードしないでください。

## GitHub Pages
Settings → Pages → Build and deployment
- Source: Deploy from a branch
- Branch: main
- Folder: /(root)

公開URLの例:
https://あなたのユーザー名.github.io/fictional-map-maker/

## 保存データ
作成した地図はGitHubには送信せず、端末内へ保存します。
外部保存先を設定すると、選択した親フォルダ内に
「架空マップメーカー_保存データ」
が作成されます。

## 更新
今後の更新は同名ファイルを新しい版へ置き換えて main にコミットします。
Service Worker のキャッシュ名も版ごとに変更します。
