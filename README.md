# How_to_Pulsar2

* Pulsar2 を雰囲気で使ってみよう
* https://speakerdeck.com/anoken/pulsar2-wofen-wei-qi-deshi-tutemiyou

 ## Enviroment Install
 * Pytorchのインストール  
https://pytorch.org/get-started/locally/  
 *  ONNX/ONNXRUNTIMEのインストール  
  https://onnxruntime.ai/  
 * Pulsar2のインストール  
  https://pulsar2-docs.readthedocs.io/en/latest/user_guides_quick/quick_start_prepare.html#install-pulsar2-toolchain  

 ## How to ONNX to AXMODEL
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

![image](https://github.com/user-attachments/assets/84300a39-5381-45e9-950a-8872317ac572)


 ## How to run M5Stack Module-LLM
```
root@m5stack-LLM:# cd run_ModuleLLM
root@m5stack-LLM:# python3 axmodel_run.py
root@m5stack-LLM:# python3 onnxrutime_run.py
```
