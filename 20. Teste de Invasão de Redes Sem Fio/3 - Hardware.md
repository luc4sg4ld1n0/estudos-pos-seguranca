# Hardware

1) Adaptadores USB Wi-Fi (com suporte a monitor mode e packet injection)

Úteis para captura de frames 802.11, análises com Wireshark/aircrack-ng e para operar ferramentas de auditoria em Linux.
	•	Exemplos populares/úteis para laboratórios: adaptadores com chipsets Atheros/Realtek/RT3070/RTL8812AU (verifique suporte a monitor mode / injection na distro que usar). Um adaptador barato muito citado é o TP-Link TL-WN722N (atenção: versões do hardware têm chipsets diferentes — verifique a revisão).

2) Dispositivos especializados para auditoria Wi-Fi (frameworks / appliances)

São equipamentos prontos para operações de avaliação, detecção de rogue APs, captura e automação de testes — ótimos para aprendizado e demonstrações em ambiente autorizado.
	•	Ex.: WiFi Pineapple (Hak5) — plataforma focada em avaliação de segurança Wi-Fi, captive portals, rogue APs e avaliações em laboratório. Use apenas em redes que você tem permissão para testar.

3) Rádio definido por software (SDR)

Permite analisar/emitir sinais em ampla faixa (útil para pesquisa de espectro, experimentos com sinais e em alguns casos para entender interferência/radar). Requer conhecimento avançado e atenção regulatória (transmissão em bandas restritas pode ser ilegal).
	•	Ex.: HackRF One (SDR 1 MHz–6 GHz) — bom para experimentação de espectro e pesquisa.

4) Placas SBC / mini-computadores (para montar APs, sniffers, servidores RADIUS, controladoras)

Raspberry Pi e similares são excelentes para laboratórios portáteis (rodar hostapd, rádios USB, servidores RADIUS, captura em campo).
	•	Ex.: Raspberry Pi 4 — baixo custo, várias interfaces USB/Ethernet; comum em labs portáteis.

5) Access Points profissionais / empresariais (para testes de configuração/firmware)

Ter APs comerciais idênticos aos que o cliente usa permite reproduzir problemas de configuração, testar hardening e atualizações de firmware.
	•	Marcas/linhas populares: Ubiquiti UniFi, Cisco, Aruba, Ruckus — por exemplo Ubiquiti UniFi (modelos como UniFi 6 Lite/Pro/7) são comuns em pequenas/ médias infraestruturas.

6) Antenas (omnidirecionais e direcionais)

Melhoram alcance e permitem testes de cobertura/sinal. Antenas direcionais (yagi/panel) são úteis para focar sinais em auditorias de cobertura e isolamento.

7) Analisadores de espectro / sondas USB

Para diagnosticar interferência, sobreposição de canais e problemas RF (produtos dedicados ou dongles SDR com software). São dispositivos importantes ao investigar problemas de qualidade de serviço.

8) Ferramentas para IoT / rádio sub-GHz

Se a auditoria envolver dispositivos IoT que usam 433/868/915 MHz, ferramentas como Yardstick One e SDRs ajudam a analisar esses protocolos (atenção às regras de transmissão).

9) Baterias portáteis, cases e equipamentos de campo

Power banks, cases resistentes, cabos USB-Ethernet, adaptadores e um bom notebook com Linux (Kali/Parrot/Ubuntu) completam o kit de campo.

⸻

Recomendações práticas de compra e compatibilidade
	•	Verifique chipset e versão de hardware: alguns modelos mudam o chipset entre revisões (ex.: adaptadores TP-Link/Alfa) — isso altera se têm monitor mode e packet injection no Linux. Sempre confira a revisão/hardware ID antes de comprar.
	•	Compatibilidade com drivers: prefira adaptadores com suporte conhecido em Linux (Atheros/ath9k, ath10k, rt2800, rtl8812au com drivers estáveis).
	•	SDR e transmissão: usar SDRs para transmitir requer conhecimento de espectro e conformidade legal — em muitos países transmitir em certas frequências sem licença é ilegal.
	•	Firmware e updates: ao comprar APs para testes, mantenha firmwares atualizados e prefira modelos que suportem modos de gestão seguros (HTTPS, SSH, 802.1X).

⸻

Kit mínimo sugerido para começar (lab controlado / portável)
	1.	Notebook com Linux (Kali/Ubuntu), 8+ GB RAM.
	2.	1–2 adaptadores USB Wi-Fi com suporte a monitor/injection (diferentes chipsets).
	3.	Raspberry Pi 4 (ou similar) para montar serviços de laboratório (RADIUS, AP, sniffers).
	4.	Uma WiFi Pineapple ou dispositivo equivalente para entender fluxo de ferramentas (apenas em testes autorizados).
	5.	Uma SDR básica (opcional, para estudar espectro) — ex.: HackRF One, se for estudar sinais RF mais a fundo.
	6.	Cabos, power bank, antenas extra e um AP comercial (Ubiquiti/Cisco/Aruba) para testes de configuração.
