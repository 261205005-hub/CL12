# 左右反転画像 生成プログラム flip.py
## 1. 概要
引数で指定した画像の左右反転を作成する python3 で動作するプログラムです。

## 2. ソースコード
＃このプログラムは python3用です。
```python3
# このプログラムは python3用です。
# あらかじめ pip install pillow で pillow で pillow をインストールしておきます。
from PIL import Image
import sys

# コマンドライン引数から入力画像と出力画像のファイル名を取得
input_image = sys.argb[1]
output_image = sys.argb[2]

# 画像の読み込み
img = Image.open(input_image)

# 画像の左右反転
img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

# 画像の保存
img_flip.save(output_image)
```
