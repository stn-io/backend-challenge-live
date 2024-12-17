# 🕹️ Live-Coding: API de Gerenciamento de Tarefas

### Bem-vindo(a) 👋

Parabéns por aceitar nosso desafio de Backend! Este é o momento de mostrar suas habilidades.

Divirta-se, programe e mostre do que você é capaz! 💪

## Objetivo

O objetivo deste desafio é avaliar suas habilidades em Node.js com TypeScript no desenvolvimento de uma API RESTful.

Você irá construir uma API simples para gerenciar "Tarefas" (Tasks). O desafio deve ser realizado em **até 1 hora**.

## Requisitos Técnicos

- Utilize **Node.js** com **TypeScript**.
- Utilize um **framework de sua preferência**, como **Express**, **NestJS**, **Koa** ou outro.
- Utilize um banco **em memória** simples com **JSON** (sem necessidade de banco relacional).
- A aplicação deve seguir princípios de **Clean Code** e **boas práticas REST**.
- Teste a API utilizando uma ferramenta como **Postman** ou **cURL**.
- A API deve ser funcional e incluir os endpoints abaixo.

**_antes de começar..._**

1. Feche todas as janelas não necessárias.
2. Compartilhe toda a sua tela.
3. Desative qualquer IA de apoio ao desenvolvimento.
4. Crie um repositório no Github.

## Contexto

Imagine que você está criando uma API para um sistema de gerenciamento de tarefas pessoais. Cada tarefa possui os seguintes campos:

- **id**: identificador único (UUID).
- **title**: título da tarefa (obrigatório).
- **description**: descrição da tarefa (opcional).
- **completed**: booleano indicando se a tarefa está concluída ou não (padrão: false).

## Funcionalidades da API

Sua API deve implementar os seguintes endpoints:

1. **Criar uma nova tarefa**
   - **POST /tasks**
   - Request body:
     ```json
     {
       "title": "Titulo da tarefa",
       "description": "Descricao da tarefa"
     }
     ```
   - Response:
     ```json
     {
       "id": "<UUID>",
       "title": "Titulo da tarefa",
       "description": "Descricao da tarefa",
       "completed": false
     }
     ```

2. **Listar todas as tarefas**
   - **GET /tasks**
   - Response:
     ```json
     [
       {
         "id": "<UUID>",
         "title": "Titulo da tarefa",
         "description": "Descricao da tarefa",
         "completed": false
       }
     ]
     ```

3. **Atualizar o status de uma tarefa para concluída**
   - **PATCH /tasks/:id/complete**
   - Response:
     ```json
     {
       "id": "<UUID>",
       "title": "Titulo da tarefa",
       "description": "Descricao da tarefa",
       "completed": true
     }
     ```

4. **Excluir uma tarefa**
   - **DELETE /tasks/:id**
   - Response:
     ```json
     {
       "message": "Task deleted successfully."
     }
     ```

## Critérios de Avaliação

Sua solução será avaliada com base nos seguintes aspectos:

1. **Organização do código**:
   - Estrutura simples do projeto.
   - Uso de boas práticas com TypeScript.

2. **Implementação**:
   - A API está funcional e atende aos requisitos.
   - Uso de um banco em memória simples (JSON armazenado em variável).

3. **Tratamento de erros**:
   - Validação de entradas obrigatórias (ex.: title).
   - Respostas adequadas em casos de erro (ex.: tarefa não encontrada).

4. **Simplicidade e clareza**:
   - Implementação clara e objetiva.

## ✅ Entrega

Ao final do desafio, a API deve estar funcional com os seguintes arquivos principais:

1. **package.json** com as dependências utilizadas.
2. **server.ts** ou **index.ts** contendo a inicialização da API.
3. **tasks.ts** com a lógica principal (armazenamento e manipulação das tarefas).
4. **routes/tasks.routes.ts** contendo as rotas da aplicação.

**Para entregar...**

1. Envie seu código para o repositório criado no início do desafio.
2. Conceda acesso ao repositório para o usuário [`@marcosleal-prd`](https://github.com/marcosleal-prd).

## Dicas

- Use bibliotecas como **uuid** para gerar IDs únicos.
- Utilize uma estrutura simples sem complexidade de banco de dados.
- Valide apenas os campos obrigatórios.
- Realize commits sempre que possível.


---

**Nota**: O framework a ser utilizado é de livre escolha, como **Express**, **NestJS**, **Koa** ou qualquer outro de preferência.

**Boa sorte!** 🚀
