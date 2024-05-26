[DemoShopping.postman_test_run.json](https://github.com/VikaDov/api/files/15447650/DemoShopping.postman_test_run.json)# Тестирование API
1. Postman: вызов методов для Products, Users, Cart, Orders и Payment:  https://www.postman.com/grey-crescent-917725/workspace/my-workspace/collection/30810094-9de6a186-98b8-4d64-be75-994dec930c56?action=share&creator=30810094
2. Прогон Products: [Up{
	"id": "72dd4fc4-0cf1-4226-ba53-08ba172f52d7",
	"name": "DemoShopping",
	"timestamp": "2024-05-26T13:43:13.312Z",
	"collection_id": "30810094-9de6a186-98b8-4d64-be75-994dec930c56",
	"folder_id": "30810094-a229e9cd-2ceb-4bf3-a7c8-40c303f86da0",
	"environment_id": "0",
	"totalPass": 36,
	"delay": 0,
	"persist": true,
	"status": "finished",
	"startedAt": "2024-05-26T13:43:10.029Z",
	"totalFail": 7,
	"results": [
		{
			"id": "78745961-e1ac-44c7-87a7-ef97996a031b",
			"name": "Вывод списка всех товаров",
			"url": "https://qa.demoshopping.ru/products",
			"time": 158,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус код 200": true
			},
			"testPassFailCounts": {
				"Статус код 200": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				158
			],
			"allTests": [
				{
					"Статус код 200": true
				}
			]
		},
		{
			"id": "d93a1f02-320f-44ce-a3ac-6f58375b30d9",
			"name": "Добавление нового товара",
			"url": "https://qa.demoshopping.ru/add-product",
			"time": 112,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус код 200": true,
				"Введены валидные данные для добавления нового товара": true,
				"ID товара сохранен в переменной коллекции": true
			},
			"testPassFailCounts": {
				"Статус код 200": {
					"pass": 1,
					"fail": 0
				},
				"Введены валидные данные для добавления нового товара": {
					"pass": 1,
					"fail": 0
				},
				"ID товара сохранен в переменной коллекции": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				112
			],
			"allTests": [
				{
					"Статус код 200": true,
					"Введены валидные данные для добавления нового товара": true,
					"ID товара сохранен в переменной коллекции": true
				}
			]
		},
		{
			"id": "845ae345-897a-49e2-8da1-40bd8e9d47cd",
			"name": "Ввод числа в название товара при добавлении товара (400)",
			"url": "https://qa.demoshopping.ru/add-product",
			"time": 16,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {
				"Статус код 400": true,
				"Наличие ключа 'name'": true,
				"Значение ключа 'name' является строкой": false
			},
			"testPassFailCounts": {
				"Статус код 400": {
					"pass": 1,
					"fail": 0
				},
				"Наличие ключа 'name'": {
					"pass": 1,
					"fail": 0
				},
				"Значение ключа 'name' является строкой": {
					"pass": 0,
					"fail": 1
				}
			},
			"times": [
				16
			],
			"allTests": [
				{
					"Статус код 400": true,
					"Наличие ключа 'name'": true,
					"Значение ключа 'name' является строкой": false
				}
			]
		},
		{
			"id": "f1202562-aeec-4d04-8894-f55ba515ebae",
			"name": "Ввод строки в цену товара при добавлении товара (400)",
			"url": "https://qa.demoshopping.ru/add-product",
			"time": 16,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {
				"Статус код 400": true,
				"Наличие ключа 'price'": true,
				"Значение ключа 'price' является числом": false
			},
			"testPassFailCounts": {
				"Статус код 400": {
					"pass": 1,
					"fail": 0
				},
				"Наличие ключа 'price'": {
					"pass": 1,
					"fail": 0
				},
				"Значение ключа 'price' является числом": {
					"pass": 0,
					"fail": 1
				}
			},
			"times": [
				16
			],
			"allTests": [
				{
					"Статус код 400": true,
					"Наличие ключа 'price'": true,
					"Значение ключа 'price' является числом": false
				}
			]
		},
		{
			"id": "56f7e2d0-b9c8-4f30-910a-311a4f1b02d4",
			"name": "Поиск товара по ID",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 117,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Path Variable 'productId' существует и имеет значение": true,
				"Статус код 200": true,
				"Path Variable 'productId' используется в URL запроса": true
			},
			"testPassFailCounts": {
				"Path Variable 'productId' существует и имеет значение": {
					"pass": 1,
					"fail": 0
				},
				"Статус код 200": {
					"pass": 1,
					"fail": 0
				},
				"Path Variable 'productId' используется в URL запроса": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				117
			],
			"allTests": [
				{
					"Path Variable 'productId' существует и имеет значение": true,
					"Статус код 200": true,
					"Path Variable 'productId' используется в URL запроса": true
				}
			]
		},
		{
			"id": "b23e787a-c8e1-4d3b-828f-db3a9019388c",
			"name": "Ввод спецсимволов в ID при поиске товара по ID (400)",
			"url": "https://qa.demoshopping.ru/products/id/@$%^",
			"time": 36,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {
				"Path Variable 'productId' существует и имеет значение": true,
				"Path Variable 'productId' содержит число": false,
				"Статус код 400": true
			},
			"testPassFailCounts": {
				"Path Variable 'productId' существует и имеет значение": {
					"pass": 1,
					"fail": 0
				},
				"Path Variable 'productId' содержит число": {
					"pass": 0,
					"fail": 1
				},
				"Статус код 400": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				36
			],
			"allTests": [
				{
					"Path Variable 'productId' существует и имеет значение": true,
					"Path Variable 'productId' содержит число": false,
					"Статус код 400": true
				}
			]
		},
		{
			"id": "5dd691c6-6293-4f1f-ab4f-2b3405a433e4",
			"name": "Ввод несуществующего ID товара при поиске товара по ID (404)",
			"url": "https://qa.demoshopping.ru/products/id/100000",
			"time": 37,
			"responseCode": {
				"code": 404,
				"name": "Not Found"
			},
			"tests": {
				"Path Variable 'productId' существует и имеет значение": true,
				"Статус код 404": true,
				"GET запрос не имеет тела": true
			},
			"testPassFailCounts": {
				"Path Variable 'productId' существует и имеет значение": {
					"pass": 1,
					"fail": 0
				},
				"Статус код 404": {
					"pass": 1,
					"fail": 0
				},
				"GET запрос не имеет тела": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				37
			],
			"allTests": [
				{
					"Path Variable 'productId' существует и имеет значение": true,
					"Статус код 404": true,
					"GET запрос не имеет тела": true
				}
			]
		},
		{
			"id": "98d4236e-6275-4bde-80cf-2357b3b51913",
			"name": "Полное обновление товара по ID",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 80,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Успешний PUT запрос": true,
				"Введены валидные данные для полного обновления товара": true,
				"Запрос PUT содержит тело": true
			},
			"testPassFailCounts": {
				"Успешний PUT запрос": {
					"pass": 1,
					"fail": 0
				},
				"Введены валидные данные для полного обновления товара": {
					"pass": 1,
					"fail": 0
				},
				"Запрос PUT содержит тело": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				80
			],
			"allTests": [
				{
					"Успешний PUT запрос": true,
					"Введены валидные данные для полного обновления товара": true,
					"Запрос PUT содержит тело": true
				}
			]
		},
		{
			"id": "0e078ac5-715e-41fe-8008-33c6e868ef8b",
			"name": "Ввод числа в 'freeShipping' при полном обновлении товара (400)",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 11,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {
				"Статус код 400": true,
				"Наличие ключа 'freeShipping'": true,
				"Значение ключа 'freeShipping' является boolean": false,
				"Запрос PUT содержит тело": true
			},
			"testPassFailCounts": {
				"Статус код 400": {
					"pass": 1,
					"fail": 0
				},
				"Наличие ключа 'freeShipping'": {
					"pass": 1,
					"fail": 0
				},
				"Значение ключа 'freeShipping' является boolean": {
					"pass": 0,
					"fail": 1
				},
				"Запрос PUT содержит тело": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				11
			],
			"allTests": [
				{
					"Статус код 400": true,
					"Наличие ключа 'freeShipping'": true,
					"Значение ключа 'freeShipping' является boolean": false,
					"Запрос PUT содержит тело": true
				}
			]
		},
		{
			"id": "98be3c90-c54d-4c6a-a2bc-a0f8f431a65a",
			"name": "Полное обновление товара с несуществующим ID (404)",
			"url": "https://qa.demoshopping.ru/products/id/-100",
			"time": 300,
			"responseCode": {
				"code": 404,
				"name": "Not Found"
			},
			"tests": {
				"Path Variable 'productId' существует и имеет значение": true,
				"Path Variable 'productId' не является отрицательным числом": false,
				"Статус код 404": true,
				"Запрос PUT содержит тело": true
			},
			"testPassFailCounts": {
				"Path Variable 'productId' существует и имеет значение": {
					"pass": 1,
					"fail": 0
				},
				"Path Variable 'productId' не является отрицательным числом": {
					"pass": 0,
					"fail": 1
				},
				"Статус код 404": {
					"pass": 1,
					"fail": 0
				},
				"Запрос PUT содержит тело": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				300
			],
			"allTests": [
				{
					"Path Variable 'productId' существует и имеет значение": true,
					"Path Variable 'productId' не является отрицательным числом": false,
					"Статус код 404": true,
					"Запрос PUT содержит тело": true
				}
			]
		},
		{
			"id": "06142f2f-243a-49e0-8ee6-806f56b4eed8",
			"name": "Частичное обновление товара по ID",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 122,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Успешний PATCH запрос": true,
				"Введены валидные данные для частичного обновления товара": true,
				"Запрос PATCH содержит тело": true
			},
			"testPassFailCounts": {
				"Успешний PATCH запрос": {
					"pass": 1,
					"fail": 0
				},
				"Введены валидные данные для частичного обновления товара": {
					"pass": 1,
					"fail": 0
				},
				"Запрос PATCH содержит тело": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				122
			],
			"allTests": [
				{
					"Успешний PATCH запрос": true,
					"Введены валидные данные для частичного обновления товара": true,
					"Запрос PATCH содержит тело": true
				}
			]
		},
		{
			"id": "aaa95fe7-30a8-4946-a53b-138968fabc44",
			"name": "Частичное обновление товара по ID с пустым name  (400)",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 54,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {
				"Статус код 400": true,
				"Ключ 'name' существует и он не пустой": false,
				"Запрос PATCH содержит тело": true
			},
			"testPassFailCounts": {
				"Статус код 400": {
					"pass": 1,
					"fail": 0
				},
				"Ключ 'name' существует и он не пустой": {
					"pass": 0,
					"fail": 1
				},
				"Запрос PATCH содержит тело": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				54
			],
			"allTests": [
				{
					"Статус код 400": true,
					"Ключ 'name' существует и он не пустой": false,
					"Запрос PATCH содержит тело": true
				}
			]
		},
		{
			"id": "3c9b2953-353b-44f8-91c9-94a3cb8badce",
			"name": "Частичное обновление товара без тела запроса (500)",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 84,
			"responseCode": {
				"code": 500,
				"name": "Internal Server Error"
			},
			"tests": {
				"Статус код 500": true,
				"Запрос PATCH содержит тело": false
			},
			"testPassFailCounts": {
				"Статус код 500": {
					"pass": 1,
					"fail": 0
				},
				"Запрос PATCH содержит тело": {
					"pass": 0,
					"fail": 1
				}
			},
			"times": [
				84
			],
			"allTests": [
				{
					"Статус код 500": true,
					"Запрос PATCH содержит тело": false
				}
			]
		},
		{
			"id": "b935296c-95e0-4b91-93f3-f59a02bc5b6f",
			"name": "Удаление товара по ID",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 45,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Успешный DELETE запрос": true,
				"Введен валидный ID товара для его удаления": true,
				"Path Variable 'productId' используется в URL запроса": true
			},
			"testPassFailCounts": {
				"Успешный DELETE запрос": {
					"pass": 1,
					"fail": 0
				},
				"Введен валидный ID товара для его удаления": {
					"pass": 1,
					"fail": 0
				},
				"Path Variable 'productId' используется в URL запроса": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				45
			],
			"allTests": [
				{
					"Успешный DELETE запрос": true,
					"Введен валидный ID товара для его удаления": true,
					"Path Variable 'productId' используется в URL запроса": true
				}
			]
		},
		{
			"id": "12845503-6d2c-41c5-a230-7fb3b8641fd8",
			"name": "Удаление товара, который запрещен к удалению (403)",
			"url": "https://qa.demoshopping.ru/products/id/1",
			"time": 15,
			"responseCode": {
				"code": 403,
				"name": "Forbidden"
			},
			"tests": {
				"Статус код 403": true
			},
			"testPassFailCounts": {
				"Статус код 403": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				15
			],
			"allTests": [
				{
					"Статус код 403": true
				}
			]
		},
		{
			"id": "5c89ced7-2d74-4c26-919b-b1ccafc1eeb6",
			"name": "Удаление уже удаленного товара по ID (404)",
			"url": "https://qa.demoshopping.ru/products/id/10506",
			"time": 24,
			"responseCode": {
				"code": 404,
				"name": "Not Found"
			},
			"tests": {
				"Статус код 404": true
			},
			"testPassFailCounts": {
				"Статус код 404": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				24
			],
			"allTests": [
				{
					"Статус код 404": true
				}
			]
		}
	],
	"count": 1,
	"totalTime": 1227,
	"collection": {
		"requests": [
			{
				"id": "78745961-e1ac-44c7-87a7-ef97996a031b",
				"method": "GET"
			},
			{
				"id": "d93a1f02-320f-44ce-a3ac-6f58375b30d9",
				"method": "POST"
			},
			{
				"id": "845ae345-897a-49e2-8da1-40bd8e9d47cd",
				"method": "POST"
			},
			{
				"id": "f1202562-aeec-4d04-8894-f55ba515ebae",
				"method": "POST"
			},
			{
				"id": "56f7e2d0-b9c8-4f30-910a-311a4f1b02d4",
				"method": "GET"
			},
			{
				"id": "b23e787a-c8e1-4d3b-828f-db3a9019388c",
				"method": "GET"
			},
			{
				"id": "5dd691c6-6293-4f1f-ab4f-2b3405a433e4",
				"method": "GET"
			},
			{
				"id": "98d4236e-6275-4bde-80cf-2357b3b51913",
				"method": "PUT"
			},
			{
				"id": "0e078ac5-715e-41fe-8008-33c6e868ef8b",
				"method": "PUT"
			},
			{
				"id": "98be3c90-c54d-4c6a-a2bc-a0f8f431a65a",
				"method": "PUT"
			},
			{
				"id": "06142f2f-243a-49e0-8ee6-806f56b4eed8",
				"method": "PATCH"
			},
			{
				"id": "aaa95fe7-30a8-4946-a53b-138968fabc44",
				"method": "PATCH"
			},
			{
				"id": "3c9b2953-353b-44f8-91c9-94a3cb8badce",
				"method": "PATCH"
			},
			{
				"id": "b935296c-95e0-4b91-93f3-f59a02bc5b6f",
				"method": "DELETE"
			},
			{
				"id": "12845503-6d2c-41c5-a230-7fb3b8641fd8",
				"method": "DELETE"
			},
			{
				"id": "5c89ced7-2d74-4c26-919b-b1ccafc1eeb6",
				"method": "DELETE"
			}
		]
	}
}loading DemoShopping.postman_test_run.json…]()

