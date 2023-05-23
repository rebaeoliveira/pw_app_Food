# app_Food
# Preparação do ambiente de desenvolvimento:

## Terminal do Visual Studio Code:

# Instalar o pacote npm (é criada a pasta node_modules)
npm install

# Instalar o pacote yarn
npm i -g yarn

# Inicializar o programa
yarn dev

# Caso ocorra erro ao conectar no mongoDB:
# (1ª opção):
Abrir um novo terminal no Visual Studio Code
docker ps -a
docker run -p 27017:27017 mongo
Voltar ao 1º terminal

# (2ª opção):
docker ps -a
docker rm (CONTEINER ID)
docker run -p 27017:27017 mongo

# (3ª opção):
docker run --name mongo --volume /save/mongo:/data/db -p 27017:27017 -d mongo

# Inicializar o programa
yarn dev

## Insomnia:
Criar uma nova pasta chamada Categories;
# Para cadastrar uma categoria:
New HTTP Requests;
POST http://localhost:4000/categories, text JSON;
Clicar em Send
[
	{
		"_id": "646d47626c71592bc8656155",
		"name": "beer",
		"icon": "🍺",
		"__v": 0
	},
	{
		"_id": "646d47e46c71592bc8656157",
		"name": "pizza",
		"icon": "🍕",
		"__v": 0
	},
	{
		"_id": "646d47ea6c71592bc8656159",
		"name": "pizza",
		"icon": "🍕",
		"__v": 0
	},
	{
		"_id": "646d48986c71592bc865615c",
		"name": "hamburger",
		"icon": "🍔",
		"__v": 0
	}
]
# Para listar:
New HTTP Requests;
GET http://localhost:4000/categories;
Clicar em send



# Para cadastrar um produto:
New HTTP Requests;
POST http://localhost:4000/products, multiparts form;
name: Coca-Cola
description: Coca-Cola gelada
image: coca-cola
price: 10
category: 646d48986c71592bc865615c
Clicar em Send
[
	{
		"_id": "646d47626c71592bc8656155",
		"name": "beer",
		"icon": "🍺",
		"__v": 0
	},
	{
		"_id": "646d47e46c71592bc8656157",
		"name": "pizza",
		"icon": "🍕",
		"__v": 0
	},
	{
		"_id": "646d47ea6c71592bc8656159",
		"name": "pizza",
		"icon": "🍕",
		"__v": 0
	},
	{
		"_id": "646d48986c71592bc865615c",
		"name": "hamburger",
		"icon": "🍔",
		"__v": 0
	}
]
# Para listar:
New HTTP Requests;
GET http://localhost:4000/products;
Clicar em send
