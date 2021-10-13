# 改良版 SNESAPU.DLL (v2.19.0 以降) のスクリプト
***
## 概要
[改良版 SNESAPU.DLL](https://github.com/dgrfactory/spcplay) (v2.19.0 以降) で動作するスクリプトファイルです。  
- サウンドドライバファンクションを利用して、音楽データや圧縮波形データ等を APU RAM に転送し音楽を演奏します。
- サウンドドライバファンクションを利用して、効果音を演奏します。

### 動作
- v2.19.0 以降 で使用可能な `wi` コマンドで、SPC700 が指定した入力ポートを読み込むまで待機可能になりました。  
データ転送などで、 `w` コマンドを使用し待ち時間を調整する必要がなくなりました。
- v2.19.0 以降 で使用可能な `wo` コマンドで、SPC 出力ポートの値が変化しているか確認を省略することが可能になりました。   
データ転送などで、 `w` コマンドを使用し待ち時間を調整する・値が更新されたかどうかを確認する必要がなくなりました。

### ライセンス
[MITライセンス](https://opensource.org/licenses/mit-license.php)