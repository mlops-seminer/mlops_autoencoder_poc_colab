# MLOps Autoencoder - Colab持ち帰り版

元の `main.py`、`model.py`、`dataset.py` は変更していません。

変更したのは `config/config.yaml` の次の2項目だけです。

- `dataset.root_dir`: `autoencoder_poc/data/kinoko` → `data/kinoko`
- `mlflow.tracking_uri`: `http://localhost:8080` → `sqlite:///mlflow.db`

## Colabでの実行

1. GoogleアカウントでログインしColabを開きます。
2. 新しいノートブックを開き以下を実行します。
ドライブと連携します。
```
from google.colab import drive
drive.mount("/content/drive")
```
保存先に移動します
```
import os
DRIVE_DIR = "/content/drive/MyDrive"
os.chdir(DRIVE_DIR)
print(os.getcwd())
```
GitHubからプロジェクトをcloneします。
```
!git clone https://github.com/mlops-seminer/mlops_autoencoder_poc_colab.git
```
2. 数分後、Driveにmlops_autoencoder_poc_colabが保存されるので`mlops_autoencoder_colab_minimal.ipynb` を直接クリックしColabで開きます。
3. ランタイムから「ランタイムのタイプを変更」を選択しGPU環境にします。
4. config.yamlで設定を行い上から順番にセルを実行します。

MLflowの履歴はプロジェクトフォルダ内の `mlflow.db` と `mlartifacts/` に保存されます。
