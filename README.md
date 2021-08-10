## Automação FakeRESTApi.Web V1

  Projeto para validar a [FakeRESTApi.Web V1](https://fakerestapi.azurewebsites.net/index.html) de forma automatizada, o qual utiliza as seguintes ferramentas:

  - **[Ruby](https://www.ruby-lang.org/en/)**;
  - **[Cucumber](https://cucumber.io)** para escrita **[Gherkin](https://cucumber.io/docs/gherkin/reference/)**;
  - **[HTTParty](https://github.com/jnunemaker/httparty)**;
  - **[RSpec](https://github.com/rspec/rspec)**.

## Pré-requisito: 

  - [Ruby](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-18-04-pt) instalado. (**OBS.** Neste projeto foi usada a versão 2.6.1 do ruby).

### Instalando gemas do Ruby

  - A partir da pasta de seu projeto, execute no terminal o comando: `bundle`.

### Configuração do ambiente

  - **OBS.** Para este desafio não é necessário seguir os próximos passos desta etapa de configuração, pois o arquivo `.env` já está preenchido. Contudo, caso esse projeto estivesse validando dados reais de uma organização, os valores de variáveis de ambiente e demais conteúdos que exigem privacidade da equipe responsável, a recomendação seria seguir as próximas etapas desta secção de modo a manter seguros os dados sensíveis do projeto, além de adicionar o arquivo `.env` dentro do `.gitignore`.
  - Duplique o arquivo `.env.sample` e o renomeie para `.env`;
  - Consulte o(s) QA(s) do time, o(s) qual(is) mantém este projeto para obter os valores das chaves para preencher o arquivo `.env` criado no passo anterior.

### Execução

  - Para visualizar o resultado de todos os testes e gerar seu relatório em **.html** executar no terminal a partir da pasta raiz do projeto o comando: `cucumber -p default`.

  - Reports disponíveis em: **/report**, para visualizá-lo abra o arquivo `report.html` em um navegador de sua preferência.

---

## Testes Manuais com Postman

  Projeto para testar a [FakeRESTApi.Web V1](https://fakerestapi.azurewebsites.net/index.html) de forma manual, o qual utiliza o [Postman](https://www.postman.com) como ferramenta de validações

  [Postman](https://www.postman.com/downloads)

## Pré-requisito: 

  - [Postman](https://www.postman.com/downloads) instalado.

## Configuração do ambiente

### Importando o projeto

  - Com a aplicação do Postman aberta clique em: **File > Import**
  - Na aba **File**, clique no botão **Upload Files** e navegue até a pasta do projeto de automação **teste-faker > postman** e selecione o arquivo com a coleção de requisições (`requests_fake_rest_api_v1.postman_collection.json`) e clique no botão **Import**;
  - Repita o processo clicando em: **File > Import**
  - Na aba **File**, clique no botão **Upload Files** e navegue até a pasta do projeto de automação **teste-faker > postman** e agora selecione o arquivo com as variáveis de ambiente (`environment_variables_fake_rest_api_v1.postman_environment.json`) e clique no botão **Import**;

### Execução

  - Com a aplicação do Postman aberta navegue até a aba **Collections > FakeRESTApi.V1**
  - Agora basta selecionar dentro das pastas: **Autores** ou **Livros**, a requisição que deseja testar e clicar no botão **Send**