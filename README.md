# 学振LaTeX (2020年度採用分対応)

[![Build Status](https://travis-ci.org/ken-nakanishi/gakushinLaTeX.svg?branch=master)](https://travis-ci.org/ken-nakanishi/gakushinLaTeX)

DC・PD申請のための非公式LaTeXテンプレートです。
公式LaTeXテンプレートは
[科研費LaTeX](http://osksn2.hep.sci.osaka-u.ac.jp/~taku/kakenhiLaTeX/)
です。

ダウンロードは[こちら](https://github.com/ken-nakanishi/gakushinLaTeX/releases)からできます。

## 非公式LaTeXテンプレートを作った理由
- 簡潔なコードにしたい
- 容易に調整可能なコードにしたい
- SyncTeXで記述内容に飛べるようにしたい

と思い、自分のために作成しました。
要望を複数受けて公開することにしました。

## 必要な環境
TeX Live 2017以降
(TeX Live 2015, 2016でもおそらく大丈夫)

## コンパイル方法
dc または pd のディレクトリ内で
```
latexmk main.tex
```

## 書き換える場所
- main.texの名前
- (数字)_hogehoge.tex
    - (数字)は申請書の記述欄の番号に対応

## 注意点
複数ページにまたがる記述欄において、
枠の終わるページの次のページまで文章がはみ出した場合、
後のページがすべてズレます。

## 開発者向け
バグを見つけた場合はissueやpull requestで報告お願いいたします。
改善案があればissueでご提案いただきたいです。

## platexを使いたい人向け
uplatexではなくplatexを使いたい方は次のように変更
 
- main.texの`ujarticle`を`jarticle`または`jsarticle`に変更
- latexmkrcの`uplatex`と`upbibtex`から`u`を削除
