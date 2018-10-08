# Conhecendo nossas opcoes computacionais.


## Google Compute Engine

Caso voce esteja familiarizado com o *aaS da vida, o compute engine e o IaaS da GCP.
Nele voce consegue criar maquinas virtuais (que ele chama de instancias) de acordo com a sua vontade, de forma simples e rapida! 

Esse e a opcao com maior possibilidade de personalizaca, ja que podemos escolher quase todo o hardware e todo software que ira rodar dentro da VM.

Se voce quer ter todo o trabalho/liberdade de gerenciar suas maquinas de forma micro, por qualquer motivo que seja, essa e a opcao que voce procura.

## Google App Engine

Ainda pensando na familia *aaS, o GAE e uma PaaS (Plataforma como servico), deve ser a maneira mais simples para dar liberdade para os desenvolvedores que nao possuem conhecimento de infra, ja que eles podem focar apenas no codigo da aplicacao e no maximo entender um pouco de containers caso precisem utilizar uma imagem customizada (falaremos mais a seguir).

Recomendado para aplicacoes escalaveis e backends para aplicacoes mobile.

Utilizando essa opcao voce:
- Nunca vai tocar na infraestrutura responsavel por rodar suas aplicacoes.
- Deploy, manutencao e escalabilidade nao sao sua responsabilidade
- Reduz o custo operacional.

Nessa opcao temos 2 formatos, o padrao (Standard) e o flexivel (Flexible).
Na opcao padrao, temos apenas 4 linguagens suportadas no momento que escrevo esse texto.
- Python
- Java
- PHP
- Go

A flexivel, e um pouco mais... flexivel, e suporta as seguintes linguagens:
- Java 8 / Servlet 3.1 / Jetty 9
- Python 2.7 / 3.5
- Node.Js
- Ruby
- PHP
- .NET Core
- Go
- e caso voce precise, pode rodar uma imagem customizada do docker!


## Google Container Engine

Esse e o Kubernetes by Google! Sim, voce pode ter o seu proprio cluster de kubernetes gerenciado pelo google e melhor ainda, sem pagar nada a mais alem do valor das instancias usadas.

~Leia a proxima linha com a voz do Ciro Botini~
E tem mais... voce nao paga pelo Master! :)

E importante voce entender o que e e quando usar um cluster de Kubernetes, ele traz um custo alto geralmente e nao e uma bala de prata. Lembre-se sempre disso *Kubernetes nao e uma pala de prata!*

Usando o GCE voce deixa de se preocupar com o sistema operacional e para a se preocupar mais com a aplicacao em si. 

"Administre aplicacoes, nao maquinas!"

## Google Cloud Funtions (Serverless)

Aqui  temos o hypado FaaS (Funcao como servico), a ideia e ter endpoints preparados para responder a eventos.

Evite funcoes complexas aqui, a ideia e ter funcoes simples e rapidas. Elas precisa ser escritas em Javascript e seram executadas no Node.JS

Elas costumam ser baratas se utilizadas da forma correta, mas sempre vale a pena fazer uma analise para saber exatamente onde vale a pena ter maquinas rodando 24/7 e onde vale a pena utilizar as functions. 

## Dicas

Antes de sair codando qualquer coisa, entenda as necessidades do projeto. Nao so da parte da aplicacao como tambem da infraestrutura (espero eu que voce esteja codando sua infra). 
Nao jogue dinheiro fora, a facilidade de utilizar servicos nao deve ser desculpa para voce nao trabalhar com arquiteto.


## Links

- https://cloudplatform.googleblog.com/2017/07/choosing-the-right-compute-option-in-GCP-a-decision-tree.html
