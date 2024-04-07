# Preparação de Ambiente Backend


## Requisitos para preparação

- Genrenciador de Pacotes Node o [NVM](https://duckduckgo.com).
- Instalar o Node na versão LTS.

### Criar projeto

- Criar uma nova pasta
- Criar um `package.json` (*Esse arquivo é responsavel para gerenciar dependências, configurações e scripts do seu projeto*)
  
  ```bash
    npm init -y
  ```
- Criar arquivos principal para o projetos `src/server.ts`

### Configurar Typescript

- Instalar Typescript como dependências de desenvolvimento.
  
  ```Bash
  npm install typescript --save-dev
  ```
- Instalar definição de tipagem par ao Node como dependencias de desenvolvimento
  
  ```Bash
  npm install @types/node --save-dev
  ```
- Arquivo TS config

  ```Bash
    npx tsc --init
  ```
- Configurar o `tsconfig.json` acessa: [tsc config bases](https://github.com/tsconfig/bases) e copiar a configuração recomendada de acordo com sua versão.
- adicionar no `tsconfig.json` - `"includes": ["src"]` isso fará com que o typescript observe os arquivos apara converter para javascript.
- Instalar o pacote tsx para executar os arquivo .ts e compilar para javascript.

  ```bash
  npm install tsx --save-dev
  ````
- Adiconar no `package.json` um novo comando de script -- `"dev": "tsx watch --env-file .env src/server.ts"`

### Instalação do framework

- Instalar o [Fastify](https://fastify.dev/).
 
    ```bash
      npm install fastify
    ```

- Validação de rotas instalar [Zod](https://www.npmjs.com/package/zod#from-npm-nodebun). e o plugin [Fastify Type Provider Zod](https://www.npmjs.com/package/fastify-type-provider-zod).
- Documentação de Rotas fastifySwagger e fastifySwaggerUI   
  
### Instalar ORM

- Instalar o [Prisma](https://www.prisma.io/docs/getting-started/quickstart).
