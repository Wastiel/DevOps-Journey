# Introdução a Cultura DevOps

- Instalado o Virtual Box para poder testar e aprender os comandos. 

vboxuser
changeme

# Instrutor Giuseppe Lopes

# O que é DevOps

## Objetivo: 
- [Introdução](https://www.youtube.com/watch?v=L45k6lzCA58&t=88s)
- Entender o que é DevOpes?
- Imcorporar essa culutra no dia a dia
- Quais técnicas podemos usar
- Quais Ferramentas podemos adotar
- Como isso aprimora nosso ciclo de desenvolvimento.


# Linux

- [Vídeo Aula](https://youtu.be/-Qn9cu_H9hw)
- Entender o que é o linux
- Conforto ao utilizar o terminal do Linux com exepmlos práticos de necessidades do dia a dia. Buscar informações de ajuda para cada comando que for aprendido assim como uma lista essencial para trabalhar diretamente no terminal
- Introduação a comandos de auxilio

## Parte 1: O que é Linux e comandos básicos
-----------
Nesse primeiro vídeo vamos nos contextualizar com o que é de fato o Linux, o que podemos fazer com ele e onde ele é usado. Começaremos a ver alguns comandos iniciais quase tornarão mais complexos à medida que avançamos nos módulos, então, capricha nos estudos e bora lá!
-----------

- [Vídeo Aula](https://youtu.be/wZC0_0J8ELc)
- O que é Linux
	- Sistemas que utilizam Kernel Linux, inspirados em Unix.
	- Código Livre
	- Portabilidade alta
	- Facil personalização
	- Seguro por essência
	- Possui compiladores ja instalados por padrão
	- Bom para quem vai desenvolver
- ubuntu, linux, - Elementary OS, Muitos outros.
- Vamos começar a ver o linux em sí e trabalhar comandos e os argumentos dos mesmos.
- pwd
	- Conseguir vizualisar o diretório que estamos.
- man
	- Manual de comandos do determinado comando
	- Ex: man pwd
- ls
	- Lista o conteudo de um diretorio que eu estou.
	- Itens listados com cores diferentes, diferenciam entre eles, pastas, arquivos e etc..
- ls -lah 
	- conteudos na vertical com mais dados
	- Vimos a diferneça dos arquivos totais.
- Podemos criar atalhos no meu terminal.
- Navegar entre diretórios.
- cd
	- Navegar entre diretórios:
	- Ex:
		- cd vai direto para a home
		- cd Downloads - Vai para o argumento
		- cd /tmp - vou para a raiz e depois para o diretório.
		- cd .. para subir um nível no diretório. 
- tab (Tecla)
	- utilizado para completar a frase.
- mkdir
	- Criar diretórios.
	- podemos criar o diretório em qualquer lugar
		- mkdir /tmp/teste
	- mkadir -p
		- Conseguimos criar uma arvore inteira de diretórios.
		- mkdir -p terminal2/comandos
- touch
	- Criar arquivos
	- touch arquivo.txt
	- touch arquivo.txt arquivo3.txt
- cp
	- copiar arquivo
	- cp arquivo.txt arquivo_copia.txt
	- Copiar a longa distancia
		- cp /tmp/linux/arquivo.txt /tmp/linux/arquivo_3.txt
- cp -r terminal
	- copiar o diretório
	- cp -rp conserva tudo do original, horario e assim por diante.
- mv
	- mover pastas
	- mv terminal3 terminal5
	- da para mover a distancia.
- rm 
	- Remover arquivos
	- rm arquivo.txt
	- Remover diversos arquivos
		- rm * .txt.
	- forçar a remoção 
	- rm -rf força a exclusão de algo dentro da pasta.
- rm -r
	- remover diretório
	- rm -r linux

- Resumo dos comandos:
	- pwd - Em que diretório estamos
	- man - abrir o manual de comandos
	- ls - listar o conteúdo de um diretório
	- cd - navegar entre diretórios
	- mkdir - criar um diretório. 
	- touch - criar um arquivo
	- cp - copiar um arquivo/diretorio
	- mv - para mover um arquivo/diretorio
	- rm - removerum arquivo ou um diretorio
	- exit - encerramos o terminal


## Parte 2: Comandos de edição e gestão de arquivos
-----------
Salve pessoal! Como combinado, a partir de agora os comandos passam a ficar um pouco mais complexos, mas calma, nada de pânico, a princípio busquei explicá-los de forma progressiva. Tenha atenção aos comandos "cat", "| (pipe)" e "grep". Então, confere aí e depois comenta comigo se algo não ficou claro! Bons estudos.
-----------

- [Vídeo Aula](https://youtu.be/DDuu9Wrh9f8)
- Gerenciador de pacotes no terminal
	- Com ele gerenciamos os pacotes instalados no nosso linux.
- tive que setar um password para o meu root com um comando su -
	- Depois só setei o password.
- Executado o comanddo apt-get update para atualizar os pacotes.
- apos vamos instalar o tree
	- apt-install tree
- Depois executamos o tree
	- Com isto conseguimos ver os dados de arquivos do nosso linux, 
- tree -L 1 
	- Mostrarmos somente um nível de programas instalados
- tree -L 2 
	- Mostrarmos dois níveis de programas instalados
- apt purge
	- Remove um aplicativo e todos os arquivos de configuração do mesmo
- vi ou vim
	- editor de arquivo simples open source
- i
	- mudamos o editor para modo edição
- Esc + q!
	- saimos sem salvar o arquivo
- Esc + wq
	- Saimos salvando o arquivo.
- buscar algo dentro do arquivo dentro do vi
	- /palavra a ser buscada
	- n, vai para a próxima ocorrencia.
	- Busca, case sensitive.
	- dd, sem estar no modo de edição, deletamos uma linha
	- 5dd, deleto 5 linhas.
	- u, desfaz a nossa ultima atualização, tipo um ctrl+z
	- gg, leva o cursos para o inicio do arquivo.
	- shift + g, vai para o final do arquivo. 
	- ir para uma linha - esc + : + numero da linha
- cat
	- Le o arquivo de texto e mostra o mesmo na tela
	- cat -e, identificar os caracteres especiais, tipo quebra de linha.
	- cat arquivo.txt | more - isto vai pegar o arquivo de texto e jogar em outra aferramenta.
- tail arquivo.txt
	- Vai trazer o final do arquivo.
	- tail -1 arquivo.txt, vai trazer a ultima linha do arquivo.
- head arquivo.txt
	- vai trazer o topo de um arquivo. 
	- head -1 arquivo.txt, vai trazer somente uma linha do topo
- grep
	- Busque alguma coisa em um arquivo ou uma saida.
	- cat texto.txt | grep "Texto a ser buscado"
	- cat texto.txt | grep - n "Texto a ser buscado", vai trazer a linha que tem a palavra.
- cat arquivo.txt | grep -v "Palavra", vai trazer tudo que nao tem este termo que estamos procurando
- cat arquivo.txt | grep -v "Palavra" | grep -v "Palavra", Da para concatenar o comando.
- grep com expressão regular
	- cat arquivo.txt | egrep -v "Nao trazer|este erro|este erro" - isto vai trazer tudo que diferente dos erros posicionados.
- tar
	- Serve para unir arquivo e compactar arquivos.
	- tar -cvf comandos.tar projeto/.  
		- o comando pega tudo que tem dentro da pasta projeto e gera um unico arquivo chamado comandos.tar
	- tar -xvf comandos.tar - vou desfazer a junção que eu tinha feito antes.
	- tar como copactação
		- tar -zcvf comandos.tar.gz linux/ - compactação geral dos arquivos da pasta linux
		- tar -zxvf comandos.tar.gz linux/ - compactação geral dos arquivos da pasta linux	
- zip 
	- zip arquivo .zip linux/ - mesma ideia do tar
	- unzip arquivo.zip - mesma ideia do tar

- Resumo dos comandos:
	- apt: instalar e desinstalar programas.
	- tree: listar uma pasta no formato visual.
	- vi ou vim: editar arquivos no terminal.
	- cat: para ler e jogar na tela um conteudo.
	- |(pipe): para redirecionar a saída de um comando.
	- more: gerar uma pausa entre telas.
	- tail: ler e exibir o inicio de um arquivo.
	- head: ler e exibir o inicio de um arquivo.
	- grep: procurar por um termo em um arquivo/conteúdo.
	- egrep: procurar por um tempo (com conteúdo regular) em um arquivo.
	- tar: gerar um arquivo unico com varios arquivo/diretórios
	- zip: compactar um arquivo/pasta


## Parte 3: Comandos de rede e processos
-----------
Dando continuidade aos nossos estudos, estamos aprendendo a utilizar os comandos para diagnosticar a rede do nosso ambiente Linux, são comandos muitos específicos e importantes! Prestem bem atenção, pois eles são nossas ferramentas para diagnostico de eventuais problemas em nosso ambiente Linux! 
-----------

- [Vídeo Aula](https://youtu.be/OS10ach2qSM)
- apt install net-tools (Para instalar o ifconfig)
- ifconfig
	- vizualisar as informações da nossa interfaçe de rede.
- ip addr show 
	- vizualisar as informações da nossa interfaçe de rede.
- ping
	- direcionar um teste de pacote par aum endereço
	- ping www.google.com.br
	- as vezes consegue resolver, mas nao recebe pacotes de volta.
- telnet www.google.com.br 80
	- Teste de porta dos serviços; 
- ssh
	- Conexão em um host remoto.
	- ssh usuario@servidor - Exemplo "ssh guiseppelopes@guiuseppelopes.com"
	- ssh tem porta padrão
	- Vou estar no servidor.
	- consigo usar comandos no servidor remotos.
- netstat
	- Tudo de conexões ativas e portas ativas no meu linux.
	- netstat -lpt para ver serviços com portas especificas.
	- ps - processos em execução
	- ps aux - mais detalhes dos processos em execução
	- Consegumos validar portas que estão ativas e serviços 
- kill - encerra o processo. 
	- kill -9 id processo, ele vai encerrar na hora
	- kill -2 id porcesso, encerra, mas espera para encerrar, deixa o programa encerrar na hora. 
- top
	- processos em execução e o consumo de recursos que os mesmos estão executando.
	- no inicio é o que mais esta sendo executado.
- df
	- Disco em espaço livre no ambiente
	- df -h - melhor detalhado.
- du
	- Tamanho dos arquivos no local que eu estou
	- du -s 
	- du -h - facil para a gente entender
- env
	- Todas as variaveis de ambiente no meu linux
	- export test=ola, criamos um programa como variavel de ambiente.

- Resumo dos comandos:
	- ifconfig: Para nossas configurações de rede.
	- ip -a: Obter informações de IP.
	- ping: testar conectividade com um endereço remoto.
	- telnet: testar conectividade com um endereço reomoto com a porta
	- ssh: conectar em um linux remoto
	- netstat: verifica o status de rede
	- df: verificar espaço livre em disco
	- du: verificar espaço utilizado pelos arquivos/pastas
	- top: verificar processos e carga de processamento
	- ps: lisagem de processo
	- env: verificar as variaveis de ambiente em um linux

# Git

# Virtualização e Provisionamento

# Conteiners e Orquestração

# Integração

# Monitoramento