# tutorial-docker-datascience
データサイエンス用dockerイメージを順を追って作る。(jupyter-labなどのpython開発環境を作成する)

## 1.基本的な機能について
todoをこなして以下の用語を理解する
```
dockerイメージ
dockerコンテナ
docker build
docker run
docker ps
```
- todo
- [ ] ローカルにdocker環境を用意する。(docker hello worldができるか？)
- [ ] https://qiita.com/sitilma/items/86609dc46e7e8835f7de


## 2.Dockerfile作成
Dockerfileを作成します。 以下のキーワードを理解を理解してください。
```
base iamage
Dockerfile
```

- todo
python で開発する環境をdockerでつくります(jupyterはいらない)。(参考: https://github.com/fkubota/Docker/tree/master/data_science)

以下のことができるDockerfileを作成してください。

- [ ] Dockerfile に 右のベースイメージを使ってください。 nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04
- [ ] Dockerfile に Python3 をいれる。さらにデフォルトのPythonをPython3にしてください。
- [ ] requirements.txt を作ってnumpyだけ書いてください。
- [ ] pip3 install でrequirements.txtのライブラリをインストールできるようにしてください。
- [ ] 作成したDockerfileでビルドを行ってください。
- [ ] 作成したイメージのコンテナを立ち上げて、python を立ち上げて、import numpy ができるか確かめてください。
