# MITRE D3FEND

🔎 O que é o MITRE D3FEND?
	•	Um catálogo de técnicas defensivas de cibersegurança.
	•	Estrutura padronizada de contramedidas que podem ser aplicadas contra as técnicas ofensivas descritas no ATT&CK.
	•	Ajuda a criar uma linguagem comum entre equipes de segurança, Red Team, Blue Team e gestores.

⸻

🛡️ Estrutura do MITRE D3FEND

O framework é dividido em seis categorias principais de defesa:
	1.	Harden – Reduzir a superfície de ataque
	•	Ex.: hardening de sistema, patch management, privilégios mínimos.
	2.	Detect – Identificar comportamentos suspeitos
	•	Ex.: análise de logs, monitoramento de rede, detecção de anomalias.
	3.	Isolate – Conter e limitar movimentação do atacante
	•	Ex.: microsegmentação, isolamento de processos, sandboxing.
	4.	Deceive – Enganar e atrasar o adversário
	•	Ex.: honeypots, honeytokens, falsificação de respostas de serviço.
	5.	Evict – Remover presença maliciosa
	•	Ex.: revogação de credenciais, reinstalação de imagens limpas, killing de processos.
	6.	Recover – Restaurar sistemas e dados
	•	Ex.: backups, restauração de snapshots, reconstrução de infraestrutura.

⸻

🌐 Exemplo em Ambientes de Nuvem
	•	Ataque (ATT&CK): Credential Access
	•	Defesa (D3FEND):
	•	Credential Hardening (MFA, rotacionar chaves).
	•	Credential Monitoring (alerta de uso anômalo).
	•	Ataque (ATT&CK): Lateral Movement via VPC Peering
	•	Defesa (D3FEND):
	•	Network Segmentation (subnets privadas).
	•	Traffic Flow Control (firewalls e regras restritivas).
	•	Ataque (ATT&CK): Data Exfiltration (S3 público)
	•	Defesa (D3FEND):
	•	Data Loss Prevention.
	•	Bucket Policy Enforcement.
	•	Encryption at Rest & In Transit.

⸻

✅ Benefícios de usar o MITRE D3FEND
	•	Mapear defesas diretamente contra ataques conhecidos.
	•	Apoiar planos de defesa baseados em risco.
	•	Padronizar comunicação entre Blue/Red Team.
	•	Melhorar compliance e governança em ambientes de nuvem.