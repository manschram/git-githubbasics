# Git Basic
* Instalar o [Git](https://git-scm.com/downloads)
## Configurações iniciais (apenas na instalação):
* Configurar as informações do usuário global do sistema de versionamento.
	´´´
	$ git config --global user.name "Your Name Comes Here"
	$ git config --global user.email you@yourdomain.example.com
	´´´
## Começando a versionar um projeto:
* Incluir a pasta do projeto no sistema de versionamento;
	```
	/* Navegar até a pasta do projeto e usar o comando dentro do diretorio */
	$ cd projeto
	$ git init
* Colocar ou criar os primeiros arquivos dentro da pasta do projeto;
* Adicionar todos os arquivos da pasta do projeto no controle de versão
	```
	$ git add .
	```