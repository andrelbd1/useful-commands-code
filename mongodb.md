### [MongoDB](https://docs.mongodb.com/manual/) commands

- Iniciar MongoDb
````bash
mongo --quiet
````

- Exibindo Databases
````bash
show dbs
````

- Usando/Criando Database
````bash
use name_dabase
````

- Removendo Database
````bash
db.dropDatabase()
````

- Mostrando as coleções da database
````bash
show collections
````

- Criando coleções
````bash
db.createCollection("name_collection")
````

- Mostrando a que documento pertence a coleção
````bash
db.name_collection
````

- Inserindo registros na coleção
````bash
db.name_collection.insert({attribute: 'value', attribute1:['value1','value2'], attribute2: 'value3'})
````

- Mostrando todos os registros de uma coleção
````bash
db.name_collection.find()
````

- Mostrando todos os registros de uma coleção sem retornar o atributo '_id'
````bash
db.name_collection.find({}, {_id:0}) // O primeiro argumento é a query e o segundo é quais campos queremos ou não retornar.
````

- Mostrando todos os registros de uma coleção mostrando apenas alguns atributos
````bash
db.name_collection.find({}, {_id:0, attribute: 1, attribute1: 1})
````

- Mostrando a quantidade de valores de um atributo
````bash
db.name_collection.find({attribute: 'value'}).count()
db.name_collection.find({attribute1: {$in: ['value2']} }).count()
````

- Simulando um "LIKE" do SQL e buscar valores por parte do seu nome. 
````bash
db.name_collection.find({attribute: /UF(.*)/ }) // Valores que começam com as letras 'UF'
````

- Atualizando um registro da coleção
````bash
db.name_collection.update({attribute: 'value'}, {$set: {attribute2: 'value4'} })
````

- Removendo um registro da coleção
````bash
db.name_collection.remove({attribute: 'value'})
````

- Para ver a implementação de um método no shell db.<method name> without the parenthesis (())
````bash
db.method_name
````