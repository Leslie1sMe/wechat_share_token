# wechat_share_token

微信分享token

使用方法：composer require leslie/wx_token


<?php

use Leslie\WxToken\GetWxToken;

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



