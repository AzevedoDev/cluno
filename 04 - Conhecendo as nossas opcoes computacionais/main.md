# Conhecendo nossas opções computacionais.


## Google Compute Engine

Caso você esteja familiarizado com o *aaS da vida, o compute engine e o IaaS da GCP.
Nele você consegue criar maquinas virtuais (que ele chama de instancias) de acordo com a sua vontade, de forma simples e rápida! 

Esse e a opção com maior possibilidade de personalizada, já que podemos escolher quase todo o hardware e todo software que ira rodar dentro da VM.

Se você quer ter todo o trabalho/liberdade de gerenciar suas maquinas de forma micro, por qualquer motivo que seja, essa e a opção que você procura.

## Google App Engine

Ainda pensando na família *aaS, o GAE e uma PaaS (Plataforma como servico), deve ser a maneira mais simples para dar liberdade para os desenvolvedores que não possuem conhecimento de infra, já que eles podem focar apenas no código da aplicação e no máximo entender um pouco de containers caso precisem utilizar uma imagem customizada (falaremos mais a seguir).

Recomendado para aplicações escaláveis e backends para aplicações mobile.

Utilizando essa opção você:
- Nunca vai tocar na infraestrutura responsável por rodar suas aplicações.
- Deploy, manutenção e escalabilidade não são sua responsabilidade
- Reduz o custo operacional.

Nessa opção temos dois formatos, o padrão (Standard) e o flexível (Flexible).
Na opção padrão, temos apenas quatro linguagens suportadas no momento que escrevo esse texto.
- Python
- Java
- PHP
- Go

A flexível, e um pouco mais... flexível, e suporta as seguintes linguagens:
- Java 8 / Servlet 3.1 / Jetty 9
- Python 2.7 / 3.5
- Node.Js
- Ruby
- PHP
- .NET Core
- Go
- e caso você precise, pode rodar uma imagem customizada do docker!


## Google Container Engine

Esse e o Kubernetes by Google! Sim, você pode ter o seu próprio cluster de kubernetes gerenciado pelo google e melhor ainda, sem pagar nada a mais além do valor das instancias usadas.

~Leia a próxima linha com a voz do Ciro Botini~
E tem mais... você não paga pelo Master! :)

E importante você entender o que é e quando usar um cluster de Kubernetes, ele traz um custo alto geralmente e não e uma bala de prata. Lembre-se sempre disso *Kubernetes não e uma pala de prata!*

Usando o GCE você deixa de se preocupar com o sistema operacional e para a se preocupar mais com a aplicação em si. 

"Administre aplicações, não maquinas!"

## Google Cloud Funtions (Serverless)

Aqui temos o hypado FaaS (Função como servico), a ideia e ter endpoints preparados para responder a eventos.

Evite funções complexas aqui, a ideia e ter funções simples e rápidas. Elas precisam ser escritas em Javascript e serão executadas no Node.JS

Elas costumam ser baratas se utilizadas da forma correta, mas sempre vale a pena fazer uma analise para saber exatamente onde vale a pena ter maquinas rodando 24/7 e onde vale a pena utilizar as functions. 

## Dicas

Antes de sair codando qualquer coisa, entenda as necessidades do projeto. Não só da parte da aplicação como também da infraestrutura (espero eu que você esteja codando sua infra). 
Não jogue dinheiro fora, a facilidade de utilizar serviços não deve ser desculpa para você não trabalhar com arquiteto.


## Links

- https://cloudplatform.googleblog.com/2017/07/choosing-the-right-compute-option-in-GCP-a-decision-tree.html
