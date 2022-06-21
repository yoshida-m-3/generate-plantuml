# generate-plantuml

## commit-plantuml-action

repository:
https://github.com/abekoh/commit-plantuml-action

良さそう。  

- ubuntuコンテナにjavaのPlantUml環境を構築してコンテナ内部で図を生成している
  - 外部に投げていないのが良い！
- PR作成タイミングで実行される
- PRのbranchに生成した図がcommitされる
- PRのコメントにbefore/afterが追加される
  - https://github.com/yoshida-m-3/generate-plantuml/pull/2#pullrequestreview-1013541793
- PRサンプル
  - https://github.com/yoshida-m-3/generate-plantuml/pull/2

作者は日本人だった
https://blog.abekoh.dev/posts/plantuml-action

- 

## Generate Plantuml

repository:
https://github.com/marketplace/actions/generate-plantuml

星が一番多かったけどイマイチ  
外部リクエストして図を生成しているのが致命的

- markdownの中に書いたplantumlを出力できるのは良い（1markdownに複数定義も可）
- rootに配置されたファイルをカレントパス(.)で生成しようとするとエラー
  - 必ず1つディレクトリを挟む必要がある
- svgファイル名に日本語を指定するとumlとして認識されなくなる
- 外部へリクエストして画像化しているセキュリティ...
  - http://www.plantuml.com/plantuml/svg/${encoded}
