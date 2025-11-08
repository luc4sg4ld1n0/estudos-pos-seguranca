# Dorks

Google dorks = buscas com operadores (ex.: site:, inurl:, filetype:, intitle:) que refinam resultados para tipos de arquivo, caminhos, domínios, títulos etc. Usadas por pesquisadores, jornalistas e também por atores maliciosos para identificar conteúdo público relevante — às vezes conteúdo que não deveria estar público.

⸻

Operadores comuns (conceito — seguros para aprender)
	•	site: — limita a busca a um domínio (ex.: pesquisar apenas dentro de exemplo.com).
	•	filetype: — busca por tipo de arquivo (PDF, DOCX, XLSX).
	•	inurl: — procura termos no URL.
	•	intitle: — procura termos no título da página.
	•	cache: — mostra versão em cache de uma página.

Nota: os nomes dos operadores são ensináveis; não vou combinar esses operadores em consultas que possam localizar dados sensíveis.

⸻

Como atacantes usam dorks (defensivo — para você reconhecer o padrão)
	•	Encontram arquivos de backup, planilhas, ou documentos com credenciais expostas.
	•	Localizam páginas com diretórios indexados (listas de arquivos).
	•	Descobrem endpoints administrativos, painéis, ou relatórios esquecidos.
	•	Reúnem informações públicas para apoio a ataques de engenharia social (ex.: listas de funcionários, organogramas, e-mails).

⸻

Riscos principais
	•	Vazamento de credenciais e documentos sensíveis.
	•	Exposição de endpoints administrativos que facilitam ataques técnicos.
	•	Escalada de impacto por combinação de informações públicas (reconhecimento).

⸻

Medidas de defesa práticas e imediatas
	1.	Inventário e classificação de conteúdo público
	•	Mapeie o que está publicado (sites, buckets S3, repositórios públicos, mirrors).
	•	Classifique o que é sensível e o que é público.
	2.	Remoção ou proteção de artefatos sensíveis
	•	Remova arquivos desnecessários do público.
	•	Mova relatórios/backs para repositórios autenticados.
	•	Controle versionamento (não comitar segredos em repositórios públicos).
	3.	Controle de indexação
	•	Use robots.txt e metatags noindex como complemento, não como única proteção.
	•	Evite expor páginas sensíveis mesmo que noindex esteja presente — trate como defesa em camadas.
	4.	Autenticação e autorização
	•	Painéis administrativos e páginas com dados sensíveis devem estar atrás de autenticação forte e não expostos publicamente.
	•	Desative listagem de diretório no servidor.
	5.	Remoção segura de backups e arquivos antigos
	•	Wipe/destrua backups que não deveriam ficar públicos; revise rotinas de deploy que geram artifact leaks.
	6.	Criptografia e segregação
	•	Criptografe dados sensíveis em repouso; minimize dados em arquivos públicos.
	7.	Políticas e treinamento
	•	Treine desenvolvedores e equipes para não deixarem chaves, senhas ou PII em arquivos públicos.
	•	Revisão de código e pre-commit hooks para impedir commits de segredos.
	8.	Monitoramento e resposta
	•	Monitore logs web e padrões de acesso incomuns (varredura, requisições repetitivas).
	•	Use alertas para tráfego que tenta acessar caminhos administrativos ou muitos downloads em sequência.
	9.	Remediação e processo de remoção de conteúdo
	•	Tenha um processo claro para remover conteúdo indexado (remoção do site + pedido de remoção via Search Console / DMCA quando aplicável).

⸻

Detectando uso malicioso de dorks (o que olhar nos logs)
	•	Padrões: muitos acessos sequenciais a páginas com nomes previsíveis (backup.zip, admin/, wp-admin/).
	•	Picos de tráfego vindo de poucos IPs tentando várias URLs.
	•	Requisições com User-Agent suspeitos ou sem Referer em sequência.
	•	Requisições que solicitam diretamente arquivos estáticos não vinculados por navegação normal.

⸻

Boas práticas para equipes de segurança
	•	Rodar varreduras internas periódicas (scanner de conteúdo público) para descobrir o que está indexado — e corrigir.
	•	Implementar prevenção de exposição automática (CI/CD que remove artefatos sensíveis antes do deploy).
	•	Fazer auditoria de repositórios públicos (GitHub, GitLab) e buckets em nuvem.
	•	Habilitar e revisar alertas do Google Search Console / Bing Webmaster Tools.
	•	Criar playbooks de resposta a descoberta de dados expostos.

⸻

Limites legais e éticos
	•	Usar dorks para encontrar e explorar dados sensíveis sem autorização é ilegal e antiético.
	•	Se você encontrar dados de terceiros por acaso, siga o processo legal/corporativo para notificar e remover — não os utilize.