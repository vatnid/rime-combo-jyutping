# 宮保粵拼 Combo Jyutping

Schema： ℞ **combo_jyutping**

[Rime](https://rime.im) 宮保粵拼輸入方案

## 簡介

宮保粵拼係由[淵維](https://github.com/vatnid)同理烏以[佛振](https://github.com/lotem)嘅[宮保拼音](https://github.com/rime/home/wiki/ComboPinyin)爲基礎設計嘅並擊（chord typing）粵拼輸入法。

咩係 chord typing？一般嘅粵拼輸入法係要逐個字母輸入，就算打得快都要順次序輸入字母。Chord typing 不同之處係你只要撳啱同一個 combination 嘅掣，唔使理次序都可以打到想要嘅音節，就好似彈鋼琴演奏和絃（彈 chord）一樣。

呢個係宮保粵拼嘅 layout：

![Combo Jyutpung layout](https://github.com/vatnid/combo_jyutping/blob/master/layout.png "宮保粵拼 layout")

例如你想打「光復香港時代革命」八個字，首先你要知道每一個音節嘅粵拼，之後就可以開始拆聲母韻母。例如第一個「光」字係 gwong，首先左手要打聲母 gw-，即係 layout 上面嘅 [s][h][g] 三個掣。韻母係 -ong，所以可以直接打 [o][-ng]。所以只要 [s][h][g][o][-ng] 五個掣同時撳，就可以出到 gwong 呢個音節。

其他音節可以照板煮碗：  
光 gwong = [s][h][g][o][-ng]  
復 fuk = [f][u][-ng][入] （ ← 呢度韻尾係 -k，鍵盤空間所限所以要打 [-ng] 再加入聲掣 [入]）  
香 hoeng = [h][oe][-ng]  
港 gong = [g][oe][-ng]  
時 si = [s][i]  
代 doi = [d][o][i]  
革 gaak = [g][aa][-ng][入]  
命 ming = [m][i][-ng]  

即係話，只要撳八個「chord」就可以打到八個字出嚟喇！

上圖會見到某啲韻母組合有多過一個方法輸入，例如 -ing 可以係 [i][-ng] 或者 [e][-n][i]，因爲打 [i][-ng] 手指要跨行，而且 -ing 係常用韻母，所以加多咗一個唔使跨行嘅 shortcut，可以自由選擇。只有 -iu 同 -ui 唔可以靠單撳 [i][u] 得出，因爲呢個輸入法忽略輸入次序，所以電腦得到 [i][u] 呢個 chord 就唔知道係 -iu 定 -ui，所以一定要用 [i][yu] 同 [u][oe] 兩組 chord。其他韻母組合都可以照常理推斷，不過唔用 shortcut 有機會會因爲按鍵位置導致難以輸入。

## 安裝

首先請裝咗粵拼方案（有聲調版）先，然後 download `combo_jyutping.schema.yaml` 呢個 file 放入自己 Rime 嘅 folder 入面，再重新部署就可以。

  - [粵語拼音](https://github.com/rime/rime-cantonese) ℞ **`jyut6ping3`**

授權條款：見 [LICENSE](LICENSE)
