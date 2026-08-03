# MLOps Autoencoder - Colab持ち帰り版（最小変更）

元の `main.py`、`model.py`、`dataset.py` は変更していません。

変更したのは `config/config.yaml` の次の2項目だけです。

- `dataset.root_dir`: `autoencoder_poc/data/kinoko` → `data/kinoko`
- `mlflow.tracking_uri`: `http://localhost:8080` → `sqlite:///mlflow.db`

## Colabでの実行

1. このフォルダをGoogle Driveの `MyDrive` に保存します。
2. `mlops_autoencoder_colab_minimal.ipynb` をColabで開きます。
3. `PROJECT_DIR` を実際の保存先に合わせます。
4. 上から順番にセルを実行します。

MLflowの履歴はプロジェクトフォルダ内の `mlflow.db` と `mlartifacts/` に保存されます。
