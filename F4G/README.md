# FINAL FANTASY IV 改造サウンドドライバ のスクリプト

## 概要
[FINAL FANTASY IV の改造サウンドドライバ](https://github.com/GodGnilda/F4G-0) 20211224-0 以降の SPC ファイル用のスクリプトファイルです。  
[改良版 SNESAPU.DLL](https://github.com/dgrfactory/spcplay) (v2.19.0 以降) で動作します。

## スクリプト一覧
- [ROM のデータを使用して音楽を演奏するスクリプト](https://github.com/GodGnilda/Script700/blob/main/F4G/F4G_F4G.700) ( [MD ファイル]([https://github.com/GodGnilda/Script700/blob/main/F4G/F4G_F4G.md) )
- [音楽と圧縮波形のデータファイルを使用して音楽を演奏するスクリプト](https://github.com/GodGnilda/Script700/blob/main/F4G/F4G_1.700) ( [MD ファイル]([https://github.com/GodGnilda/Script700/blob/main/F4G/F4G_1.md) )

## ファイル
- [FINAL FANTASY IV の改造サウンドドライバ](https://github.com/GodGnilda/F4G-0) が転送された状態の SPC ファイルが必要です。  
スナップショットを保存せずそのまま演奏する場合は、ジングル類を演奏終了状態の SPC をお使いになることで、ノイズ発生を抑制することが可能です。

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
- [SNES SPC700 Player](https://github.com/dgrfactory/spcplay)
  - SPC とスクリプトのファイル名が同じ場合は、SPC ファイルを開きます。  
  スクリプトファイルが自動的に読み込まれ、指定した曲のテータを転送し演奏開始します。
  - SPC とスクリプトのファイル名が異なりスクリプトファイルが自動的に読み込まれない場合は、SPC ファイルを開いた後にスクリプトファイルをドラッグ & ドロップします。  
  スクリプトファイルが更新され、指定した曲のテータを転送し演奏開始します。演奏状態は初期化されます。
  - ブレークポイントコマンド `bp` を使用したスナップショット保存をご利用になれます。
- [黒猫SPC](https://kurohane.net/seisanbutu.html)
  - SPC とスクリプトのファイル名を同じにして、SPC ファイルを開きます。  
  スクリプトファイルが自動的に読み込まれ、指定した曲のテータを転送し演奏開始します。
  - ブレークポイントコマンド `bp` を使用したスナップショット保存はご利用になれません。

## 演奏開始直前のスナップショット保存
ブレークポイントを利用可能なプレイヤーのみ保存可能です。
- [SNES SPC700 Player](https://github.com/dgrfactory/spcplay)  
スクリプトの `bp` コマンドを有効にし、SPC700 の PC レジスタの値が $05AE で停止している状態であることを確認後に SPC ファイルを保存してください。  
保存するタイミング次第では DSP のキーオンフラグがクリアされずにノイズが発生する場合がございます。この不具合は SPC ファイルの $1014C を $00 に書き換えることで解消可能です。
  <details>
  <summary>以前のバージョンのブレークポイント</summary>

  |バージョン|ブレークポイント|
  |:----:|:----:|
  |20211122-0|$0544|
  |20211124-0|$0544|
  |20211224-0|$05AE|
  </details>

## ライセンス
[MITライセンス](https://opensource.org/licenses/mit-license.php)
