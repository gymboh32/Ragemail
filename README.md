# Ragemail
basic config file for insecure mail server

sudo apt-get install postfix

sudo dpkg-reconfigure postfix

Internet Site
mail.example.com
steve
mail.example.com, localhost.localdomain, localhost
No
127.0.0.0/8 [::ffff:127.0.0.0]/104 [::1]/128 192.168.0.0/24
0
+
all

cp /etc/postfix/main.cf

sudo service postfix restart

sudo apt-get install dovecot-common

cp /etc/dovecot/conf.d/10-master.conf

cp /etc/dovecot/conf.d/10-auth.conf

sudo service dovecot restart

telnet mail.example.com 25
ehlo mail.example.com

sudo apt-get install dovecot-imapd dovecot-pop3d

cp /etc/dovecot/dovecot.conf

cp /etc/dovecot/conf.d/10-mail.conf

sudo service dovecot restart

telnet localhost pop3

cp /etc/dovecot/conf.d/10-ssl.conf
