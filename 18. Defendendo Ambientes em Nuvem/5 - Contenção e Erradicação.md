# Contenção e Erradicação

🔹 1. Contenção

Objetivo: limitar o impacto do incidente e impedir que o ataque se espalhe.
Estratégia: “ganhar tempo” para investigar e planejar a erradicação.

Tipos de Contenção
	•	Curto prazo (imediata):
	•	Desconectar sistemas comprometidos da rede.
	•	Bloquear endereços IP/domínios maliciosos.
	•	Desativar credenciais comprometidas.
	•	Ativar regras emergenciais em firewall ou WAF.
	•	Longo prazo (estratégica):
	•	Segmentar a rede.
	•	Redirecionar tráfego malicioso (sinkhole).
	•	Usar ambientes de quarentena.
	•	Aumentar monitoramento em áreas críticas.

📌 Exemplo em nuvem:
	•	Suspender instâncias suspeitas em sandbox para análise.
	•	Restringir IAM roles afetados.
	•	Revogar tokens temporários de sessão.

⸻

🔹 2. Erradicação

Objetivo: remover a causa raiz do incidente e eliminar qualquer persistência.
Estratégia: “limpar a casa” antes de restaurar a normalidade.

Ações comuns
	•	Deletar malware, backdoors e scripts persistentes.
	•	Revogar ou redefinir credenciais comprometidas.
	•	Reinstalar sistemas a partir de imagens confiáveis.
	•	Aplicar patches de vulnerabilidades exploradas.
	•	Ajustar configurações incorretas (ex.: bucket S3 público).

📌 Exemplo em nuvem:
	•	Apagar VMs ou containers comprometidos.
	•	Remover chaves de API expostas no GitHub.
	•	Reconfigurar storage com políticas restritivas.
	•	Aplicar security baseline em IaC (Terraform/CloudFormation).

⸻

🔹 Relação com o ciclo completo

Metodologia (ex. NIST 800-61):
	1.	Preparação
	2.	Detecção e Análise
	3.	Contenção ✅
	4.	Erradicação ✅
	5.	Recuperação
	6.	Lições aprendidas

⸻

✅ Em resumo:
	•	Contenção = impedir a propagação do ataque e proteger o ambiente.
	•	Erradicação = eliminar a ameaça e corrigir a vulnerabilidade raiz.
	•	Ambas são essenciais para minimizar danos e evitar reinfecção.
