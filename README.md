# generate-plantuml

## Generate Plantuml

星が一番多かったけどイマイチ  
外部リクエストして図を生成しているのが致命的

repository:
https://github.com/marketplace/actions/generate-plantuml

- rootに配置されたファイルをカレントパス(.)で生成しようとするとエラー
  - 必ず1つディレクトリを挟む必要がある
- svgファイル名に日本語を指定するとumlとして認識されなくなる
- 外部へリクエストして画像化しているセキュリティ...
  - http://www.plantuml.com/plantuml/svg/${encoded}
