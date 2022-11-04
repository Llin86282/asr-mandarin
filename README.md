
## 環境

## 訓練軟硬體需求
### 硬體
* CPU: 4核 (x86_64, amd64) +
* RAM: 16 GB +
* GPU: NVIDIA, Graph Memory 11GB+ (1080ti起步)
* HDD: 500 GB 机械硬盘(或固态硬盘)

### 軟體
* Linux: Ubuntu 18.04 + / CentOS 7 +
* Python: 3.7 +
* TensorFlow: 2.5 +

## 訓練


準備環境：
```shell
$ cd asr_mandarin

$ python3 -m venv venv

$ source venv/bin/activate

$ pip3 install -r requirements.txt
```

準備訓練資料：
```shell
$ mkdir $PROJECT_HOME/data/speech_data

$ cd $PROJECT_HOME/data/speech_data

$ wget -c https://www.openslr.org/resources/33/data_aishell.tgz

$ tar zxf data_aishell.tgz -C /data/speech_data/

$ cd data_aishell/wav

$ cat *.tar.gz | tar zxvf - -i

$ rm *.tar.gz
```

開始訓練：
```shell
$ python3 train_speech_model.py
```

測試模型：
```shell
$ python3 evaluate_speech_model.py
```
