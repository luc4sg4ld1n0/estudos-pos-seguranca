# XSS

XSS (Cross-Site Scripting) é uma vulnerabilidade de segurança em aplicações web que permite que um atacante injete código JavaScript malicioso em páginas visualizadas por outros usuários. 🌐⚠️

Quando isso acontece, o navegador da vítima executa o script como se fosse parte legítima do site.

Esse tipo de falha está listado entre as vulnerabilidades do OWASP Top 10 mantido pela OWASP.

⸻

Como funciona um ataque XSS

O ataque geralmente ocorre quando um site não valida ou não filtra corretamente os dados enviados pelo usuário.

Fluxo simplificado:
	1.	O atacante envia um conteúdo com script para o site
	2.	O site salva ou exibe esse conteúdo sem filtrar
	3.	Outro usuário abre a página
	4.	O navegador executa o script automaticamente

Consequências possíveis:
	•	Roubo de cookies de sessão 🍪
	•	Redirecionamento para sites maliciosos
	•	Execução de ações no nome da vítima
	•	Roubo de dados do usuário

⸻

Tipos principais de XSS

1. Stored XSS (persistente)

O script fica armazenado no servidor (ex: banco de dados).

Exemplo:
	•	comentários
	•	fóruns
	•	perfis de usuário

Quando qualquer pessoa abre a página, o script executa.

⸻

2. Reflected XSS

O script é enviado em uma requisição (URL ou formulário) e refletido imediatamente na resposta da página.

Muito comum em:
	•	páginas de busca
	•	mensagens de erro

⸻

3. DOM-based XSS

O problema ocorre no JavaScript do lado do cliente, manipulando o DOM de forma insegura.

⸻

Impacto de um XSS

Dependendo da aplicação, pode permitir:
	•	roubo de sessão
	•	acesso à conta da vítima
	•	phishing dentro do próprio site
	•	execução de ações sem consentimento

⸻

Como prevenir XSS

Boas práticas usadas por desenvolvedores:
	•	Escapar saída HTML
	•	Validar entrada de usuário
	•	Usar Content Security Policy (CSP)
	•	Evitar inserir dados diretamente no DOM
	•	Usar frameworks modernos que fazem sanitização

Ferramentas usadas para encontrar esse tipo de falha incluem:
	•	Burp Suite
	•	OWASP ZAP