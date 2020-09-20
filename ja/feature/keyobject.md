# 長押しと短押しで別のキーを割り当てる

## 定義されている場所

`cpkf/key_object.py`

## 記法

```
from adafruit_hid.keycode  import Keycode as KC
from cpkf.key_object import LT, LO, MO

LT(1, KC.A)
LO(KC.Z, KC.LEFT_CONTROL)
MO(1)
```

## 機能


## 依存ライブラリ

`config.py`に`TAPPING_TERM`を設定しておく必要があります。

```

```

## 定義されているキー

### `LT(layer, keycode)`
短く押すと`keycode`が入力され, 長押しすると`layer`番目のレイヤーに一時的に移動します。

### `LO(tap, press)`
短く押すと`tap`のキーが入力され, 長押しするとキーを離すまで`press`のキーが押された状態になります。

### `MO(layer)`
押すと`layer`番目のレイヤーに移動し, 離すと元のレイヤーに戻ります。