# Destaques sobre Bancos de dados, MYSQL E NOSQL
by: Lucas Dionísio Machado Martins


* Já se deparou com um sistema de cadastros em algum curso, newsletter ou concurso?

* Ou ainda ja foi a um supermercado cheio de produtos e quando passa no caixa ele sabe exatamente o que passou e as informações?

* Ou ainda mais, já foi em um site de compras e estava tudo organizado, classificado por categorias, possibilidade de pesquisar, filtrar por preços e ainda separar por marca X ou Y...? 

Se para alguma dessas questões você respondeu afirmativamente, saiba que muito provavelmente elas contam com soluções de bancos de dados (BD), pois não adianta você digitar seu nome e email no cadastro e ele ficar apenas no seu navegador, sem ser usado pelo sistema desejado. Além disso, não seria nada legal ter que rolar infinitas telas de um site de compras estático para achar o produto desejado e fazer o pedido via email ou telefone, sem poder filtrar e selecionar o pagamento e se cadastrar para comprar ali mesmo.

Os bancos de dados estão cada vez mais presentes em nossas vidas, pois o volume de dados produzido e consumido diariamente é elevado, e eles precisam estar guardados e organizados em algum lugar para que possam ser apresentados e utilizados.

Desta forma, cada dia mais se faz necessário o conhecimento mais aprofundado no tema, pois o futuro reserva grandes volumes de dados de diversos tipos para diversos fins. Portanto, aqui está um breve resumo que fiz para o desafio do Bootcamp de Bancos de Dados da Digital Innovation ONE - DIO. 


## SGBD

SGBD ou sistema de gerenciamento de banco de dados é um ambiente em que se pode criar, manipular e exportar bancos, estruturas e até mesmo fazer consultas, sendo que alguns apresentam ferramentas visuais para montar esquemas e modelos, facilitando os trabalhos dos profissionais da área. Normalmente apresentam interface visual, ide e interface gráfica amigável, possilitando uma curva de aprendizado interessante para quem realmente deseja estudar a área.

Existem diversos clientes de SGBDs e cada um tem suas particularidades, devendo o responsável pelos BDs conhecer um pouco sobre cada um para entender quando é melhor usar cada um e adaptar as particularidades dos problemas às ferramentas disponíveis pelos SGBDs. 

O ideal é entender o contexto do banco e buscar utilizar o sistema que mais consiga atender às necessidades do uso, principalmente quando se trata de bancos não relacionais, pois apresentam particularidades mais diversificadas. Neste ponto, o ideal é conhecer os requisitos do problema e tentar encontrar uma identidade com os sistemas disponíveis. Para não se perder nas variedades existentes no mercado, recomenda-se iniciar com casos de problemas semelhantes, tentando aplicar a solução do seu problema com o mesmo sistema de outro caso parecido; e para isso, estudar casos diversos, analisar e estudar sistemas com proximidade ao do problema é fundamental para carregar uma bagagem de conhecimento a respeito de como funciona e qual é mais adequado para cada situação.

Embora pode escolher um banco não relacional, deve-se estabelecer critérios para a escolha e requisitos para atender, facilitando o embasamento e possíveis mudanças.

## Banco de Dados relacional (SQL)

Usado para armazenar informações que apresentam relações ou ligações lógicas claras entre si, com um padrão das informações, esquema rígido, consistente e com poucas ou nenhuma duplicação nas informações. Também é chamado de Banco de Dados SQL, pois normalmente se usa esta linguagem ou alguma de suas subvariações. Costuma seguir os requisitos ACID.

## ACID


* A - Atomicidade: conceito em que a transação só é considerada com sucesso quando todas as suas operações forem concluídas com sucesso. 
* C - Consistência: é a propriedade em que só será realizada uma transação quando os dados e solicitações forem permitidos e dentro dos padrões do banco em questão, evitando que informações fora do padrão sejam inseridas ou usadas em trasações.. 
* I - Isolamento: é a propriedade em que transações paralelas (concorrentes) sejam tratadas de forma isoladas e sequenciais, ou seja, caso 2 transações envolvendo os mesmos dados forem iniciadas, a que finalizar primeiro será considerada e a segunda não, evitando conflito. 
* D - Durabilidade: é a propriedade em que uma vez realizada uma transação com sucesso, os dados atualizados serão gravados no banco de forma duradoura, e para isso ele deve estar armazenado em uma memória não-volátil. Assim, a informação deve permanecer no banco enquanto não for deletada propositalmente ou alterada.

## Banco de Dados não relacional (NOSQL)

Usado para armazenar dados que podem ou não apresentar relacionamento entre si (não necessariamente estruturada), possui maior flexibilidade em relação ao modelo e esquema (não precisa ter um padrão bem definido), ampliando a diversidade de tipos dados suportados e modelos possíveis. Possui um maior suporte à escalabilidade horizontal. Não veio para substituir, mas para complementar o relacional e ampliar suas possibilidades, acompanhando as necessidades computacionais dos sistemas e tecnologias atuais (principalmente devido ao alto volume e diversidade dos dados). Pode quebrar o padrão ACID, devido principalmente à liberdade maior de consistência e até mesmo um isolamento parcial.

