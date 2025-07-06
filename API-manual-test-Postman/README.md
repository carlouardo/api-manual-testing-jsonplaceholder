# Projeto de Testes Manuais de API - JSONPlaceholder

## Visão Geral

Este repositório apresenta um projeto prático de testes manuais de API (Application Programming Interface). Utilizei a ferramenta **Postman** para interagir diretamente com a API de simulação de dados **JSONPlaceholder**, com o objetivo de demonstrar minha capacidade de projetar, executar e documentar cenários de teste para APIs RESTful, validando seus comportamentos e respostas.

## Objetivo

* Compreender e aplicar conceitos fundamentais de teste de API.
* Desenvolver e aprimorar habilidades no uso do Postman para diferentes métodos HTTP (GET, POST, PUT, DELETE).
* Analisar e validar estruturas de requisições e respostas no formato JSON.
* Documentar de forma clara e organizada os cenários de teste, resultados e evidências geradas.

## Tecnologias e Ferramentas Utilizadas

* **Postman:** Ferramenta líder para construção, execução e organização de requisições e testes de API.
* **JSONPlaceholder:** Uma API REST falsa e gratuita, ideal para prototipagem e testes, simulando um ambiente real.
* **GitHub:** Plataforma essencial para versionamento de código, controle de alterações e hospedagem do projeto, facilitando a colaboração e visualização.
* **Markdown:** Linguagem de marcação leve utilizada para a formatação desta documentação.

## Estrutura do Repositório

O repositório está organizado de forma intuitiva para facilitar a navegação e compreensão do projeto:

* `./`: Diretório raiz, contendo este arquivo `README.md` com a visão geral do projeto.
* `Test-Cases/`: Contém a documentação detalhada dos cenários de teste executados.
    * `API_Test_Results.md`: Arquivo Markdown com a descrição completa de cada cenário de teste, incluindo requisições, resultados esperados e reais, e o status da execução.
* `Evidences/`: Pasta dedicada a armazenar todas as capturas de tela (screenshots) das requisições e respostas do Postman, servindo como evidência visual dos testes executados.
* `Postman_Collection/`: ** Esta pasta armazena o arquivo exportado da coleção do Postman. 

## Como Visualizar e Replicar os Testes

Para explorar este projeto e replicar os testes em seu ambiente:

1.  **Clone o Repositório:** Utilize o comando `git clone [URL_DO_SEU_REPOSITORIO]` em seu terminal.
2.  **Acesse a Documentação Detalhada:** Navegue até a pasta `Test-Cases/` e abra o arquivo `API_Test_Results.md` para uma análise aprofundada dos cenários de teste e seus resultados.
3.  **Importe a Coleção Postman (Recomendado):** Se você tiver o Postman instalado e a coleção `.json` disponível na pasta `Postman_Collection/`, importe-a na ferramenta para visualizar e executar as requisições que foram testadas.
4.  **Verifique as Evidências:** As imagens que comprovam os resultados dos testes estão organizadas na pasta `Evidences/`.

## Observação Importante sobre a API JSONPlaceholder

É fundamental entender que o **JSONPlaceholder é uma API de simulação e não tem capacidade de persistir dados**. Isso significa que:

* Ao realizar requisições `POST` (para criar recursos) ou `PUT` (para atualizar recursos), a API responderá com sucesso (por exemplo, `201 Created` para um `POST`) e retornará um objeto JSON com um ID, simulando a operação.
* No entanto, esses dados **não são realmente gravados ou salvos** em um banco de dados permanente no servidor do JSONPlaceholder.
* Consequentemente, se você tentar uma requisição `GET` subsequente para o ID de um recurso que você "criou" ou "atualizou", **ele não será encontrado**, pois a informação não foi persistida.

Esta característica é intencional para o propósito de testes, permitindo validar o fluxo de sucesso das operações sem a necessidade de um ambiente de banco de dados real. É um ponto crucial de aprendizado sobre as limitações e propósitos de APIs mockadas.

## Contato

Sinta-se à vontade para entrar em contato ou deixar um feedback!

* **Autor:** Carlos Eduardo Gama
* **LinkedIn:** https://www.linkedin.com/in/eduardo-gama-54099b183/