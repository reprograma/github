## GIT e GITHUB - E um pouquinho de linha de comando

***

### O que é Git?
É um programa open source de controle de versão de código,  criado pelo mesmo desenvolvedor do Linux.
Com o GIT podemos desenvolver projetos colaborativos, onde outras pessoas podem trabalhar simultaneamente no mesmo código sem riscos de perdermos nada do trabalho.
Com o Git também conseguimos ter um histórico de tudo que foi alterado nos arquivos ao longo do tempo, além de mostrar quem foi o autor da mudança.

Resumidamente: Você trabalha na sua máquina e salva versões do seu código no GitHub, e também pode baixar versões de código do GitHub para a sua máquina.

### Por que é importante?

1. Organização: Porque você não vai lembrar o que mudou no projeto, o Git cria uma timeline com tudo que aconteceu desde o início do projeto).
2. Projetos com várias pessoas: Evita o “final_valendo_valendo2_oficial” Ajuda trabalho em equipe ( entender o que foi feito, onde parou, quem fez o que).
3. Segurança:  Se algo der errado, você pode resgatar uma versão anterior, além  de ter o seu código salvo em um lugar seguro.
4. Versatilidade: Você pode guardar qualquer tipo de arquivo no git/Github, não necessariamente código.


### O que é GitHub?
É uma espécie de rede social muito utilizada principalmente por desenvolvedores, onde você pode publicar e compartilhar todos os seus projetos, além de colaborar com projetos de pessoas e empresas de todo o mundo.
Você pode salvar todos seus projetos de forma pública no seu perfil, e de forma privada  por $7/m.


### Por que é importante?
1. Portfólio - Porque é um lugar para guardar e mostrar seus projetos.
2. Organização - Porque permite que todo mundo trabalhe no mesmo projeto (seja um projeto da sua empresa ou um Open Source).
3. Ferramentas - Porque oferece funcionalidades extras ao git, como interface visual, documentação, bug tracking, feature requests, pull requests, etc.

### O que é linha de comando?
imagem
É aquela tela preta que aparece nos filmes, normalmente com alguém hackeando algum sistema.
Mexer com o terminal assusta um pouco porque ele não é nem um pouco visual. Mas é muito simples mexer nele.
Sabe quando a gente arrasta arquivos para uma pasta ou cria uma pasta nova? No terminal você faz tudo isso também, mas sem interface gráfica. A gente insere comandos, e ele executa.

### Por que é importante trabalhar com linha de comando?
 Na linha de comando você controla melhor o que está rolando com o seu computador - inclusive o versionamento. O git é sempre usado através de linha de comando. (O GitHub tem ferramentas visuais para uso do Git, mas é importante saber se virar pela linha de comando)

### Comandos básicos do terminal
```
ls - LISTAR (ele traz uma lista de tudo o que está naquela pasta - documentos, outras pastas, etc) *às vezes é dir no windows
pwd - Present working directory (onde estou?) Ele traz todo o caminho onde você está (em que pasta e onde essa pasta fica)
cd - change directory (use para se locomover entre as pastas)
cd ~ - volta para a raiz
cd . - volta uma pasta acima
cd nome-da-pasta - para entrar em uma pasta (você precisa conseguir enxergar ela quando listar os arquivos)
touch nome-do-arquivo.extensão - criar arquivo mkdir nome-do-diretorio - cria diretório mv - mover (renomear)
whoami - "quem sou eu?" identifica o usuário que está mexendo no sistema.
```

***

### Começando com o Git

Algumas palavras novas que vamos usar com o Git/GitHub

`Repositório` É um espaço digital aonde o seu projeto vai ser salvo. No seu computador ele é a pasta aonde o seu projeto está salvo.

`Controle de versão` É a proposta básica do Git, um histórico de tudo o que aconteceu com o/s arquivo/s que você está trabalhando. Por exemplo, quando você salva um arquivo do Word no seu computador, você perde todas as versões anteriores, ficando somente com o conteúdo atual. Com o Git você tem todas as versões antigas dos arquivos.

