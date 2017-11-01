# Не работает отправка почты 1C Bitrix (GMail)
<h2>Решение</h2>
<p>
1. Создать вручную файл ".msmtprc" (В виртуальной машине иногда не создается этот файл. Причину не выяснил.)
</p>

<p>
2. В этом файле вписать следующий код:
</p>

```php
account default
logfile /home/bitrix/.msmtp.log
host smtp.gmail.com
port 587
from <логин>@gmail.com
auth on
user <логин>@gmail.com
password <пароль>

tls on
tls_starttls on
tls_certcheck off
```
<p>
P.S: user и password надо использовать от GMail.
</p>

<p>
  3. Установить разрешение на самой почте GMail <a href="https://myaccount.google.com/lesssecureapps">Разрешить ненадежным приложениям доступ</a>
</p>
