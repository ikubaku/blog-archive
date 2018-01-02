---
title: "私の近況"
date: 2017-12-11 23:45 +0900
categories: etc
---
この記事は[KMCアドベントカレンダー](https://adventar.org/calendars/2323 "KMC Advent Calendar 2017")11日目の記事です。

### はじめに
どうも、Ikubakuです。かれこれ3ヶ月半ここを更新してませんね......。面白い話があったら書くつもりでしたが結局何も書きませんでした。ちょっと反省。

私[^1]は今年、KMC(京大マイコンクラブ)に入部しました。そこではKMC-ID[^2]:polarisとしていろいろな活動をしているのですが、その一つである「n週間に1度ゲームを作るやつ」でやったことについてまず話そうと思います。そのあと最近家のパソコンを使って挑戦したグラフィックカードのPCIパススルーについて少し話そうと思います。

[^1]:1,[自己紹介](https://h-teramura.github.io/about/ "自己紹介")に何も書いていませんでしたね......。この機会にちょっと追記しようと思うのでまた見てみてください。
[^2]:2,KMCの中での通称。部内ではこれで呼び合う習慣がある。

### n週間に1度ゲームを作るやつ
これは、隔週月曜日に決められたテーマに沿っていたり沿っていなかったりするゲームを参加しているメンバー各々で作ってこようという趣旨のイベントです[^3]。最近始まったプロジェクトの一つで、ちょうど今日2回目の集まりがありました。1回目に決めた「3分」というテーマを元に（？）したゲームが全部で4つ発表されました。ブラウザベースのゲームのほかトランプのゲームなど4つとはいえ様々なゲームがありました。私が作ったゲーム"MZFND"は迷路を探索して3分間内にどれだけたくさんの宝物を手に入れられるかを競うテキストベースのゲームで、Nintendo 3DS上で動くBASIC処理系の「プチコン3号」を使って作りました。前に作った迷路探索ゲームを元にして作ったので技術的な知見はほぼなかったですが、高得点の宝物の点数をどれだけにするかや、宝物が一定時間内にどれだけスポーンするかのようなゲームバランスの調整に挑戦することができたので面白かったと思います。 ~~あと、タッチスクリーン上の仮想キーボードを使うのがすごく大変でした。~~
実はこのゲームは1日で仕上げてしまった代物なので、次はもっと凝ったものを作ってこようと思います。ちなみに次のテーマは「クリスマス」です。

"MZFND"はプチコン3号の公開サーバに公開キー __DRV3V3DJ__ で公開しているのでよければ遊んでみてください！（プレイには3DSと「プチコン3号」が必要です。

[^3]:3,つまりn=2。

### グラフィックカードを仮想マシンでも使いたい！
続いてPCIパススルーの話です。でも別にやり方を紹介するのではなくて、今のところうまく行っていないという話をします。

PCIパススルーというのは仮想マシンでホストのマシンに接続されている未使用のPCIバス上デバイスに直接アクセスして使うというものです。私は家のパソコンのOSとしてLinuxをよく使うのですが、どうしてもWindows向けのアプリケーションを使うたいことがあります。それもたいていグラフィックパフォーマンスを必要とするものが多くて普通はマシンを2台用意するかデュアルブートするしかないのですが、やっぱり1台のパソコンでやりたい＋なんか面白そうだからやってみたいという理由でPCIパススルーに挑戦してみようと思ったわけです。

PCIパススルー自体は最近のマシンであれば多くの知見が得られていてやりやすいようなのですが、当の家にあるマシンがIntel IvyBridge世代のマシンなので「これできるんか？」というのが正直なところです。[これについてのArchLinuxのWikiページ](https://wiki.archlinux.jp/index.php/OVMF_%E3%81%AB%E3%82%88%E3%82%8B_PCI_%E3%83%91%E3%82%B9%E3%82%B9%E3%83%AB%E3%83%BC "OVMFによるPCIパススルー")を参考にしながら進めているのですが、どうも使っているマザーボードがPCI Express x16ポートを1つしか持っていないのと、BIOSがCPU内蔵グラフィックスを起動グラフィックカードとして用いるオプションを持っていないようなのでむずかしいなあと思っています[^4]。PCIポートが2つついているのでそれを利用してできないかなということで試行錯誤してみようと思います。

[^4]:4,要はグラフィックカードを2つつなぐことがむずかしいということ。

### おわりに
「え、『10代のおわり』については？」とつっこみがきそうですが、はい、これについてはまた来年書こうと思います。もうすぐ20才になることに関していろいろ考えることはあるのですがまだまとめられていないので、私の中で整理がついてから改めて書こうと思います（期待していた方々、ごめんなさい）。

ここらへんで私のアドベントカレンダーの話題をしめようと思います。明日の[KMCアドベントカレンダー](https://adventar.org/calendars/2323 "KMC Advent Calendar 2017")の記事は同じKMC1回生のbu4君の記事です。またKMCでは並行して[KMCお絵かき Advent Calendar 2017](https://adventar.org/calendars/2325 "KMCお絵かき Advent Calendar 2017")も行っています。ぜひご覧ください。

では、また。

*****
脚注