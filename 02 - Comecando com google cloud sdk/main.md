# Conhecendo o SDK

### Instalando

[Clique aqui](https://cloud.google.com/sdk/docs/quickstarts) e descubra como instalar no seu SO!

Caso voce esteja utilizando um MacOS e utilizando o brew:

```
brew tap caskroom/cask
brew cask install google-cloud-sdk
```

Para validar se o gcloud foi instalado com sucesso execute o seguinte comando:

```
gcloud --version
```

Ele deve te retornar algo como:

![gcloud --version](./img/gcloud-version.png)

### Configurando o gcloud

Comece executando o comando 

```
gcloud init
```

e siga o passo a passo.

* De um nome para a configuracao
* Faca login com sua conta do google
* Escolha o projeto criado ou crie um novo

E isso, agora voce ja tem seu projeto cadastrado e podemos comecar a utilizar a cli (command line interface) para executar nossos comandos!



### Criando um projeto pela sdk

A primeira dica vai pro comando `man`, muito provavelmetne voce nao conhece os parametros de nenhum comando do gcloud. Entao voce vai precisar bastante do `man`. 

Faca o seguinte digito o comando `man gcloud` e aperta tab. 
Voce deve estar vendo uma lista gigante de comandos. Mas nos queremos ver comandos relacionados a projetos, entao vamos tentar reduzir essa lista executando `man gcloud_projects` e prescionando tab novamente.
Beleza, agora temos uma lista bem menor...

Voce consegue ate ler as opcoes, e ver que temos uma que e create. 
Seguimos com o comando `man gcloud_projects_create`.
De uma lida em como o comando funciona e todos os parametros.

Caso voce nao queira ler agora, basta digital `gcloud projects create $id_unico`, trocando $id_unico para o id do seu projeto. 

![gcloud projects create](./img/new-project.png)

