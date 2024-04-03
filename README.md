
# NLW Unite - Trilha C#

Este repositório contém os recursos e materiais relacionados à trilha C#.

## Sobre o NLW Unite

O Next Level Week Unite (NLW Unite) é um evento online organizado pela Rocketseat que tem como objetivo proporcionar uma semana intensiva de aprendizado e desenvolvimento para desenvolvedores de software em diversas tecnologias.

## Trilha C#

Nesta trilha, exploraremos o desenvolvimento de aplicativos utilizando a linguagem de programação C#. Durante o evento, abordaremos os seguintes tópicos:

- Construção de APIs RESTful com ASP.NET Core
- Conexão com banco de dados usando Entity Framework
- Handlers  - Gerenciador de Exceções
- Retornos HTTP utilizando Status Code
- DDD - Domain Driven Design


## Recursos

Este repositório contém os seguintes recursos:

- **Projetos**: Projetos de aplicativos desenvolvidos durante o evento.

**Sobre o Projeto**: Este projeto tem por objetivo o gerenciamento de eventos. Responsável pelo cadastro do evento, dos participantes e check-in e também o gerenciamento da quantidade maxima de participantes por evento.




## Documentação da API

### Attendees - Participantes
#### Cadastrar os participantes por Evento

```http
  POST /api/attendees/${eventId}/register
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `eventId` | `GUID` | **Obrigatório**: Informar o Id do Evento |

#### Buscar os participantes por Evento

```http
  GET /api/attendees/${eventId}
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `eventId`      | `GUID` | **Obrigatório**: Informar o Id do Evento |


### CheckIn - Check In
#### Cadastrar a participação no evento

```http
  POST /api/checkin/${attendeeId}
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `attendeeId` | `GUID` | **Obrigatório**: Informar o Id do Participante |


### Events - Eventos
#### Cadastrar o evento

```http
  POST /api/events/
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `Title` | `string` |  Informar o nome do evento |
| `Details ` | `string` |  Informar uma descrição do evento |
| `MaximumAttendees ` | `int` |  Informar a quantidade máxima de participantes |

#### Buscar os Eventos cadastrados

```http
  GET /api/events/${id}
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `GUID` | **Obrigatório**: Informar o Id do Evento |


## Stack utilizada

**Back-end:** .NET 8.0, C#, SQLite

**Documentação API:** Swagger

