# IAM - Identity and Access Management (vulgo quem pode acessar oque)

A não ser que você tenha um time muito maduro e trabalhe numa empresa que abraça o caos todos os dias pela manha, você (na verdade seu gestor) vai se preocupar bastante com o fato de quem tem permissão para criar, acessar e usar determinados serviços ou projetos.

![who-can-which](./img/who-can-which.png)

Uma dica e utilize sempre o principio do menor privilegio possível. 
O que isso quer dizer?
Se você precisar criar um usuário com permissão para VER algo, busque uma maneira dele ter APENAS a possibilidade de VER. Não libere acesso de ADMIN para essa pessoa, pois isso pode acarretar em diversos problemas. (Se quiser que explique com mais detalhes abre uma issue ai que eu detalho melhor!)


O Google separa os usuários em dois grupos principais.

* Pessoas
  * Conta do Google
  * Grupo do Google
  * Dominio do G Suite
  * Cloud Identity Domain
    * E um tipo de domínio da organização e não necessariamente um domínio do Google.
* Conta de serviço


## Conta de Serviço

Esse tipo de conta e extremamente indicado para, pasme, serviços. Se você tem um serviço de backup por exemplo, crie um usuário de serviço e utilize ele para que a aplicação se conecte ao outro serviço.

"A mais eu uso a minha própria conta e não deu nenhum problema!" (Ops, Dev).

Sim, e provavelmente isso nunca vai ser um problema para você, mas cera___2 um grande problema para os amiguinhos que ficarem quando você sair da empresa ou precisar se afastar e por medidas de segurança desativarem seu usuário. :)


Por padrão esse usuários de serviço seguem o seguinte formato:

`<project_number>@developer.gserviceaccount.com`


# Roles

Role nada mais e que um conjunto de permissões.

O primeiro ponto positivo de usar uma role e ter facilidade em passar as mesmas permissões para um novo usuário que acabou de entrar na empresa.

Ai você que esta apenas estudando pode pensar:

"não vou criar role, não tem necessidade no meu caso”.

Mas você esta enganado, na GCP você não pode anexar permissões a usuários. Só apenas roles anexadas a eles. 

As permissões seguem um padrão de `$servico.$recurso.$verbo`, por exemplo `compute.instances.delete`!

![role-permissions](./img/role-permissions.png)

# Politicas de IAM

![politica-de-hierarquia](./img/hierarquia.png)

As politicas de hierarquia da GCP são bem granulares e funcionam de cima pra baixo (nesse desenho pelo menos).

Vamos imaginar o seguinte, Bianca acabou de chegar na empresa e vai fazer parte do projeto `example-dev`. No entanto ela só vai precisar de acesso ao `Compute Engine`, não precisa se preocupar em saber detalhes mas a titulo de curiosidade são as VMs na GCP, mas somente para *visualizar*. 

Você como uma pessoa que conhece o principio do menor privilegio vai liberar para ela apenas a *visualização* do recurso `Compute Engine`.

Depois que você foi pra casa, Bianca percebeu que precisa também ter acesso ao `Cloud Storage` para validar algumas coisas.
Uma pessoa mais desatualizada recebeu essa solicitação e apos ver que ela já tinha acesso ao `Compute Engine` resolveu liberar acesso de *Admin* ao projeto.

Liberar esse tipo de acesso ao projeto tem efeito em todos os recursos abaixo, mas... como você acha que ficariam as permissões da Bianca no `Compute Engine`?

Obviamente ela teria acesso de *Admin* no `App Engine` e `Cloud Storage` mas manteria o de *Viewer* no `Compute Engine` correto?


Nope! Quanto mais pra cima for dado um privilegio, toda "raiz" daquele recurso/projeto herdara seu privilegio.

No caso, como a Bianca tem acesso de admin ao projeto, também terá o mesmo acesso de *Admin* todos os sub-recursos! 


# Links uteis

- https://cloud.google.com/iam/docs/understanding-roles#predefined_roles
