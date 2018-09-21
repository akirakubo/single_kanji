# single_kanji

## itaiji.txt

Mozcの[variant_rule.txt](https://github.com/google/mozc/blob/master/src/data/single_kanji/variant_rule.txt)を元に、以下の条件を順次適用して作成したものです。

1. JIS X 0208範囲外→JIS X 0208の事例を削除 (例: 𠮟→叱(異体字)を削除)
2. A→B、B→A両方向の事例が存在する場合は共に削除 (例: 伜→倅(正字)、倅→伜(俗字)を共に削除)
3. A→Bの事例に対してB→Cの事例が存在する場合は後者を削除 (例: 体→體(旧字体)と體→軆(俗字)について、後者を削除)

### ファイルフォーマット

```
漢字1\t漢字2
```

漢字1は、[variant_rule.txt](https://github.com/google/mozc/blob/master/src/data/single_kanji/variant_rule.txt)において

> more popular

と記述がある側の漢字です。

## itaiji_removed.txt

先に示した条件によって除外された事例です。
