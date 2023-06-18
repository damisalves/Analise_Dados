# Análise de Dados Exploratória dos Voos Domésticos no Brasil

![Capa do Projeto](https://storage.stwonline.com.br/180graus/uploads/ckeditor/pictures/2280353/240919---jet-smart.jpg)

# 1. Introdução 

Voos domésticos no Brasil são aqueles que realizam trajetos entre cidades brasileiras, sem cruzar fronteiras internacionais. São operados por diversas companhias aéreas, que oferecem diferentes opções de horários, preços e serviços aos passageiros. 
É uma opção popular para quem deseja viajar pelo país com rapidez e conforto, evitando as longas distâncias das estradas e as incertezas das condições climáticas. O transporte aéreo brasileiro conquistou novos clientes nas duas últimas décadas, recebeu empresas mais eficientes e assistiu a melhora na gestão. 
Em vinte anos a aviação comercial tornou-se o principal modal de transporte em ligações de média e longa distância dentro do país, substituindo o ônibus que reinava absoluto por várias décadas. Segundo dados da ANAC, apenas em 2022, foram transportados 98 milhões de passageiros em voos domésticos e internacionais, maior marca desde o início da crise sanitária, há três anos. Ainda assim, inferior a série histórica que em alguns momentos esteve acima dos 100 milhões. 
No entanto, os voos comerciais ainda enfrentam questionamentos como o preço da passagem, questões sanitárias pós covid-19 e a dificuldade de acesso para pessoas de áreas remotas. 
O presente trabalho tem como objetivo mostrar a evolução desses aspectos baseando-se nos dados da Agência Nacional de Aviação Civil – ANAC, que retratam o desenvolvimento da categoria no país desde o ano de 2002. 
Através da análise exploratória de dados e a partir do estudo quantitativo das informações, o propósito é a estruturação dos dados demonstrando a evolução da quantidade de voos de acordo com os dados das diversas companhias aéreas, que oferecem diferentes opções de serviços aos passageiros, demonstrando, em conjunto, a mensuração das regiões do país com maior incidência de viagens e o tempo recorrido para a execução das mesmas.  
A organização da análise é composta pelo banco de dados, o tratamento das informações relevantes de acordo com o tema abordado e a estruturação analítica do relatório. 
A evolução do número de voos domésticos no Brasil tem contribuído para o aumento da conectividade entre as diferentes regiões do país, facilitando o deslocamento de pessoas e bens. Isso tem impactado positivamente o turismo, o comércio e a economia em geral, gerando empregos e aumentando a competitividade do país.

# 1.1 Objetivos

O objetivo deste estudo é realizar uma Análise Exploratória dos Dados (Exploratory Data Analysis - EDA) do conjunto de dados **voos-anac-2000a2023**, adaptado pelo autor e disponível em data/titanic3.csv; a fim de entender melhor através de dados reais o funcionamento e a evolução dos voos domésticos no país. Especificiamente serão respondidas as seguintes questões de pesquisa:

1. Quais as regiões do Brasil que mais fazem voos?
2. Evolução da quantidade de voos no Brasil?
3. Quais meses e anos tivemos mais voos domésticos?
4.Qual empresa realiza a maior quantidade de voos?
5.Quais os maiores destinos por região do Brasil?
6.Qual a média de horas voadas por companhia e mês?

# 2. Metodologia

O tópico apresentará um dicionário de dados, a realização do mapeamento, o processo de transformação e o tipo de modelagem utilizada.

# 2.1 Dicionário de Dados

![Dicionário de Dados](https://github.com/damisalves/Template-Repositorio/assets/137001435/9b5021a1-2caa-4afc-9fd5-bda71e207fbb)

# 2.1.1. Observações

A base de dados é descrita por quantidade de voos realizados por mês e ano de acordo com os demais campos.

`distancia_voada_km:` a quantidade descrita de km/h;
`decolagens:` Refere-se ao número de decolagens que ocorreram entre os aeródromos de origem e destino da etapa;
`natureza:`  etapas remuneradas que são realizadas sob uma numeração de Horário de Transporte (HOTRAN). Recebem esse nome, pois possuem a característica de serem realizadas regularmente; 
`passageiros pagos:` Refere-se aos passageiros que ocupam assentos comercializados ao público e que geram receita, com a compra de assentos, para a empresa de transporte aéreo. Incluem-se nesta definição as pessoas que viajam em virtude de ofertas promocionais, as que se valem dos programas de fidelização de clientes, as que se valem dos descontos concedidos pelas empresas, as que viajam com tarifas preferenciais, as pessoas que compram passagem no balcão ou através do site de empresa de transporte aéreo e as pessoas que compram passagem em agências de viagem;
`passageiros grátis:` Refere-se aos passageiros que ocupam assentos comercializados ao público mas que não geram receita, com a compra de assentos, para a empresa de transporte aéreo. Incluem-se nesta definição as pessoas que viajam gratuitamente, as que se valem dos descontos de funcionários das empresas aéreas e seus agentes, os funcionários de empresas aéreas que viajam a negócios pela própria empresa e os tripulantes ou quem estiver ocupando assento destinado a estes;



# Índice/Sumário

* [Sobre](#sobre-o-projeto)
* [Sumário](#índice/sumário)
* [Requisitos Funcionais](#requisitos-funcionais)
* [Tecnologias Usadas](#tecnologias-usadas)
* [Contribuição](#contribuição)
* [Autores](#autores)
* [Licença](#licença)
* [Agradecimentos](#agradecimentos)


# Requisitos Funcionais 

- [x] **Cadastrar Usuário**
- [x] **Fazer Login**
- [ ] Matricular em Curso
- [ ] Cancelar Matricula
- [ ] Visualizar Notas
- [ ] Visualizar e Atualizar Informações do Estudante

# Tecnologias Usadas

- [Flutter](https://flutter.dev/)
- [Node.js](https://nodejs.org/en/)
- [React](https://pt-br.reactjs.org/)
- [React Native](https://reactnative.dev/)
- [TypeScript](https://www.typescriptlang.org/)

# Contribuição

Leia o arquivo [CONTRIBUTING.md](CONTRIBUTING.md) para saber detalhes sobre o nosso código de conduta e o processo de envio de solicitações *pull* (*Pull Request*) para nós.

# Autores

[Exemplo](https://github.com/testing-library/react-testing-library#contributors)

# Licença

Este projeto está licenciado sob a Licença MIT,  consulte o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

# Agradecimentos

Seção livre para você agradecer a todos que contribuiram para a execução do seu projeto.
