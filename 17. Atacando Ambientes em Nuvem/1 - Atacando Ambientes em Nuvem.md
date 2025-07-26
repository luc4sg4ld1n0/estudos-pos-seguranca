# Atacando Ambientes em Nuvem

🔐 Testes de Segurança em Ambientes de Nuvem (Cloud Pentesting)

☁️ Principais vetores de ataque em nuvem:
	1.	Credenciais expostas (S3, GitHub, GitLab)
	•	Tokens de acesso mal configurados ou vazados
	•	Chaves IAM da AWS publicadas por engano
	2.	Má configuração de permissões IAM
	•	Privilégios excessivos atribuídos a usuários ou serviços
	•	Uso incorreto de roles e políticas
	3.	Serviços mal configurados (S3 buckets, RDS, Cloud Functions)
	•	Buckets públicos acessíveis sem autenticação
	•	APIs expostas sem controle de acesso
	4.	Movimentação lateral e escalonamento de privilégios
	•	Explorar permissões para mudar entre serviços e escalar privilégios (ex: de um container ECS para root IAM)
	5.	Exploração de metadata services
	•	Ataques SSRF para acessar http://169.254.169.254/ e roubar tokens temporários
	6.	Senhas e segredos mal armazenados
	•	Em variáveis de ambiente
	•	Em arquivos de configuração ou repositórios de código

⸻

🔧 Ferramentas comuns usadas em cloud pentest:

Ferramenta	Finalidade
Pacu (by Rhino Security)	AWS exploitation framework
ScoutSuite	Análise estática de configurações de nuvem
CloudSploit / Prowler	Detecção de má configuração na AWS
TruffleHog	Busca por chaves e segredos em repositórios
S3Scanner	Identificação de buckets públicos na AWS
nuclei + templates para nuvem	Scanners de vulnerabilidades baseados em YAML


⸻

📌 Boas práticas (e limites éticos):
	•	Só realizar testes em ambientes que você controla ou tem autorização formal.
	•	Utilize contas isoladas para pentest.
	•	Evite causar DDoS involuntário (ex: fuzzing sem controle).
	•	Tenha logs e monitoramento para revisar comportamentos suspeitos.

⸻