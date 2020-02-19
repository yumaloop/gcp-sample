# hoge

```bash
# Build docker image from Dockerfile
$ docker image build --rm -t <image_name>:<tag_name> <PATH_TO_DOCKERFILE>
```

```bash
# Create new docker container from docker images
$ docker run -it <image_name>:<tag_name>
```

Options:
- d: バックグランドで実行
- i: コンテナの標準入力を開く
- t: ttyを確保する
- p: ポートフォワード


