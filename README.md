# How_to_Pulsar2

```
　# Pulsar2(docker)を起動
user@ubuntu$ sudo docker run -it --net host -v $PWD:/data pulsar2:3.3
　# pulsar2 buildでモデル変換(量子化＆コンパイル)
root@:/data# pulsar2 build --config matmul_model.json
```

```
root@m5stack-LLM:# cd run_ModuleLLM
root@m5stack-LLM:# python3 axmodel_run.py
root@m5stack-LLM:# python3 onnxrutime_run.py
```
