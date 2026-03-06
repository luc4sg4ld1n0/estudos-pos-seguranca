# DOM-based XSS

DOM-based XSS é um tipo de Cross-Site Scripting em que a vulnerabilidade acontece no lado do navegador (client-side), manipulando o DOM (Document Object Model) com dados não confiáveis. 🌐⚠️

Esse tipo de falha também é tratado nas recomendações da OWASP e aparece nas categorias do OWASP Top 10.

⸻

O que é DOM

O DOM (Document Object Model) é a estrutura que representa a página HTML no navegador.

JavaScript usa o DOM para:
	•	alterar conteúdo da página
	•	ler parâmetros da URL
	•	modificar elementos HTML
	•	criar novos elementos

Quando dados vindos do usuário entram no DOM sem validação, pode surgir um DOM-based XSS.

⸻

Como funciona o DOM-based XSS

Diferente de outros XSS, o servidor não está envolvido diretamente.

Fluxo simplificado:
	1.	O usuário abre uma URL manipulada
	2.	O JavaScript da página lê dados da URL
	3.	O script insere esses dados no DOM sem sanitização
	4.	O navegador executa o código malicioso

Exemplo de fonte de dados perigosos:
	•	location.hash
	•	location.search
	•	document.referrer
	•	window.name

⸻

Exemplo simplificado

Código vulnerável:

var name = location.hash;
document.getElementById("output").innerHTML = name;

Se alguém acessar:

site.com/#<script>alert(1)</script>

O script pode ser executado porque foi inserido diretamente no innerHTML.

⸻

Principais “sources” e “sinks”

Em segurança web, DOM-XSS costuma ser analisado com dois conceitos:

Sources (fontes de dados controlados pelo usuário)
	•	location
	•	document.URL
	•	document.referrer
	•	window.name

Sinks (locais perigosos onde o dado é inserido)
	•	innerHTML
	•	outerHTML
	•	document.write
	•	eval()
	•	setTimeout(string)

Quando source → sink sem validação, pode ocorrer DOM-XSS.

⸻

Como prevenir DOM-based XSS

Boas práticas:
	•	evitar innerHTML com dados do usuário
	•	usar textContent em vez de HTML
	•	validar e sanitizar dados
	•	aplicar Content Security Policy (CSP)
	•	usar bibliotecas de sanitização

⸻

Ferramentas usadas para detectar

Profissionais de segurança usam ferramentas como:
	•	Burp Suite
	•	OWASP ZAP