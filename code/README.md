# global-dating

A Nodejs project

## setup

### install packages

```
$ npm install
```

### setup env

create `.env` from `.env.example`.

```
$ cp .env.example .env
$ vi .env
```

### setup database
1. Install mysql

2. Copy database's config
```
$ cp config/config.json.example config/config.json
```

3. Change database's config in `config/config.json`

4. Create and migrate db
```
npx sequelize-cli db:create
npx sequelize-cli db:migrate
```
5. Seeds DB
```
npx sequelize-cli db:seed:all
```
## run

### dev server

```
$ npm run dev
```

### run server with ssl on local
```
$ npm install ngrok -g
$ ngrok http $PORT
```

### Deployment

```
Deploy code base from develop branch: `cap staging deploy`
Deploy code from branch A: `cap staging deploy DEPLOY_REF=A`
```

