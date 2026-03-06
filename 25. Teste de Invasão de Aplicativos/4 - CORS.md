# CORS

CORS (Cross-Origin Resource Sharing) é um mecanismo de segurança dos navegadores que controla quais sites podem acessar recursos de outro domínio via requisições web (como APIs). 🌐🔒

Ele foi criado para flexibilizar uma regra de segurança chamada Same-Origin Policy, um conceito importante da segurança web estudado em OWASP e abordado no OWASP Top 10.

⸻

O que é Same-Origin Policy

Por padrão, navegadores bloqueiam requisições entre domínios diferentes.

Exemplo:

Site A:

https://siteA.com

Site B:

https://api.siteB.com

O Site A não pode acessar diretamente dados do Site B sem permissão.

É aí que entra o CORS.

⸻

Como o CORS funciona

O servidor define quem pode acessar seus recursos usando headers HTTP.

Exemplo de header:

Access-Control-Allow-Origin: https://siteA.com

Isso significa:

👉 Apenas siteA.com pode fazer requisições para essa API.

Outros headers comuns:

Access-Control-Allow-Origin
Access-Control-Allow-Methods
Access-Control-Allow-Headers
Access-Control-Allow-Credentials


⸻

Exemplo de fluxo CORS

1️⃣ O navegador envia uma requisição com header:

Origin: https://siteA.com

2️⃣ O servidor responde:

Access-Control-Allow-Origin: https://siteA.com

3️⃣ O navegador permite o acesso.

Se o domínio não estiver autorizado → o navegador bloqueia.

⸻

Tipos de requisição CORS

Simple request

Requisições simples como:
	•	GET
	•	POST
	•	HEAD

Sem headers especiais.

⸻

Preflight request

Para requisições mais complexas, o navegador envia primeiro um OPTIONS request para verificar permissões.

Exemplo:

OPTIONS /api

Isso verifica se a requisição real é permitida.

⸻

Problemas de segurança com CORS

Configurações erradas podem permitir vazamento de dados.

Exemplos perigosos:

1️⃣ Allow origin wildcard

Access-Control-Allow-Origin: *

Qualquer site pode acessar.

⸻

2️⃣ Reflect origin

Servidor retorna qualquer origin enviado:

Origin: evil.com
Access-Control-Allow-Origin: evil.com

Isso pode permitir roubo de dados.

⸻

3️⃣ Credentials + wildcard

Configuração insegura:

Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true

Pode expor sessões autenticadas.

⸻

Ferramentas usadas para testar CORS
	•	Burp Suite
	•	OWASP ZAP