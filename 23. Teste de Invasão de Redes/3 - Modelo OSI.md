# Modelo OSI

O Modelo OSI (Open Systems Interconnection) é um modelo conceitual que divide a comunicação de redes em 7 camadas, facilitando o entendimento, o projeto e a análise de segurança, inclusive em ambientes OT.

⸻

Modelo OSI – Visão Geral

O objetivo do modelo OSI é padronizar a comunicação, separando responsabilidades por camada.

7 ─ Aplicação
6 ─ Apresentação
5 ─ Sessão
4 ─ Transporte
3 ─ Rede
2 ─ Enlace de Dados
1 ─ Física


⸻

As 7 camadas do Modelo OSI

Camada 7 – Aplicação

Onde os sistemas interagem com o usuário ou processos.

Exemplos:
	•	HTTP / HTTPS
	•	FTP
	•	SMTP
	•	Protocolos OT: Modbus TCP, DNP3, OPC UA, EtherNet/IP

Riscos comuns:
	•	Falta de autenticação
	•	Comandos não validados
	•	Protocolos industriais sem criptografia

⸻

Camada 6 – Apresentação

Responsável por formatação, criptografia e compressão.

Exemplos:
	•	TLS / SSL
	•	Codificação de dados

Em OT:
	•	Muitos protocolos não usam criptografia
	•	Dados trafegam em texto claro

⸻

Camada 5 – Sessão

Gerencia sessões de comunicação.

Exemplos:
	•	RPC
	•	NetBIOS Session

Riscos:
	•	Sessões persistentes sem controle
	•	Falta de timeout

⸻

Camada 4 – Transporte

Responsável por confiabilidade e controle de fluxo.

Exemplos:
	•	TCP
	•	UDP

OT:
	•	Muitos sistemas usam TCP sem segurança
	•	UDP para baixa latência (mais difícil de controlar)

⸻

Camada 3 – Rede

Responsável por endereçamento e roteamento.

Exemplos:
	•	IP
	•	ICMP
	•	IPsec

Riscos:
	•	Falta de segmentação
	•	Rotas diretas entre IT e OT

⸻

Camada 2 – Enlace de Dados

Cuida da comunicação local e endereçamento MAC.

Exemplos:
	•	Ethernet
	•	ARP
	•	VLANs

OT:
	•	Redes planas
	•	Pouco uso de VLANs
	•	ARP spoofing possível

⸻

Camada 1 – Física

Transmissão dos sinais elétricos, ópticos ou rádio.

Exemplos:
	•	Cabos Ethernet
	•	Fibra óptica
	•	Rádio industrial

Riscos OT:
	•	Acesso físico não controlado
	•	Portas expostas em painéis

⸻

Modelo OSI aplicado à segurança OT

Camada	Exemplo de risco em OT
7	Comandos não autenticados para PLC
6	Dados industriais sem criptografia
5	Sessões eternas em HMIs
4	TCP sem inspeção
3	Falta de segmentação
2	Rede industrial plana
1	Acesso físico aos painéis


⸻

Por que o OSI é importante em OT
	•	Ajuda a mapear vulnerabilidades
	•	Facilita comunicação entre TI e Engenharia
	•	Permite definir controles por camada
	•	Base para firewalls industriais e IDS OT

⸻

Exemplo prático (OT)

👉 Um atacante não precisa explorar todas as camadas:
	•	Acesso físico (Camada 1)
	•	Spoofing ARP (Camada 2)
	•	Envio de comandos Modbus (Camada 7)

Tudo isso sem malware sofisticado.

⸻

Relação OSI × Purdue (OT)
	•	OSI: como os dados se comunicam
	•	Purdue: onde os sistemas estão na arquitetura industrial

Ambos se complementam.