A consulta não relacional pode facilitar o armazenamento, uma vez que o modelo pode ser feito com base na necessidade e formato da consulta (organizado com base na consulta, mesmo sem rigidez, facilitando o uso e reduzindo gargalos e latências). As consultas, embora não feitas em um sistema estruturado, podem ocorrer através de chaves, índices ou outras formas de identificar as informações; e para isso deve ser pensado nas características do banco e nas informações a serem retornadas e priorizadas (modelagem deve levar isso em consideração). 

## SQL

A SQL - Structured Query Language ou linguagem de consulta estruturada (em tradução livre) é a principal linguagem de manipulação de banco de dados relacionais, sendo muito utilizada para se referir a bancos de dados relacionais. Ela é subdividida em: 


* DQL - Data Query Language (Linguagem de Consulta de Dados) - comandos da consulta de dados (comando SELECT);

* DML - Data Manipulation Language (Linguagem de Manipulação de Dados) - divisão responsável pela manipulação de dados (INSERT, UPDATE e DELETE);

* DDL - Data Definition Language (Linguagem de Definição de Dados) - comandos para criação (CREATE), alteração (ALTER) e remoção (DROP) de tabelas, views, índices;

* DCL - Data Control Language (Linguagem de Controle de Dados) - comandos para controlar o acesso aos dados, adicionando (GRANT) e removendo (REVOKE) permissões de acesso;

* DTL - Data Transaction Language (Linguagem de Transação de Dados) - comandos para gerenciar as transações executadas no banco de dados, sendo: iniciar uma transação (BEGIN), confirmar transação (COMMIT) ou desfazer transação (ROLLBACK).


## Projetando

Antes de iniciar um projeto, é necessário entender a situação a ser armazenada, os dados que serão persistidos, os níveis de acesso, as formas de consultas e manipulações inerentes à situação-problema. Deve-se fazer perguntas a respeito do que será armazenado e de que forma será apresentada, que tipo de dado será armazenado e se apresenta alguma relação. 

Após ter em mente as definições básicas do projeto, cria-se um projeto conceitual, com as informações coletadas, prioridades, relações e atributos inerentes a cada item. 

A partir do projeto conceitual, é feito o modelo lógico, onde já se utiliza SGBDs para criar o esqueleto e organizar conforme o planejamento. 

Há ainda uma outra etapa, que é relacionada a como o BD será armazenado e como será acessado, quais dados serão armazenado em qual sistema (núvem, privado, híbrido). Esta etapa é muito importante para a segurança e garantia da durabilidade destes. 

## Persistindo dados

A partir dos do tipo de BD será possível a inserção de determinados (ou uma gama de) tipos de dados, e para isso normalmente se integra o banco a uma outra aplicação, possibilitando que outros departamentos possam persistir os dados, ou ainda o armazenamento é feito com base em coletas automatizadas de sistemas de sensores ou estações. 


## Pesquisando e selecionando a forma de visualização

Cada tipo de Banco de dados apresenta uma forma particular de consulta, porém elas devem ser realizadas de acordo com as necessidades modeladas, possibilitando que os usuários tenham acesso de acordo com a sua permissão e cumprindo o papel de armazenamento de dados. Para isso, são modeladas as visualizações, para limitar e facilitar o acesso às informações necessárias conforme o nível de uso e necessidade de cada usuário. Além da visualização, há também a possibilidade de pesquisa dentro do banco, conforme a organização e modelagem de identificação dos dados dentro do BD.

## Armazenamento: Privado, Nuvem ou Híbrido?

A escolha entre armazenamento privado, em núvem ou híbrido ocorre de acordo com as nuances do negócio e dos requisitos específicos do uso do banco. Ex: uma empresa de tecnologia que realiza diversas pesquisas e está planejando novos produtos considerados inovadores está muito preocupada em deixar dados fora de suas propriedades tanto com medo de espionagem industrial, invasão, vazamentos, entre outros. 

Há também aqueles que preferem o modelo em núvem, como um pequino site de vendas de cosméticos, cujos custos para estrutura são demasiados para seu tamanho de negócio, além de que a praticidade de soluções prontas para fazer sites e possibilidade de acessar em diferentes locais é um dos atrativos. 

Para serviços como bancos e corretoras, há a possibilidade de armazenar os dados menos sensíveis em núvem, como estrutura do site, imagens, e textos usados para a estrutura da plataforma web e aplicativo; porém as informações sensíveis dos clientes podem ser armazenadas em servidor privado, evitando indisponibilidade e reduzindo os riscos por estar fora de suas propriedades. Enquadrando assim um modelo híbrido. 


## Complexidade

O tipo de banco de dados dirá a forma como será trabalhado, retornado e quais as características dos processos serão limitadas ou mais flexíveis. Não necessariamente SGBD A será mais complexo que o B, ou o BD SQL será mais simples que o NOSQL, mas a forma com que o problema será solucionado e a carga para processamento destas informações será diferente e podendo ser mais complexo entre um e outro conforme o escopo, amplitude e nuances de cada projeto. 

## Ciência de Dados x Engenharia de Dados

Normalmente o engenheiro é responsável por planejar, estruturar e deixar os dados disponível para que os cientistas possam manipular e utilizar em diferentes fins, como tomada de decisões, pesquisas, treinamento de Inteligência Artificial, mineração de dados, entre outros. Assim, um complementa o outro, sendo que o cientista ajuda o engenheiro passando informações sobre os requisitos necessários para o uso; enquanto o engenheiro realiza o planejamento e monta o banco para oferecer os dados.