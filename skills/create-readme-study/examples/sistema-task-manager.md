[JAVA__BADGE]: https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk&logoColor=white
[MAVEN__BADGE]: https://img.shields.io/badge/Maven-3.x-red?style=for-the-badge&logo=apachemaven&logoColor=white
[MIT__BADGE]: https://img.shields.io/github/license/Naereen/StrapDown.js.svg

<h1 align="center" style="font-weight: bold;">Task Manager</h1>

![java][JAVA__BADGE]
![maven][MAVEN__BADGE]
![mit][MIT__BADGE]

<p align="center">
  <a href="#sobre">Sobre</a> • 
  <a href="#como_executar">Como Executar</a> • 
  <a href="#objetivo">Objetivo de Aprendizado</a> • 
  <a href="#detalhamento">Detalhamento</a> • 
  <a href="#melhorias">Próximas Melhorias</a> •
  <a href="#licenca">Licença</a>
</p>

<br>
<p align="center">
    <img src="./img/img_projeto2.png" alt="Imagem do Projeto" width="600px">
</p>
<br>

<h2 id="sobre">📌 Sobre</h2>
<p>O Task Manager é uma aplicação de linha de comando (CLI) que permite criar e gerenciar tarefas de forma simples e eficiente.</p>
<p>O projeto foi desenvolvido como prática dos seguintes tópicos:</p>
<ul>
  <li>Programação Orientada a Objetos</li>
  <li>Collections Framework</li>
  <li>Manipulação de Arquivos</li>
  <li>Streams e Lambdas</li>
  <li>Generics</li>
  <li>Enums</li>
  <li>Tratamento de Exceções</li>
  <li>Organização em Camadas</li>
</ul>
<p>Todas as tarefas são armazenadas localmente em um arquivo de dados, permitindo que as informações sejam preservadas entre diferentes execuções do programa.</p>
<p>Este projeto foi criado com o objetivo de consolidar conhecimentos fundamentais da linguagem Java antes do estudo de tópicos mais avançados como concorrência, banco de dados, frameworks web e testes automatizados.</p>

<br>
<br>

<h2 id="como_executar">▶️ Como Executar</h2>

<h3>⚙️ Pré-requisitos</h3>
<p>Para executar o projeto é necessário possuir:</p>
<ul>
  <li><a href="https://www.oracle.com/br/java/technologies/downloads/">Java 21 ou superior</a></li>
</ul>
<p>Verifique sua versão instalada:</p>

```bash
java --version
```

<h3>Executando uma Release</h3>
<p>Baixe o arquivo <code>.jar</code> da última release disponível (<a href="https://github.com/JoaoVitorDomingos/Task-Manager/releases">clique aqui</a>).</p>
<p>Execute:</p>

```bash
java -jar task-manager-1.0.0.jar
```

<h3>Compilando Localmente</h3>
<p>Clone o repositório:</p>

```bash
git clone https://github.com/JoaoVitorDomingos/Task-Manager.git
```

<p>Entre na pasta do projeto:</p>

```bash
cd Task-Manager/task_manager/
```

<p>Compile o projeto:</p>

```bash
mvn clean package
```

<p>O arquivo gerado estará em:</p>

```text
target/
```

<p>Execute:</p>

```bash
java -jar target/task-manager-1.0.0.jar
```

<h3>📦 Releases</h3>
<p>As versões estáveis do projeto são disponibilizadas na área de Releases do GitHub (<a href="https://github.com/JoaoVitorDomingos/Task-Manager/releases">clique aqui</a>).</p>
<p>Para consultar o histórico completo de alterações entre as versões, veja o arquivo <a href="./CHANGELOG.md"><code>CHANGELOG.md</code></a>.</p>

<br>
<br>

<h2 id="objetivo">🎯 Objetivo de Aprendizado</h2>
<p>Este projeto foi desenvolvido após o estudo dos seguintes tópicos:</p>
<ul>
  <li>Java Básico</li>
  <li>Orientação a Objetos</li>
  <li>Exceções</li>
  <li>Lambdas</li>
  <li>Anotações</li>
  <li>Optional</li>
  <li>Manipulação de Arquivos</li>
  <li>Collections Framework</li>
</ul>
<p>Seu principal objetivo foi consolidar esses conhecimentos em um projeto prático antes do avanço para tópicos como:</p>
<ul>
  <li>Concorrência</li>
  <li>Networking</li>
  <li>Banco de Dados</li>
  <li>Frameworks Web</li>
  <li>Testes Automatizados</li>
  <li>Logging</li>
