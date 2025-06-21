# LH Games

## Descrição do Projeto

Este projeto, **LH Games**, foi desenvolvido como parte de um curso SENAI, com o objetivo principal de guiar o aprendizado na **estrutura de projetos Angular CLI**, na **interação com APIs**, na **documentação de APIs** e no **tratamento de erros amigáveis ao usuário**. Além disso, o projeto introduz e explora conceitos fundamentais de **segurança da informação**, como a criptografia assimétrica, que são cruciais para o desenvolvimento de aplicações robustas e seguras.

Ele abrange desde a construção de um layout responsivo, passando pela criação e consumo completo de uma API local simulada (`json-server`), a formalização dessa API através de documentação, até a implementação de um sistema de feedback visual para o usuário e a compreensão de princípios de segurança.

**Etapas e Conceitos Abordados:**

1.  **Preparação do Ambiente e Layout:**
    * Configuração inicial do projeto Angular, instalação e integração de **Bootstrap** e **Angular Material**.
    * Criação e estruturação de componentes (`inicio`, `login`, `menu`, `rodape`).
    * Configuração de **rotas** para navegação.
    * Otimização visual (favicon, imagens).
    * Publicação inicial no GitHub.

2.  **Criação e Consumo de API:**
    * **Criação de uma API REST simulada** utilizando `json-server` e um arquivo `db.json` para persistência de dados.
    * Definição de **Modelos de Dados (Cliente)** em TypeScript para tipagem forte.
    * Desenvolvimento de **Serviços Angular** (`ClienteService`) para encapsular a lógica de comunicação com a API.
    * Utilização do **`HttpClient` do Angular** e **`Observables` (RxJS)** para lidar com requisições assíncronas.
    * **Implementação completa das operações CRUD:** Create, Read, Update, Delete.

3.  **Documentação de API:**
    * Introdução ao **Swagger Editor** para criar e visualizar documentação de API no padrão **OpenAPI (versão 3.0.3)**.
    * Detalhamento da estrutura da especificação OpenAPI, incluindo `info`, `servers` e `paths` (endpoints).
    * Documentação dos métodos **GET** e **POST** para a rota `/produtos`.

4.  **Configuração de Mensagens de Erro:**
    * Integração do componente **`MatSnackBarModule` do Angular Material** para exibir mensagens pop-up no navegador.
    * Implementação de um método **`showMessage()`** no `ClienteService` para exibir feedback visual (sucesso/erro).
    * Utilização de `catchError` do RxJS para **interceptar e tratar erros** em requisições HTTP.

5.  **Conceitos de Segurança da Informaçã:**
    * Abordagem da **Criptografia Assimétrica** como um pilar de segurança em comunicações digitais.
    * Entendimento do funcionamento das **chaves pública e privada** para cifragem e decifragem de informações, garantindo a confidencialidade.
    * Demonstração conceitual do processo de **geração de chaves** baseado em números primos, exemplificado pelo algoritmo **RSA**.
    * Compreensão de como a criptografia assimétrica contribui para a segurança de dados sensíveis em aplicações web.

Este projeto proporciona uma compreensão completa do ciclo de vida de desenvolvimento de uma aplicação front-end com Angular, desde a concepção do layout e a interação com um *backend* (simulado) para gerenciar dados, até a formalização e documentação da API, o aprimoramento da experiência do usuário através de feedback visual, e a fundamental base em conceitos de segurança da informação.

---

## Tecnologias Utilizadas

