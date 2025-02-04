# How_to_Pulsar2

```
　# Pulsar2(docker)を起動
user@ubuntu$ sudo docker run -it --net host -v $PWD:/data pulsar2:3.3
　# pulsar2 buildでモデル変換(量子化＆コンパイル)
root@:/data# pulsar2 build --config matmul_model.json
```
