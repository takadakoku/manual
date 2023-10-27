#Virtual Hostでドメインの登録
##1.移動
>>cd /etc/apache2/sites-available

##2.設定ファイル作成
>>cp 000-default.conf takadakoki.conf

##3.ファイル編集
```
<VirtualHost *:80>
        ...
        ServerName takadakoki.com
        DocumentRoot /var/www/wordpress/ 
        ...
</VirtualHost>
```

##4.Virtual Hostに登録
>>a2ensite takadakoki.conf

##5. apacheの再起動
>>systemctl restart apache2


参考
https://qiita.com/i-tanaka730/items/3f28150eb1b3b7f8183c
