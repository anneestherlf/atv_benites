# Questão solicitada pelo professor Cristiano: Explique com suas palavras o funcionamento do models, controller e fale sobre endpoints no projeto.

Resposta: <br>
Models são as tabelas de dados do projeto. São os arquivos JavaScript responsáveis por representar e manipular os dados das entidades principais: nesse caso, alunos, cursos e professores.

Controller é responsável por transportar os dados para a parte visual do projeto. Nesse repositório, o controller é responsável por receber as requisições do usuário (quando você clica em "Adicionar", "Editar" ou "Deletar" professor), chamar os métodos do model (como o professor.js) e decidir qual página (view) mostrar como resposta.

Os endpoints são os "endereços" (caminhos/URLs) que o navegador usa para se comunicar com o servidor. Eles dizem para onde os dados do formulário devem ser enviados quando você clica em "Adicionar", "Editar" ou "Deletar".

No projeto, eu utilizei endpoints nos atributos action dos formulários (arquivos index.ejs) para adicionar, editar e deletar professores, alunos e cursos. Esses caminhos são usados pelo navegador para enviar os dados para o servidor.

---------------

# Sobre o projeto:

## Requisitos

- Node.js (versão X.X.X)
- PostgreSQL (versão X.X.X)

## Instalação

1. **Clonar o repositório:**

```bash
   git clone https://github.com/seu-usuario/seu-projeto.git
   cd seu-projeto
```

2. **Instalar as dependências:**
    
```bash
npm install
```
    
3. **Configurar o arquivo `.env`:**

Renomeie o arquivo `.env.example` para `.env` e configure as variáveis de ambiente necessárias, como as configurações do banco de dados PostgreSQL.
    

Configuração do Banco de Dados
------------------------------

1. **Criar banco de dados:**
    
    Crie um banco de dados PostgreSQL com o nome especificado no seu arquivo `.env`.
    
2. **Executar o script SQL de inicialização:**
    
```bash
npm run init-db
```
    
Isso criará as tabelas `users`, `aluno`, `curso` e `professor` no seu banco de dados PostgreSQL com UUID como chave primária e inserirá alguns registros de exemplo.
    

Funcionalidades
---------------

* **Padrão MVC:** Estrutura organizada em Model, View e Controller.
* **PostgreSQL:** Banco de dados relacional utilizado para persistência dos dados.
* **UUID:** Utilização de UUID como chave primária na tabela `users`.
* **Scripts com `nodemon`:** Utilização do `nodemon` para reiniciar automaticamente o servidor após alterações no código.
* **Testes:** Inclui estrutura básica para testes automatizados.

Scripts Disponíveis
-------------------

* `npm start`: Inicia o servidor Node.js.
* `npm run dev`: Inicia o servidor com `nodemon`, reiniciando automaticamente após alterações no código.
* `npm run test`: Executa os testes automatizados.
* `npm run test:coverage`: Executa os testes e gera um relatório de cobertura de código.

Estrutura de Diretórios
-----------------------

* **`config/`**: Configurações do banco de dados e outras configurações do projeto.
* **`controllers/`**: Controladores da aplicação (lógica de negócio).
* **`models/`**: Modelos da aplicação (definições de dados e interações com o banco de dados).
* **`routes/`**: Rotas da aplicação.
* **`tests/`**: Testes automatizados.
* **`views/`**: Views da aplicação (se aplicável).

Licença
-------

Este projeto está licenciado sob a Licença MIT.