`Commit` Quando você faz um commit com o Git, você está criando um controle de versão (histórico) daquele arquivo .

`Pull` O pull serve para se comunicar entre a sua máquina e o repositório remoto. Esse comando faz uma cópia do repositório remoto e baixa ele para a sua máquina.

`Push` O push também serve para se comunicar entre a sua máquina e o repositório remoto. Esse comando faz uma cópia do repositório local e envia ele para o repositório remoto.

`Clone` O comando clone faz exatamente o que ele sugere: uma cópia exata do arquivo, que você vai baixar do repositório remoto para a sua máquina.


### Fluxo do git
imagem
Tudo isso está acontecendo apenas localmente no seu computador!

Cada etiqueta vai gerando um ponto na nossa timeline. Essa etiqueta se chama
 commit, e com essa pequena descrição fica mais fácil se achar entre as versões.

 imagem

### Instalando/verificando se o Git está instalado

Digite git status na linha de comando, e várias instruções e sugestões do git devem aparecer.
 Comandos para usar uma vez na vida: (assim o git sabe quem está fazendo as alterações) 

```
git config --global user.name “Patricia Tonella" 
git config --global user.email “patricia.tonella@gmail.com”

Para remover o usuário
git config --global --unset-all user.name "Patricia Tonella"
git config --global --unset-all user.email “patricia.tonella@gmail.com”
````

### Formas de trabalhar com o Git/GitHub

Baixar um projeto que está hospedado no GitHub para a nossa máquina

2)  Iniciar um projeto na minha máquina e subir para o GitHub

Baixar um projeto que está hospedado no GitHub para a nossa máquina

Acessar https://github.com/ptonella
2)  Acessar o repositório github-aula-1
3)  Copiar a url abaixo:
imagem


4)  Navegar até a pasta aonde você vai fazer o clone do projeto
5) git clone url-que-vocês-copiaram


2) Iniciar um projeto local e subir pro GitHub

1) Navegar pela linha de comando até a pasta desejada
2)  Rodar o comando  git status
  Provavelmente o Git não vai estar iniciado nessa pasta, então vamos rodar um comando para avisar para o Git começar a versionar essa pasta:  git init
3) Criar uma conta no GitHub
4) Criar um repositório no GitHub  (colocar o nome do projeto de vocês)
5) Copiar a url  do repositório (igual vocês fizeram no exemplo anterior)
6) git add . (para adicionar todos os arquivos de uma vez) ou git add caminho-do-arquivo
git commit -m “Aqui você escreve uma mensagem que ajude quem estiver lendo a saber o que você adicionou/modificou nos arquivos“
git remote add origin url-que-voces-copiaram-do-github
git remote -v (vai mostrar as urls, provavelmente duas)
git push origin master
Abrir o repositório no GitHub. Os arquivos que estavam na máquina de vocês agora devem estar salvos no GitHub 🎉
7) Agora uma cópia do trabalho de vocês até agora está salvo no GitHub, e o Git está monitorando essa pasta.

8)  A partir de agora, sempre que vocês modficarem/adicionarem/removerem arquivos nessa pasta, o Git vai saber e  vai mostrar tudo o que foi modificado/adicionado/removido.

9) Para os próximos passos, os comandos que vocês vão usar sempre são (nessa sequência):
6)  git status (para ver a lista do que foi modificado)
7) git add . (para adicionar todos os arquivos de uma vez) ou git add caminho-do-arquivo
8) git commit -m “Mensagem”
9) git pull origin master (SEMPRE FAZER UM PULL ANTES DO PUSH)
10) git push origin master


### Pra não esquecer:
(comandos que mais vamos usar)
6)  git status (para ver a lista de arquivos modificados)
7) git add . (para adicionar todos os arquivos de uma vez) ou git add caminho-do-arquivo

8) git commit -m “Mensagem” (cria um histórico daquele arquivo com uma etiqueta explicando o que foi feito)

9) git pull origin master (o comando PULL pega a versão do arquivo que está no repositório remoto e baixa para sua máquina. Fazer isso sempre antes do push para evitar conflitos e evitar apagar alguma informação remota)

10) git push origin master (envia as modificações para o repositório remoto)

### GitHub Pages
Quem tem uma conta no GitHub pode ter acesso a uma hospedagem gratuita  para os projetos que estão com o código hospedado no GitHub.

 Criar um repositório no GitHub: username.github.io  (username deve ser o seu username do GitHub)
Clonar repositório na sua máquina
Add arquivos
Fazer o commit
Push para o GitHub
Acessar https://username.github.io


### Branch
O git tem uma linha do tempo principal chamada master, que é branch base criado junto com cada repositório. Quando trabalhamos sozinhas em um repositório não tem problema trabalharmos sempre no master, mas quando começamos a trabalhar com outras pessoas em um projeto, surge a necessidade de ter uma cópia do projeto que seja livre de bugs e que esteja funcionando 100%. Essa cópia é o master.

A partir do código que está no master podemos gerar outras cópias para serem modificadas e depois devolvidas para o master.

Essas cópias são chamadas de branch.

imagem
imagem


Comando para criar um novo branch:
git checkout -b nome-do-branch

Comando para trocar de branch:
git checkout  nome-do-branch

Comando para listar todos os branches locais:
git branch

### Merge

Depois de criar um branch e fazer alterações no código, você precisa devolver essa sua cópia para o master. Você faz isso com o comando merge.

Merge é mesclar um branch dentro de outro, juntando as alterações que já estavam no código do master com as alterações do outro branch.


Se duas ou mais pessoas mexerem no mesmo arquivo simultaneamente, isso pode gerar conflito de código.
O Git consegue resolver alguns desses conflitos automaticamente, mas em outros casos o desenvolvedor que está fazendo o merge tem que resolver esse conflito e depois continuar com o merge.

imagem

Comando para fazer merge de um branch em outro:

git merge nome-do-branch-que-vai-ser-mergeado

Importante:
Quando você rodar esse comando, o merge do nome-do-branch-que-vai-ser-mergeado vai ser feito com o branch em que você está no momento

Pra saber em qual branch você está: git status

### Fork

Um fork é uma cópia de um projeto de outra pessoa dentro do seu GitHub. É como quando você faz o clone de um repositório do seu GitHub pra sua máquina.

Normalmente você faz um fork de um projeto para fazer melhorias no código. Depois das melhorias feitas, você vai abrir um pull request para o dono do repositório, e se suas modificações forem aceitas, seu código vai ser ‘mergeado' no código original.

https://github.com/octocat/Spoon-Knife

https://github.com/octocat/Spoon-Knife/pulls

### Pull request

Quando você faz um fork de um projeto, ou quando você trabalha em uma empresa com mais desenvolvedores, é normal que as demais pessoas envolvidas no projeto façam um review do seu código antes de ele ir pro master, afinal você pode ter cometido algum erro no desenvolvimento, ou alguma parte do seu código pode ser melhorada.

Um pull request é quando você quer fazer merge do seu código em outro branch, mas você precisa da autorização das outras pessoas envolvidas no projeto.

Git e Github (textos e vídeos): https://guides.github.com/activities/hello-world/
Curso Gratuito - https://www.udemy.com/git-e-github-para-iniciantes/
Live Mastertech “Guia Completo de Git” - https://www.youtube.com/watch?v=BWjcsuxFUmQ
Live Mastertech “Github na prática” - https://www.youtube.com/watch?v=pcNX1VqC8Po
Tutorial Code School - https://www.codeschool.com/courses/try-git
