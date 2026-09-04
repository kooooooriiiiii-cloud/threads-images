# threads-images

Threads投稿に添付する画像の置き場。

Threads API の `image_url` は「Threads側のサーバが取得できる公開URL」しか受け取れず、
ローカルのファイルパスを渡せない。予約投稿の実行役（Mac側のアプリ・GitHub Actions）が
画像付きで投稿するために、ここへ置いた画像の raw URL を渡している。

- 置き場所: `<アカウントID>/<YYYYMMDD>_<slug>/01.jpg` …
- 参照URL: `https://raw.githubusercontent.com/kooooooriiiiii-cloud/threads-images/main/<パス>`
- 追加は `.claude/scripts/publish_images.py` から行う（手で置かない）

公開リポジトリなので、ここに置いてよいのは投稿に載せる画像だけ。
トークン・個人情報・投稿本文は置かない。
