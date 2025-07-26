# APT

🔍 O que é APT em Segurança da Informação?

APT = Advanced Persistent Threat
Ou seja, Ameaça Persistente Avançada.

✅ Definição:

Um APT é um grupo altamente especializado e bem financiado, geralmente com objetivos políticos, econômicos ou militares, que realiza ataques cibernéticos sofisticados e prolongados contra alvos específicos (empresas, governos, infraestruturas críticas).

⸻

🧠 Características de um APT:

Característica	Explicação
Avançado	Uso de técnicas sofisticadas (0-days, malware personalizado, engenharia social precisa)
Persistente	Invasão dura semanas, meses ou até anos – foco em manter o acesso sem ser detectado
Ameaça real	São grupos humanos (não apenas scripts), com motivação e recursos
Alvo definido	Não são ataques de massa — são altamente direcionados (ex: espionagem industrial)


⸻

🔥 Fases típicas de um ataque APT (kill chain):
	1.	Reconhecimento – coleta de dados públicos (OSINT)
	2.	Engenharia social / Exploração inicial – spear phishing, exploração de falhas
	3.	Instalação de malware – backdoors, trojans personalizados
	4.	C2 (Comando e Controle) – canal seguro de comunicação com o alvo
	5.	Movimentação lateral – escalar privilégios, acessar outros sistemas
	6.	Extração de dados / sabotagem – exfiltração silenciosa ou ataque visível
	7.	Persistência – criar formas de manter o acesso mesmo após resets

⸻

🏴‍☠️ Exemplos reais de grupos APT:

Nome do grupo	Atribuição provável	Famoso por…
APT28 (Fancy Bear)	Rússia (GRU)	Ataques à OTAN, eleições EUA
APT29 (Cozy Bear)	Rússia (SVR)	SolarWinds hack
Lazarus Group	Coreia do Norte	WannaCry, ataques a bancos e cripto
APT10 (Stone Panda)	China	Espionagem industrial global
Charming Kitten	Irã	Phishing contra ativistas e pesquisadores


⸻

🧰 Ferramentas e técnicas usadas por APTs:
	•	Malware customizado (fileless, polimórfico)
	•	Exploitation frameworks (Cobalt Strike, Metasploit, Sliver)
	•	Zero-days (falhas ainda não conhecidas publicamente)
	•	DNS tunneling, tor, proxy chains para C2
	•	Credential dumping com Mimikatz
	•	Living off the land: usam ferramentas nativas (PowerShell, WMI)

⸻

🛡️ Como se proteger de APTs:
	•	Monitoramento contínuo (SIEM, EDR)
	•	Segmentação de rede e controle de acesso
	•	Atualizações e patching constantes
	•	Treinamento contra phishing (ataque mais comum)
	•	Zero Trust e MFA sempre
	•	Análise de comportamento (UEBA)

⸻