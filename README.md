# How_to_Pulsar2

 # 事前準備
 * Pytorchのインストール  
https://pytorch.org/get-started/locally/  
 *  ONNX/ONNXRUNTIMEのインストール  
  https://onnxruntime.ai/  
 * Pulsar2のインストール  
  https://pulsar2-docs.readthedocs.io/en/latest/user_guides_quick/quick_start_prepare.html#install-pulsar2-toolchain  

 
```
　# Pulsar2(docker)を起動
user@ubuntu$ sudo docker run -it --net host -v $PWD:/data pulsar2:3.3

　# ONNXモデルを生成
root@:/data# python onnx_matmul_export.py

　# キャリブレーションのデータセットを生成
root@:/data# python gen_calib_dataset.py

　# pulsar2 buildでモデル変換(量子化＆コンパイル)
root@:/data# pulsar2 build --config matmul_model.json
```

```
root@m5stack-LLM:# cd run_ModuleLLM
root@m5stack-LLM:# python3 axmodel_run.py
root@m5stack-LLM:# python3 onnxrutime_run.py
```
