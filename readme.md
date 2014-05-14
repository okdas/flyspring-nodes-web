apt-get update && apt-get dist-upgrade -y
apt-get install nginx git -y

cd /var
git clone https://github.com/okdas/flyspring-nodes-web

mv /var/flyspring-nodes-web/default.conf /etc/nginx/conf.d/default.conf
/etc/init.d/nginx restart