# 宮保粵拼 Combo Jyutping

配方：℞ `combo_jyutping`

## 簡介

宮保粵拼係由[淵維](https://github.com/vatnid)同理烏以[佛振](https://github.com/lotem)嘅[宮保拼音](https://github.com/rime/home/wiki/ComboPinyin)爲基礎設計嘅並擊（chord typing）[粵拼](https://www.jyutping.org/jyutping/)輸入法。呢個輸入法要配合 [Rime](https://rime.im) 使用。

咩係 chord typing？一般嘅粵拼輸入法係要逐個字母輸入，就算打得快都要順次序輸入字母。Chord typing 不同之處係你只要撳啱同一個 combination 嘅掣，唔使理次序都可以打到想要嘅音節，就好似彈鋼琴演奏和絃（彈 chord）一樣。

### 鍵盤配置

呢個係宮保粵拼嘅 layout：

![Combo Jyutpung layout](https://github.com/vatnid/combo_jyutping/blob/master/layout.png "宮保粵拼 layout")

左邊嘅黃色掣係聲母，右邊嘅白色掣係韻母，左手負責打聲母，右手負責打韻母，互相配合。某啲聲母需要用多過一個掣組合，例如 m- 需要用左手同時撳 [f][b] 兩個掣。韻母一般嘅拼法係直接連打韻腹同韻尾，例如 -oeng 就係用右手連打 [oe][-ng] 兩個掣。左右手同時並擊聲母同韻母，即使實際按鍵次序不一，都一樣可以打到相應嘅音節。

### 例子

例如你想打「光復香港時代革命」八個字，首先你要知道每一個音節嘅粵拼，之後就可以開始拆聲母韻母。例如第一個「光」字係 gwong，首先左手要打聲母 gw-，即係 layout 上面嘅 [s][h][g] 三個掣。韻母係 -ong，右手可以直接打 [o][-ng]。所以只要 [s][h][g][o][-ng] 五個掣同時撳，就可以出到 gwong 呢個音節。

其他音節可以照板煮碗：  
光 gwong = [s][h][g][o][-ng]  
復 fuk = [f][u][-ng][入] （ ← 呢度韻尾係 -k，鍵盤空間所限所以要打 [-ng] 再加入聲掣 [入]）  
香 hoeng = [h][oe][-ng]  
港 gong = [g][o][-ng]  
時 si = [s][i]  
代 doi = [d][o][i]  
革 gaak = [g][aa][-ng][入]  
命 ming = [m][i][-ng]  

即係話，只要撳八個「chord」就可以打到八個字出嚟喇！

### 特殊組合

上圖會見到某啲韻母組合有多過一個方法輸入，例如 -ing 可以係 [i][-ng] 或者 [e][-n][i]，因爲打 [i][-ng] 手指要跨行，而且 -ing 係常用韻母，所以加多咗一個唔使跨行嘅 shortcut，可以自由選擇。只有 -iu 同 -ui 唔可以靠單撳 [i][u] 得出，因爲呢個輸入法忽略輸入次序，所以電腦得到 [i][u] 呢個 chord 就唔知道係 -iu 定 -ui，所以一定要用 [i][yu] 同 [u][oe] 兩組 chord。其他韻母組合都可以照常理推斷，不過唔用 shortcut 有機會會因爲按鍵位置導致難以輸入。

另一方面，某啲組合因爲鍵盤 wiring 所限所以普通打法會好難輸入，例如 -aap，所以呢個輸入法將 -aap/aat/aak 同 -ap/at/ak 合流。

仲有其他特殊例子，呢度唔詳列，請參考下面嘅對照表。

## 安裝

1. 安裝 [Rime](https://rime.im/download/)
2. 安裝咗粵拼方案（有聲調版）
3. 下載 `combo_jyutping.schema.yaml` 呢個 file
4. 放入自己 Rime 嘅 folder 入面，再重新部署

  - [粵語拼音](https://github.com/rime/rime-cantonese) ℞ **`jyut6ping3`**

授權條款：見 [LICENSE](LICENSE)

## 聲韻母按鍵對照

|聲母/韻母|主要組合|次要組合（一）|次要組合（二）|次要組合（三）|
|--------|------|------------|-----------|------------|
|b|[b]||||
|p|[p]||||
|m|[f][b]||||
|f|[f]||||
|d|[d]||||
|t|[t]||||
|n|[l][d]||||
|l|[l]||||
|g|[g]||||
|k|[k]||||
|ng|[h][g]||||
|h|[h]||||
|gw|[s][h][g]||||
|kw|[h][g][k]||||
|z|[z]||||
|c|[c]||||
|s|[s]||||
|j|[gk]||||
|w|[bp]||||
|aa|[aa]||||
|aai|[aa][i]||||
|aau|[aa][u]||||
|aam|[aa][-m]||||
|aan|[aa][-n]|[aa][-m][i]|||
|aang|[aa][-ng]|[aa][-m][i][.]|||
|aap|[aa][-m][入]|[-m][入]|||
|aat|[aa][-n][入]|[-n][入]|[aa][-m][i][入]||
|aak|[aa][-ng][入]|[-ng][入]|[aa][-m][i][.][入]||
|ai|[a][i]||||
|au|[a][u]||||
|am|[-m]||||
|an|[-n]||||
|ang|[-ng]||||
|ap|[-m][入]||||
|at|[-n][入]||||
|ak|[-ng][入]||||
|o|[o]||||
|oi|[o][i]|[o][-ng][u][oe]|||
|ou|[o][u]||||
|on|[o][n]|[e][-n][i][yu]|||
|ong|[o][-ng]||||
|ot|[o][n][入]|[e][-n][i][yu][入]|||
|ok|[o][-ng][入]||||
|oe|[oe]||||
|eoi|[oe][i]|[-ng][u][oe]|||
|eon|[oe][-n]|[-n][i][yu]|||
|oeng|[oe][-ng]||||
|eot|[oe][-n][入]|[-n][i][yu][入]|||
|oek|[oe][-ng][入]||||
|e|[e]||||
|ei|[e][i]|[i][u]|||
|eu|[e][u]||||
|em|[e][-m]|[i][-m]|||
|eng|[e][-ng]|[e][-n]|[i][-ng]|[e][-n][i]|
|ep|[e][-m][入]|[i][-m][入]|||
|ek|[e][-ng][入]|[e][-n][入]|[i][-ng][入]|[e][-n][i][入]|
|i|[i]||||
|iu|[i][yu]||||
|im|[i][-m]||||
|in|[i][-n]||||
|ing|[i][-ng]|[e][-n][i]|||
|ip|[i][-m][入]||||
|it|[i][-n][入]||||
|ik|[i][-ng][入]|[e][-n][i][入]|||
|u|[u]||||
|ui|[u][oe]||||
|un|[u][-n]|[o][-ng][u]|||
|ung|[u][-ng]||||
|ut|[u][-n][入]|[o][-ng][u][入]|||
|uk|[u][-ng][入]||||
|yu|[yu]||||
|yun|[yu][-n]||||
|yut|[yu][-n][入]||||
|m|[f][b]||||
|ng|[h][g]||||
