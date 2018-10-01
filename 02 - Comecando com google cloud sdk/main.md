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



