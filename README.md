# homework_login_or_member
上課作業---登入或會員專頁

前置條件:需要phpmyadmin,並且建立資料庫叫:test_for_homework

並建立Table:Account     欄位:Account(char) Password(char) nickname(char)

「

create database test_for_homework  character set  utf8;  

use  test_for_homework;

create table Account(Account char(20),Password char(20),nickname char(20));

」




1:homework_index.php
為首頁，有註冊、登入、會員專用頁功能

點選註冊會進到homework_register.php

為註冊頁面

點選登入會進到homework_login.php

為登入頁面

點選會員專用頁會進到homework_secret.php

為會員專用頁


2:homework_register.php

簡易的註冊功能，註冊完的帳號密碼會上傳至資料庫

為避免重新整理會再次上傳資料，於是使用了session

方式:html表單產生一個隨機數字給PHP存session，如果重新整理後PHP讀到一樣的session

那PHP就不再執行一次。

註冊完畢建立帳號密碼的COOKIE,並進入homework_index_for_secret.php


3:homework_login.php

簡易登入功能，輸入帳號密碼，至資料庫搜尋

如果符合，則建立帳密COOKIE並進入homework_index_for_secret.php


4:homework_secret.php

進入此頁面時，如果已登入會員

會直接進入homework_index_for_secret.php

若無，則進到homework_login.php

5:homework_index_for_secret.php

會員專用頁，有登出功能

登出功能:刪除帳密COOKIE，並回到homework_login.php
