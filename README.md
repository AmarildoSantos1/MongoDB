# MongoDB
Código em Java com uso de XML, em que conecta com banco de dados no MongoDB
O código está hospedado em , "localhost:27017" na classe "App.java" na linha 23;
Para alterar o banco de dados é em "POM.XML" na linha 28 em diante : https://mvnrepository.com/artifact/org.mongodb/mongo-java-driver/3.12.14 , o código usado para conexão foi:
<!-- https://mvnrepository.com/artifact/org.mongodb/mongo-java-driver -->
<dependency>
    <groupId>org.mongodb</groupId>
    <artifactId>mongo-java-driver</artifactId>
    <version>3.12.14</version>
</dependency>
Para manipular os dados de produto é na classe "App.java" na linha 29 em diante:
Para adicionar: collection.insertOne(new Produto(1,"Arroz", 5));
Para atualizar: collection.updateOne(new Document("_id", 1), set ("descricao","Arroz Parbolizado"));
Para remover/deletar: collection.deleteOne(new Document("descricao","Arroz Parbolizado")); 
Feito isto. Para conectar ao MongoDb , use o MongoDb.compass: https://www.mongodb.com/try/download/shell , o usado em questão é o .exe 
Instalado. Inicie a conexão , crie um database e coloque as seguintes informações 1-"exemplo" 2-"Produto"
Rode o programa "app.java", e "find" no mongodb  e será printado o seu dado
Importação de biblioteca foi usada : http://mongodb.github.io/mongo-java-driver/3.12/bson/pojos/
