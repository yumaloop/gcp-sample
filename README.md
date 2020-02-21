# gcp-sample code

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

「Ctrl+P, Ctrl+Q」でコンテナ43aaef3339fdから抜ける

```
$ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
43aaef3339fd        uchiumi:latest      "/bin/bash"         11 seconds ago      Up 10 seconds                           keen_shaw

```

コンテナ43aaef3339fdへあったち．
```
$ docker attach 43aaef3339fd
```

nvidia-docker2を使ってコンテナを起動
```
$ docker run --name <container_name> --rm --runtime=nvidia -it -p 8888:8888 nvidia/cuda /bin/bash
```
