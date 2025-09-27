# WiGLE

WiGLE (Wireless Geographic Logging Engine) é uma base de dados colaborativa que mapeia pontos de acesso Wi-Fi (SSID, BSSID/MAC, tipo de encriptação, coordenadas GPS, etc.). Usuários podem subir observações (via app Android, cliente ou uploads) e depois consultar o banco para procurar APs por localização, BSSID ou SSID. É amplamente usado por pesquisadores, entusiastas de wardriving e profissionais de segurança para análise e visualização de cobertura Wi-Fi.  ￼

Como isso é útil em pentests / OSINT
	•	Reconhecimento/Correlações: permite confirmar a existência e localização aproximada de APs vistos durante um reconhecimento passivo (ouvidos em campo) e correlacioná-los com outras informações.  ￼
	•	Verificação de inventário: ver se o cliente tem APs divulgados em locais inesperados (ex.: equipamentos fora do prédio).
	•	Pesquisa de histórico: ver quando e onde um BSSID foi observado (pode revelar mobilidade/distribuição).
	•	Integração programática: há APIs que permitem consultas automatizadas (necessário registro e limites de uso).  ￼

Observação importante: WiGLE fornece dados de observação pública (o AP transmitiu informações radiadas). Ele não é uma lista de redes “para invadir” — o uso deve ser sempre autorizado e ético.

Limites, termos e práticas de uso (o que você precisa saber)
	•	Acesso e API: muitos endpoints/funcionalidades exigem conta e chave/API; há limites de requisições diárias e regras de uso. Consulte a documentação/terms antes de automatizar consultas.  ￼
	•	Cobertura e qualidade dos dados: a base é crowd-sourced — densidade e precisão variam por região; há duplicatas e erros ocasionais.  ￼
	•	Privacidade e remoção: WiGLE tem procedimentos para remoção/opt-out — proprietários podem pedir remoção de um registro (existem contatos/admins e pedidos via e-mail descritos por comunidades/guia). Se você encontrar um AP do seu cliente ou da sua casa, há formas de solicitar remoção.  ￼
	•	Legalidade / ética: usar dados para perseguir/assediar, para invasão ou sem autorização pode ter implicações legais. Em pentests, inclua WiGLE no escopo do teste e documente a fonte das evidências.

Preocupações práticas de privacidade
	•	Mesmo que o SSID/BSSID sejam públicos por natureza do rádio, a agregação em bases como o WiGLE torna mais fácil localizar e rastrear infraestruturas (e, em alguns cenários, padrões de movimento). Por isso muitos administradores optam por pedir remoção ou por reduzir a exposição (hardening, SSID genérico, segmentação).  ￼

Alternativas e fontes complementares
	•	OpenCellID — base aberta para antenas/cell towers (útil para geolocalização celular).  ￼
	•	Mozilla Location Service (MLS) — era um serviço crowdsourced de geolocalização por Wi-Fi/cell; foi descontinuado/retirado (importante saber ao escolher fontes). (nota histórica).  ￼

Como usar o WiGLE de forma responsável numa auditoria (boas práticas)
	1.	Defina o escopo por escrito: incluir consultas a bases públicas (WiGLE) como fonte de reconhecimento.
	2.	Registre evidências: guarde prints/queries/horários e vincule-os ao escopo do cliente.
	3.	Não execute ataques baseados apenas em dados de bases públicas sem autorização explícita.
	4.	Respeite limites de API e os termos de uso (evite scraping massivo sem permissão).  ￼
	5.	Ao encontrar dados sensíveis (ex.: BSSID associado a endereço residencial), sugira remoção/contato ao proprietário e documente o pedido de remoção se apropriado.