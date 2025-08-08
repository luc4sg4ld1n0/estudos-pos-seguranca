# Zero Trust

🔐 O que é Zero Trust?

Zero Trust é uma filosofia de segurança baseada no princípio de:

“Nunca confie, sempre verifique.”

Isso significa que nenhum usuário, dispositivo ou aplicação é automaticamente confiável, mesmo dentro da rede corporativa.

⸻

🧠 Princípios Fundamentais do Zero Trust
	1.	Verificação contínua (Verify explicitly)
	•	Autenticação forte e constante
	•	MFA (autenticação multifator)
	•	Verificação de identidade, localização, dispositivo, etc.
	2.	Privilégios mínimos (Least privilege access)
	•	Usuários só acessam o que precisam, por tempo limitado
	•	Controle de acesso granular (RBAC/ABAC)
	3.	Presumir violação (Assume breach)
	•	Tratar toda rede como comprometida por padrão
	•	Isolar segmentos, monitorar e auditar tudo

⸻

🧱 Componentes principais de uma arquitetura Zero Trust

Componente	Descrição
Identidade	Controle forte de identidade de usuários e máquinas (IdPs, IAM)
Dispositivo	Verificação da integridade e estado do dispositivo
Acesso adaptativo	Política baseada em risco, contexto e confiança
Rede segmentada	Microsegmentação para impedir movimento lateral
Monitoramento e resposta	Telemetria em tempo real, alertas, automação de resposta
MFA em tudo	Acesso nunca confiado apenas por senha


⸻

🏛️ Comparando: Perímetro tradicional vs. Zero Trust

Modelo Tradicional	Zero Trust
“Confia na rede interna”	“Nada é confiável por padrão”
Firewalls e VPNs	Identidade, contexto e verificação
Acesso amplo	Acesso granular (mínimo necessário)
Segurança no perímetro	Segurança embutida em todos os níveis


⸻

🚀 Tecnologias que apoiam Zero Trust:
	•	IAM (Identity & Access Management) – Okta, Azure AD, Auth0
	•	MFA / SSO – Duo, Microsoft Authenticator
	•	ZTA Platforms – Google BeyondCorp, Zscaler ZPA, Cloudflare Zero Trust
	•	EDR/XDR – CrowdStrike, SentinelOne, Microsoft Defender
	•	SIEM – Splunk, Elastic, Azure Sentinel
	•	Microsegmentação – VMware NSX, Illumio

⸻

💼 Exemplos de uso real:
	•	Google: Implementou o conceito com o projeto BeyondCorp
	•	Empresas com trabalho remoto: Substituem VPN por soluções ZTNA
	•	Ambientes com dados sensíveis: Financeiras, saúde, defesa

⸻

📋 Benefícios do Zero Trust

✅ Reduz superfície de ataque
✅ Impede movimentação lateral de atacantes
✅ Melhora controle e auditoria
✅ Aumenta segurança em ambientes híbridos/nuvem

⸻