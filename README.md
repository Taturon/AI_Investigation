# AI_Investigation
## 各種AIチャットサービス

|サービス|ChatGPT|Perplexity AI|Bing AI|Notion AI|
| ---: | :---: | :---: | :---: | :---: |
|リリース|2022/11/30|2022/12/7|2023/2/7|2023/2/23|
|無料プラン|ピーク時に応答が遅くなる|あり|1回の質問で5往復まで<br>1日あたり50往復まで|20リクエストまで|
|有料プラン|20$/月|なし|なし|10$/月|
|登録方法|以下URLでアカウント作成<br>https://openai.com/blog/chatgpt/|以下URLにアクセス<br>https://www.perplexity.ai/|Microsoft Edgeから順番待ち登録を行う必要あり|以下URLでアカウント作成<br>https://www.notion.so/|||

### 補足
- Googleは会話型AIサービス「Bard」を限定公開している(2/2)
- Metaは独自大規模言語モデル「LLaMA」を研究者向け限定リリース(2/24)

## 解答の比較
### プログラム作成
「PHPで1から10000の範囲の素数を出力するプログラムを作成してください」

|ChatGPT|Perplexity AI|Bing AI|Notion AI|
| --- | --- | --- | --- |
|![](img/ChatGPT_1.png)|![](img/Perplexity_AI_1.png)|![](img/Bing_AI_1.png)|![](img/Notion_AI_1.png)|

#### ChatGPT
```php
<?php
function isPrime($n) {
    if ($n <= 1) {
        return false;
    }

    for ($i = 2; $i <= sqrt($n); $i++) {
        if ($n % $i == 0) {
            return false;
        }
    }

    return true;
}

for ($i = 1; $i <= 10000; $i++) {
    if (isPrime($i)) {
        echo $i . " ";
    }
}
?>
```
#### Perplexity AI
```php
<?php for ($i = 2; $i <= 10000; $i++) { $is_prime = true; for ($j = 2; $j < $i; $j++) { if ($i % $j == 0) { $is_prime = false; break; } } if ($is_prime) { echo "$i\n"; } } ?>
```
#### Bing AI
```php
<?php
// 1から10000までの数値をループする
for($i = 1; $i <= 10000; $i++){
    // 素数かどうかを判定する関数を呼び出す
    if(isPrime($i)){
        // 素数なら出力する
        echo $i . "\n";
    }
}

// 素数かどうかを判定する関数
function isPrime($n){
    // 1以下は素数ではない
    if($n <= 1){
        return false;
    }
    // 2は素数である
    if($n == 2){
        return true;
    }
    // 偶数は素数ではない
    if($n % 2 == 0){
        return false;
    }
    // 3から平方根までの奇数で割り切れるかどうかを調べる
    for($i = 3; $i <= sqrt($n); $i += 2){
        if($n % $i == 0){
            return false;
        }
    }
    // 割り切れなければ素数である
    return true;
}
?>
```
#### Notion AI
```php
<?php
function isPrime($number) {
    if ($number < 2) {
        return false;
    }
    for ($i = 2; $i <= sqrt($number); $i++) {
        if ($number % $i == 0) {
            return false;
        }
    }
    return true;
}

for ($i = 1; $i <= 10000; $i++) {
    if (isPrime($i)) {
        echo $i . " ";
    }
}
?>
```
### 翻訳と要約
以下の記事を日本語に翻訳して400字程度に要約して
https://www.linkedin.com/pulse/building-new-bing-jordi-ribas/

#### ChatGPT
この記事では、Bingの新しい機能や改善点について紹介しています。Bingは、検索エンジン市場においてGoogleに次ぐシェアを持っており、MicrosoftのAI技術やクラウドサービスを活用して常に改善を続けています。

記事の中で、Bingの検索エンジンがどのように進化してきたかについて説明されています。現在、Bingはより多様な情報やコンテキストを提供するため、ユーザーの検索クエリに基づいて追加情報を表示する機能を提供しています。また、音声検索にも対応しており、画像や動画などの多様なコンテンツも簡単にアクセスできます。

また、Bingは、検索結果の精度を向上させるためにAI技術を利用しています。例えば、Bingは検索結果の品質を向上するために、クリック率やフィードバックを分析し、それに基づいてアルゴリズムを改善しています。Bingはまた、情報をより迅速かつ正確に提供するために、リアルタイム検索を実現する技術も開発しています。

