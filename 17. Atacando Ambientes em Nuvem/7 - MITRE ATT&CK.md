# MITRE ATT&CK

🛡️ O que é o MITRE ATT&CK?

O MITRE ATT&CK (Adversarial Tactics, Techniques & Common Knowledge) é uma base de conhecimento pública criada pela MITRE Corporation que descreve táticas, técnicas e procedimentos (TTPs) usados por cibercriminosos e grupos APT no mundo real.

Ele é usado para:
	•	Mapear como ataques acontecem, do início ao fim
	•	Planejar defesa (Blue Team) e testes de segurança (Red Team)
	•	Criar relatórios e inteligência de ameaças (Threat Intelligence)
	•	Treinar SOC, DFIR, Threat Hunters

⸻

📂 Estrutura do MITRE ATT&CK

O framework é dividido em táticas (objetivos do atacante) e técnicas (como ele realiza o objetivo).

1. Táticas (colunas do ATT&CK Matrix)

São o “porquê” de cada ação do atacante.
Exemplos:
	•	Reconnaissance – Coleta de informações
	•	Initial Access – Primeira entrada no sistema
	•	Execution – Executar código malicioso
	•	Persistence – Manter acesso
	•	Privilege Escalation – Ganhar mais privilégios
	•	Defense Evasion – Evitar detecção
	•	Credential Access – Roubo de credenciais
	•	Discovery – Descobrir informações internas
	•	Lateral Movement – Movimento lateral na rede
	•	Collection – Coletar dados
	•	Exfiltration – Roubar dados
	•	Impact – Danos e destruição

⸻

2. Técnicas e Subtécnicas

São o “como” cada objetivo é atingido.
Exemplo:
	•	T1078 – Valid Accounts (uso de contas legítimas)
	•	Subtécnica: T1078.003 – Cloud Accounts (usar credenciais AWS, Azure, etc.)

⸻

🏴 Como é usado na prática

🔹 Red Team / Pentest:
	•	Escolhem técnicas do MITRE para simular ataques realistas
	•	Ex: usar T1059 (Command and Scripting Interpreter) para execução de payloads

🔹 Blue Team / SOC:
	•	Criam detecções no SIEM/EDR para técnicas específicas
	•	Ex: regras para detectar T1003 (Credential Dumping) no Windows Event Log

🔹 Threat Intelligence:
	•	Associam grupos APT às técnicas que eles usam
	•	Ex: APT29 é conhecido por T1566 (Phishing) + T1078 (Valid Accounts)

⸻

📊 Tipos de matrizes do MITRE ATT&CK
	•	Enterprise – Sistemas corporativos (Windows, Linux, macOS, Cloud, SaaS)
	•	Mobile – Ataques a Android e iOS
	•	ICS – Sistemas industriais (SCADA, OT)

⸻

🛠 Ferramentas que usam o MITRE ATT&CK
	•	ATT&CK Navigator – Para criar sua própria matriz personalizada
	•	Caldera – Automação de Red Team baseada no ATT&CK
	•	OpenCTI / MISP – Plataformas de Threat Intelligence
	•	Sigma rules – Para criar detecções alinhadas ao ATT&CK

⸻