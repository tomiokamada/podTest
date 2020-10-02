# podTest

gitPod をベースに C/C++ の初歩教育をおこなうための環境テスト

## gitPod での使い方

初回アクセス

1. github にアカウントをとっておく
2. https://gitpod.io/#https://github.com/tomiokamada/podTest にアクセス
3. 1-2分待ったほうがよいかも。（いくつかplugin が load されたりします）

２回目からのアクセス

1. https://gitpod.io/workspaces/ から、自分の実行したい workspace を選びましょう。
	* 14日使っていない状態が続くと、workspace が消滅します。
	* ファイルなどを置いておきたい人は、このページから `Download` ボタンを押せばよいでしょう。

プログラムの実行（ターミナル）

1. `Terminal` -> `New Terminal` でターミナルが開きます。
2. あとは、gcc なりでコンパイルして、実行してみましょう。
3. 以下は、`samples` directory の `hello.c` をコンパイルして実行した例

```
gitpod /workspace/podTest $ cd samples
gitpod /workspace/podTest/samples $ ls
hello.c
gitpod /workspace/podTest/samples $ gcc hello.c 
gitpod /workspace/podTest/samples $ ./a.out 
Hello World!
gitpod /workspace/podTest/samples $ 
```

プログラムの実行（例）

1. `samples/hello.c` を開いてください。`samples` をクリックすると、directory の中のファイルも見えるはず。
2. 実行対象プログラムをEditor 上で選択した状態(`hello.c`選択）で、"Terminal"->"Run Build Task.." でコンパイル可能。選択肢が出ますので、`build gcc`をえらびましょう。同じ directory に `hello` ができれば成功
   * `注1`: 違うファイルを選択していると、コンパイルできません。
   * `注2`: explorer 側で選択するだけでなく、エディタのフォーカスがあっている必要があるようです。
3. `Debug`->`Start Debugging` でデバッグ開始

情報共有

* 演習時間中などに、学生の workspace の状態をみたければ、workspace 実行時の URL を送ってもらえば OK.
  * `注`： https://gitpod.io/workspaces/ にて、当該 workspace を公開状態にしてもらう必要がある。


## 中身のファイルの解説

* .theia
  * tasks.json: Build の選択肢設定
  * launch.json: プログラム起動の選択肢設定
* tests
  * 今回ファイルをおいた場所
  * 別にプログラムファイルはお好きな場所に。
* .gitpod.Dockerfile, .gitpod.yml: 実行環境の docker 設定および extension 設定 (参考：[C/C++](https://www.gitpod.io/docs/languages/cpp/), [.gitpod.yml](https://www.gitpod.io/docs/config-gitpod-file/))
* README.md: このファイル





  

