# Teste de Invasão de Aplicativos

Um pentest de aplicativo consiste em analisar um sistema (web, mobile ou API) para encontrar falhas como:
	•	Falhas de autenticação
	•	Problemas de autorização
	•	Vazamento de dados
	•	Injeções de código
	•	Configurações inseguras

Essas falhas são exploradas de forma ética para entender o impacto.

Um guia muito usado nesse processo é o OWASP e especialmente o projeto OWASP Top 10, que lista as vulnerabilidades mais comuns em aplicações web.

⸻

Tipos de teste de invasão

Existem diferentes abordagens:

1. Black Box
	•	O testador não tem acesso ao código ou arquitetura
	•	Simula um hacker externo

2. Grey Box
	•	O testador tem acesso parcial
	•	Simula um usuário interno

3. White Box
	•	O testador tem acesso completo ao código e infraestrutura
	•	Permite análise profunda

⸻

Principais vulnerabilidades testadas

Alguns exemplos comuns incluem:
	•	SQL Injection
	•	Cross-Site Scripting (XSS)
	•	Broken Authentication
	•	Broken Access Control
	•	Exposição de dados sensíveis

Essas falhas estão documentadas no OWASP Top 10.

⸻

Ferramentas usadas em pentest de aplicativos

Algumas ferramentas populares:
	•	Burp Suite
	•	OWASP ZAP
	•	Metasploit
	•	Nmap

Essas ferramentas ajudam a automatizar análise de vulnerabilidades.

⸻

Etapas de um pentest
	1.	Reconhecimento – coleta de informações
	2.	Mapeamento – identificação de endpoints e funcionalidades
	3.	Análise de vulnerabilidades
	4.	Exploração controlada
	5.	Relatório técnico com riscos e recomendações