# MLOps Autoencoder - Colab版
きのこの山異常検知モデルのPOCをColab上で体験できるようにしました。

## Colabでの実行

1. GoogleアカウントでログインしColabを開きます。
2. 新しいノートブックを開き以下をセルにコピーして順に実行します。
ログインしているアカウントでドライブと連携します。
```
from google.colab import drive
drive.mount("/content/drive")
```
プロジェクトの保存先に移動します
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
3. 数分後、Driveにmlops_autoencoder_poc_colabが保存されるので`mlops_autoencoder_colab_minimal.ipynb` を直接クリックしColabで開きます。
4. ランタイムから「ランタイムのタイプを変更」を選択しGPU環境にします。
5. config.yamlで設定を行い上から順番にセルを実行します。

MLflowの履歴はプロジェクトフォルダ内の `mlflow.db` と `mlartifacts/` に保存されます。
