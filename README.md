# Banco De Dados
Desafio da DIO, para praticar o processo de configuração de uma instância de Banco de Dados na plataforma Microsoft Azure.
<img align="right" height="200" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ4xRmJAr1RW2g9yaEJS-OMT09nVx53t-TKrw&s">

Como entregável, o desafio proposto é a criação de um repositório contendo resumos, anotações e dicas sobre o uso da Azure, servindo como material de apoio para estudos e futuras implementações.  resumos, anotações e dicas sobre o uso da Azure.

## O que é Banco de Dados?

Imagine um banco de dados como uma grande biblioteca digital, onde todas as informações são cuidadosamente organizadas para que você possa encontrar exatamente o que precisa em poucos segundos. Ele funciona como um armário bem arrumado, onde cada coisa tem seu lugar como textos, números, imagens, vídeos e qualquer outro tipo de dado, tudo sendo quardado em sua pasta específica, na qual são armazenados de forma lógica e estruturada, prontos para serem usados quando necessário. No dia a dia, os bancos de dados estão por trás de quase tudo o que fazemos online. Quando você entra em uma rede social, como o Instragran e o Facebook , é o banco de dados que guarda seu perfil, suas fotos e suas mensagens. Quando faz uma compra na internet, como nos sites Mercado Livre e Ifood, ele armazena os produtos, os pedidos e os dados de pagamento. Até mesmo os aplicativos de mensagem, como WhatsApp, dependem deles para manter o histórico das suas conversas.

Para gerenciar tudo isso, existe um software especial chamado Sistema de Gerenciamento de Banco de Dados (SGBD). Ele é como se fosse um bibliotecário ou o organizador desse armário digital, controlando quem pode acessar, alterar ou adicionar informações, garantindo que tudo funcione de maneira segura e eficiente.
Os bancos de dados podem ser divididos em dois grandes grupos, cada um com suas características e usos específicos. Os bancos de dados relacionais, também conhecidos como SQL, organizam as informações em tabelas, parecidas com planilhas do Excel, onde os dados se relacionam entre si. Por exemplo, uma tabela pode ter clientes e outra de pedidos, e é possível conectar as duas para saber quem comprou o quê.
Para trabalhar com esse tipo de banco, usa-se a linguagem SQL, que permite buscar, inserir, atualizar e apagar dados com comandos simples. Alguns exemplos populares são MySQL, PostgreSQL e Oracle.
Já os bancos de dados não relacionais, ou NoSQL, são mais flexíveis e não usam tabelas. Eles são ideais para guardar informações que não se encaixam bem em estruturas rígidas, como posts de redes sociais, dados de sensores inteligentes ou até mesmo os registros de um jogo online. Entre os mais conhecidos estão o MongoDB, que armazena dados em formato de documentos, o Redis, que trabalha com dados em memória para respostas ultrarrápidas, e o Neo4j, especializado em lidar com relações complexas, como as conexões entre pessoas em uma rede social.

Em um mundo cada vez mais digital, os bancos de dados são a base que sustenta praticamente todos os sistemas que que são usados. Eles garantem que as informações sejam armazenadas com segurança, organizadas de forma inteligente e recuperadas em um piscar de olhos quando presisar delas. 

O Banco de Dados SQL do Azure se diferencia significativamente das soluções tradicionais de gerenciamento de dados por sua abordagem como serviço gerenciado na nuvem. Enquanto soluções convencionais exigem amplo conhecimento técnico para configuração e manutenção de infraestrutura, a versão Azure simplifica radicalmente esse processo. A principal diferença está na natureza PaaS (Plataforma como Serviço), que transfere para a Microsoft a responsabilidade pelo gerenciamento do hardware, atualizações de sistema e manutenção rotineira.

Diferentemente de implementações tradicionais onde é necessário planejar capacidade antecipadamente e lidar com upgrades complexos, o Banco de Dados SQL do Azure oferece escalabilidade instantânea para atender a demandas flutuantes. O modelo de custo também apresenta uma diferença marcante - em vez de investimentos iniciais em hardware, os usuários pagam apenas pelo que consomem, com opções que variam desde planos básicos até configurações de alto desempenho.

A segurança integrada representa outra distinção importante, com proteções como firewall nativo e controle granular de acesso já incorporados ao serviço, eliminando a necessidade de configurações manuais complexas. Essa abordagem permite que equipes de desenvolvimento dediquem mais tempo à criação de valor através de aplicativos, enquanto a plataforma cuida da camada de infraestrutura subjacente, adaptando-se automaticamente às necessidades em evolução de cada projeto.


## Crindo Danco de Dados SQL na Microsoft Azure
<img align="right" height="80" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Microsoft_Azure.svg/1200px-Microsoft_Azure.svg.png">
Neste projeto, explorei na prática o processo de configuração e utilização do Azure SQL Database, o serviço de banco de dados relacional da Microsoft na nuvem. A experiência permitiu compreender desde a criação inicial da instância até a integração com uma aplicação real.

O primeiro passo foi a configuração do ambiente no portal Azure, onde criei um novo servidor SQL (meuservidor-sql.database.windows.net) com um banco de dados chamado Teste, utilizando o modelo sem servidor Gen5. Durante essa etapa, aprendi sobre aspectos importantes como a seleção da região (Brazil South), configuração do tier de desempenho e definição das regras de firewall para permitir o acesso.

Para conectar uma aplicação ao banco de dados, desenvolvi um projeto Spring Boot utilizando Java no IntelliJ IDEA. A configuração da conexão foi feita através do arquivo application.properties, onde especifiquei a URL de conexão JDBC, credenciais de acesso e parâmetros adicionais de segurança. Implementei uma entidade Produto com Spring Data JPA, que foi automaticamente mapeada para uma tabela no banco de dados graças ao recurso de auto-configuração do Hibernate.

Os testes de conexão e operações CRUD foram realizados tanto através da aplicação quanto diretamente no Editor de Consultas do Azure Portal, o que permitiu validar o funcionamento correto de todas as camadas. Uma descoberta valiosa foi a importância de configurar adequadamente as regras de firewall para permitir o acesso a partir do IP de desenvolvimento.

Esta experiência prática proporcionou uma compreensão sólida dos benefícios do Azure SQL Database, incluindo sua escalabilidade, disponibilidade e integração com outras ferramentas Microsoft. Como próximos passos, pretendo explorar recursos avançados como replicação geográfica, tuning de performance e opções de backup automatizado.


