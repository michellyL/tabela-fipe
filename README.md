# Tabela FIPE

Projeto desenvolvido durante a formação de **Java: Trabalhando com lambdas, streams e Spring Framework** na ALURA, com o objetivo de praticar o consumo de APIs externas, manipulação de dados em JSON e aplicação dos conceitos de Java.

## Sobre o projeto

O **Tabela FIPE** é uma aplicação que permite consultar informações de veículos utilizando dados disponibilizados pela **API da Tabela FIPE**.

Ao executar o programa, o usuário pode escolher entre:

* 🚗 Carros
* 🏍️ Motos
* 🚚 Caminhões

A partir da categoria escolhida, é possível consultar as marcas disponíveis, selecionar uma marca, pesquisar modelos e, por fim, consultar os valores do veículo de acordo com os diferentes anos disponíveis.

## ⚙️ Funcionalidades

O projeto permite:

1. Escolher o tipo de veículo que deseja consultar;
2. Listar as marcas disponíveis;
3. Selecionar uma marca pelo código;
4. Listar os modelos pertencentes à marca escolhida;
5. Pesquisar modelos utilizando parte do nome;
6. Selecionar um modelo pelo código;
7. Consultar os anos disponíveis para o modelo;
8. Exibir os valores dos veículos para cada ano encontrado.


## 🌐 Consumo da API

A aplicação utiliza a API pública da **Parallelum FIPE** para realizar as consultas.

As informações são obtidas através de requisições HTTP e retornadas no formato JSON.

O projeto utiliza `HttpClient` para realizar as requisições:

```java
HttpClient client = HttpClient.newHttpClient();
```

Depois, os dados recebidos são convertidos de JSON para objetos Java utilizando **Jackson**.

## 🧩 Estrutura do projeto

O projeto foi organizado separando as principais responsabilidades:

```text
src
└── main
    └── java
        └── br.com.alura.TabelaFipe
            ├── model
            │   ├── Dados.java
            │   ├── Modelos.java
            │   └── Veiculo.java
            │
            ├── principal
            │   └── Principal.java
            │
            ├── service
            │   ├── ConsumoApi.java
            │   ├── ConverteDados.java
            │   └── IConverteDados.java
            │
            └── TabelaFipeApplication.java
```

### 📦 `model`

Contém os `records` responsáveis por representar os dados recebidos da API, como marcas, modelos e informações dos veículos.

### 🔧 `service`

Responsável pelas funcionalidades relacionadas ao consumo e conversão dos dados.

* `ConsumoApi` → realiza as requisições HTTP;
* `ConverteDados` → converte os dados JSON para objetos Java;
* `IConverteDados` → define os métodos de conversão.

### 🖥️ `principal`

Contém a classe responsável pelo fluxo principal da aplicação, interação com o usuário e realização das consultas.

## 🛠️ Tecnologias utilizadas

* ☕ **Java 17**
* 🌱 **Spring Boot**
* 📦 **Maven**
* 🌐 **API REST**
* 🔄 **HttpClient**
* 🗂️ **JSON**
* 🔧 **Jackson**
* 💻 **IntelliJ IDEA**

## 📚 Conceitos praticados

Durante o desenvolvimento do projeto, foram praticados conceitos importantes de Java, como:

* Programação Orientada a Objetos;
* Records;
* Interfaces;
* Generics;
* Listas e coleções;
* Stream API;
* Expressões lambda;
* `HttpClient`;
* Requisições HTTP;
* Consumo de APIs REST;
* Manipulação de JSON;
* Desserialização de objetos;
* Organização do código em pacotes;
* Maven e gerenciamento de dependências.
