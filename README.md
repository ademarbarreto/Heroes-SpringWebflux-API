

## Desenvolvimento de API para cadastrar super heróis com Spring WebFlux utilizando o Banco de Dados DynamoDB da AWS usado localmente. 

### Stack utilizada:

  * Java8
  * Spring Webflux
  * Spring Data
  * DynamoDB
  * Junit
  * sl4j
  * Reactor

 

## Abrir conta na AWS:

- Baixar o AWS CLI para ser utilizado na máquina local

  [AWS CLI - Interface de linha de comando - Amazon Web Services](https://aws.amazon.com/pt/cli/)

- Através do IAM criar um usuário e baixar as credenciais do mesmo (AWS Access Key ID e AWS Access Key ID )

-  Configurar as credenciais através do comando 

  **aws configure**

  AWS Access Key ID [******************]:
  AWS Secret Access Key [*******************]:
  Default region name [sa-east-1]:
  Default output format [json]:



## IDE utilizada: 

- Intelijj com gerenciador de pacotes Maven

### Slides de palestra: 

- https://speakerdeck.com/kamilahsantos/live-coding-dio-api-de-herois-com-spring-webflux

### Palestra gravada: 

- https://www.youtube.com/watch?v=1VllPZYn6RI&t=3257s

### Executar DynamoDB: 

 Na pasta em que o jar está baixado: 

- **java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb**

$ java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
Initializing DynamoDB Local with the following configuration:
Port:   8000
InMemory:       false
DbPath: null
SharedDb:       true
shouldDelayTransientStatuses:   false
CorsParams:     *



Para listar as tabelas criadas:  

- **aws dynamodb list-tables --endpoint-url http://localhost:8000**



$ aws dynamodb list-tables --endpoint-url http://localhost:8000
{
    "TableNames": [
        "Heroes_Api_Table"
    ]
}

### Documentação gerada pela aplicação swagger:

-  http://localhost:8080/swagger-ui-heroes-reactive-api.html



![image-20211202163000747](C:\Users\adema\AppData\Roaming\Typora\typora-user-images\image-20211202163000747.png)



## Teste da API com o POSTMAN:



- [API HEROES WEB FLUX (getpostman.com)](https://documenter.getpostman.com/view/17990544/UVJfjvHN)



![image-20211202164441979](C:\Users\adema\AppData\Roaming\Typora\typora-user-images\image-20211202164441979.png)
