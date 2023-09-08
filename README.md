<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2023/08/logo-github-cwmkt.svg" alt="DispZap Whats Marketing" width="240" />
<p align="center">Seja bem-vindo ao Guia de Instalação Chatwoot 🚀</p>
</p>
  
<p align="center">
<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
<span>Grupo WhatsaAPP: </span>
<a href="https://link.cwmkt.com.br/grupo-whats" target="_blank">Grupo</a>
</p>

<hr />
<hr />

<details>
<summary>Manual de Instalação ChatWoot</summary>

```bash
sudo apt update && apt upgrade -y
```

```bash
wget https://get.chatwoot.app/linux/install.sh
```

```bash
chmod +x install.sh
```

```bash
./install.sh --install
```

Use as opções abaixo

yes

app.dominio.com.br

contato@dominio.com.br

yes para todos


### Alterando Idioma e ativando sua tela de cadastro

</p>
cd /home/chatwoot/chatwoot
</p>
nano .env
</p>
Altere a linha
</p>
DEFAULT_LOCALE=pt_BR
</p>
ENABLE_ACCOUNT_SIGNUP=true
</p>
sudo systemctl restart chatwoot.target
</p>
Acesse: seudominio.com.br
</p>
Faça seu cadastro
</p>

### Habilitando configurações ocultas do Chatwoot

```bash
sudo -i -u postgres psql
\c chatwoot_production
update installation_configs set locked = false;
\q
```

</details>

<details>

<summary>Instalação da API e configurações</summary>

Acesse seu chatwoot e crie uma nova caixa de entrada desde

Configurações 
Caixas de Entrada
Adicionar Caixa de Entrada
Escolha um canal
API
Nombre de canal
URL do Webhook: https://dominio.com/chatwootMessage

```bash
npm update -g pm2@latest
```

```bash
cd /home
```

```bash
git clone https://github.com/nestordavalos/whatsapp-web-chatwoot1
```

```bash
cp .env.example .env
```

```bash
nano .env
```

PORT                                          = 8080
CHATWOOT_API_URL                              = "https://app.chatwoot.com/api/v1"
CHATWOOT_API_KEY                              = "YOUR_CHATWOOT_API_KEY"
CHATWOOT_ACCOUNT_ID                           = "CHATWOOT_ACCOUNT_ID"
CHATWOOT_WW_INBOX_ID                          = "CHATWOOT_API_CHANNEL_ID"
CHATWOOT_WW_GROUP_PARTICIPANTS_ATTRIBUTE_NAME = "group_participants"
REMOTE_PRIVATE_MESSAGE_PREFIX                 = "REMOTE: "
PREFIX_AGENT_NAME_ON_MESSAGES                 = true
#SLACK_TOKEN                                  = "YOUR_SLACK TOKEN"
#SLACK_CHANNEL_ID                             = "YOUR_SLACK_CHANNEL_ID"

```bash
npm install
```

```bash
sudo apt-get install -y libgbm-dev wget unzip fontconfig locales gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
```

```bash
sudo apt install ./google-chrome-stable_current_amd64.deb
```

```bash
sudo apt install nginx
```

```bash
nano /etc/nginx/sites-available/whatsapp-web-v2
```

```bash
server {

  server_name api.dominio.com;
  
  listen 443 ssl http2;
  listen [::]:443 ssl http2;
  underscores_in_headers on;

  access_log /var/log/nginx/chatwoot_access_443.log;
  error_log /var/log/nginx/chatwoot_error_443.log;

  location / {

   proxy_pass http://127.0.0.1:8080;
   proxy_pass_header Authorization;
   proxy_set_header Upgrade $http_upgrade;
   proxy_set_header Connection "upgrade";
   proxy_set_header Host $host;
   proxy_set_header X-Forwarded-Proto $scheme;
   proxy_set_header X-Forwarded-Ssl on; # Optional
   proxy_set_header X-Real-IP $remote_addr;
   proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
   proxy_http_version 1.1;
   proxy_set_header Connection "";
   proxy_buffering off;
   client_max_body_size 0;
   proxy_read_timeout 36000s;
   proxy_redirect off;
  }
}
```

```bash
ln -s /etc/nginx/sites-available/webapi /etc/nginx/sites-enabled
```

```bash
sudo apt-get install snapd
```

```bash
sudo snap install notes
```

```bash
sudo snap install --classic certbot
```

```bash
certbot --nginx
```

```bash
npm start
```

Escanear QRCODE 


  
NOMES CHATWOOT TERMOS E POLITICA DE PRIVACIDADE

Acesse super Admin

https://seudominio.com.br/super_admin

Opção>installation_configs

LOGO

LOGO_THUMBNAIL

NOMES CHATWOOT:

Alterando nomes na plataforma

INSTALLATION_NAME

BRAND_NAME

TERMOS E POLITICA DE PRIVACIDADE

TERMS_URL

PRIVACY_URL

BRAND_URL

WIDGET_BRAND_URL
