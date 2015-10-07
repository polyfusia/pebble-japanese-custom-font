# Pebble japanese custom font

Font set generated from Google Noto Sans CJK JP thin weight (Apache Licence).

- https://www.google.com/get/noto/

Original character set is referring `michi_j23.pbl` from below.

- https://drive.google.com/folderview?id=0B3XsaTcJZ4A3fmNWUVFmTEpzb2lHODkwR0t4ajU2SjlHSktEYVhZdzhXLTJhdjhzZ0Y1OHc#

To make custom language pack, need Pebble Firmware Utils.

- https://github.com/xndcn/pebble-firmware-utils

also, need custom fontgen.py by medicalwei.

- https://gist.github.com/medicalwei/c9fdcd9ec19b0c363ec1

## build example

example is below.

```
# generate font file.

## 001/002 for height 14. offset is 2.
$ python fontgen.py pfo --extended --list codepoints.json --heightoffset 2 12 NotoSansCJKjp-Thin.otf 001

## 003/004 for height 18. offset is 4
$ python fontgen.py pfo --extended --list codepoints.json --heightoffset 4 14 NotoSansCJKjp-Thin.otf 003

## 005/006 for height 24. offset is 7
$ python fontgen.py pfo --extended --list codepoints.json --heightoffset 7 17 NotoSansCJKjp-Thin.otf 005

## 007/008 for height 28. offset is 8
$ python fontgen.py pfo --extended --list codepoints.json --heightoffset 8 20 NotoSansCJKjp-Thin.otf 007

# packing

$ python pbpack_tool.py pack pbl/NotoSans-ja_JP.pbl custom_font/*
```


## reference and thanks!!

- https://github.com/xndcn/pebble-firmware-utils
- http://d.hatena.ne.jp/aoshimak/20150626
- http://www.ekesete.net/log/?p=7972
- http://blog.kuro.ro/pebble-time-chinese-japanese-language-pack/
- https://drive.google.com/folderview?id=0B3XsaTcJZ4A3fmNWUVFmTEpzb2lHODkwR0t4ajU2SjlHSktEYVhZdzhXLTJhdjhzZ0Y1OHc#

## Contact

- twitter
 - https://twitter.com/polyfusia
