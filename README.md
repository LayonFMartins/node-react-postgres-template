## node-react-postgres-template

Principais tecnologias escolhidas para o template:

| Banco de Dados | Frontend                  | Backend                        |
| -------------- | ------------------------- | ------------------------------ |
| PostgreSQL     | React + Typescript + Vite | Node.js + Express + Typescript |

## Banco de Dados

Utiliza o PostgreSQL como Sistema Gerenciador de Banco de Dados Relacional (SGBD), com hospedagem na plataforma [Neon](https://neon.com/).

A comunicação com o banco de dados é realizada pelo backend utilizando a biblioteca `pg` [[node-postgres](https://node-postgres.com/)] para estabelecer a conexão e executar comandos os comandos SQL.

As credenciais de acesso são armazenadas em variáveis de ambiente, evitando sua exposição no código-fonte.

## Guia de Instalação

Para instalar o projeto corretamente, certifique-se de que os requisitos abaixo estão instalados:

## Pré-requisitos

- node.js 22.x
- npm 
- git

### Linux

 Para instalar o Node.js com o npm no Linux: 

1. `sudo apt update`
2. `sudo apt install -y curl`
3. `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash`
4. Feche e abra o terminal novamente.
5. `nvm install 22`
6. Defina como padrão: `nvm alias default 22` e `nvm use 22`

O npm já vem incluído na instalação do Node.js pelo NVM, então não é necessário instalá-lo separadamente.

## Git Hub

Na sequência escolha uma pasta em seu computador e clone o repositório do projeto:

    git clone https://github.com/LayonFMartins/incluirnometemplate

## Instalação do Projeto

Para o banco de dados vamos usar a credencial de conexão da plataforma Neon.
<br>
 **Não compartilhe essa variável com IA, por e-mail e/ou similares. Nem inclua arquivos .env em commits.**



Abra o terminal na pasta raiz do projeto. 

1. Execute: `npm ci`
2. Copie o .env: `cp backend/.env.example backend/.env`
3. Abra `backend/.env` no editor e preencha `DATABASE_URL` com a credencial de desenvolvimento autorizada do Banco de Dados hospedado na Neon.
4. Em seguida `npm run dev:frontend` e `npm run dev:backend` em dois terminais **separados**.
5. Teste `http://localhost:5173` e `http://localhost:3000/api/health/database`
