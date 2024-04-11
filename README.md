## Polls

O Polls é um projeto focado em back-end para a criação de um sistema de votações. Foram usadas as tecnologias Node.js Prisma, Zod e o Fastify.


#### Criando o banco de dados

>[!Terminal]
>```
>npx prisma migrate
>```

#### Iniciando o Docker

>[!Terminal]
>```
>docker compose up -d
>```

#### Iniciando o back-end

>[!Terminal]
>```
>npm run dev
>```


### Rotas

#### Criar enquete

**Método:** POST 
**URL:** http://localhost:3333/polls

**Json**
```
{
	"title": "Qual melhor comida?", 
	"options": ["Pizza", "Lazanha", "Aparmegiana", "Macarrão"]
}
```

#### Pesquisa uma enquete

**Método:** GET 
**URL:** http://localhost:3333/polls/{__pollId__}

#### Votar em uma enquete

**Método:** POST
**URL:** http://localhost:3333/polls/{__pollId__}/votes

**Json** 
```
{
	"pollOptionId": "{pollOptionId}"
}
```