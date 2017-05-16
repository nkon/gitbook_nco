# Introduction

これまで、ブザーを鳴らすのに PWM を使って、フルスイングの矩形波を発生して圧電ブザーを鳴らしていた。そうではなく、DACを使って、音量調整可能な波形を発生する方法について述べる。

独自の、自分で考えた方法ではなく、デジタル信号処理の分野で NCO と呼ばれている方法の解説である。オレオレプログラムではなく、バグが少なく、効率的で、理論的にも明確なので安心して欲しい。

## gitbook

この文書は gitbook スタイルで作られている。gitbook を使わずに見る場合は、SUMMERY.md からファイルをたどって欲しい。

### install

* Node.js をインストールする。
* `npm install -g gitbook-cli`。
* `gitbook build` でHTMLファイルがビルドされる。
* `gitbook serve` でサーバが立ち上がり、`http://localhost:4000`で、gitbook にアクセスできる。

