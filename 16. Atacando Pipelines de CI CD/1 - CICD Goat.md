# CI/CD Goat

O CI/CD Goat (do repositório cider‑security‑research/cicd‑goat) é um ambiente de aprendizado deliberadamente vulnerável, criado para treinar profissionais em segurança de pipelines CI/CD 🐐  ￼.

⸻

🛠 O que é e como funciona
	•	É um projeto open‑source (licença Apache‑2.0), mantido pela Cider Security (agora parte da Palo Alto Networks)  ￼.
	•	Executa uma infraestrutura realística usando containers Docker, incluindo:
	•	Gitea, Jenkins (controller + agent), LocalStack, GitLab, GitLab‑Runner, ambiente “Prod” com Docker‑in‑Docker e CTFd  ￼.
	•	Oferece 10–11 desafios (CTF), cada um representando vulnerabilidades reais – como PPE (Poisoned Pipeline Execution), abuso da cadeia de dependências, PBAC, controle de fluxo insuficiente etc.  ￼.

⸻

🚩 Exemplos de desafios
	•	Caterpillar (PPE via Pull Request): permite injetar código malicioso num Jenkinsfile via PR, resultando em vazamento de segredos e escalonamento de acesso  ￼.
	•	Cheshire‑cat (execução no Controller): mostra como escapar do agente e executar código diretamente no servidor Jenkins, onde estão os segredos mais sensíveis  ￼.

⸻

🎯 Para que serve
	1.	Educação prática: ensina os 10 principais riscos de segurança em CI/CD, conforme OWASP. Ideal para DevOps, Security Engineers e profissionais de infraestrutura  ￼.
	2.	Simulações realísticas: trata-se de um ambiente completo e configurável, reproduzindo pipelines reais executadas localmente.
	3.	Cultura DevSecOps: estimula a adoção de boas práticas como:
	•	revisão de pipeline,
	•	controle de branches,
	•	isolamento de agentes/contêineres,
	•	privilégios mínimos,
	•	sandboxing e autenticação de fontes de código.

⸻

Como começar
	1.	Baixe o docker-compose.yaml do GitHub:

curl -o cicd‑goat/docker‑compose.yaml --create-dirs \
  https://raw.githubusercontent.com/cider‑security‑research/cicd‑goat/main/docker-compose.yaml
cd cicd-goat && docker compose up -d


	2.	Aguarde até ~5 minutos para todos os serviços subirem.
	3.	Acesse o CTFd (localhost:8000):
	•	user/senha: alice/alice
	4.	Use as credenciais indicadas para acessar Jenkins, Gitea e GitLab e inicie os desafios  ￼ ￼ ￼.

⸻

🗣 Comunidade

Reações no Reddit mostram empolgação pela iniciativa:

“Interesting idea … security is often an after thought in CI/CD itself.”  ￼
“goated thing man, thank you!”  ￼

⸻

✅ Conclusão

O CI/CD Goat é um laboratório prático e didático para quem quer entender e mitigar ameaças a pipelines CI/CD. Ele coloca você na posição do atacante — e isso é excelente para internalizar a importância de boas práticas de segurança em pipelines de integração e entrega contínua.