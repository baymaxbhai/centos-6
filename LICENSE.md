seting squid proxy n centos

sed -i 's/#cache_dir/cache_dir/g' /etc/squid/squid.conf

touch /etc/squid/passwd
chown root.squid /etc/squid/passwd
chmod 640 /etc/squid/passwd

htpasswd /etc/squid/passwd baymaxbhai

yum install httpd-devel

perl -le ‘print crypt(“password_anda“, “salt”)’
