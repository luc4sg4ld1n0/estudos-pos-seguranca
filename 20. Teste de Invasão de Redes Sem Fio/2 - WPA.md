# WPA

	•	WPA (WPA1) — substituto emergencial do WEP. Usa TKIP (projeto para compatibilidade com hardware antigo). Hoje está obsoleto e não é seguro.
	•	WPA2 — introduziu AES-CCMP (criptografia forte) e é o padrão amplamente usado por muitos anos. Pode operar em modo Personal (PSK) ou Enterprise (802.1X/EAP).
	•	WPA3 — evolução do WPA2 com melhorias de autenticação (principalmente SAE em modo Personal), proteção contra ataques off-line de dicionário, requisitos mais fortes de criptografia e melhorias para redes abertas (OWE) e para ambientes Enterprise (opção de perfil de segurança de 192 bits).

Principais diferenças técnicas (resumido)
	•	Autenticação
	•	WPA-Personal (WPA/WPA2): PSK (senha compartilhada).
	•	WPA2-Enterprise / WPA3-Enterprise: 802.1X / RADIUS (EAP methods, idealmente EAP-TLS).
	•	WPA3-Personal: SAE (Simultaneous Authentication of Equals) — resistência a ataques off-line.
	•	Criptografia
	•	WPA (WPA1): TKIP (fraco / legado).
	•	WPA2: AES-CCMP (forte).
	•	WPA3: algoritmos mais modernos; suporte a GCMP-256 em modos de alta segurança (e modo 192-bit para necessidades regulatórias).
	•	Proteção de frames de gerenciamento
	•	WPA2 pode ter PMF (802.11w) opcional.
	•	WPA3 espera/encoraja PMF (melhora proteção contra spoofing/disassociation).
	•	Redes abertas
	•	WPA2: redes abertas não cifram tráfego (captive portals comuns).
	•	WPA3: OWE (Opportunistic Wireless Encryption) oferece cifragem individual mesmo em redes sem senha (não autentica, só cifra).
	•	Resistência a ataques de dicionário
	•	WPA2-PSK: vulnerável a ataques off-line se a senha for fraca (captura do handshake + força bruta local).
	•	WPA3-Personal (SAE): evita ataques off-line — o atacante não consegue testar senhas offline facilmente.

Vulnerabilidades e pontos de atenção
	•	WPA (WEP/TKIP): não usar — inseguro e sujeito a quebra rápida.
	•	WPA2 com PSK e senhas fracas: ainda vulnerável a quebra por força bruta / dicionário.
	•	WPA2 Enterprise mal configurado (ex.: EAP-MD5, certificados inválidos, RADIUS mal protegido) pode ser tão fraco quanto PSK.
	•	Transição/WPA2-WPA3 mixed mode: permite compatibilidade, mas pode reduzir segurança se clientes fracos forem permitidos — atenção ao ambiente.
	•	Implementações/firmware: bugs (ex.: KRACK em 2017) mostram que patches/firmware são essenciais.

Boas práticas / recomendações (pronto para auditoria)
	1.	Desativar WPA/WEP/TKIP — não permitir modos legados.
	2.	Preferir WPA3-Personal (SAE) para redes de usuário, quando dispositivos suportarem.
	3.	Para ambientes corporativos, usar WPA2/WPA3-Enterprise com 802.1X e EAP-TLS (certificados) — é a opção mais robusta.
	4.	Habilitar PMF (802.11w) sempre que possível.
	5.	Desabilitar WPS e interfaces de gerenciamento inseguras (HTTP sem TLS, credenciais padrão).
	6.	Forçar senhas longas e únicas se usar PSK; preferir o modelo Enterprise para ambientes sensíveis.
	7.	Isolar a rede guest / IoT (VLANs / políticas de firewall).
	8.	Atualizar firmwares de APs/controladores e aplicar patches de segurança.
	9.	Monitorar e detectar rogue APs / ataques de desautenticação (IDS/IPS Wi-Fi).
	10.	Evitar mixed-mode quando possível; se usar, entender trade-offs e documentar risco residual.

O que checar num pentest/avaliação
	•	Ver se APs aceitam TKIP/WEP ou modos legados.
	•	Ver se PMF está ativado.
	•	Identificar SSIDs em mixed mode (WPA2/WPA3).
	•	Testar se guest está isolado da LAN interna.
	•	Revisar método de autenticação (PSK vs 802.1X), força das senhas/PSKs.
	•	Verificar logs/RADIUS, validade de certificados, proteção do servidor RADIUS.
	•	Conferir configuração de gerenciamento (TLS, ACLs, contas administrativas).