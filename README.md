
# Cashforce Frontend - Vue.js

Projeto construído em Vue.js para um teste técnico de uma aplicação Fullstack da Cashforce.


## Autores

- [@RafaelMoraes](https://www.github.com/rafarello)


## Inicialização

Para iniciar o projeto basta seguir os passos a seguir:

- Baixar uma cópia do repositório ou realizar o clone em sua máquina
- Executar o comando `npm install` para instalar as dependências
- Executar o comando `npm start` para iniciar a aplicação

## Sobre

O Teste contempla uma tela de pedidos, onde esta é alimentada pela API criada no Backend.

## Componentes

Os componentes foram basicamente divididos da seguinte forma:

- Barra de navegação lateral
- Seção de conteúdo
- Header

Onde a `Seção de conteúdo` é responsável por renderizar o componente `Header` e o roteamento das `Views`
## Views - Vistas de Telas

A aplicação para este teste consiste de apenas uma `View`, que representa a seção da Tabela de `Pedidos` que é alimentada pela API
## Tabela - Pedidos

Esta possuí as colunas:

- Nota fiscal
- Sacado (Nome do `Comprador`)
- Cedente (Nome do `Provedor`)
- Emissão (Data de emissão)
- Valor da Transação
- Status (Status da Transação)

## Funções de Formatação - Tabela

Para renderização dos valores das colunas da tabela corretamente foram necessárias a criação de alguns métodos, entre eles estão:

- Formatação de `Data de Emissão`
- Formatação `Valor da Transação` na moeda Real
- Renderização de `Status` de acordo com o código estipulado na tabela enviada por E-mail


## Variáveis de Ambiente

Para esse projeto foi encontrada muita dificuldade em configurar as `Variáveis de Ambiente`, portanto foi configurado manualmente na `Url Base` do **Axios** as Variáveis **Host** e **Port**, portanto para a aplicação executar corretamente é necessário editar esse documento caso o Host seja diferente de  *localhost* e porta *3001* previamente configuradas no Backend


## Dificuldades

Além da dificuldade configurando as variáveis de ambiente, como já comentado no tópico anterior, foram encontrado dificuldades em entender inicialmente o método de renderização do Vue e as estruturas dos Componentes, visto que é relativamente bem diferente a lógica de construção se comparado com React, que é o Framework no Frontend que tive mais contato até o momento.

Foram consumidos alguns bons minutos lendo documentação e tutoriais de apenas como os arquivos eram estruturados, como por exemplo que o `script`, a página `html` e a `estilização` eram feitas na mesma página.

Também foi encontrado dificuldade em tratar da requisição de buscar as informações ao renderizar a página e sua assincronicidade

Por último, mas já um pouco mais calejado devido a dificuldade anterior, foi a criação dos métodos que são as funções de suporte para renderização dos items na tela
## Aprendizados

Absolutamente foi um desafio incrível e divertido aprender um novo Framework de Frontend, ainda mais tendo tantas dificuldades iniciais no primeiro contato.

Mas resumindo os pontos que tive maior aprendizado foram:

- Estrutura geral do Vue
- Utilizar Roteamento de Vistas (No momento acredito ter dúvidas quanto ao seu funcionamento, mas já é perceptível que possui um potencial incrível)
- Criação de Componentes
- Criação de Vistas



## Screenshots

[Cashforce App](https://prnt.sc/F9fcc7WCvrXK)

