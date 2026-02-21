# Lanchonete

## Descrição
Este repositório contém um projeto Java que simula um sistema de lanchonete. Ele utiliza uma arquitetura em camadas (N-Layer) para organizar o código e as responsabilidades.

## Tecnologias Utilizadas
- **Java**: Linguagem de programação principal.
- **Maven**: Ferramenta de automação de build e gerenciamento de dependências.
- **JUnit**: Framework para testes unitários (versão 3.8.1).

## Estrutura do Projeto
A estrutura do projeto segue o padrão Maven e uma organização em camadas:
- `pom.xml`: Arquivo de configuração do Maven, definindo dependências e informações do projeto.
- `src/main/java/com/lanchenlayer/`: Contém o código-fonte principal da aplicação.
  - `Console.java`: Provavelmente a classe principal que interage com o usuário via console.
  - `applications/ProdutoApplication.java`: Lógica de aplicação relacionada a produtos.
  - `entities/Produto.java`: Classe de entidade para representar um produto.
  - `facade/ProdutoFacade.java`: Camada de fachada para simplificar a interação com o sistema de produtos.
  - `interfaces/IProdutoRepository.java`, `IProdutoService.java`: Interfaces que definem contratos para repositórios e serviços de produto.
  - `repositories/ProdutoRepository.java`, `ProdutoRepositoryMySQL.java`: Implementações de repositório para persistência de produtos (incluindo uma versão MySQL).
  - `services/ProdutoService.java`, `ProdutoServiceDropbox.java`: Implementações de serviço para a lógica de negócios de produtos (incluindo uma versão com Dropbox).
- `src/main/resources/images/`: Contém recursos de imagem (e.g., `1.jpg`, `2.jpg`).
- `src/test/java/com/lanchenlayer/AppTest.java`: Contém os testes unitários da aplicação.

## Instalação e Execução
Para configurar e executar o projeto localmente, siga os passos abaixo:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/HSaimon/lanchonete.git
   cd lanchonete
   ```

2. **Compile o projeto com Maven:**
   ```bash
   mvn clean install
   ```

3. **Execute a aplicação:**
   Como este é um projeto Maven, você pode executá-lo a partir da linha de comando (assumindo que `Console.java` tem um método `main`):
   ```bash
   mvn exec:java -Dexec.mainClass="com.lanchenlayer.Console"
   ```
   Ou, se preferir, importe o projeto em uma IDE (como IntelliJ IDEA ou Eclipse) e execute a classe principal `Console.java`.

## Testes
Para executar os testes unitários, utilize o Maven:
```bash
mvn test
```

## Contribuição
Contribuições são bem-vindas! Se você tiver sugestões ou encontrar algum problema, por favor, abra uma issue ou envie um pull request.

## Licença
Este projeto é de uso pessoal. Sinta-se livre para adaptá-lo conforme necessário.
