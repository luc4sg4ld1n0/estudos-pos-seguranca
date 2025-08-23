# Metodologia NIST

A metodologia NIST (National Institute of Standards and Technology, dos EUA) é um dos padrões mais usados mundialmente para segurança da informação e cibersegurança. Ela fornece frameworks, guias e controles para ajudar organizações a gerenciar riscos, proteger ativos e responder a incidentes.

Os dois mais importantes para defesa de ambientes digitais (inclusive em nuvem) são:

⸻

🔹 1. NIST Cybersecurity Framework (NIST CSF)

Criado em 2014, atualizado em 2018 e com nova versão (CSF 2.0) em 2024.
É baseado em funções centrais que estruturam a segurança:
	1.	Identify (Identificar)
	•	Mapear ativos, riscos e dependências.
	•	Ex.: inventário de recursos na nuvem, classificação de dados.
	2.	Protect (Proteger)
	•	Implementar controles preventivos.
	•	Ex.: criptografia, controle de acessos (IAM), firewall, MFA.
	3.	Detect (Detectar)
	•	Monitorar atividades e identificar anomalias.
	•	Ex.: SIEM, logs de auditoria, UEBA, alertas de tráfego suspeito.
	4.	Respond (Responder)
	•	Ter planos de resposta a incidentes.
	•	Ex.: playbooks, contenção de ataques, comunicação em crise.
	5.	Recover (Recuperar)
	•	Restaurar operações após incidentes.
	•	Ex.: backups, disaster recovery, resiliência operacional.

➡️ Esse ciclo é contínuo e deve ser aplicado tanto em data centers tradicionais quanto em cloud.

⸻

🔹 2. NIST 800-53 e 800-171

São catálogos de controles de segurança que detalham o como implementar segurança:
	•	NIST SP 800-53: controles para sistemas de informação federais e críticos.
	•	NIST SP 800-171: proteção de informações sensíveis em empresas privadas que trabalham com o governo.

Exemplos de controles:
	•	Gerenciamento de identidades.
	•	Proteção criptográfica.
	•	Monitoramento de atividades.
	•	Resposta e recuperação.

⸻

🔹 3. NIST em Nuvem

O NIST também publicou documentos específicos para cloud computing (ex.: NIST SP 500-292, NIST SP 800-144).
	•	Define características essenciais da nuvem (elasticidade, self-service, multitenancy).
	•	Aponta modelos de implantação (IaaS, PaaS, SaaS; nuvem pública, privada, híbrida, comunitária).
	•	Destaca riscos e recomendações de segurança, como:
	•	Responsabilidade compartilhada.
	•	Segurança de APIs.
	•	Isolamento de workloads.
	•	Proteção de dados em trânsito e repouso.

⸻

✅ Resumo:
A metodologia NIST ajuda a estruturar a governança de segurança em qualquer ambiente, incluindo cloud, trazendo:
	•	Framework (CSF): visão estratégica e ciclo de segurança.
	•	Controles (800-53, 800-171): medidas técnicas e operacionais.
	•	Guias cloud (SP 500 e 800): práticas específicas para ambientes em nuvem.