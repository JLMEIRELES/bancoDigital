# bancoDigital

Objetivo da API é representar um sistema bancario com algumas ferramentas, cadastrar clientes, como criar contas para estes clientes, fazer transações entre as contas criadas, além de ser capaz de exibir 
um extrato que para cada conta mostrando todas as transações feitas.

```- Requisitos para testar a aplicação```

* Necessário ter o Java 16 instalado em sua máquina.
* Uma IDE de sua preferência 
* Um programa que seja capaz de disparar requisições através dos métodos implementados na API(Postman por exemplo)

```-Instruções para teste```

É possível rodar a aplicação atraves da IDE de sua preferência, b
astando esperar o download das dependencias utilizadas que estão no arquivo pom.xml e rodar
a aplicação como Springboot Aplication

Também pode ser feito executando o arquivo .jar disponibilizado neste repositório. 
Para isso é necessário: Abrir o Local em que está baixado o executável .jar e clicar nele para dar inicio a aplicação. 
Contudo, para ter certeza que teve sucesso em executar ela como esperado, 
é recomendado fazer isso pelo terminal :

* Abra o cmd
* abra o diretório do projeto
* digite "Java -jar banco-0.0.1-SNAPSHOT.jar"
* Se a porta 8080 não estiver em uso, tudo deverá funcionar corretamente

**MÉTODO PARA CRIAR CLIENTE**

Para conseguir criar clientes será necessario passar como requisição no postman: 'localhost:8080/clientes' 
ultilizando o metodo POST, passando como parametro nome, e cpf. Exemplo: 

``` 
{
"nome" : "Joao",
"cpf" : "70801167167"
}
```

**MÉTODO PARA CRIAR CONTA**

Para conseguir criar as contas será necessario passar como requisição no postman: 'localhost:8080/contas' 
ultilizando o metodo POST, passando como parametro cpf, numero, agencia. Exemplo:

``` 
{
"cpf" : "70801167167",
"numero" : 222,
"agencia" 222
}
```

**MÉTODO PARA FAZER UM SAQUE**

Para conseguir fazer um saque necessario passar como requisição no postman: 'localhost:8080/contas/saca' 
ultilizando o metodo POST, passando como parametro numero da conta, e o valor a ser sacado. Exemplo:

``` 
{
"numero" : 222,
"valor" : 80
}
```

**MÉTODO PARA FAZER UM DEPÓSITO**

Para conseguir fazer um depósito será necessario passar como requisição no postman: 'localhost:8080/contas/deposita' 
ultilizando o metodo POST, passando como parametro numero da conta, e o valor a ser depositado. Exemplo:

``` 
{
"numero" : 222,
"valor" : 80
}
```

**MÉTODO PARA FAZER UMA TRANSFERÊNCIA**

Para conseguir fazer uma transferência será necessario passar como requisição no postman: 'localhost:8080/contas/transfere' 
ultilizando o metodo POST, passando como parametro numero da conta de origem, numero da conta de destino, e o valor a ser sacado. Exemplo:

``` 
{
"numContaSaida" : 222,
"numContaEntrada" : 111,
"valor" : 80
}
```

**MÉTODO PARA EXIBIR UM EXTRATO**

Para conseguir exibir o extrato será necessario passar como requisição no postman: 'localhost:8080/contas/extrato' 
ultilizando o metodo GET, passando como parametro o numero da conta que deseja exibir o extrato. Exemplo:

``` 
{
"numero" : 222,
}
```

**MÉTODOS GET**

É possível exibir todas as contas e clientes cadastrados, utilizando o método GET sem parâmetros em 'localhost:8080/contas' ou 'localhost:8080/clientes'

