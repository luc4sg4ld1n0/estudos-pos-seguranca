# Baiting

Baiting é uma técnica de engenharia social em que o atacante oferece “isones” — algo atraente ou curioso — para induzir a vítima a executar uma ação que comprometa segurança (p. ex. conectar um dispositivo, baixar um arquivo, fornecer credenciais). A isca explora curiosidade, ganância, ou a mentalidade de “é só um clique rápido”.

Tipos comuns (alto nível)
	•	Físico: pen drives, CDs, ou outros objetos “perdidos” deixados onde funcionários os encontrem.
	•	Digital: ofertas de downloads grátis (software crackeado, filmes, músicas), anúncios “imperdíveis”, ou arquivos aparentemente legítimos em sites/links.
	•	Social/Promoção falsa: cupons, brindes ou concursos que exigem cadastro com dados sensíveis.

Importante: estou omitindo detalhes operacionais que ajudariam a realizar um ataque. Aqui o foco é defesa.

Por que funciona (psicologia)
	•	Curiosidade (“o que tem nesse pen drive?”).
	•	Ganância/oferta irresistível (“50% off só hoje!”).
	•	Pressa/urgência (“baixe antes que acabe”).
	•	Confiança na aparência (marca falsa, layout profissional).

Indicadores de baiting (sinais para ficar atento)
	•	Objetos inesperados em áreas comuns (pen drives, CDs).
	•	Arquivos anexos com nomes muito atrativos ou ambíguos.
	•	Ofertas que pedem instalação de software ou execução de arquivos executáveis.
	•	Links curtos/encurtadores em e-mails que prometem conteúdo “exclusivo”.
	•	Pedidos para inserir mídias físicas em computadores corporativos.

Como se proteger (controles práticos — defensivos)
	1.	Política de mídia removível: proibir ou limitar o uso de USBs pessoais; fornecer meios aprovados para transferência de arquivos.
	2.	Desativar execução automática (autorun/autoexecute) em estações de trabalho.
	3.	Endpoint protection + DLP: impedir execução de executáveis a partir de mídias externas e bloquear transferência de dados sensíveis.
	4.	Bloqueio de sites/filtragem de downloads e análise de arquivos por sandbox antes de desembarcar na rede.
	5.	Inventário e controle de endpoints: gerenciar dispositivos autorizados (MDM/EDR).
	6.	Treinamento regular: exercícios de conscientização sobre iscas físicas e digitais.
	7.	Canais claros para reportar achados: “encontrei um pen drive — e agora?” deve ter resposta e processo.
	8.	Física: câmeras/segurança e patrulha para áreas críticas (reduz chance de “pen drives perdidos” serem deixados).
	9.	Segregação de ambientes: máquinas isoladas (air-gapped) para lidar com mídias externas quando necessário.
	10.	Backups e planejamento de resposta: para limitar impacto caso algo malicioso seja executado.

Detecção e investigação (o que observar nos logs)
	•	Eventos de montagem de mídia USB em host incomum.
	•	Novos processos iniciados a partir de caminhos “removíveis”.
	•	Transferências de dados incomuns logo após inserção de mídia.
	•	Alerta de sandbox/antivírus sobre arquivos recém-acessados.
	•	Acesso a sites de compartilhamento/download logo após clique em isca.

Como responder a um incidente de baiting (resumo)
	1.	Isolar o host imediatamente (rede/product).
	2.	Desconectar mídias removíveis e preservá-las para análise forense.
	3.	Coletar logs e imagens de disco se suspeita de comprometimento.
	4.	Rodar análise em ambiente controlado/sandbox.
	5.	Restaurar a partir de backup limpo se necessário.
	6.	Comunicar partes interessadas e atualizar políticas/treinamentos com a lição aprendida.

Ideias seguras para exercícios de conscientização (treinamentos)
	•	Tabletop: apresentar um cenário (pen drive encontrado) e pedir que a equipe descreva passos corretos.
	•	Quiz interativo com exemplos de e-mails/ofertas e perguntas “o que você faria?” (sem enviar iscas reais que causem dano).
	•	Campanha de comunicação: cartazes e lembretes sobre não inserir mídias desconhecidas e como reportar.
	•	Simulações controladas digitais: campanhas de phishing educativas que não coletam senhas (apenas mostram ensino) — sempre com consentimento/limites do RH e jurídico.