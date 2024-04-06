# 本リポジトリについて
## 概要
Omron NJ/NX/NY (SysmacStudio)で使用することができるClock FB（ファンクションブロック）です。  
指定周期ごとにON、OFFを繰り返す信号を出力することができます。
Pull request（改善したプログラムの公開）、Issue（質問、バグ報告）大歓迎です。
  
## ファイル  
- ClockFB.csm2：プロジェクトファイル。ClockFBとClockFBの使用例が含まれています。
- ClockFB.slr：ライブラリファイル。ClockFBが含まれています。  
  
「ClockFB.slr」ではコードの変更することができないので、コードを変更したい方は、「ClockFB.csm2」を使用してください。
  
## 使用方法
- ClockFB.csm2を使用する場合：  
  SysmacStudioがインストールされたPCで、ダウンロードした「ClockFB.csm2」をダブルクリックすると、本プログラムが開きます。
  使用したいプロジェクトにファンクションブロックをコピーしてください。
- ClockFB.csm2を使用する場合：  
  「[Sysmac Studio Version 1 オペレーションマニュアル (SBCA-470)](https://www.fa.omron.co.jp/products/family/3077/download/manual.html)」の「9-3-2 ライブラリの利用」を参照してください。

  
# ClockFB
## 機能
指定した周期のクロック信号（ON、OFFを繰り返す信号）を出力します

## 入出力変数
| Left align | Right align | Center align |
|:-----------|------------:|:------------:|
| This       | This        | This         |
| column     | column      | column       |
| will       | will        | will         |
| be         | be          | be           |
| left       | right       | center       |
| aligned    | aligned     | aligned      |

## タイミングチャート
- Enableの立上りで、OutはTRUEになります。（出力ONから始まります）　　
- Enable=FALSEで、OutはFALSEになります。

<img width="500" alt="タイミングチャート" src="https://github.com/yuyuTds/ClockFB/blob/main/TimingChart.png?raw=true">


## 使用名前空間
- yuyuTds

## 注意点
- 入力変数Periodは、タスク周期の倍数を指定してください。倍数ではない場合、エラーになりませんが、出力の周期にズレが発生します。
- 本FBは、プライマリ定周期および、定周期タスクでのみ、使用可能です。


# ライセンスについて
本プログラムはMITライセンス
