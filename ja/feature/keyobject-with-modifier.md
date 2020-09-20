# キーコンビネーションを1つのキーに割り当てる

## 定義されている場所

`cpkf/key_object.md`

## 記法

```
from adafruit_hid.keycode import Keycode as KC
from cpkf.key_object import C, Alt, CtrlAlt, S

C(KC.A) // select all
Alt(KC.GRAVE_ACCENT) // 英字キーボードにおける全角半角にあたるキー
CtrlAlt(KC.DELETE) // kill
S(KC.ONE) // !
```

## 依存ライブラリ

```
adafruit_hid/keycode.py
```

## 定義されているキー

### `C(kc)`
Ctrlキーを押しながらkcキーを押します。

### `Alt(kc)`
Altキーを押しながらkcキーを押します。

### `CtrlAlt(kc)`
CtrlキーとAltキーを押しながらkcキーを押します。

### `S(kc)`
Shiftキーを押しながらkcキーを押します。