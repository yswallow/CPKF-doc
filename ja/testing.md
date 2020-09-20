# テスト環境

記載以外の環境でのテストは行っていません。

## マイコン
* Adafruit Feather nrf52840 Express
    * nrf52840, Cortex-M4F 64MHz, 256KB RAM, 1MB Flash
    * Bluetooth 機能
* Adafruit ItsyBitsy M4 Express
    * ATSAMD51, Cortex-M4 120MHz, 192KB RAM, 512KB Flash, 2MB SPI Flash

## キーボード
* [パンダスプリット](https://github.com/yswallow/panda_split)
    * MCP23017の端子をキースイッチに直結し, マイコンからはI2Cで読み取る形式