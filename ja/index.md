# CPKF-doc
これは[CPKF](https://github.com/yswallow/CPKF)の使い方をまとめたリポジトリです。

## ハードウェア要件

* 192KB以上のメモリを持つCircuitPythonが実行可能なマイコン
    * [CircuitPythonのSupport Matrix](https://circuitpython.readthedocs.io/en/latest/shared-bindings/support_matrix.html)で`usb_hid`がサポートされていること
    * メモリが32KBのCortex-M0マイコンでは動きません
* Bluetooth機能を使うために: [CircuitPythonのSupport Matrix](https://circuitpython.readthedocs.io/en/latest/shared-bindings/support_matrix.html)で`_bleio`がサポートされていること


## インストール方法
1. [CPKF](https://github.com/yswallow/CPKF)のZIPファイルをダウンロードして展開する
2. 展開したファイルを`CIRCUITPY`ドライブのルートに置く
3. [Adafruitのライブラリファイル](https://github.com/adafruit/Adafruit_CircuitPython_Bundle/releases)をダウンロードして展開する。(`mpy`でも`py`でも可)
4. ライブラリファイルから, 以下に挙げるものを`(CIRCUITPY/)lib/`にコピーする。この際, ZIPファイルを展開したフォルダーの`lib/folder/file.py`は`(CIRCUITPY/)lib/folder/file.py`にコピーする。`mpy`を利用する場合は拡張子を読み替えてください。ここにはキーボードとしての動作に最低限必要なものしか記載しません。使用する機能によって他のライブラリが必要になります。
    * `adafruit_hid/__init__.py`
    * `adafruit_hid/keyboard.py`
    * `adafruit_hid/keycode.py`
5. 使用するキーボードの定義ファイルを`(CIRCUITPY/)lib/keyboard/`にコピーする
5. ファイルの書き込みが完了するとキーボードのデフォルトキーマップを読み込んで動作するはずです。

## 機能
* [押すとキーを入力する](./feature/keycode.md)
* [長押しと短押しで違う動作を割り当てる](./feature/keyobject.md)
* [キーコンビネーションを1つのキーに割り当てる](./feature/keyobject-with-modifier.md)
* [マウス操作](./feature/mouse.md)
* [音量調整など](./feature/consumer_control.md)
* [Bluetooth](./feature/bluetooth.md)

## LEDの色と意味

### 点灯している
正常に動作しています

#### 緑色
USBキーボードとして動作している, またはBluetoothの接続がLEDに反映されていません

#### 赤色
USBキーボードとして動作しています

#### 青色
Bluetoothキーボードとして動作しています

### 点滅している
エラーが発生して動作が停止しています。ファイル書き込み直後でないなら, リセットボタンを押してください。

詳しくは[Adafruitのドキュメント](https://learn.adafruit.com/welcome-to-circuitpython/troubleshooting#circuitpython-rgb-status-light-2978455-20)を参照

## カスタマイズ方法

### キーマップを変更する

`lib/keyboard/default-keymap.py`を`(CIRCUITPY/)keymap.py`にコピーし, 書き換えることでキーマップを変更できます。キーの種類については[機能一覧](`./feature`)を参照してください。

## 独自のキーボードを定義する

## サポートを受ける

### エラーログを取る

#### シリアルモニタを利用できる場合
シリアルモニタに表示されたエラーメッセージをコピペしてください。

#### シリアルモニタを利用できない場合
`log`フォルダーに`error-output-enable.txt`という名前のファイルを保存し, `error-checked.txt`というファイルを削除してマイコンの電源を切って入れるとエラーログが1回のみ`(CIRCUITPY/log/)error.txt`に出力されます。ただし, この状態ではファイルの書き込みができないため, 書き込む場合は再度マイコンの電源を入れ直してください。

## 現在の開発環境

[テスト環境](./testing.md)を参照

## わかっている問題

[わかっている問題](./issues.md)を参照

