# Aireplay

	•	Aireplay-ng é uma ferramenta de injeção/ataque para redes 802.11 (faz parte do conjunto Aircrack-ng).
	•	Seu propósito técnico: gerar tráfego 802.11 forçado (injetar frames), simulando comportamentos de clientes ou atacantes, para testar a resistência da rede, forçar retransmissões, provocar reautenticações, ou verificar mecanismos de defesa.
	•	Em pentests autorizados é usada para testar deteção, robustez a ataques de desautenticação, comportamento de clientes e respostas de infraestruturas (APs, controladoras).

Principais tipos de ações (descrição de alto nível)
	•	Deauthentication / Disassociation floods — envio massivo de frames que fazem clientes se desconectar; útil para testar detecção e resiliência, mas pode causar indisponibilidade.
	•	Fake authentication — fingir ser um cliente para verificar se um AP exige autenticação adequada.
	•	ARP replay (em ataques que visam recuperar PSK) — em ambientes PSK, certas técnicas de replay sobre ARP podem ajudar a gerar tráfego para capturar handshakes (técnico; não detalhe operacional).
	•	Injection de pacotes — inserir frames de dados/management para testar filtragem, isolamento de clientes, captive portals e comportamento de IDS/IPS.
	•	Rogue/AP emulação — em conjunto com outras ferramentas, enviar frames que simulam um AP (nota: isto já está em área de outras ferramentas, não exclusivamente aireplay).

Reforço: as ações acima, se feitas sem autorização, são interferência em serviço e possivelmente crime. Em um pentest devem constar no escopo e ter janelas e planos de rollback.

Usos legítimos em pentest / laboratório
	•	Verificar se soluções de detecção (WIDS/WIPS) conseguem gerar alertas para deauth floods e rogue APs.
	•	Medir impacto de ataques de desautenticação em clientes críticos dentro de uma janela controlada.
	•	Testar se um AP permite associações não autenticadas (falta de 802.1X / EAP).
	•	Validar políticas de isolamento de guest / cliente-cliente.
	•	Treino em laboratório para equipes de defesa: reconhecer e responder a incidentes.

Riscos e comportamento indesejado
	•	Pode causar interrupção de serviço para usuários e aplicações críticas.
	•	Pode prejudicar dispositivos IoT sensíveis que não recuperam bem de desconexões.
	•	Uso malicioso pode atrair responsabilidade legal (interferência de telecomunicações, invasão, dano a disponibilidade).

Como detectar atividades geradas por ferramentas de injeção (o que procurar)
	•	Aumento súbito de frames de gerenciamento (deauth/disassoc) nos contadores do AP.
	•	Picos de retransmissões e retries e queda no throughput em determinados SSIDs/canais.
	•	Alertas no WIDS/WIPS configurados para detectar floods de deauth, mudanças abruptas de BSSID, APs com múltiplas localizações aparentes.
	•	Logs do controlador/AP mostrando desconexões frequentes de muitos clientes, ou clientes que reportam associações repetidas.
	•	Sensores de rede (sniffers) mostrando muitas frames com mesma razão/assinatura de origem ou padrões de tempo típicos de ferramentas automatizadas.
	•	Correlação com eventos de sistema: problemas de conectividade relatados por usuários no mesmo horário.

Mitigações e recomendações para defesa
	•	Habilitar Protected Management Frames (PMF / 802.11w) — reduz impacto de spoofed deauth/disassoc em ambientes que suportam.
	•	WIDS/WIPS com regras para detectar e alertar sobre deauth floods, rogue APs e anomalias de frame-rate.
	•	Rate-limiting e thresholds no sistema de gestão para reduzir impacto de floods.
	•	Segmentação de rede (guest/IoT/empresa) para limitar blast radius se clientes caírem.
	•	Monitoramento ativo com sensores distribuídos e correlação centralizada (SIEM) para identificar ataques coordenados.
	•	Hardening de APs/controladoras: firmware atualizado, gestão segura, logs confiáveis e retenção adequada de eventos.
	•	Planos de contingência para redes críticas (SLA interno, procedimentos de restauração).
	•	Educação/treino: simular ataques autorizados em janelas controladas para validar playbooks de resposta.

O que incluir no escopo e no relatório quando usar ferramentas como o aireplay
	•	Especificar tipos de testes autorizados (ex.: “testes de desautenticação com limite X, janela de horário Y”).
	•	Indicar medidas de redução de risco (notificar operações, janelas de manutenção, rollback).
	•	Documentar impacto observado (quem foi afetado, duração, logs coletados, mitigação aplicada).
	•	Fornecer recomendações claras de correção e detecção (ex.: habilitar PMF, ajustar thresholds do WIDS).

Laboratório e aprendizado seguro
	•	Monte um lab isolado (APs dedicados, clientes de teste, RADIUS local) para aprender o comportamento das ferramentas sem risco legal.
	•	Use VMs/SBCs (Raspberry Pi), APs configuráveis e sensores para reproduzir cenários e validar detecção.
	•	Pratique somente com autorização por escrito em ambientes reais.