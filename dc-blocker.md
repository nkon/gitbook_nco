# DCカットフィルタ

NCOだけではあっという間にネタが尽きてしまったので、DCカットフィルタについて蛇足しておく。
デジタルの特徴を生かした「コロンブスの卵」的な方法なので、興味がある方は味わって欲しい。

センサ信号で、オフセットがあるのでDCカットしたいときがある。

どうすればよいか？

単に、微分して積分すればよい。

伝達関数的には、微分して積分したら元に戻るが、その過程でDC成分が落ちる。アナログ回路の場合は自身のオフセットや周波数特性のために、完全な微分回路、完全な積分回路を構成することは難しい。しかしデジタルの場合は、サンプリング定理の範囲内で、理想的に動作する。

数個のサンプルの平均をとって引き算するという方法よりも、記憶領域も少なくて済み、特性評価(移動平均フィルタの特性を考慮するよりも)も素直だ。

実際には、R=0.99 という係数が必要になるみたいだ。また、整数演算でもよいが符号付で演算しなければならないことに注意。

* [DC Blocker](http://bfin.sakura.ne.jp/?p=818)