![Badge Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Badge TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Badge Angular Material](https://img.shields.io/badge/Angular_Material-424242?style=for-the-badge&logo=angularjs&logoColor=white)
![Badge Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Badge json-server](https://img.shields.io/badge/json--server-6B8E23?style=for-the-badge&logo=json&logoColor=white)
![Badge Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Badge Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)
![Badge Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Badge GitHub](https://img.shields.io/badge/GitHub-161B22?style=for-the-badge&logo=github&logoColor=white)
![Badge Visual Studio Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)


* **Angular CLI**: Ferramenta de linha de comando para inicializar, desenvolver, fazer a manutenção e testar projetos Angular.
* **Angular Material**: Biblioteca de componentes de UI de alta qualidade, seguindo as diretrizes do Material Design, incluindo **SnackBar** para mensagens de feedback.
* **Bootstrap**: Framework CSS para desenvolvimento responsivo e componentes de interface (Carousel, Formulários).
* **json-server**: Ferramenta para criar uma API REST *mockada* rapidamente a partir de um arquivo JSON.
* **Swagger Editor**: Ferramenta online para criar, editar e visualizar documentação de APIs no padrão OpenAPI (Swagger).
* **HTML5, CSS3, TypeScript**: Linguagens e superset essenciais para o desenvolvimento front-end.
* **RxJS**: Biblioteca para programação reativa, utilizada com `Observables`, `map` e `catchError` para manipulação de fluxos de dados e tratamento de erros.
* **Node.js**: Ambiente de execução JavaScript fundamental para o Angular CLI e as dependências do projeto.
* **VSCode**: Editor de código utilizado para o desenvolvimento.
* **Git / GitHub**: Sistema de controle de versão para gerenciamento e hospedagem do código-fonte.

---

## Funcionalidades Implementadas

### Layout e Navegação

* **Página Inicial (Home)**: Com um **Carousel** de banners e uma seção de **Cards de Jogos** (usando Angular Material Card e Grid List).
* **Página de Login**: Formulário de login básico (usando Bootstrap Form Control).
* **Menu de Navegação (Toolbar)**: Com links para "Produtos" (Home) e "Login", e o logo da LH Games.
* **Rodapé**: Seção inferior básica com informações de desenvolvimento.
* **Navegação por Rotas**: Configuração de rotas para navegação fluida entre as páginas.
* **Favicon Personalizado**: Ícone de aba de navegador personalizado.

### Interação com API (CRUD Completo)

* **API REST Simulada**: Criação de um *endpoint* `/clientes` com dados de exemplo (ID, nome, endereço) usando `db.json` e `json-server`.
* **Modelo de Cliente**: Definição da estrutura de dados para `Cliente` (id, nome, endereco) utilizando uma classe TypeScript.
* **Serviço de Cliente (`ClienteService`)**:
    * Configuração da URL base da API.
    * Injeção de dependência do `HttpClient` para comunicação HTTP.
    * Métodos implementados para todas as operações **CRUD** (Create, Read, Update, Delete):
        * `getClientes()`: Realiza requisições `GET` para **listar** clientes.
        * `create()`: Realiza requisições `POST` para **criar** novos clientes.
        * `getCliente()`: Realiza `GET` para **buscar um cliente** específico.
        * `atualizarCliente()`: Realiza requisições `PUT` para **atualizar** clientes existentes.
        * `excluirCliente()`: Realiza requisições `DELETE` para **excluir** clientes.
* **Gerenciamento de Clientes**:
    * Componentes específicos (`ListarClienteComponent`, `CadastrarClienteComponent`, `AtualizarClienteComponent`) para interagir com as operações CRUD.
    * Utilização de diretivas Angular (`*ngFor`, `ngModel`) e interpolação de texto para interação dinâmica com a API.
    * Tratamento de dados assíncronos com **`Observables` (RxJS)**.

### Documentação de API (OpenAPI/Swagger)

* **Criação de Documentação**: Utilização do **Swagger Editor** para desenvolver e validar a documentação da API.
* **Estrutura OpenAPI 3.0.3**:
    * **Info**: Detalhes sobre a API "LH Games - Consumo", descrição para consumo de produtos, termos de serviço e contato.
    * **Servers**: Definição de um servidor de produção (`http://api.lhgames.com/v1`).
    * **Paths**: Documentação de endpoints como `/produtos` para `GET` (retorno) e `POST` (adição), incluindo schemas de exemplo e respostas HTTP.
* **Visualização e Validação**: Capacidade de visualizar a documentação em HTML e identificar erros de sintaxe em tempo real através do Swagger Editor.
* **Formatos**: Conhecimento e uso dos formatos JSON e YAML para a especificação da API.

### Tratamento de Erros e Feedback Visual

* **Mensagens Pop-up (`MatSnackBar`)**: Integração do Angular Material SnackBar para exibir feedback rápido e discreto ao usuário.
* **Método `showMessage()`**: Centralização da lógica de exibição de mensagens, permitindo indicar se é uma mensagem de sucesso ou erro (com estilização diferente).
* **Intercepção de Erros**: Utilização do `catchError` do RxJS para capturar erros em requisições HTTP no `ClienteService`.
* **Feedback ao Usuário**: Em caso de erro na comunicação com a API (ex: `json-server` desligado), uma mensagem de "Erro" é exibida ao usuário de forma clara e visível, sem a necessidade de inspecionar o console.


---

## Como Rodar o Projeto

Para executar este projeto em sua máquina local, siga os passos abaixo:

### Pré-requisitos

Certifique-se de ter o **Node.js**, **Angular CLI** e **Git** instalados globalmente em sua máquina.

* **Instalação do Angular CLI (se necessário):**
    ```bash
    npm install -g @angular/cli
    ```
* **Instalação do json-server (globalmente):**
    ```bash
    npm install -g json-server@0.17.1
    ```

### Instalação

1.  **Clone o repositório:**
    ```bash
    git clone [##]
    ```
2.  **Navegue até o diretório raiz do projeto:**
    ```bash
    cd lh-games
    ```
3.  **Instale as dependências do projeto Angular:**
    ```bash
    npm install
    ```

### Execução

1.  **Inicie a API simulada com json-server:**
    Abra um novo terminal (CMD ou Git Bash) na raiz do projeto (`lh-games/`) e execute:
    ```bash
    json-server --watch db.json
    ```
    Isso iniciará a API em `http://localhost:3000/clientes` e outros endpoints que você tiver configurado no `db.json`.

2.  **Inicie o servidor de desenvolvimento do Angular:**
    Em **outro terminal** (CMD ou Git Bash), também na raiz do projeto (`lh-games/`), execute:
    ```bash
    ng serve
    ```

3.  Abra seu navegador e acesse `http://localhost:4200/`. A aplicação Angular será carregada, permitindo a interação completa com as operações CRUD de clientes e a visualização das mensagens de feedback.

### Visualização da Documentação da API

Para visualizar a documentação da API:

1.  Acesse o **Swagger Editor online**: `editor.swagger.io`.
2.  Clique em `File` -> `Import file` e selecione o arquivo `openapi.json` (ou `openapi.yaml`, se preferir) que está na raiz do seu projeto. O editor renderizará a documentação em HTML.

---

## Publicação no GitHub

Este projeto foi publicado no GitHub, seguindo os passos de inicialização de um repositório Git, adição de arquivos, criação de commits e envio (push) para o repositório remoto.

### Comandos Git Utilizados:

* `git status`
* `git add .`
* `git commit -m "Mensagem do commit"`
* `git remote add origin [#]`
* `git push -u origin master`

---

## Próximos Passos

O projeto está robusto e pronto para ser expandido com funcionalidades adicionais, como:

* **Implementação Prática de Segurança**: Aplicar os conceitos de criptografia assimétrica e outras boas práticas de segurança (ex: JWT para autenticação) diretamente no backend e/ou frontend para proteger dados e comunicações.
* **Autenticação e Autorização**: Desenvolver um sistema de login e controle de acesso mais sofisticado para as rotas e funcionalidades restritas.
* **Validação de Formulários Avançada**: Aprimorar a validação de entrada de dados nos formulários para garantir a integridade dos dados e melhorar a experiência do usuário.
* **Testes Unitários e de Integração**: Desenvolver testes para garantir a robustez e a manutenibilidade do código.
* **Deployment em Produção**: Realizar o *deploy* da aplicação para um ambiente de produção real, garantindo que a API e o frontend estejam acessíveis publicamente.

---

## Contato

Conecte-se e saiba mais sobre o meu trabalho:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/perfil-linkedin)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/Jonathanlucas777)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/37991042878)

