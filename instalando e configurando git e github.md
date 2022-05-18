# instalando e configurando git e github

### instalando o git na sua maquina 

adicione o repositorio ppa

>add-apt-repository ppa:git-core/ppa

faça um update e instale o git   

>sudo apt update
>sudo apt install git


### configurando chave SSH 

>ssh-keygen -t ed25519 -c email

>cd/home/davs/.ssh 

>ls

vai aparecer a chave publica e privada 

>cat id_'chave publica q aparecer no ls'

cadastrar chave no github

>eval $(ssh-agent -s)

>ssh-add 'chave privada q aparecer no ls'

crie uma pasta de teste e clone um repositorio no github para validar a chave 

> git clone + 'ssh do repositorio q vc pegou no github'

confirme com o yes e pronto 

### configuração do git 

>git config --global user.email " 'mesmo email no github' "

use o mesmo email usado no github

>git config --global user.name 'mesmo nome no github'

>git config --list (para listar e verificar nome e email)

caso seja necessario mudar esses dados
>git config --global --unset user.email "email"

>git config --global --unset user.name

### colocando repositorio no servidor local

priemeiro vc deve criar o repositorio git na pasta q vc deseja colocar no servidor local

então dentro da pasta coloque o comando 

>git init

>ls -a (para listar as pastas ocultas)

nesse ls devera aparecer uma pasta chamada .git

com o arquivo pronto vc deve adicionalo 

> git add *

faça esse comando para confirmar se todos os arquivos foram adicionados ou commitados

> git status

para commitar um arquilo vc fara esse comando 

> git commit -m "mensagem"

## enviar arquivo para servidor remoto 

no github crie um repositori, copie url

de volta no terminal

> git remote add origin + 'url copiado'

- origin é o apelido dado ao url para fazer o push

>git remote -v (mostra o vai ser push)


> git push origin master 

fazer um refresh no repositorio criado no github.