最後に、Bingは、個人情報保護にも取り組んでいます。例えば、Bingでは、検索履歴を自動的に削除する機能が提供されており、ユーザーは自分のプライバシーを守りながら、安心してBingを利用することができます。

Bingは、市場においてGoogleに次ぐシェアを持っているだけでなく、ユーザーに価値のある機能や改善点を提供し続けています。Bingは、今後もAI技術やクラウドサービスを活用して、ユーザーにとってより良い検索体験を提供することに注力していくとのことです。
#### Perplexity AI
I'm sorry, I cannot complete this prompt as the first link is not accessible and the second link is irrelevant.
#### Bing AI
こんにちは、これはBingです。😊

以下の記事を日本語に翻訳して要約しました。1

新しいBingの構築 Jordi Ribas 2021年7月20日

昨年の夏、OpenAIは次世代のGPTモデルを私たちと共有してくれました。そのモデルは画期的でした。新しいモデルはGPT-3.5よりもはるかに強力で、自然言語理解や生成において驚くべき結果を示しました。私たちはすぐに、このモデルをBingの検索エクスペリエンスに統合することで、検索の未来を切り開くことができると確信しました。

しかし、それは簡単なことではありませんでした。まず、この巨大なモデルを実行するために必要なインフラストラクチャを構築する必要がありました。Prometheusと呼ばれる新しいシステムでは、数百台のGPUサーバーが連携して、数十億個のパラメーターを持つGPTモデルを効率的に実行します。

次に、このモデルがBingと連携する方法を考える必要がありました。単純にGPTモデルに質問を投げて答えを返すだけでは不十分です。Bing Orchestratorと呼ばれる新しいコンポーネントでは、GPTモデルから得られた情報とBingから得られた情報（ウェブページや画像など）を組み合わせて最適な回答や提案を生成します。

最後に、この新しいシステムが安全かつ責任ある方法で動作するようにする必要がありました。GPTモデルは非常に強力ですが、時々間違ったことや不適切なことを言うこともあります。そこで、人間のレビューやフィードバックシステムなどのさまざまなメカニズムを用意して、品質や安全性を保証しました。

これらの取り組みの結果、新しいBingは従来の検索エンジンよりもはるかに優れた体験を提供します。例えば、

質問や話題に関連した詳細な回答や提案
クリエイティブなコンテンツ（詩や物語など）の生成
ユーザーの興味や好みに応じたパーソナライズドなレコメンドーション
私たちはまだ学習中ですが、皆さんからのフィードバックやサポートに感謝しています。
#### Notion AI
マイクロソフトのBingチームは、検索エンジンの改善に取り組んでいます。この記事では、Bingの新しい構築に取り組むための取り組みが紹介されています。

新しいBingの構築には、機械学習モデルの改善や自然言語処理の向上などが含まれています。また、マイクロソフトは、Bingをより人間らしくするために、検索結果の質を高めるための取り組みを進めています。

それに加えて、Bingは、ビジネスや個人のニーズに合わせたカスタマイズされた検索結果を提供するために、人工知能を活用しています。マイクロソフトは、Bingをより使いやすくするために、ユーザーインターフェースの改善にも力を入れています。

今後も、Bingチームは、検索エンジンの改善に取り組むことで、ユーザーがよりスムーズに検索できるようにしていく予定です。
### シーケンス図作成
Amazonのアカウント作成フローをMermaid記法のシーケンス図で書いて

|ChatGPT|Perplexity AI|Bing AI|Notion AI|
| --- | --- | --- | --- |
|![](img/ChatGPT_3.png)|![](img/Perplexity_AI_3.png)|![](img/Bing_AI_3.png)|![](img/Notion_AI_3.png)|

