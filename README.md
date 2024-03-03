# Sistema de Gerenciamento de Doações de Sangue

Este projeto é um sistema de gerenciamento de doações de sangue. Ele facilita o registro e a gestão de doadores, locais de coleta, e as doações realizadas, fornecendo uma interface completa de CRUD (Create, Read, Update, Delete) para todas as tabelas envolvidas.

## Estrutura do Projeto

O projeto é dividido em duas partes principais:
- `server`: Backend implementado com Node.js e Express, usando Prisma como ORM para interações com o banco de dados.
- `web-vite`: Frontend criado com React e TypeScript, empregando Vite como ferramenta de construção.

## Modelo de Dados

![CSI606-sistema-doacao-sangue (2)](https://github.com/Andre023/Projeto-doacao-sangue/assets/89217876/bcedf3ab-05a1-472e-9d36-57f7a529e92d)

O modelo de dados é composto pelas seguintes tabelas principais:
- `locais_coleta`: Armazena informações dos locais onde as doações são realizadas.
- `doacoes`: Registra os detalhes das doações de sangue, associando doadores e locais de coleta.
- `pessoas`: Contém informações sobre os doadores de sangue.
- `cidades` e `estados`: Gerenciam informações de localização para doadores e locais de coleta.
- `tipos_sanguineos`: Registra os diferentes tipos sanguíneos dos doadores.

## Pré-requisitos

Antes de instalar o projeto, você deve ter o Node.js e o npm/yarn instalados em sua máquina.

## Instalação

Primeiramente, clone o repositório do GitHub:

```bash
git clone https://github.com/UFOP-CSI477/csi606-2023-02-atividades-Andre023.git
```

Configuração do Backend

Navegue até a pasta do servidor e instale as dependências:

```bash
cd server
npm install
```

Crie um arquivo .env baseando-se no .env.example e configure as variáveis de ambiente necessárias para o seu ambiente de desenvolvimento.
Exemplo:

```bash
DATABASE_URL = "file:./aplicacao.sqlite"
```

Execute as migrações do banco de dados:

```bash
npx prisma migrate dev
```

## Configuração do Frontend

Navegue até a pasta do frontend e instale as dependências:

```bash
cd web-vite
npm install
```

## Executando o Projeto

Para executar o backend, utilize:

```bash
npm start
```

Para executar o frontend, em uma nova janela do terminal, use:

```bash
npm run dev
```

O sistema de gerenciamento de doações de sangue estará acessível através do navegador no endereço http://localhost:5173/.
