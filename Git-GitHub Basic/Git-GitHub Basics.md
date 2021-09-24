# Git Basic
* Instalar o [Git](https://git-scm.com/downloads)
## Configurações iniciais (apenas na instalação):
* Configurar as informações do usuário global do sistema de versionamento.
	```
	$ git config --global user.name "Your Name Comes Here"
	$ git config --global user.email you@yourdomain.example.com
	```
## Começando a versionar um projeto:
* Incluir a pasta do projeto no sistema de versionamento;
	```
	/* Navegar até a pasta do projeto e usar o comando dentro do diretorio */
	$ cd projeto
	$ git init
	```
* Colocar ou criar os primeiros arquivos dentro da pasta do projeto e depois adicionar esses arquivos ao repositorio;
	```
	$ git add file1 file2 file3
	```
* Para adicionar todos os arquivos da pasta do projeto no controle de versão
	```
	$ git add .
	```
* Checar o que foi incluído em "stage" pronto para "commit"
	```
	$ git status
	```
* Caso já exista algum arquivo, podemos checar se existem diferenças entre os arquivos em "stage" e os arquivos já existentes no repositorio
	```
	$ git diff --cached
	```
	NOTA: Se usarmos o `$ git diff` a diferença seria apenas entre os arquivos já no repositório.

## Criando conteúdo e manipulando o repositório
Quando iniciamos um repositório, ele normalmente será a branch `main` ou `master`.
Podemos criar uma nova branch para efetuar modificações ou testar algo diferente antes de aplicar à `main`.

* Para listar as brunchs existentes
	```
	$ git branch
	```
* Para criar nova branch
	```
	$ git branch novaBrunch
	```
* Para mudar de uma branch para outra
	```
	$ git switch novaBrunch
	```
	Podemos efetuar todas as modificações nos arquivos da novaBrunch, sem impacto para a main.
	Precisamos realizar o commit da novaBrunch para reter essas mudanças.
	Caso desejemos, podemos aplicar essas mudanças a brunch principal (main).
* Mesclar uma branch com a principal (main)
	```
	$ git merge novaBrunch
	```
* Se algum aviso de inconscistência aparecer, podemos avaliar usando diff
	```
	$ git diff
	```
* Após resolver os conflitos e realizar o merge com sucesso, é necessário dar o commit
	```
	$ git commit -a
	```
	NOTA: Com a opção -a não é necessário adicionar os arquivos em stage para depois realixar o commit.
	Essa opção pressupõe que tudo deve ser adicionado (arquivos novos e modificados) e o commit realizado.
* Visualizar graficamente as brunchs e as modificações realizadas
	```
	$ gitk
	```
* Após o merge, a novaBrunch pode ser apagada, pois suas mudanças já foram incorporadas a main
	```
	$ git branch -d novaBrunch
	```