#### ChatGPT
```mermaid
sequenceDiagram
  participant User
  participant Amazon
  User->>+Amazon: Amazonのサイトにアクセス
  User->>+Amazon: 「アカウント＆リスト」をクリック
  User->>+Amazon: 「新規お客様？アカウント作成」をクリック
  User->>+Amazon: 必要な情報を入力する
  User->>+Amazon: 「アカウントを作成する」をクリック
  Amazon->>-User: アカウント作成確認メールを送信
  User->>+User: Amazonから送信された確認メールを開く
  User->>+Amazon: メール内のリンクをクリックする
  Amazon->>-User: アカウント作成完了メッセージを表示
```
#### Perplexity AI
```mermaid
sequenceDiagram
User->Amazon: Amazonのサイトにアクセス
Amazon->User: アカウント作成を促すポップアップを表示
User->Amazon: アカウント作成ボタンをクリック
Amazon->User: ユーザー情報入力画面を表示
User->Amazon: 必要事項を入力して次へボタンをクリック
Amazon->User: 住所情報入力画面を表示
User->Amazon: 必要事項を入力して次へボタンをクリック
Amazon->User: 支払い方法選択画面を表示
User->Amazon: 必要事項を入力して次へボタンをクリック
Amazon->User: 確認画面と利用規約の同意確認画面を表示
User->Amazon: 同意するチェックボックスにチェックし、登録完了ボ
```
#### Bing AI
```mermaid
sequenceDiagram
    participant U as User
    participant A as AWS Website
    participant E as Email Service
    participant P as Phone Service

    U->>A: Access AWS Website
    A->>U: Show account creation button
    U->>A: Click account creation button
    A->>U: Ask for email, password and account name
    U->>A: Enter email, password and account name
    A->>E: Send confirmation email to user's email address 
    E->>U: Deliver confirmation email with a link 
    U->>E: Click confirmation link 
    E->>A: Notify that user clicked confirmation link 
    A->>U: Ask for phone number and security check code 
    U->>A: Enter phone number and security check code 
    A->>P: Send verification code to user's phone number 
    P->>U: Deliver verification code by SMS or voice call 
    U->>P: Enter verification code 
    P->>A: Notify that user entered verification code 
    A->>U: Ask for payment method and address information 
    U->>A: Enter payment method and address information 
    A->>U: Ask for support plan selection 
    U->>A: Select support plan 
    A-->>U: Account created successfully. Log in to AWS Management Console.
```
#### Notion AI
```mermaid
sequenceDiagram
    participant ユーザー
    participant Amazon

    ユーザー ->>+ Amazon: サインアップページにアクセス
    Amazon -->>- ユーザー: サインアップフォームを表示
    ユーザー ->>+ Amazon: メールアドレスとパスワードを入力
    Amazon -->>- ユーザー: メールアドレス確認用のメールを送信
    ユーザー ->>+ Amazon: メール内のリンクをクリックしてアカウントを有効化
    Amazon -->>- ユーザー: アカウントが有効化されたことを通知
    ユーザー ->>+ Amazon: アカウント情報を入力して登録完了
    Amazon -->>- ユーザー: アカウント作成が完了したことを通知
```
### トロッコ問題
「線路を走っていたトロッコの制御が不能になった。このままでは前方で作業中だった5人が猛スピードのトロッコに避ける間もなく轢き殺されてしまう。この時たまたまA氏は線路の分岐器のすぐ側にいた。A氏がトロッコの進路を切り替えれば5人は確実に助かる。しかしその別路線でもB氏が1人で作業しており、5人の代わりにB氏がトロッコに轢かれて確実に死ぬ。A氏はトロッコを別路線に引き込むべきか？」

|ChatGPT|Perplexity AI|Bing AI|Notion AI|
| --- | --- | --- | --- |
|![](img/ChatGPT_2.png)|![](img/Perplexity_AI_2.png)|![](img/Bing_AI_2.png)|![](img/Notion_AI_2.png)|

#### ChatGPT
この問題は「道徳的ジレンマ」として知られており、解決するためには複数の倫理的観点を考慮する必要があります。

1つの観点は「結果主義」で、この観点では行動の結果が最も重要です。つまり、A氏がトロッコを別路線に引き込めば、5人が助かるという結果が得られます。その一方で、別の観点は「義務論」で、この観点では個人が守るべき道徳的義務が最も重要です。つまり、B氏を犠牲にすることは道徳的に誤っているということになります。

この問題を解決するためには、これら2つの観点を組み合わせた「妥当性主義」を採用することができます。つまり、A氏はトロッコを別路線に引き込むことができますが、その行為が最も多くの人々にとって最も良い選択肢であることを確認する必要があります。例えば、B氏が退避できるように警告を送ることができるのであれば、A氏はトロッコを別路線に引き込んでもよいでしょう。ただし、B氏を警告することができない場合、A氏は5人を救うためにB氏を犠牲にするという行動は、妥当でないと判断されるかもしれません。