</ul>

<br>
<br>

<h2 id="detalhamento">📋 Detalhamento</h2>
<p>Nesta seção detalharei sobre o projeto, citando os pontos mais importantes sobre ele e sua criação.</p>
<details>
  <summary><h3>Sumário</h3></summary>
  <ol>
    <li><a href="#funcionalidades">Funcionalidades</a></li>
    <li><a href="#arquitetura">Arquitetura</a></li>
    <li><a href="#conceitos_aplicados">Conceitos Aplicados</a></li>
    <li><a href="#persistencia_dados">Persistência dos Dados</a></li>
  </ol>
</details>

<h3 id="funcionalidades">🚀 Funcionalidades</h3>

<strong>Gerenciamento de Tarefas</strong>
<ul>
  <li>Criar tarefas</li>
  <li>Editar tarefas</li>
  <li>Remover tarefas</li>
  <li>Marcar tarefas como concluídas</li>
</ul>

<strong>Sistema de Tags</strong>
<ul>
  <li>Adicionar tags às tarefas</li>
  <li>Remover tags das tarefas</li>
  <li>Evitar tags duplicadas</li>
</ul>

<strong>Busca e Filtragem</strong>
<ul>
  <li>Buscar tarefas por ID</li>
  <li>Filtrar tarefas por status</li>
  <li>Filtrar tarefas por tag</li>
</ul>

<strong>Ordenação</strong>
<ul>
  <li>Ordenação utilizando Comparator</li>
  <li>Suporte a diferentes critérios de ordenação</li>
</ul>

<strong>Persistência</strong>
<ul>
  <li>Salvamento automático ao encerrar o programa</li>
  <li>Carregamento automático ao iniciar o programa</li>
</ul>

<h3 id="arquitetura">🏗️ Arquitetura</h3>
<p>O projeto foi organizado seguindo uma separação simples de responsabilidades:</p>

```text
Main
 │
 ▼
TaskService
 │
 ▼
TaskRepository
 │
 ▼
Arquivo TXT
```

<p><strong>Main:</strong> Responsável pela interação com o usuário através do terminal.</p>
<p><strong>TaskService:</strong> Contém as regras de negócio da aplicação.</p>
<p><strong>TaskRepository:</strong> Responsável pela persistência dos dados em arquivo.</p>
<p><strong>Task:</strong> Representa a entidade principal do sistema.</p>

<h3 id="conceitos_aplicados">📚 Conceitos Aplicados</h3>

<strong>Collections Framework</strong>
<ul>
  <li>List</li>
  <li>Map</li>
  <li>Set</li>
  <li>Iterator</li>
  <li>Comparable</li>
  <li>Comparator</li>
</ul>

<strong>Programação Funcional</strong>
<ul>
  <li>Streams</li>
  <li>Lambdas</li>
  <li>Method References</li>
</ul>

<strong>Manipulação de Arquivos</strong>
<ul>
  <li>File</li>
  <li>Path</li>
  <li>Files</li>
  <li>BufferedReader</li>
  <li>BufferedWriter</li>
</ul>

<strong>Outros Conceitos</strong>
<ul>
  <li>Generics</li>
  <li>Enums</li>
  <li>Exceptions</li>
  <li>Optional</li>
  <li>Try-With-Resources</li>
</ul>

<h3 id="persistencia_dados">💾 Persistência dos Dados</h3>
<p>Os dados são armazenados localmente em um arquivo de texto.</p>
<p>Na primeira execução, o programa cria automaticamente a seguinte estrutura:</p>

```text
repository/
└── data.txt
```

<p><strong>Observação:</strong> a pasta <code>repository</code> não precisa existir previamente. Ela será criada automaticamente durante a primeira execução do programa.</p>

<br>
<br>

<h2 id="melhorias">🔮 Próximas Melhorias</h2>
<p>Algumas ideias para versões futuras:</p>
<ul>
  <li>Persistência em banco de dados</li>
  <li>Exportação para JSON</li>
  <li>Sistema de logs</li>
  <li>Testes automatizados</li>
  <li>Interface gráfica</li>
  <li>API REST utilizando Spring Boot</li>
</ul>

<br>
<br>

<h2 id="licenca">📃 Licença</h2>
<p>Este projeto está licenciado sob a <a href="./LICENSE">licença MIT</a>.</p>
<br>
<br>
