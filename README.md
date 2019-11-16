# salyonye
How to configuration Vim settings:

create .exrc file in /home directory (sudo touch .exrc)
set the values:
   set showcmd
   set showmatch
   set ts=4
   set number

How to run localhost via Nginx:

create in / next folder (sudo mkdir -p data/www/)
in /www add index.html file with random text
sudo sh
etcho “randomtext” > index.html
open nginx.conf file (sudo vi /etc/nginx/nginx.conf)
    clear file via *number_of_rows + dd
    put in to file next values:
   
events { }
http {
        server {
                location / {
                        root /data/www;
                }
        }
}

run nginx 
open in browser http://localhost
enjoy 

How to create SSH ket for Git

ssh-keygen -t rsa -b 4096 -C "salyonaya@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa


How to clone repo from Git

git clone https://github.com/salyonaya/salyonye.git

