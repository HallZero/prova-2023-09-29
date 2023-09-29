# prova-2023-09-29

# Criando instâncias EC2

![EC2 Console](./media/EC2-console.png)
![EC2 Instances](./media/EC2-instances.png)
![EC2 Launch Instances](./media/EC2-Launch.png)
![EC2 Configuring](./media/EC2-config.png)
![EC2 Network Settings](./media/EC2-Network.png)
![EC2 Instances Frontend & Backend](./media/EC2-front-back.png)

Entenda aqui a criação análoga do frontend e backend\

## Permissões da instância
![EC2 Inbound](./media/EC2-Backend-inbound.png)

## Adicionando IP elástico à instância Backend

![Elastic IP](./media/Elastic-IP.png)
![Elastic Config](./media/Elastic-config.png)
Note que o IP associado é o da instância backend!
# Criando uma instância RDS

![RDS Console](./media/RDS-console.png)
![RDS Database](./media/RDS-database.png)
![RDS Config](./media/RDS-config.png)
![RDS Free Tier](./media/RDS-free-tier.png)
![RDS Public](./media/RDS-public.png)
![RDS Monitoring](./media/RDS-Monitoring.png)

![RDS Inbound](./media/RDS-inbound.png)

# Testando a comunicação utilizando DBeaver
![DBeaver](./media/Dbeaver-connect.png)

## Comandos dentro da Instância Frontend 

Comandos para alocar os arquivos para rodar o frontend utilizando Apache\

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

## Comandos dentro da Instância Backend

```bash
sudo apt update
sudo apt upgrade -y

git clone https://github.com/HallZero/prova-2023-09-29.git

sudo apt install python3-pip

cd prova-2023-09-29/backend

python3 criar_banco.py

python3 main.py
```

# Alteração no arquivo script.js

Configurei um IP elástico para a instância de EC2 do backend para poder fazer requisições a partir do frontend

![IP Elástico](./media/Scripts-Elastic.png)