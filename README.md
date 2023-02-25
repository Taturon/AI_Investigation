# AI_Investigation
## 各種AIチャットサービス
|サービス|ChatGPT|Bing AI|Perplexity Ask|Notion AI|Google Bard|
|リリース|2022/11/30|2023/2/7|2022/12/7|2023/2/23|未定|

### 同じ回答を投げてみた
#### 「PHPで1から10000の範囲の素数を出力するプログラムを作成してください」

|Bing Ai|ChatGPT|Perplexity AI|Notion AI|
| --- | --- | --- | --- |
|![](img/Bing_AI_1.png)|![](img/ChatGPT_1.png)|![](img/Perplexity_AI_1.png)|![](img/Notion_AI_1.png)|
##### Bing AI
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
##### ChatGPT
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
##### Perplexity AI
```php
<?php for ($i = 2; $i <= 10000; $i++) { $is_prime = true; for ($j = 2; $j < $i; $j++) { if ($i % $j == 0) { $is_prime = false; break; } } if ($is_prime) { echo "$i\n"; } } ?>
```
##### Notion AI
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