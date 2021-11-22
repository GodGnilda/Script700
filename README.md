# 改良版 SNESAPU.DLL (v2.19.0 以降) のスクリプト

## 概要
[改良版 SNESAPU.DLL](https://github.com/dgrfactory/spcplay) (v2.19.0 以降) で動作するスクリプトファイルです。  
- サウンドドライバファンクションを利用して、音楽データや圧縮波形データ等を APU RAM に転送し音楽を演奏します。
- サウンドドライバファンクションを利用して、効果音を演奏します。
- スクリプトの動作は同ファイル名の MD ファイルでご確認ください。

## 動作
- v2.19.0 以降 で使用可能な `wi` コマンドで、SPC700 が指定した入力ポートを読み込むまで待機可能になりました。  
データ転送などで、 `w` コマンドを使用し待ち時間を調整する必要がなくなりました。
- v2.19.0 以降 で使用可能な `wo` コマンドで、SPC 出力ポートの値が変化しているか確認を省略することが可能になりました。   
データ転送などで、 `w` コマンドを使用し待ち時間を調整する・値が更新されたかどうかを確認する必要がなくなりました。

## プレイヤーの設定など
- [SNES SPC700 Player](https://github.com/dgrfactory/spcplay)
  - SNES SPC700 Player を起動し、バージョンを確認します。  
  v2.19.0 以降のバージョンではない場合は https://github.com/dgrfactory/spcplay/releases から spcplay-x.xx.x.xxxx.zip (v2.19 以降) をダウンロードし SNES SPC700 Player を更新します。
- [黒猫SPC](https://kurohane.net/seisanbutu.html)
  - 演奏設定ウィンドウ 黒猫 タブで、**使用する SNESAPU** を **Sunburst** に設定します。
  - メインウィンドウで [改良版 SNESAPU.DLL](https://github.com/dgrfactory/spcplay) のバージョンを確認します。  
  v2.19.0 以降のバージョンではない場合は 黒猫SPC を終了し、 https://github.com/dgrfactory/spcplay/releases から snesapu-x.xx.x.xxxx.zip (v2.19 以降) をダウンロードし、黒猫SPC の SNESAPU Sunburst フォルダの DLL を上書きします。
  - 演奏設定ウィンドウ SNESAPU タブの **NoScript700** のチェックを**オフ**にし、スクリプトを有効にします。

## 使用方法
### ROM のデータを転送して音楽演奏
- [SNES SPC700 Player](https://github.com/dgrfactory/spcplay)
  - SPC とスクリプトのファイル名が同じ場合は、SPC ファイルを開きます。  
  スクリプトファイルが自動的に読み込まれ、指定した曲のテータを転送し演奏開始します。
  - SPC とスクリプトのファイル名が異なりスクリプトファイルが自動的に読み込まれない場合は、SPC ファイルを開いた後にスクリプトファイルをドラッグ & ドロップします。  
  スクリプトファイルが更新され、指定した曲のテータを転送し演奏開始します。演奏状態は初期化されます。
  - ブレークポイントコマンド `bp` を使用したスナップショット保存をご利用になれます。  
保存するタイミング次第では DSP のキーオンフラグがクリアされずにノイズが発生する場合がございます。この不具合は SPC ファイルの $1014C を $00 に書き換えることで解消可能です。
- [黒猫SPC](https://kurohane.net/seisanbutu.html)
  - SPC とスクリプトのファイル名を同じにして、SPC ファイルを開きます。  
  スクリプトファイルが自動的に読み込まれ、指定した曲のテータを転送し演奏開始します。
  - ブレークポイントコマンド `bp` を使用したスナップショット保存はご利用になれません。

## フォルダ
- F4
  - FINAL FANTASY IV
- F4G
  - FINAL FANTASY IV 改造サウンドドライバ
- QN
  - 新・熱血硬派くにおたちの挽歌

## ライセンス
[MITライセンス](https://opensource.org/licenses/mit-license.php)
