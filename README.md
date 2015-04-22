# Curso git



# Projeto

Criar um protótipo de um framework genérico de notificação ao usuário, que possa ser usado em diferentes aplicativos.

# Problema

O sistema precisa notificar o usuário em diversas ocasiões, por exemplo, quando o backup não é foi feito a alguns dias, quando o usuário tem tarefas vencidas ou vencendo, quando uma tarefa é designada para ele, etc.

# Tipos de notificação

Alguns exemplos:

- **Diárias**: Todo dia o sistema enviará um e-mail em um determinado horário para o usuário
- **Imediatas**: Determinadas ações devem notificar o usuário imediatamente
- **Agendadas**: A notificação deverá ser enviada ao usuário em uma data e hora pré determinadas.

# Formas de receber as notificações

- **Dentro do sistema**: Ao fazer login ou estar logado no sistema, caso receba uma nova notificação será mostrada ao usuário.

- **Externas**: SMS, Twitter, e-mail, etc, ou seja: O framework deverá suportar diversos tipos de notificações que poderão ser plugadas, no caso de Twitter por exemplo a notificação seria enviada para a API e poderá ser instantânea, agendada, etc

## Casos de uso

Abaixo alguns exemplos de casos de uso para facilitar o entendimento do problema:

- **Notificação de backup**: Quando não for efetuado um backup após um determinado período, os usuários que assinaram essa notificação deverão ser notificados.

- **Notificação de tarefa vencida**: Caso o usuário tenha uma tarefa vencida o sistema deverá enviar um e-mail, sms, etc  diário para ele com as tarefas vencidas.

- **Notificação de nova tarefa**: Quando uma tarefa for determinada a um usuário, ele deverá receber imediatamente uma notificação, seja dentro do próprio sistema, por e-mail, twitter, etc.

# Objetivo do framework

Ser um framework de notificações genérico e extensível que possa ser utilizado para notificar o usuário de diversas formas.

O uso do código deverá ser simples por exemplo, para enviar uma notificação o desenvolvedor que estiver usando o framework precisará apenas chamar um método informando o ID do usuário e passando os dados da notificação e o framework se encarregará de entregar a notificação para o usuário de acordo com os meios de envio que ele assinou.

# Implementação e avaliação

A implementação deverá ser feita em um protótipo, não precisa ser um aplicativo completo ou visual, mas deverá mostrar o uso do framework e que ele funciona.

Avaliaremos a solução dada para o problema, as decisões de design tomadas e também a forma como foram implementadas, sinta-se livre para ser criativo na solução, pensar em mais casos de uso, novos meios de envio e o que mais conseguir implementar.

# Requisitos

- O usuário deverá selecionar quais notificações deseja receber
- Permitir que o usuário configure os meios que deseja receber as notificações
- Novos canais de envio poderão ser adicionados a qualquer momento sem alterações nos demais e no framework

## Implementação das formas de envio

**Não é necessário implementar e fazer funcionar as formas de envio**, ou seja, o protótipo não precisa realmente enviar um e-mail, iremos avaliar a estrutura e código do projeto, apenas escrever no console ou mostrar uma mensagem por exemplo "Enviando e-mail" é suficiente.

# Como codificar

- Implemente o protótipo usando testes automatizados (DUnit ou DUnitX).
- Entregar um protótipo simples que demonstre o framework funcionando.
- Todos os commits devem estar neste repositório, de preferência vá dando push no repositório conforme for implementando para acompanharmos o processo.
- Em caso de dúvidas criar issues no próprio repositório.

# O que será avaliado?

- Simplicidade e clareza
- Arquitetura
- Estilo de código
- Testes

# Dicas

- Registre o que achar importante:
- Ideias que gostaria de implementar se tivesse tempo
- Decisões tomadas e seus porquês
- Arquiteturas testadas e os motivos de terem sido modificadas ou abandonadas
- Crie um arquivo markdown no repositório para salvar esses comentários.

# Avaliação 

Ao finalizar o projeto, iremos analisar o código e fazer perguntas sobre ele, portanto documente suas decisões durante o desenvolvimento para facilitar esta etapa.
