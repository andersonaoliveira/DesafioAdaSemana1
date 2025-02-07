# Desafio 1° semana | Ada Tehch + Cielo


### Descrição <br>
Você foi designado para criar um serviço que gerencia filas de sugestões, elogios e críticas de
clientes para uma empresa, aproveitando os serviços da AWS, como SNS e SQS. O serviço deve
permitir que os clientes enviem suas sugestões, elogios e críticas, que serão enfileirados e
processados de acordo com a ordem em que foram recebidos. Além disso, deve ser possível
verificar o status da fila e obter informações sobre as mensagens recebidas.

#### Requisitos:
  1. Implemente uma classe CustomerFeedback que represente uma mensagem de
feedback com os seguintes atributos: id, type (tipo de feedback, como "Sugestão",
"Elogio" ou "Crítica"), message (mensagem do cliente) e status (status da mensagem,
como "Recebido", "Em Processamento" ou "Finalizado").
  2. Configure um tópico SNS para cada tipo de feedback (Sugestão, Elogio, Crítica) na
AWS. Quando um cliente envia um feedback, o sistema deve publicar a mensagem no
tópico SNS correspondente.
  3. Configure uma fila SQS para cada tipo de feedback (Sugestão, Elogio, Crítica) na AWS.
Configure as filas para seguir o princípio FIFO (First-In-First-Out).
  4. Implemente um consumidor de fila SQS para processar os feedbacks da fila. Este
consumidor deve ser executado em segundo plano e processar os feedbacks de acordo
com a ordem da fila. Quando um feedback for processado com sucesso, seu status
deve ser atualizado para "Finalizado".
  5. Crie um controlador REST em Java usando a biblioteca Spring Boot para expor
endpoints para as seguintes operações:
    a. Enviar um feedback (sugestão, elogio ou crítica) para a fila correspondente no
SQS.
    b. Obter o tamanho atual da fila de feedbacks para cada tipo (Sugestão, Elogio,
Crítica).
    c. Obter informações sobre todos os feedbacks na fila de cada tipo.
  6. Documente a API REST usando a especificação Swagger ou alguma outra ferramenta
de documentação de API.

## 🤝 Colaboradores
**Grupo:: Sala 4**<br>
<table>
  <tr>
    <td align="center">
      <a href="https://github.com/andersonaoliveira">
        <img src="https://avatars.githubusercontent.com/u/90530503?v=4" width="100px;" alt="Foto do Anderson de Aguiar de Oliveira no GitHub"/><br>        
        <sub>
          <b>Anderson de Aguiar de Oliveira</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/Lucasbacarinireis">
        <img src="https://avatars.githubusercontent.com/u/100075142?v=4" width="100px;" alt="Foto do Lucas Bacarini Reis no GitHub"/><br>
        <sub>
          <b>Lucas Bacarini Reis</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/JardielmaQueiroz">
        <img src="https://avatars.githubusercontent.com/u/18507854?v=4" width="100px;" alt="Foto da Jardielma Lima no GitHub"/><br>
        <sub>
          <b>Jardielma Queiroz De Lima Lopes </b>
        </sub>
      </a>
    </td>
  </tr>
</table>

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:

- [Java JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html): Necessário para executar o projeto Java
- [Spring Boot](https://spring.io/)
- [Maven](https://maven.apache.org/): Necessário para realizar o build do projeto Java
- [Swagger](https://editor.swagger.io/): 
  
## Ferramentas Utilizadas

- [IntelliJ | JetBrains](https://www.jetbrains.com/pt-br/idea/)

## 🚀 Getting started 

Para instalar o <nome_do_projeto>, siga estas etapas:

```
<comando_de_instalação>
```

 ## 📫 Contribuindo para projeto

Para contribuir com o projeto, siga estas etapas:

- Bifurque este repositório.
- Crie um branch: `git checkout -b <nome_branch>`.
- Faça suas alterações e confirme-as: `git commit -m '<mensagem_commit>'`
- Envie para o branch original: `git push origin <nome_do_projeto> / <local>`
- Crie a solicitação de pull.

