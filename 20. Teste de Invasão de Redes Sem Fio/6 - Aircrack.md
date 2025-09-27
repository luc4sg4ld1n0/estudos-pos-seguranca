# Aircrack

Aircrack-ng é um conjunto de ferramentas para análise e auditoria de redes 802.11: captura, análise de tráfego e ferramentas que, em ambiente autorizado, ajudam a testar a robustez de proteções (WEP/WPA/WPA2). É muito usado em laboratórios, educação e pentests autorizados.

⸻

Componentes principais do suite (alto nível)
	•	Sniffer / captura: ferramentas para capturar frames 802.11 (monitor mode).
	•	Análise de tráfego: analisar handshakes, beacons e outros tipos de frames.
	•	Cracking (offline): módulos que, dado um conjunto autorizado de evidências (ex.: handshake capturado em ambiente controlado), ajudam a avaliar se a senha/PSK é fraca (força bruta/dicionário).
	•	Ferramentas auxiliares: conversão de formatos, estatísticas, replay e análise de IVs (no caso de WEP).

(Obs.: nomes específicos das ferramentas fazem parte do pacote, mas não citarei comandos nem parâmetros operacionais.)

⸻

Para que é usado legitimamente em pentests
	•	Verificação de força de senhas PSK — avaliar se uma PSK é brutalmente fraca quando testada com autorização.
	•	Validação de padrões antigos — demonstrar que WEP/TKIP ou implementações antigas são inseguros.
	•	Treinamento e laboratório — ensino de conceitos de handshake, reautenticação e captura de métricas.
	•	Corroboração de achados — quando autorizado, usar evidências capturadas para demonstrar risco (ex.: mostrar que um handshake capturado permitiu confirmar/avaliar a força de uma chave).

⸻

Limitações e pontos importantes
	•	Necessita evidências prévias (captura válida) para qualquer avaliação offline — sem uma captura legítima não há base técnica.
	•	Não substitui auditoria de configuração (WPA3, 802.1X, RADIUS mal configurado, segmentação etc. exigem avaliação além de tentativa de quebra de chave).
	•	Sucesso depende de fatores: qualidade da captura, força da senha, modo de autenticação (SAE x PSK, Enterprise vs Personal), e características do ambiente.
	•	Ferramentas e métodos são legais apenas com autorização escrita — limitação absoluta.

⸻

Riscos legais / éticos
	•	Usar qualquer ferramenta do suite fora de escopo/autorização é crime em muitos países (interferência, invasão, interceptação).
	•	Em contratos: obter autorização por escrito, definir escopo, janelas, limites de impacto, e comunicar stakeholders operacionais.

⸻

Como defender / mitigar (o que verificar no cliente)
	•	Evitar PSK fraco: migrar para WPA3-Personal (SAE) ou, idealmente, WPA2/WPA3-Enterprise com EAP-TLS.
	•	Desativar WEP/TKIP e modos legados.
	•	Habilitar PMF (802.11w) para proteger frames de gerenciamento.
	•	Segmentação e isolamento (guest/IoT/LAN).
	•	Proteção do servidor RADIUS: certificados válidos, políticas de expiração, monitoramento.
	•	Política de senhas: senhas longas/aleatórias para PSK ou autenticação por certificados.
	•	Monitoramento e WIDS/WIPS: detectar captura/anomalias, spikes de handshake/floods, rogue APs.
	•	Patching/firmware: aplicar correções (ex.: vulnerabilidades históricas como KRACK).

⸻

Sinais de que alguém pode estar tentando usar ferramentas tipo Aircrack-ng
	•	Capturas/handshakes desconhecidos registrados por sensores (handshake completo aparecer fora da janela esperada).
	•	Picos no número de re-associações, retries e retransmissões nos APs.
	•	Usuários reclamando de desconexões coincidentes com atividade de pessoas em áreas específicas (wardriving).
	•	Alerts do WIDS/WIPS para sniffers, promiscuous mode devices, ou tráfego anômalo em determinado canal/SSID.

⸻

O que documentar / coletar para um relatório (quando a atividade foi autorizada)
	•	Resumo executivo: risco e impacto.
	•	Escopo e autorização (incluindo janelas horárias).
	•	Evidência técnica: picos de eventos, logs do AP/controladora, capturas (armazenadas com segurança), e correlação temporal.
	•	Método (alto nível): explicar que ferramentas de captura/avaliação foram usadas — sem comandos operacionais.
	•	Resultados: se a senha foi considerada fraca (evidência), vulnerabilidades configuracionais e recomendações prioritárias.
	•	Plano de mitigação e verificação pós-correção.

⸻

Laboratório e aprendizado seguro
	•	Monte um ambiente isolado com APs de teste, clientes e um servidor RADIUS local para reproduzir cenários.
	•	Use máquinas virtuais, Raspberry Pis, ou APs desmontáveis; não teste em redes de produção.
	•	Sempre registre autorização e mantenha backups/configs para rollback.