##  インタプリタ

* ElixirでZEAMを記述する
* ZEAMはErlang(≒Elixir)で書かれたプログラムを実行する
* すなわち，ZEAM は Elixir で書かれたプログラムを実行する Elixir のプログラムということになる
* こういうのを，自己反映計算(リフレクション: reflection) とか メタプログラミング(meta programming)という
* 定説では，インタプリタ実行をインタプリタ実行するので，**通常より10倍くらい遅い**と言われるが，Elixir では果たして。。。?!