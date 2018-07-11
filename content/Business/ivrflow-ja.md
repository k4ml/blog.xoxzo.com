Title: IVR(インタラクティブ音声自動応答)フローの構築時の、注意点
Date: 2018-07-10 12:00
Lang: ja
Author: Ai Sin Chan
Tags: api; developers; market; sms; business; 2018; voice; interactive
Slug: ivrflow
Thumbnail: images/ivrflow.jpg
Summary: インタラクティブ音声自動応答を構築する際、どういった点に気をつければいいのでしょうか？

**1）ユーザーのニーズをランク付けする：** 頻繁に要求されていることについて、顧客サポート記録内のデータから分析します。これらは、IVRフローの最初のオプションであるべきです。たとえば、ほとんどのユーザーが自分の口座残高を確認するために電話をかけていた場合は、最初のオプションを「残高を確認するには1を押してください。」としましょう。

**2）ユーザーのために自然な流れを：** IVRスクリプトのシーケンスと構造は重要です。「1を押して残高を確認する」と「残高を確認するには、1を押してください」の微妙な違いは何でしょうか？「1を押して残高を確認する」という形式を使用する場合、ユーザーは多くのオプションを巡りながら、初めに聞いた番号を念頭に持ち続けなくてはなりません。IVRが「残高を確認するには1を押してください」とアナウンスする場合、ユーザーは必要なオプションを待っていれば、何も記憶しなくても、それに応じて番号を押せばいいのです。IVRの使いやすさが向上するのです。

**3）担当者と話す選択肢：** 顧客サポートスタッフへの通話に割り当てられる番号は、業界標準ではありません。米国の300社以上の企業をリストアップ IVRチートシート に証拠付けられるように、人気のある選択肢は 0(ゼロ)で 、「担当者へつなぐには、0を押してください」など、しています。音声アナウンスが開始される前でも、IVRをとばして、担当者への通話を、ユーザー任意の時点でできるように、考えてみましょう。タイムアウト後にユーザーからの入力がなくても、常にユーザーからのコールを、カスタマーサポートチームにルーティングしましょう。こちらからユーザーのコールを切ることは絶対にしてはいけません。

**4）マーケティングをスキップ：** 全米企業500社番付 の中では 実践されているように、導入メッセージにはあなたの組織の名前と簡単な歓迎の挨拶を使用し、その他のマーケティングキャンペーンは割愛してください。商品広告、企業ニュース、プロモーションなどは不要です。ユーザーのほとんどは、電話をする前に、あなたの組織を知っているので、電話ではそれを先に進めたいと思っているのです、それを保留したりせず、ユーザーを進めさせてあげてください。

**5）短く保つ：** ペースの速い今日の世界では、時間は貴重です。ユーザーは通常、完璧な長いスピーチを聞くほど忍耐強くありません。ただキーワードをつなぎ、それで終わらせてください。経験則として、紹介メッセージを8秒未満に保ち、各オプションのアナウンスは、それぞれ4秒未満にすると良いでしょう。

**6）コールキューの管理：** カスタマーサポートスタッフが着信コールにすぐに応答できず、ユーザーがキューに入れられている場合は、コールバックオプションを提供しましょう。ユーザーに電話番号を入力して電話を切り、カスタマーサポートスタッフからの電話を待つよう指示してください。

**7）女性の声がより一般的です：** 一般に、ほとんどのIVRは男性でなく、女性の音声を使用します。そして、ほとんどのユーザーが実際に女性の音声を好むことは、生物学的、歴史的、社会的理由において広く認められています 。しかし、1990年代後半、BMWにおいて、女性の指示は受けない、というドイツ男性からの電話がヘルプデスクに殺到し、5つものシリーズモデルにて、女性の音声のGPSのリコール があった、という例外は一件あったのですが。
 
![ivrflow](/images/ivrflow.jpg)

組織またはクライアントのIVRを構築する場合は、ソリューションのパズルの一片として使用できる、APIをチェックしてください。