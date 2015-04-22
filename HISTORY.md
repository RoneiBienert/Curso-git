## 1.0.0

Desafio Monde - Ronei Bienert
-----------------------------

## Startup

Vou utilizar o Delphi XE4 no desenvolvimento do desafio.

Para o protótipo optei por uma aplicação visual, visando assim facilitar o vinculo entre usuário, notificação e forma de envio.

## Metodologia de desenvolvimento

Para o desenvolvimento do framework estou utilizando TDD. Tanto DUnit como DUnitX são novidade para mim, e estou tendo que optar por uma delas.

DUnitX parece ser a ferramenta mais completa, por isso estarei utilizando-a no desafio.  

A principio estarei trabalhando totalmente em memória para agilizar meu desenvolvimento. Mas ainda pretendo incluir no projeto um adaptor, caso seja necessário persistir os dados em base.

## Arquitetura da aplicação

* O framework ira trabalhar como um register, que ira receber os tipos de notificação e forma de envio.
* Para garantir que o framework seja extensível, as formas de notificação implementarão uma interface. Caso exista a necessidade de uma nova forma de notificação, basta criar uma classe que implemente a mesma interface e registrá-la.
* Também foi implementado um adaptador de persistência, caso seja necessário a utilização de outras formas de persistência.

## Coisas que testei / descartei / gostaria de fazer

* Comecei trabalhando com diversos VOs e ObjetList para trabalhar com praticamente todos os dados. Acabei eliminando muitos VO para não amarar as classes de persistência e a interface a eles.
* Não fiquei satisfeito com os métodos das classes de persistência. Se tivesse tempo com certeza iria mexer nisso.
* A responsabilidade de controlar, tanto o agendamento, como também o usuário logado para poder exibir a notificação na aplicação. Ficou na classe `TServicoNotificacao`, eu acredito que seria mais interessante jogar esta responsabilidade para as interfaces.
* Não foi criado nenhum tratamento de exceção que com certeza deveria existir.
* Talvez deveria existir uma forma de alertar o usuário que esta recebendo notificações mas não assinou nenhuma forma e notificação. 

