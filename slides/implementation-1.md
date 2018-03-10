##  Middleman による実装

* フィーチャーモデル上の各フィーチャーをオプション変数として与える
* **実装の注意点:**
  * **グローバル変数ではなくローカル変数として与える**
  * **動的ページ機能(Proxy)を用いる**
  * **パラメータとしてローカル変数を渡す**

```ruby
options_hash = {
  "p0-s0-i0-r0-R0-S0": {  # オプションの組み合わせをキーとして表す
      program: :none,     # オプションの詳細をハッシュにする
      session: :disable,  # 実際にはオプションとその組み合わせを表にして自動生成する
      ...
    },
  ...
}

files = [
  "index.html",           # 生成する html ファイルを配列としてリストアップする
  "about/index.html",     # 実際にはファイルシステムから読み込んで自動生成する
  ...
]

options_hash.each do |path, options|
  files.each do |file|
    options[:rootURL] = path
    proxy "#{path}/#{file}", "/#{file}", :locals => {locals: options}
  end
end
```

