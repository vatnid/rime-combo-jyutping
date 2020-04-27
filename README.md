# 宮保粵拼 Combo Jyutping（淵理方案）

配方：℞ `vatnid/rime-combo-jyutping`  
授權條款：見 [LICENSE](LICENSE)

## 簡介

宮保粵拼係由[淵維](https://github.com/vatnid)同[理烏](https://github.com/kaenif)以[佛振](https://github.com/lotem)嘅[宮保拼音](https://github.com/rime/home/wiki/ComboPinyin)爲基礎設計嘅並擊（chord typing）[粵拼](https://www.jyutping.org/jyutping/)輸入法。呢個輸入法要配合 [Rime](https://rime.im) 使用。除咗 QWERTY 鍵盤之外，本方案亦支援 Dvorak 鍵盤。

咩係 chord typing？一般嘅粵拼輸入法係要逐個字母輸入，就算打得快都要順次序輸入字母。Chord typing 不同之處係你只要撳啱同一個 combination 嘅掣，唔使理次序都可以打到想要嘅音節，就好似彈鋼琴演奏和弦（彈 chord）一樣。

## 安裝

首先安裝 [Rime](https://rime.im/download/) 同埋[粵拼方案](https://github.com/rime/rime-cantonese)。

之後可以係用[東風破](https://github.com/rime/plum)安裝指令：`bash rime-install vatnid/rime-combo-jyutping`，  
亦都可以人手下載 `combo_jyutping.schema.yaml`，再放入自己 Rime 嘅[用戶文件夾](https://github.com/rime/home/wiki/RimeWithSchemata#rime-%E4%B8%AD%E7%9A%84%E6%95%B8%E6%93%9A%E6%96%87%E4%BB%B6%E5%88%86%E4%BD%88%E5%8F%8A%E4%BD%9C%E7%94%A8)入面，再[重新部署](https://github.com/rime/home/wiki/CustomizationGuide#%E9%87%8D%E6%96%B0%E4%BD%88%E7%BD%B2%E7%9A%84%E6%93%8D%E4%BD%9C%E6%96%B9%E6%B3%95)。

### Dvorak 鍵盤

如果你用嘅唔係一般嘅 QWERTY 配置，而係 Dvorak，請打開 `combo_jyutping.schema.yaml`，然後搵出四行末標示住 `# Dvorak (x/4)` 嘅行，移除每行最頭嘅 `# `，再喺附近三行標示住 `# QWERTY (x/3)` 嘅最頭加返 `# `，噉就可以成功轉用爲 Dvorak 版本。（[圖示](https://raw.githubusercontent.com/vatnid/combo_jyutping/master/dvorak-tutorial.png)）

## 鍵盤配置

呢個係宮保粵拼嘅 layout。以下用 `[]` 嚟標示宮保粵拼鍵盤嘅按鍵，**並唔係 QWERTY 鍵盤本身嘅掣**。

![Combo Jyutpung basic layout](https://github.com/vatnid/combo_jyutping/blob/master/layout.png "宮保粵拼 layout")

## 輸入方式

宮保粵拼完全唔需要用到尾指，打字嘅時候將兩隻食指放喺 `[g]` 同埋 `[-ng]` 兩個掣上面，有需要就將食指向內移動，唔會有任何向外嘅移動。

左邊嘅黃色掣係聲母，右邊嘅白色掣係韻母，左手負責打聲母，右手負責打韻母，互相配合。某啲聲母需要用多過一個掣組合，例如 m- 需要用左手同時撳 `[f][b]` 兩個掣。韻母一般嘅拼法係直接連打韻腹同韻尾，例如 -oeng 就係用右手連打 `[oe][-ng]` 兩個掣。左右手同時並擊聲母同韻母，即使實際按鍵次序不一，都一樣可以打到相應嘅音節。

### 例子

例如你想打「光復香港時代革命」八個字，首先你要知道每一個音節嘅粵拼，之後就可以開始拆聲母韻母。例如第一個「光」字係 gwong，首先左手要打聲母 gw-，即係 layout 上面嘅 `[s][h][g]` 三個掣。韻母係 -ong，右手可以直接打 `[o][-ng]`。所以只要 `[s][h][g][o][-ng]` 五個掣同時撳，就可以出到 gwong 呢個音節。

其他音節可以照板煮碗：  
光 gwong = `[s][h][g][o][-ng]`  
復 fuk = `[f][u][-ng][入]` （ ← 呢度韻尾係 -k，鍵盤空間所限所以要打 [-ng] 再加入聲掣 [入]）  
香 hoeng = `[h][oe][-ng]`  
港 gong = `[g][o][-ng]`  
時 si = `[s][i]`  
代 doi = `[d][o][i]`  
革 gaak = `[g][aa][-ng][入]`  
命 ming = `[f][b][i][-ng]`  

即係話，只要撳八個「chord」就可以打到八個字出嚟喇！

### 特殊組合

上圖會見到某啲韻母組合有多過一個方法輸入，例如 -aan 可以係 `[aa][-n]` 或者 `[aa][-m][i]`，因爲打 `[aa][-n]` 手指要跨兩行，所以加多咗一個唔使跨行嘅 shortcut，可以自由選擇。只有 -iu 同 -ui 唔可以靠單撳 `[i][u]` 得出，因爲呢個輸入法忽略輸入次序，所以電腦得到 `[i][u]` 呢個 chord 就唔知道係 -iu 定 -ui，所以一定要用 `[i][yu]` 同 `[u][oe]` 兩組 chord。其他韻母組合都可以照常理推斷，不過唔用 shortcut 有機會會因爲按鍵位置導致難以輸入。

另一方面，某啲組合因爲鍵盤 wiring 所限所以普通打法會好難輸入，例如 -aap，所以呢個輸入法將 -aap/aat/aak 同 -ap/at/ak 合流。

仲有其他特殊例子，呢度唔詳列，請參考呢個文件下面嘅對照表。

### 進階技巧

除咗普通聲母、韻母組合之外，某啲音節喺宮保粵拼可以用更便捷嘅方式輸入。如果齋撳聲母，就會得出該聲母加 -aa 韻母（除咗兩個成音節鼻音 m 同 ng），例如就噉撳 `[s]` 會出現 saa。另外，輸入聲母再加入聲鍵（空白）亦都可以輸入某啲常用音節，例如 `[g][入]` 係 ge，`[d][入]` 係 dou。下表詳細列出所有聲母加入聲鍵嘅組合：

|聲母|常用音節|聲母|常用音節|聲母|常用音節|聲母|常用音節|
|---|-------|---|-------|---|-------|---|-------|
|b|bin|p|puk|m|mou|f|faan|
|d|dou|t|tung|n|nei|l|lai|
|g|ge|k|keoi|ng|ngo|h|hai|
|gw|gwo|kw|kwan|j|jau|w|wui|
|z|zau|c|cin|s|sin|

## 聲韻母按鍵對照

|聲韻母|主和弦|次和弦（一）|次和弦（二）|
|-----|-----|----------|----------|
|b-|`[b]`|||
|p-|`[p]`|||
|m-|`[f][b]`|||
|f-|`[f]`|||
|d-|`[d]`|||
|t-|`[t]`|||
|n-|`[l][d]`|||
|l-|`[l]`|||
|g-|`[g]`|||
|k-|`[k]`|||
|ng-|`[h][g]`|||
|h-|`[h]`|||
|gw-|`[s][h][g]`|||
|kw-|`[h][g][k]`|||
|z-|`[z]`|||
|c-|`[c]`|||
|s-|`[s]`|||
|j-|`[s][h]`|||
|w-|`[z][f]`|||
|-aa|`[aa]`|||
|-aai|`[aa][i]`|||
|-aau|`[aa][u]`|||
|-aam|`[aa][-m]`|||
|-aan|`[aa][-n]`|`[aa][-m][i]`||
|-aang|`[aa][-ng]`|||
|-aap|`[aa][-m][入]`|`[-m][入]`||
|-aat|`[aa][-n][入]`|`[-n][入]`|`[aa][-m][i][入]`|
|-aak|`[aa][-ng][入]`|`[-ng][入]`||
|-ai|`[a][i]`|||
|-au|`[a][u]`|||
|-am|`[-m]`|||
|-an|`[-n]`|||
|-ang|`[-ng]`|||
|-ap|`[-m][入]`|||
|-at|`[-n][入]`|||
|-ak|`[-ng][入]`|||
|-o|`[o]`|||
|-oi|`[o][i]`|||
|-ou|`[o][u]`|`[u]`||
|-on|`[o][n]`|||
|-ong|`[o][-ng]`|||
|-ot|`[o][n][入]`|||
|-ok|`[o][-ng][入]`|`[o][-ng][u]`||
|-oe|`[oe]`|||
|-eoi|`[oe][i]`|`[-ng][u][oe]`||
|-eon|`[oe][-n]`|`[-n][i][yu]`||
|-oeng|`[oe][-ng]`|||
|-eot|`[oe][-n][入]`|`[-n][i][yu][入]`||
|-oek|`[oe][-ng][入]`|||
|-e|`[e]`|||
|-ei|`[e][i]`|`[i]`||
|-eu|`[e][u]`|`[i][yu]`||
|-em|`[e][-m]`|`[i][-m]`||
|-eng|`[e][-ng]`|`[i][-ng]`||
|-ep|`[e][-m][入]`|`[i][-m][入]`||
|-et|`[i][-n][入]`|||
|-ek|`[e][-ng][入]`|`[i][-ng][入]`||
|-i|`[i]`|||
|-iu|`[i][yu]`|||
|-im|`[i][-m]`|||
|-in|`[i][-n]`|||
|-ing|`[i][-ng]`|||
|-ip|`[i][-m][入]`|||
|-it|`[i][-n][入]`|||
|-ik|`[i][-ng][入]`|||
|-u|`[u]`|||
|-ui|`[u][oe]`|||
|-un|`[u][-n]`|`[e][-n]`||
|-ung|`[u][-ng]`|||
|-ut|`[u][-n][入]`|`[e][-n][入]`|`[e][-n][i]`|
|-uk|`[u][-ng][入]`|||
|-yu|`[yu]`|||
|-yun|`[yu][-n]`|||
|-yut|`[yu][-n][入]`|||
|m|`[f][b]`|||
|ng|`[h][g]`|||
