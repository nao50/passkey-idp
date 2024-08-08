## setup project

```bash
$ nest new passkey-idp
$ npm run start:dev
```

# setup db

```bash
$ cd db && docker compose up -d
```

# env
```bash
$ npm install -D dotenv-cli
$ npm install -D @nestjs/config
```

# setup prisma

```bash
$ npm install -D prisma
$ npm install @prisma/client
$ npx prisma init
$ # 
$ npx dotenv -e ./env/.env.dev npx prisma migrate dev --name "init"
$ npx nest generate module prisma
$ npx nest generate service prisma
```

```bash
$ npx prisma format
$ npx prisma db seed
```

# setup swagger

```bash
$ npm install -D @nestjs/swagger swagger-ui-express
```

# setup validator

```bash
$ npm install class-validator class-transformer
```

# setup API

```bash
$ npx nest generate resource user
$ npx nest generate resource auth
```