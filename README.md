# wechat_share_token
### 微信分享token
<p>使用方法:</p>

<pre><code>
composer require leslie/wx_token

access_token; $getTicket = GetWxToken::getTicket($access); $ticket = $getTicket->ticket; $res = GetWxToken::getSignature($url,$ticket); var_dump($res); 


use Leslie\WxToken\GetWxToken;
require ('vendor/autoload.php');

$appId = "xxxxxxxxxx";
$secret = "xxxxxxxxxxxxxxxxx";
$url = "xxxxxxxxxxxxxxxxxxxxxxxxx";
$timestamp = time();
$nonceStr = GetWxToken::getAccessToken($appId,$secret);
$access = $nonceStr->access_token;
$getTicket = GetWxToken::getTicket($access);
$ticket = $getTicket->ticket;
$res =  GetWxToken::getSignature($url,$ticket);
var_dump($res);
</code></pre>

