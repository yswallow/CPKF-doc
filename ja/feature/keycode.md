# 押すとキーを入力する機能

## 定義されている場所

```
adafruit_hid/keycode.py
cpkf/keycode_jp.py
```

## 記法

```
from adafruit_hid.keycode import Keycode as KC
from cpkf.keycode_jp import KeycodeJP as JP

KC.A
JP.ATMARK
```

## 機能

キーが押された際にそのキーに割り当てられた文字が入力されます。

## 依存ライブラリ

```
cpkf/key_object.py
```

## 定義されているキー

Keycodeについては https://circuitpython.readthedocs.io/projects/hid/en/latest/api.html#adafruit-hid-keycode-keycode

KeycodeJPについては[コードを見てください](https://github.com/yswallow/CPKF/blob/master/lib/CPKF/keycode_jp.py)

