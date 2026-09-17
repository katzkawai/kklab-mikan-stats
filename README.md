# なぜみかんの収穫量は激減したのか？

農林水産省「果樹生産出荷統計」等の全国データ（1973年〜2025年）から、みかん収穫量の長期推移と背景を解説するWebサイトです。

## 公開サイト（GitHub Pages）
- URL: https://katzkawai.github.io/kklab-mikan-stats/

## 概要
- ピーク時収穫量（1975年）：3,665千トン
- 最新収穫量（2025年・概数）：656.3千トン（1975年比 -82.1%、前年比 +17.3%）
- 2024年の収穫量：559.6千トン（1975年比 -84.7%）
- 主要果実4品目（みかん・りんご・日本なし・ぶどう）の毎年の推移と、全53年の数値表
- 結果樹面積の縮小と、天候・隔年結果による年ごとの作柄を分けた説明
- 生産調整、輸入自由化、品目転換、担い手不足と近年の政策の解説

## ローカルでの表示

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

`http://127.0.0.1:8000/` を開きます。ビルドは不要です。Chart.js 4.5.1をCDNから読み込むため、グラフの表示にはインターネット接続が必要です。数値表と本文はJavaScriptなしでも閲覧できます。

## 出典
確認日：2026年9月17日。2025年産は第1報の概数で、確報や訂正により変更される可能性があります。

- 1973〜2024年：[e-Stat「果樹生産出荷統計・長期累年」](https://www.e-stat.go.jp/stat-search/files?toukei=00500215&tstat=000001013427&tclass1=000001032287&tclass2=000001037847)の全国表（2026年3月23日更新）。みかん `000040421665`、りんご `000040421905`、日本なし `000040422001`、ぶどう `000040421953`。
- 2025年：[みかん（PDF）](https://www.maff.go.jp/j/tokei/kouhyou/sakumotu/sakkyou_kazyu/pdf/syukaku_mikan_25.pdf)、[りんご（PDF）](https://www.maff.go.jp/j/tokei/kouhyou/sakumotu/sakkyou_kazyu/pdf/syukaku_ringo_25.pdf)、[日本なし・ぶどう（PDF）](https://www.maff.go.jp/j/tokei/kouhyou/sakumotu/sakkyou_kazyu/pdf/syukaku_ninasi_25.pdf)。
- 政策・歴史：[果樹農業の現状と課題について（PDF）](https://www.maff.go.jp/j/council/seisaku/kazyu/r06_01_kazyubukai/attach/pdf/241016-12.pdf)など。本文中に各説明の参照先を記載しています。

収穫量は元表のtを1,000で割り、千tで掲載しています。グラフはHTMLの数値表から描画します。更新時は表、KPI、本文、対象年・概数表示、出典、READMEを合わせて確認してください。

以前の値を公表統計と照合して修正し、4品目を同じ長期統計で確認できる1973年以降の毎年の値に統一しました。1960・1965・1970年の未確認値は掲載していません。

## 構築
初版は Antigravity (Gemini 3.8 Flash) により構築されました。
