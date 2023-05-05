# Welcome ViXtRiA !!

ViXtRiA-Systemを利用して非可逆圧縮を用いらない圧倒的な高音質と、現実のハコさながらの**音圧感**をVRChatの世界で体験してみませんか？



## 機能紹介

ViXtRiAでは以下の機能を提供します

	・最速450msの低遅延配信
	・配信者からPCM形式による無損失での音声受信
	・サーバ側処理による音声トラックのマルチチャンネル化(立体音響化)
	・PCM形式による非可逆圧縮を伴わない音声配信(PC/Desktopユーザ)
	・品質に定評のあるAppleCoreAudioAACEncoderを用いた高音質なAAC形式での音声配信(Questユーザ)
	・PC/Desktopで最大5Mbps、Questで最大3Mbpsの映像配信
	・最大3名までの配信者の同時接続と、Web画面による配信のクロスフェード切替操作機能
	・豊富な立体音響化プリセット
	・特定ワールド専用に専用チューニングを施したプリセットの作成(要相談)*
	・特定イベント専用映像・音声切替プリセットの作成(要相談)*
	・最大240人までのワールド内 同時視聴(40人ワールド 約フルインスタンス 3つ分)

	　　*ViXtRiAサーバ側への設定追加の対応を実施するため、Adminへ事前相談が必要です
	　　TwitterDM或いはDiscordにてご連絡ください


## 導入メリット・ユースケース

提供する機能から得られるメリットや、ユースケースの例を下記に示します

### イベント関連
	・簡易ビデオスイッチャー機能を使った演者間の繋ぎをシームレス化
	・イベントロゴ、ワールドロゴ等の透かし投影
	・休憩時間やイベント開始までの時間に再生しておくBGM・BGVの設定
	・同時間帯の競合イベントとの差別化
### 音響関連
	・ハコ特有の音圧感あるパワフルサウンドの再生
	・現実のライブシーンで使われているPA/SR音響機材が放つ、独特な音色の再現
	・ワールド作者、イベントオーナーの意見を基に専用チューニングを施した「専用音響」の用意
	・専用音響を作成・利用することで「そのイベントワールドでしかけ聴けない固有の音響」を実現
	・サーバ処理による音響加工をパススルーとすることで「無劣化」,「無損失」,「無加工」での音声配信

## システムの制約

ViXtRiA-Systemは個人一般が一人でサーバを維持保守しているサービスであることから

いくつかの制約があるため、それらを以下に示します

	・同一時間帯での同時利用の不可
	　→システムの構成上、時間帯当たり、一つのイベントでのみ利用することができるため、
	　　利用日時が重複する場合はどこがサービスを利用するか調整する必要があります
	
	・ワールドへのprefab組み込み
	　→複数chの音声を用いた立体音響で視聴するには本GitHubリポジトリで配布しているコンポーネントを
	　　ワールドへ組込み、Team-ViXtRiA 管理メンバによる事前の動作テストを実施する必要があります
	　　既存のTopazChatやiwasyncとの共用/共存も可能ではありますが、ある程度の技術的な知識が要求されます
	
	・OBSを用いたViXtRiAサーバへの配信
	　→本システムはOBSでの配信に依存した仕組みであるため、OBSによる配信とする必要があります

	・ViXtRiA専用プロファイルの導入
	　→通常使われる「配信開始」ボタンによる配信ではなく「録画開始」ボタンを用いるという、
	　　若干特殊な配信設定をOBSへ設定する必要があるため、本GitHubで配布しているプロファイルを導入する必要があります
	　　Windowsユーザーはexeによる簡単インストール、
	　　Macユーザーはzipを用いた手動でのプロファイルインポート操作が必要です

	・一部のVirtual Desktopユーザーで音切れが発生する
	　→Wi-Fiの実効速度(スループット)が低い、あるいは安定しないユーザーさんにおいて、
	　　視聴が困難なレベルの音切れが発生する問題があります。
	　　これは本システムが最高の品質を提供するには
	　　「映像 約5Mbps + 音声 約6Mbps=約11～12Mbps」という非常に高いビットレートで配信していることに起因します。
	　　この問題は『映像を使わない』ことで回避可能であることは確認しております。


## ViXtRiA-System_Audio_Component

ワールドへ導入するにあたって必要となる、システム推奨なAudioSourceの配置設定を組み込むためのUnityPackage資材です

	・ViXtRiA-System_Audio_Component for PCVR
	　→PCVR/Desktopワールド用のUnityPackage及びprefabデータです
	　　配信URLは「rtspt://vrc-spa-adk.v4.softether.net:8554/★Sample★」形式となります

	・ViXtRiA-System_Audio_Component for Quest
	　→Questワールド用のUnityPackage及びprefabデータです
	　　配信URL、AudioSourceの配置がPC版とは異なるため、注意が必要です
	　　配信URLは「rtspt://vrc-spa-adk.v4.softether.net:8554/q★Sample★」形式となります

## ViXtRiA-System_OBS_Profile

ViXtRiA-Systemを提供している「ViXtRiA-Server」へOBSを用いて配信を繋ぐために必要となる「OBSプロファイル」を導入するための資材です

下記のReleaseよりダウンロードしてOBSへ導入してください

https://github.com/Team-ViXtRiA/ViXtRiA-System_OBS_Profile/releases	


## ViXtRiA_Other_Contents
ViXtRiA-Systemの公式ロゴ、その他の配布物を公開します

# システム利用予約
下記のGoogleカレンダーよりシステムの利用予約をしてください。

また、予定が重複する場合は「先行予約者を優先」を基本としつつ、

当事者間で予定調整してください。


## ★システム利用 予約ページ★

https://calendar.google.com/calendar/u/0/appointments/schedules/AcZssZ3k4_TbNLPGOjPOs9iBTD8JerSWcYMDxOm56X9Tj38Jp4zK63L2VCkQlUDvaJ409Ngwg-bIHwyc

## ★システム利用 予定表★

https://calendar.google.com/calendar/u/6?cid=dnJjLnNwYUBnbWFpbC5jb20
