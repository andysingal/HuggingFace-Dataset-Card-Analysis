# Japanese Wikipedia Dataset

This dataset is a comprehensive pull of all Japanese wikipedia article data as of 20220808. 

*Note:* Right now its uploaded as a single cleaned gzip file (for faster usage), I'll update this in the future to include a huggingface datasets compatible class and better support for japanese than the existing wikipedia repo.

### Example use case:

```shell
 gunzip jawwiki20200808.json.gz
```

```python
import pandas as pd    
from datasets import load_dataset
df = pd.read_json(path_or_buf="jawiki20220808.json", lines=True)
# *your preprocessing here*
df.to_csv("jawiki.csv", index=False)
dataset = load_dataset("csv", data_files="jawiki.csv")
dataset['train'][0]
```


The wikipedia articles were processed from their compressed format into a 7 GB jsonl file with filtering removing extraneous characters using the repo: https://github.com/singletongue/WikiCleaner.

Sample Text:

```json
{"title": "東洋大学朝霞キャンパス", "pageid": 910815, "wikidata_id": "Q11527630", "categories": ["出典を必要とする記述のある記事/2018年5月", "ウィキデータにある座標", "東洋大学のキャンパス", "朝霞市の学校", "地図があるページ"], "redirects": ["朝霞キャンパス"], "n_inlinks": 47, "sections": [[[], "東洋大学朝霞キャンパス（とうようだいがくあさかきゃんぱす）は、/(埼玉県/埼玉県)//(朝霞市/朝霞市)/にある/(東洋大学/東洋大学)/のキャンパスである。"], [["概要"], "所在地は/(埼玉県/埼玉県)//(朝霞市/朝霞市)/岡48-1。元々は文系5学部（文学部、経済学部、経営学部、法学部、社会学部）の1、2年次用として開発されたキャンパスである。2005年に文系5学部の白山移転が実施されたため、/(ライフデザイン学部/ライフデザイン学部)/のキャンパスとして使用されていた。また、1号館（岡2-11-10）に設定されていた所在地表記を2006年4月1日より東洋大学朝霞事務部の入る朝霞図書館研究管理棟（岡48-1）へ変更した。なお、文系5学部移転後は1号館および3号館は使用されていない（詳細は後述）。\n\n2020年までの使用学部はライフデザイン学部、大学院は大学院福祉社会デザイン研究科ヒューマンデザイン専攻が設置。ライフデザイン学部（大学院を含む）は2021年4月に朝霞キャンパスから/(東洋大学赤羽台キャンパス/東洋大学赤羽台キャンパス)/へ移転し、2024年に/(東洋大学板倉キャンパス/板倉キャンパス)/で設置されている生命科学部、食環境科学部と、/(東洋大学川越キャンパス/川越キャンパス)/で設置されている理工学部 生体医工学科が朝霞キャンパスに移転する予定になっている。"], [["歴史"], "/(文学部/文学部)/のみの/(単科大学と総合大学/単科大学)/から複数の分野を網羅する総合大学へ脱皮するにあたって、キャンパスの面積不足は大きな課題であった。当初、工学部も含めて、全てを白山キャンパスに設置する予定でいたが、面積の問題からかなわず、川越市長/(伊藤泰吉/伊藤泰吉)/の熱心な働きかけによって工学部を川越市に設置することとなった。その後、文系学部の増強に伴って文系各学部の教養課程を分離することが必要となった。当初は川越キャンパスをそれにあてる予定であったが/(学生運動/学生運動)/の影響により、断念することとなる。しかし、1966年の経営学部設置認可は教養課程の分離を前提としてなされていたことから早急に対応する必要があり、朝霞市郊外の/(黒目川/黒目川)/河畔の広大な土地を地権者から譲渡されることとなり、朝霞キャンパスの整備計画がスタートした。\n\n東洋大学では、当初は2号館（現講義棟）の校地のみを使用してキャンパスを整備する予定でいた。しかし、朝霞キャンパス建設予定地は/(市街化調整区域/市街化調整区域)/となっており、区域変更ないしは公的建築物としての特例認可の手続きが必要であった。東洋大学では速やかに建築許可がなされると考えていたが、河川整備のなされていない/(黒目川/黒目川)/河畔であったことから国の許諾がなかなか降りず、進出計画は難航してしまった。しかし、前述の通り、経営学部の設置認可特認の手前、早急な新キャンパス開設が求められ、急遽市街化地域に土地を入手して1号館を建設。1977年から文系5学部の教養課程（ただし文学部は一部講義のみ）を朝霞キャンパスで開講できる運びとなった。その後に特例認可がなされ、2号館を建設。キャンパスとして本格的に稼動することとなる。\n\n朝霞キャンパス設置当時は郊外型キャンパスの人気が高く、環境のよい朝霞キャンパスは東洋大学の志願者増に貢献した。ところが/(バブル景気/バブル崩壊)/後、受験生の/(都心回帰/都心回帰)/傾向が強まり、さらに/(大学全入時代/大学全入時代)/を迎えると朝霞キャンパスと白山キャンパスに分断されていることがデメリットとなってしまった。そこで東洋大学では白山キャンパスの再開発事業を実施、近隣の土地を取得して2005年から再度文系5学部を白山キャンパスへ集中させた。\n\n東洋大学の当初計画では、市街化調整区域に存在していてこれ以上の拡張が望めない朝霞キャンパスは、現在設置されている体育館などの体育関連施設および学生サークル用施設を残し、他の施設は解体、教育・研究施設としての機能は廃止する予定でいた。学生数の減少による/(朝霞台駅/朝霞台駅)/（/(北朝霞駅/北朝霞駅)/）周辺の商業的なデメリットを憂慮した朝霞市は、キャンパス機能の維持に対して陳情活動が数回実施された。朝霞市による学生利用に適した道路整備など、これまで構築されてきた朝霞市との良好な関係を考慮した東洋大学では新学部を設置することで教育・研究施設としての機能を維持することを決定、2005年の文系5学部白山集中化と同時に朝霞キャンパスにライフデザイン学部を設置した。\n\nしかし、/(少子化/少子化)/や/(2018年問題/2018年問題)/の影響は避けられず、2017年9月に/(東洋大学赤羽台キャンパス/東洋大学赤羽台キャンパス)/を拡張してライフデザイン学部（大学院を含む）を2021年を目途に移転することを発表した。\n\n2015年11月に旧3号館の敷地に/(ヤオコー/ヤオコー)/朝霞岡店が開店。\n\n2018年1月に旧4号館・旧総合体育館・旧テニスコートの敷地に朝霞台中央総合病院が/(TMGあさか医療センター/TMGあさか医療センター)/と改称のうえ新築移転し、446床の新病院となった。"], [["学部"], "なし"], [["大学院"], "なし"], [["施設"], ""], [["施設", "現存する施設"], "講義棟：旧2号館。3階建てのメイン校舎。大講義室のほか、ゼミで使用する少人数教室やLL教室が設置されている。ライフデザイン学部開設に伴い、一部の教室は実習室へ改装された。この校舎の地下にはかつてサークル部室が存在していたが、現在は使用禁止となっている。\n情報実習棟：旧5号館。情報実習用に建てられた3階建ての校舎である。コンクリート打ちっぱなしのデザインは東洋大学の卒業生の手によるもの。\n研究管理棟：東洋大学朝霞事務部の入る3階建ての建物。当初は事務部のほか、文学部・社会学部専任教員用の研究室が割り当てられていた。\n大学院・研究棟：旧研究指導棟。東洋大学専任教員の研究室と大学院の講義室がある。文系5学部が朝霞にあった時代には白山と朝霞の研究室でも全専任教員用の研究室を満たすことができず、この建物が新規に建てられた。5階建てで1階は吹きさらしの屋外広場となっている。ライフデザイン学部の全専任教員の研究室が入るほか、大学院の演習や共同研究室としても使用されている。\n図書館棟：東洋大学図書館朝霞分館の入居する3階建て。2階から入場する形式となっている。この建物の地下には食堂があり、/(TBSテレビ/TBS)/系のテレビドラマ「/(HOTEL/HOTEL)/」で社員食堂シーンを撮影する際に使用されていた。\nコミュニティセンター：公認サークルおよび体育会各部の部室が入居する4階建ての学生会館。1階には演劇サークル用に多目的ホールがあり、2階には会議室と演劇サークル用の練習室、メディアサークル用の音響室が設けられている。\n人間環境デザイン学科実験工房棟：旧研究室棟。ライフデザイン学部の新設に伴い、2005年にリフォームされた。2009年に第18回/(ロングライフビル推進協会/BELCA賞)/ベストリフォーム部門受賞。\n総合体育館：旧総合体育館に代わる体育施設として2014年に竣工した地上2階建ての建物。アリーナやトレーニングルームの他、ライフデザイン学部の実習室も設置されている。"], [["施設", "現存しない施設"], "旧1号館：キャンパス設置時に建設された3階建ての校舎で、真裏は住宅地である。キャンパス開設当初に建設され、最も古く駅から遠い校舎だったが、現在は取り壊され、跡地は売却のうえ民間のマンションになっている。1階の書店では新年度始めに教科書の一斉販売が行われていた。\n旧3号館：市街化調整区域で校舎の増築がなかなか認められないことから、道路を挟んだ1号館の隣に急遽取得した土地に建てられた校舎である。音響機器や衛星通信による遠隔講義に対応した2つの大講義室と大学生協および食堂が設置されていたが、現在は取り壊され、跡地は売却のうえ/(ヤオコー/ヤオコー)/朝霞岡店になっている。\n旧4号館：かつて存在したプレハブ校舎。当初は体育科目の講義や社会学部の演習で使用されていたが、その後は音楽系サークルの練習場として使用された。5号館の設置に伴い、/(建築基準法/建築基準法)/の問題から取り壊され、跡地は芝生として整備されていた。ここの/(公衆電話/公衆電話)/は学内で一番空いているとされ、携帯電話普及前には重宝がられた。1号館などと同様に敷地は売却され、現在は/(TMGあさか医療センター/TMGあさか医療センター)/が建っている。\n旧総合体育館：体育系の講義と体育会の練習設備として使用される3階建ての建物。剣道場、柔道場、卓球場、レスリング場などのほか、フィットネスクラブで使用されている各種運動器具が配置されたトレーニングルームが設置されており、東洋大学の学生教職員であれば、一定の講習を受けることで自由に使用することができた。4号館跡地と一体で売却され、現在はTMGあさか医療センターが建っている。\n旧テニスコート：旧総合体育館隣の東武東上線の線路脇に存在し、体育系の講義やテニスサークルの活動に使用されていた。4号館や総合体育館同様、現在はTMGあさか医療センターが建っている。"], [["特徴"], "開設当初は文系5学部の教養課程を担当する目的であったことから体育施設が充実していた。また、語学用の少人数教室が多く配置されている。\n現在でも市街化調整区域となっているため、周辺の開発が進まない反面、キャンパスの拡張にも制約があり、再開発の計画は思うように進んでいない。\n5階建ての大学院・研究棟は東武鉄道の電車からもよく見え、朝霞市北部のランドマーク的な存在となっている。"], [["アクセス"], "/(東日本旅客鉄道/JR東日本)//(武蔵野線/武蔵野線)//(北朝霞駅/北朝霞駅)/東口および/(東武鉄道/東武)//(東武東上本線/東上線)//(朝霞台駅/朝霞台駅)/東口から徒歩10分\n朝霞台駅・北朝霞駅東口、東武東上線/(朝霞駅/朝霞駅)/東口より/(朝霞市内循環バス/朝霞市内循環バス)/わくわく号・根岸台線 朝霞市斎場停留所から徒歩1分"], [["脚注"], ""], [["外部リンク"], "東洋大学朝霞キャンパス案内図等"]]}
```

## Usage

Clone this repo and unzip the jsonl file using:

```sh
git clone https://huggingface.co/datasets/tensorcat/wikipedia-japanese && cd wikipedia-japanese
gunzip jawiki-20220808.json.gz
```