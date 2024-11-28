# **Java ScreenMatch**  
Um projeto desenvolvido em Java que consome a API OMDb para buscar informações de filmes e séries, organiza os dados em objetos e os salva em um arquivo JSON. Este repositório foi criado para demonstrar o uso de conceitos como consumo de APIs, manipulação de dados JSON e estruturação modular de código.

---

## **Recursos do Projeto**
- **Consumo de API**: Integração com a [API OMDb](https://www.omdbapi.com/) para obter informações detalhadas sobre filmes e séries.
- **Manipulação de JSON**: Uso da biblioteca Gson para converter dados JSON em objetos Java e vice-versa.
- **Organização Modular**: Separação do código em classes de serviço para melhorar a legibilidade e reutilização.
- **Persistência de Dados**: Salvamento das informações obtidas em um arquivo `filmes.json`.

---

## **Pré-requisitos**
- **Java**: JDK 11 ou superior.
- **Maven**: Para gerenciar dependências.
- **Chave de API OMDb**: Obtenha sua chave em [OMDb API](https://www.omdbapi.com/apikey.aspx).

---

## **Configuração e Execução**

### 1. **Clone o Repositório**
```bash
git clone https://github.com/GU1LHERMESILV4/JavaScreenMatch.git
cd JavaScreenMatch
```

### 2. **Configure a Chave de API**
- Localize a URL de requisição no código (`ApiService`).
- Substitua `YOUR_API_KEY` pela sua chave de API OMDb.

Exemplo:
```java
String endpoint = "https://www.omdbapi.com/?t=" + searchTerm.replace(" ", "+") + "&apikey=YOUR_API_KEY";
```

### 3. **Compile o Projeto**
- Use o Maven para compilar e resolver dependências:
```bash
mvn clean install
```

### 4. **Execute o Programa**
- Execute a classe principal:
```bash
java -cp target/JavaScreenMatch-1.0.jar br.com.alura.screenmatch.Principal.PrincipalComBusca
```

---

## **Como Usar**
1. Execute o programa no terminal.
2. Digite o nome de um filme ou série quando solicitado.
3. O programa buscará as informações na API OMDb.
4. Os dados serão exibidos no console e salvos no arquivo `filmes.json`.
5. Digite **"sair"** para encerrar o programa.

---

## **Estrutura do Projeto**
```
JavaScreenMatch/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── br/com/alura/screenmatch/
│   │   │   │   ├── Principal/
│   │   │   │   │   └── PrincipalComBusca.java  # Classe principal
│   │   │   │   ├── excecao/                   # Exceções customizadas
│   │   │   │   ├── modelos/                   # Modelos de dados
│   │   │   │   └── services/                  # Serviços para API, Entrada e Arquivo
│   │   └── resources/
│   │
├── pom.xml                                     # Configuração do Maven
├── filmes.json                                 # Arquivo gerado com dados salvos
└── README.md                                   # Documentação do projeto
```

---

## **Dependências**
O projeto utiliza as seguintes dependências, gerenciadas pelo Maven:
- **Gson**: Para manipulação de JSON.
```xml
<dependency>
    <groupId>com.google.code.gson</groupId>
    <artifactId>gson</artifactId>
    <version>2.8.9</version>
</dependency>
```
**Divirta-se explorando o mundo do cinema com o Java ScreenMatch!** 🎥
