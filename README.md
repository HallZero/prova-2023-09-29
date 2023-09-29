# prova-2023-09-29

```bash

sudo apt update
sudo apt upgrade -y
sudo apt install apache2 -y

git clone https://github.com/HallZero/prova-2023-09-29.git

sudo cp ./prova-2023-09-29/frontend /var/www/html

cd /var/www/html

sudo mv ./frontend/index.html /var/www/html
sudo mv ./frontend/script.js /var/www/html
sudo mv ./frontend/styles.css /var/www/html

sudo rmdir frontend

```