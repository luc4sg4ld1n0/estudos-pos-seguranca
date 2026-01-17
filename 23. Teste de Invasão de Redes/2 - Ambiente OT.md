# Ambiente OT

Testes de Invasão em Ambiente OT

O que é OT

OT engloba sistemas que controlam processos físicos, como:
	•	SCADA
	•	PLCs
	•	DCS
	•	RTUs
	•	IEDs
	•	HMIs

Usados em:
	•	Indústrias
	•	Energia
	•	Saneamento
	•	Óleo & gás
	•	Manufatura
	•	Transporte

⸻

Por que pentest em OT é crítico (e delicado)

Diferente de TI:
	•	❌ Não pode causar parada de produção
	•	❌ Não pode reiniciar dispositivos
	•	❌ Não pode gerar falhas físicas
	•	✅ Segurança humana vem antes da segurança da informação

Um teste mal conduzido pode:
	•	Parar uma planta
	•	Danificar equipamentos
	•	Gerar risco à vida

⸻

Princípios fundamentais em OT

Antes de qualquer teste:
	•	Segurança > Disponibilidade > Confidencialidade
	•	Testes majoritariamente passivos
	•	Exploração extremamente limitada ou simulada
	•	Aprovação formal de engenharia e operação

⸻

Tipos de avaliação em OT

Na prática, muitas organizações não fazem pentest agressivo, mas sim:

1. Avaliação de Segurança OT (mais comum)
	•	Análise de arquitetura
	•	Revisão de segmentação IT/OT
	•	Avaliação de firewalls industriais
	•	Verificação de acessos remotos
	•	Análise de hardening de PLCs e HMIs

2. Pentest OT Controlado

Quando permitido:
	•	Testes somente em janelas de manutenção
	•	Preferência por ambientes de teste ou simuladores
	•	Exploração lógica, não destrutiva

⸻

Escopo típico de um teste OT
	•	Zonas e conduítes (modelo Purdue)
	•	Comunicação entre IT ↔ OT
	•	Acesso remoto de fornecedores
	•	Credenciais fracas ou compartilhadas
	•	Protocolos industriais inseguros
	•	Falta de monitoramento

⸻

Principais riscos identificados em OT
	•	Redes planas (sem segmentação)
	•	Protocolos sem autenticação ou criptografia
	•	PLCs expostos
	•	Acesso remoto sem MFA
	•	Sistemas legados sem patch
	•	Dependência excessiva de fornecedores externos

⸻

Protocolos industriais comuns
	•	Modbus
	•	DNP3
	•	PROFINET
	•	EtherNet/IP
	•	OPC Classic / OPC UA
	•	IEC 61850

(Muitos foram criados sem segurança por design)

⸻

Normas e frameworks usados

Essenciais em OT:
	•	IEC 62443 (principal referência)
	•	NIST SP 800-82
	•	ISA/IEC
	•	MITRE ATT&CK for ICS
	•	ISO 27001 (adaptada para OT)

⸻

Diferença entre Pentest TI x OT

TI	OT
Exploração ativa	Análise passiva
Reboot aceitável	Reboot crítico
Patch frequente	Patch raro
CIA	Segurança física primeiro


⸻

Relatório em OT

Deve focar em:
	•	Impacto operacional
	•	Risco à segurança física
	•	Possibilidade de interrupção
	•	Recomendações realistas
	•	Priorização baseada em criticidade do processo

⸻

Ferramentas (uso controlado)

Em OT, ferramentas são usadas com extrema cautela, muitas vezes apenas para:
	•	Descoberta passiva
	•	Análise de tráfego
	•	Revisão de configurações

(Nunca scans agressivos sem autorização explícita)

⸻

Boas práticas essenciais
	•	Criar ambiente de teste OT
	•	Segmentar por zonas e conduítes
	•	Monitoramento contínuo OT
	•	Gestão de acessos remotos
	•	Inventário completo de ativos
	•	Treinamento conjunto TI + Engenharia