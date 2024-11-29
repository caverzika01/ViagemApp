<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LojaCelularAPI - README</title>
</head>
<body>
    <h1>LojaCelularAPI</h1>
    <p>A <strong>LojaCelularAPI</strong> é uma API desenvolvida para gerenciar uma loja de celulares. Ela permite realizar operações básicas de CRUD (Create, Read, Update, Delete) para gerenciar os dados dos celulares no banco de dados MongoDB.</p>

    <h2>Funcionalidades</h2>
    <ul>
        <li><strong>Obter todos os celulares</strong>: Retorna uma lista de todos os celulares cadastrados.</li>
        <li><strong>Obter celular por ID</strong>: Retorna os detalhes de um celular específico, utilizando seu ID.</li>
        <li><strong>Criar novo celular</strong>: Permite adicionar um novo celular à coleção.</li>
        <li><strong>Atualizar celular</strong>: Permite atualizar as informações de um celular existente.</li>
        <li><strong>Remover celular</strong>: Remove um celular da coleção.</li>
    </ul>

    <h2>Pré-requisitos</h2>
    <p>Antes de rodar a aplicação, certifique-se de que você tenha os seguintes requisitos instalados:</p>
    <ul>
        <li><strong>.NET SDK 6.0 ou superior</strong>: A aplicação foi desenvolvida utilizando o .NET 6.0. Para instalar, siga as instruções <a href="https://dotnet.microsoft.com/download">aqui</a>.</li>
        <li><strong>MongoDB</strong>: A aplicação utiliza o MongoDB para armazenar os dados dos celulares. Se você não tiver o MongoDB instalado, pode utilizá-lo localmente ou configurar um banco de dados MongoDB na nuvem (ex: <a href="https://www.mongodb.com/cloud/atlas">MongoDB Atlas</a>).</li>
    </ul>

    <h2>Como Rodar o Projeto</h2>
    <h3>1. Clone o repositório</h3>
    <pre><code>git clone https://github.com/seu-usuario/LojaCelularAPI.git
cd LojaCelularAPI</code></pre>

    <h3>2. Configure o MongoDB</h3>
    <p>Crie uma instância do MongoDB localmente ou use um banco de dados MongoDB na nuvem.</p>

    <h3>3. Configure as variáveis de ambiente</h3>
    <p>No arquivo <code>appsettings.json</code>, configure a string de conexão do MongoDB para o banco de dados que você está utilizando:</p>
    <pre><code>{
  "LojaCelularDatabase": {
    "ConnectionString": "mongodb://localhost:27017", // Altere para a URL do seu MongoDB
    "DatabaseName": "LojaCelularDB",
    "CelularesCollectionName": "Celulares"
  }
}</code></pre>

    <h3>4. Restaure as dependências</h3>
    <pre><code>dotnet restore</code></pre>

    <h3>5. Execute a aplicação</h3>
    <p>Agora, você pode executar o projeto com o seguinte comando:</p>
    <pre><code>dotnet run</code></pre>
    <p>A API será iniciada no endereço <code>https://localhost:5001</code> (ou o endereço configurado no seu ambiente).</p>

    <h3>6. Teste a API</h3>
    <p>A API agora está rodando e você pode usar o Swagger para testar as funcionalidades. Acesse a interface Swagger da API em:</p>
    <pre><code>https://localhost:5001/swagger</code></pre>
    <p>Através da interface Swagger, você pode testar os seguintes endpoints:</p>
    <ul>
        <li><strong>GET /api/celulares</strong>: Retorna todos os celulares.</li>
        <li><strong>GET /api/celulares/{id}</strong>: Retorna um celular específico, utilizando o ID.</li>
        <li><strong>POST /api/celulares</strong>: Cria um novo celular. Envie um corpo JSON com os dados do celular.</li>
        <li><strong>PUT /api/celulares/{id}</strong>: Atualiza um celular existente.</li>
        <li><strong>DELETE /api/celulares/{id}</strong>: Remove um celular da coleção.</li>
    </ul>

    <h2>Estrutura do Projeto</h2>
    <ul>
        <li><strong>Controllers</strong>: Contém a lógica de roteamento e as ações para os endpoints da API.</li>
        <li><strong>Models</strong>: Contém as definições das entidades (e.g., <code>Celulares</code>), que representam os documentos no MongoDB.</li>
        <li><strong>Services</strong>: Contém a lógica de negócio para interagir com o banco de dados MongoDB.</li>
        <li><strong>appsettings.json</strong>: Contém as configurações do MongoDB (string de conexão, nome do banco de dados, etc.).</li>
    </ul>

    <h2>Contribuindo</h2>
    <p>Contribuições são bem-vindas! Para adicionar novas funcionalidades ou corrigir bugs, siga os passos abaixo:</p>
    <ol>
        <li>Faça um fork deste repositório.</li>
        <li>Criar uma branch para sua nova feature (<code>git checkout -b feature-nova</code>).</li>
        <li>Faça suas alterações e commit com uma mensagem descritiva.</li>
        <li>Envie suas alterações para o seu fork (<code>git push origin feature-nova</code>).</li>
        <li>Abra um pull request.</li>
    </ol>

    <h2>Licença</h2>
    <p>Este projeto está licenciado sob a MIT License - veja o arquivo <code>LICENSE</code> para mais detalhes.</p>
</body>
</html>
