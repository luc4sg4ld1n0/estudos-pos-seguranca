# Network Building Blocks

Network Building Blocks são os componentes fundamentais que formam uma rede, servindo como “blocos de construção” para projetar, operar e proteger redes, tanto em TI quanto em OT. Em ambientes industriais, esses blocos precisam priorizar disponibilidade e segurança física.

⸻

Network Building Blocks – Visão Geral

Eles podem ser organizados em camadas lógicas, alinhadas ao Modelo OSI, Modelo Purdue e boas práticas de segurança.

⸻

1. Dispositivos de Rede

🔹 Dispositivos Ativos
	•	Switches (gerenciáveis / industriais)
	•	Roteadores
	•	Firewalls (tradicionais e industriais)
	•	Gateways OT
	•	Access Points industriais

📌 Em OT:
	•	Suporte a temperatura, vibração
	•	Longo ciclo de vida
	•	Firmware raramente atualizado

⸻

2. Meios de Comunicação

🔹 Cabeados
	•	Ethernet (Cat5e, Cat6)
	•	Fibra óptica
	•	Serial (RS-232, RS-485)

🔹 Sem fio
	•	Wi-Fi industrial
	•	Rádio
	•	Cellular (4G/5G industrial)

📌 Risco OT:
	•	Interferência
	•	Falta de criptografia em rádio
	•	Acesso físico fácil

⸻

3. Protocolos de Rede

🔹 Protocolos Gerais
	•	ARP
	•	IP
	•	ICMP
	•	TCP / UDP

🔹 Protocolos Industriais
	•	Modbus TCP
	•	DNP3
	•	PROFINET
	•	EtherNet/IP
	•	OPC UA
	•	IEC 61850

📌 Muitos não possuem segurança nativa.

⸻

4. Endereçamento e Identidade
	•	Endereços IP
	•	Endereços MAC
	•	VLANs
	•	Sub-redes
	•	NAT (em alguns cenários OT)

📌 OT:
	•	IPs estáticos
	•	Pouca visibilidade de ativos
	•	Dispositivos legados sem autenticação forte

⸻

5. Segmentação de Rede
	•	VLANs
	•	Zonas e Conduítes (IEC 62443)
	•	DMZ industrial
	•	Firewalls entre IT ↔ OT

📌 Segmentação é o principal controle de segurança em OT.

⸻

6. Serviços de Rede
	•	DNS
	•	NTP
	•	DHCP (uso limitado em OT)
	•	Active Directory (para HMIs/servidores)

📌 Riscos:
	•	Dependência de serviços de TI
	•	Falta de redundância

⸻

7. Monitoramento e Visibilidade
	•	IDS / IPS
	•	Monitoramento de tráfego OT
	•	Syslog
	•	SNMP

📌 Em OT:
	•	Preferência por monitoramento passivo
	•	Evitar impacto operacional

⸻

8. Controles de Segurança
	•	Firewalls industriais
	•	Whitelisting de protocolos
	•	Controle de acesso remoto
	•	MFA para fornecedores
	•	Jump servers

⸻

9. Redundância e Resiliência
	•	Anéis industriais (MRP, PRP, HSR)
	•	Redundância de links
	•	Failover de dispositivos

📌 Objetivo:
	•	Zero downtime
	•	Alta disponibilidade

⸻

10. Gestão e Governança
	•	Inventário de ativos
	•	Gestão de configuração
	•	Backup de PLCs e switches
	•	Gestão de mudanças (MOC)

⸻

Network Building Blocks em OT (resumo)

Bloco	Importância
Dispositivos	Robustez e longevidade
Protocolos	Segurança limitada
Segmentação	Controle crítico
Monitoramento	Passivo
Redundância	Essencial
Governança	Reduz risco humano


⸻

Relação com Modelos
	•	OSI: função técnica
	•	Purdue: localização na arquitetura
	•	IEC 62443: segurança por zonas