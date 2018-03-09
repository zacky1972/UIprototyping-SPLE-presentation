##  Motivating Example (1/2)

* [SWEST(組込みシステム技術に関するサマーワークショップ)](https://swest.toppers.jp)
  * 毎年8月頃に開催
  * 産学連携が特徴
  * 情報処理学会組込みシステム研究会とも連携
* 2017年からウェブサイトのリニューアルに着手した
  * 当初は WordPress を用いていた
  * プログラムページのみRubyスクリプトによるデザインと実装を行った
* 2017年のイベント終了後に[報告ページ](https://swest.toppers.jp/SWEST19/program/)を実装した
  * Rubyベースの静的ウェブサイト生成器 **Middleman**を採用した
  * 高い記述性・再利用性により，たった数日程度の短期間で開発できた