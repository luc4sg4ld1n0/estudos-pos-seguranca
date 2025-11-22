# MXToolBox

O MXToolbox é uma plataforma online que oferece um conjunto de ferramentas para diagnóstico, análise e monitoramento de serviços de e-mail, DNS e infraestrutura de rede. Ele é muito usado por administradores de TI, equipes de segurança e profissionais de e-mail para identificar problemas rapidamente.

⸻

✅ O que o MXToolbox faz?

Ele permite verificar e analisar diversos aspectos de infraestrutura, principalmente relacionados a envio e recebimento de e-mails. Entre as funções principais:

1. MX Lookup (Registros MX)

Mostra quais servidores são responsáveis por receber e-mails de um domínio.
É útil para verificar configurações corretas em serviços como Microsoft 365, Google Workspace, Zimbra etc.

2. DNS Lookup

Consulta vários tipos de registros DNS:
	•	A
	•	AAAA
	•	CNAME
	•	TXT
	•	SPF
	•	DKIM
	•	DMARC
	•	SOA
	•	NS

Essas informações ajudam a validar se o domínio está configurado corretamente.

3. Blacklist Check

Verifica se um domínio ou endereço IP está listado em bases públicas de bloqueio (RBLs).
Se estiver, pode afetar a entrega de e-mails.

4. SMTP Test

Testa a comunicação com um servidor SMTP.
Avalia:
	•	Conectividade
	•	Resposta do servidor
	•	TLS/SSL
	•	Possíveis erros de configuração

5. Diagnóstico de e-mail

Permite testes avançados, como:
	•	Trace de rota de e-mail (Email Trace)
	•	Análise de delays
	•	Entrega e autenticação

6. Monitoramento contínuo (versão paga)

Envio de alertas quando:
	•	Um servidor sai do ar
	•	Um IP aparece em uma blacklist
	•	DNS falha
	•	E-mail não está sendo entregue corretamente

⸻

⚙️ Como o MXToolbox funciona?

De forma geral, ele funciona realizando consultas diretas a servidores DNS, listas RBL e serviços de e-mail, usando protocolos padrões da internet como:
	•	DNS (53/UDP/TCP)
	•	SMTP (25/TCP)
	•	HTTP/HTTPS
	•	TCP/ICMP para testes de disponibilidade

Ele reúne tudo isso em uma interface simples, facilitando diagnósticos que, manualmente, exigiriam muitos comandos diferentes.

⸻

🎯 Para que serve na prática?

O MXToolbox é útil para:
	•	Diagnosticar falhas no recebimento/envio de e-mails
	•	Verificar se um domínio está em listas de spam
	•	Validar configurações de SPF, DKIM e DMARC
	•	Analisar registros DNS
	•	Identificar problemas de infraestrutura
	•	Monitorar saúde de servidores e serviços