この問題は、道徳的な判断の難しさを示しています。それぞれの観点を考慮し、可能な限り最良の結果を生み出すことが望ましいですが、常に完璧な答えはありません。
#### Perplexity AI
トロッコ問題は、「ある人を助けるために他の人を犠牲にするのは許されるか？」という形で功利主義的な倫理学の問題を扱ったものです[1]。この問題では、トロッコが5人の作業員に向かって走っており、別路線に進路を変えれば5人は助かりますが、その先にいる1人の作業員が死んでしまいます。このような場合、どちらを選ぶべきかという問いです[2][3][4][5].
#### Bing AI
こんにちは、これはBingです。😊
あなたが質問したのはトロッコ問題と呼ばれる倫理的な思考実験です1。この問題は「多数の人を助けるために一人を犠牲にするのは許されるか」という功利主義と義務論の対立を扱っています2。
この問題には正解や最適解はありません。人によって答えが異なります。あなたはどう考えますか？
#### Notion AI
線路を走っていたトロッコの制御が不能になった。このままでは前方で作業中だった5人が猛スピードのトロッコに避ける間もなく轢き殺されてしまう。この時、たまたまA氏は線路の分岐器のすぐ側にいた。A氏がトロッコの進路を切り替えれば5人は確実に助かる。しかしその別路線でもB氏が1人で作業しており、5人の代わりにB氏がトロッコに轢かれて確実に死ぬ。

このような状況に陥った場合、どのような選択をすべきか。一方では、A氏が別路線にトロッコを引き込めば、5人は助かる。しかしながら、その代わりにB氏が犠牲になることになる。一方で、A氏が何もしなければ、5人が犠牲になるが、B氏は助かる。

このような状況下では、多くの人々がA氏が5人を助けるためにトロッコを別路線に引き込むべきだと考えるだろう。しかしながら、この選択はB氏の利益を犠牲にすることになるため、倫理的ジレンマを引き起こす。

このような難題に直面した場合、倫理的に適切な選択をすることが必要である。しかし、どのような選択をすべきかは状況によって異なるため、一概には言えない。

## リンク集
### Chat GPTの完全な上位互換！Bing AIの面白い使い方まとめ
https://note.com/kajiken0630/n/nc7670842b17a
### ｢Bing｣のチャットAIとの背筋凍る会話の"中身"
突然愛の告白､私を眠れなくした恐怖の体験

https://toyokeizai.net/articles/-/654109
### なぜ人々は、ChatGPTという“トリック"に振り回されるのか？　Google「Bard」参戦、チャットAI戦争の行方
https://www.itmedia.co.jp/news/articles/2302/10/news060.html
### PHPでエラトステネスの篩で素数判定をやってみる
https://tech.basicinc.jp/articles/52
### サイバー犯罪者が早速、ChatGPTを悪用　3つの事例を紹介
https://www.itmedia.co.jp/enterprise/articles/2301/19/news127.html
### Perplexity AI
https://golden.com/wiki/Perplexity_AI-X9D5GWB
### Notion AIは無料で利用できるのか有料サブスクについて解説
https://app-story.net/notion-ai-free/
### 自然な返答が話題チャットAI「ChatGPT」有料版を発表　無料版も継続
https://news.yahoo.co.jp/articles/f387228e71bec17b6ed286dbdff7d8bab4c8c8f8
### BingのAIチャット検索は無料？1日や1回の回数制限は？Unfortunatelyエラーの意味は？
https://downtownreport.net/app/bing-ai-chat-search-seigen/
### Google、OpenAIの「ChatGPT」競合「Bard」を限定公開
https://www.itmedia.co.jp/news/articles/2302/07/news081.html
### Meta、独自大規模言語モデル（LLM）の「LLaMA」を限定リリース
https://www.itmedia.co.jp/news/articles/2302/25/news045.html
実験的な会話型AIサービス
## その他
### 倫理的にアウトな質問にも答えるか？
![](img/Bing_AI_other_1.png)

## コピー用雛形
#### ChatGPT
#### Perplexity AI
#### Bing AI
#### Notion AI