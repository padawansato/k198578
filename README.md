- 実行環境
	- OS：ubuntu 18.04
- データセット
	- movie lens 100k dataset
- 利用した主要なライブラリ
	- scikit-learn (0.22.1)
	- notebook (5.1.0)
	- jupyter (1.0.0)
	- jupyter-client (5.1.0)
	- jupyter-console (5.2.0)
	- jupyter-core (4.3.0)
	- numpy (1.19.5)
	- pandas (0.20.3)
	- pickleshare (0.7.4)
	- lime (0.2.0.1)
	- fastFM (0.2.11)


- 再現方法
	- 環境構築1
		- requirement.txtを参考に環境構築をする。
	- 環境構築2
		- dockerhubを用いてコンテナをダウンロードする。
		- 'docker pull padawane15/ubuntu_py3.5.1_fastfm:sklearn22'
	- 実験の再現手引(追加実験を除く)
		- ファイル名："Scaling + LIME + BigData.ipynb"
		- Jupiternotebookファイルを実行することで、順次実験結果を得る。
	- 追加実験の再現手引
		- ファイル名："randomsampling.ipynb"
		- 追加実験ではlimeライブラリを一部改正したmylimeを呼び出す。そのため、実行環境(pythonラインタイム)が呼び出すlimeライブラリのpathを調べる。
		- limeを改変した、mylimeライブラリをJupyternotebookファイルから呼び出せる場所(本実験の場合、同一階層のディレクトリ)に配置しJupyternotebookファイルを実行すること実験結果を得る。
		- 追加実験では、ランダムサンプリングではないデータセットを生成し、それをLIMEライブラリを一部改変したライブラリから呼び出すことでLIMEアルゴリズムがランダムサンプリングして疑似データを生成する過程の代わりに自作のデータセットを渡すことで自作のデータセットを用いた推論結果を得た。
- ソースコード
	- github:'https://github.com/psato/k198578'
	- dockerhub:'padawane15/ubuntu_py3.5.1_fastfm:sklearn22'


