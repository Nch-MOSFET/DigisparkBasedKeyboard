# DigisparkBasedKeyboard について

## ディレクトリ構造

- archives
  - 過去バージョンのファームウェアを保存しています
- bootloader
  - 使用しているブートローダのデータです
- latest
  - 最新版ファームウェアはこちら

## ハードウェア仕様

実装されている2つのスイッチ、「SW1」と「SW2」はそれぞれプルアップ抵抗を介して「PB0」と「PB2」に接続されています </br>
このキーボードはコントローラ部分にDigisparkマイコンを使用しているため「Digispark」として認識されます </br>
PCに接続する際は金色の端子が4本並んでいるところをUSB-A端子に挿入します </br>

## ソフトウェア仕様

`digitalRead();` 関数を用いて各スイッチの状態を取得し、一つ前のデータと比較して「押された瞬間」にそのスイッチに割り当てられている文字列をキーボード入力します </br>
PC側に`Google 日本語入力` を導入することでマルチバイト文字まで拡張することも可能です </br>
