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
[todo]
- [ ] ローカルにdocker環境を用意する。(docker hello worldができるか？)
- [ ] https://qiita.com/sitilma/items/86609dc46e7e8835f7de


## 2.Dockerfile作成
Dockerfileを作成します。 以下のキーワードを理解を理解してください。
```
base iamage
Dockerfile
```

[todo]
python で開発する環境をdockerでつくります(jupyterはいらない)。(参考: https://github.com/fkubota/Docker/tree/master/data_science)

以下のことができるDockerfileを作成してください。

- [ ] Dockerfile に 右のベースイメージを使ってください。 nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04
- [ ] Dockerfile に Python3 をいれる。さらにデフォルトのPythonをPython3にしてください。
- [ ] requirements.txt を作ってnumpyだけ書いてください。
- [ ] pip3 install でrequirements.txtのライブラリをインストールできるようにしてください。
- [ ] 作成したDockerfileでビルドを行ってください。
- [ ] 作成したイメージのコンテナを立ち上げて、python を立ち上げて、import numpy ができるか確かめてください。


## 3. ローカルのファイルをコンテナに渡す
docker run の以下のオプションを理解してください。
```
--rm
-it
-v
```
[todo]
ローカルにあるファイル(wavファイルにしましょう)をコンテナから見れるようにしたいと思います。 (参考: https://github.com/fkubota/Docker/tree/master/data_science)

task2 を改良したDockerfileを作成してください。(参考リポジトリと同様、entorypointを作成してもいいです。)
以下のことを行ってください。

- [ ] ローカルのディレクトリ(wavファイルがある)をマウントして、dockerコンテナ側から見れるようにしてください。
- [ ] docker コンテナを立ち上げてpythonスクリプト(check_recording_time.py)を書いてください。
- [ ] wavを読み込んでwavの時間をprintで出力するだけのスクリプト
- [ ] スクリプトの場所はマウントした場所と同じ
- [ ] コンテナから出て、作成したcheck_recording_time.py スクリプトをローカル環境で編集しようとしてください。(権限の問題でできないはず)
- [ ] check_recording_time.py スクリプトの権限を確認してください。
- [ ] 上記の問題(dockerで作ったファイルをローカルから触れない)を解決してください。参考リポジトリでは、ユーザーをdockerに渡すということをしています。


## 4. jupyter-lab をdokcer内で使えるようにする
最後です。

[todo]
- [ ] docker内にjupyter-labを入れて、webブラウザでjupyter-labが使えるか確認してください。
	- task3と同様、権限の問題も回避するようにしてください。 (参考: https://github.com/fkubota/Docker/tree/master/data_science)
