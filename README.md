# A Evolução dos Voos Domésticos no Brasil

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

# 1.1. Objetivos

O objetivo deste estudo é realizar uma Análise Exploratória dos Dados (Exploratory Data Analysis - EDA) do conjunto de dados **voos-anac-2000a2023**, adaptado pelo autor e disponível em (https://sistemas.anac.gov.br/dadosabertos/Voos%20e%20opera%C3%A7%C3%B5es%20a%C3%A9reas/Dados%20Estat%C3%ADsticos%20do%20Transporte%20A%C3%A9reo/); a fim de entender melhor através de dados reais o funcionamento e a evolução dos voos domésticos no país. Especificiamente serão respondidas as seguintes questões de pesquisa:

1. Quais as regiões do Brasil que mais fazem voos?
2. Evolução da quantidade de voos no Brasil?
3. Quais meses e anos tivemos mais voos domésticos?
4. Qual empresa realiza a maior quantidade de voos?
5. Quais os maiores destinos por região do Brasil?
6. Qual a média de horas voadas por companhia e mês?

# 2. Metodologia

O tópico apresentará um dicionário de dados, a realização do mapeamento, o processo de transformação e o tipo de modelagem utilizada.

# 2.1. Dicionário de Dados

![Dicionário de Dados](https://github.com/damisalves/Template-Repositorio/assets/137001435/9b5021a1-2caa-4afc-9fd5-bda71e207fbb)

# 2.1.1. Observações

A base de dados é descrita por quantidade de voos realizados por mês e ano de acordo com os demais campos.

- `distancia_voada_km:` a quantidade descrita de km/h;
- `decolagens:` Refere-se ao número de decolagens que ocorreram entre os aeródromos de origem e destino da etapa;
- `natureza:`  etapas remuneradas que são realizadas sob uma numeração de Horário de Transporte (HOTRAN). Recebem esse nome, pois possuem a característica de serem realizadas regularmente;
- `passageiros pagos:` Refere-se aos passageiros que ocupam assentos comercializados ao público e que geram receita, com a compra de assentos, para a empresa de transporte aéreo. Incluem-se nesta definição as pessoas que viajam em virtude de ofertas promocionais, as que se valem dos programas de fidelização de clientes, as que se valem dos descontos concedidos pelas empresas, as que viajam com tarifas preferenciais, as pessoas que compram passagem no balcão ou através do site de empresa de transporte aéreo e as pessoas que compram passagem em agências de viagem;
- `passageiros grátis:` Refere-se aos passageiros que ocupam assentos comercializados ao público mas que não geram receita, com a compra de assentos, para a empresa de transporte aéreo. Incluem-se nesta definição as pessoas que viajam gratuitamente, as que se valem dos descontos de funcionários das empresas aéreas e seus agentes, os funcionários de empresas aéreas que viajam a negócios pela própria empresa e os tripulantes ou quem estiver ocupando assento destinado a estes.

  # 2.2. Mapeamento dos Dados
  
Para melhor identificar quais as cidades dos aeroportos de origem e destino, foram realizadas as criações das dimensões Cidade Origem e Cidade Destino.

![Mapeamento de Dados - Origem](https://github.com/damisalves/Analise_Dados/assets/137001435/8e1860ee-632f-4e0e-86e7-e28164fdfe90) ![Mapeamento de Dados - Destino](https://github.com/damisalves/Analise_Dados/assets/137001435/3fccd5c7-85a3-49a2-be7b-7970499104e1)

# 2.3. Organização e Limpeza dos Dados

Foi realizado a extração dos dados brutos no site **anac.com.br** no formato CSV e transformado em XLSX para conexão na plataforma Power BI.

# 2.3.1. Extração em CSV e transformação em XLSX

# 2.3.2. Limpeza dos dados em branco

Não foi necessário a realização de limpeza de dados em branco.

# 2.3.3. Remoção das colunas: 

As colunas: CORREIO_KG, ASK, ATK, RTK, CARGA_GRATIS_KM, CARGA_PAGA_KM, CORREIO_KM, PAYLOAD, BAGAGEM_KM foram removidas por serem desnecessárias para análise. 

# 2.3.4. Filtragem e Classificação:

Foi realizado a filtragem das colunas: NATUREZA: doméstica e GRUPO_DE_VOO: regular, para melhor visualização dos dados e identificação dos critérios necessários para análise. 

# 2.4. Transformação

Para melhor calcular as horas voadas, foi transformado a coluna dimensão HORAS_VOADAS em MIN_VOADA, multiplicando a dimensão HORAS_VOADAS vezes 60, para identificar a quantidade de minutos.

![Transformação](https://github.com/damisalves/Analise_Dados/assets/137001435/52148c75-10c9-4e38-80a1-3058cd353cd3)

# 2.5. Processo de Modelagem

O processo de modelagem foi realizado seguindo os preceitos da modelagem multidimensional, no modelo Star Schema (Esquema Estrela), além disso foi realizado a criação de medidas e a criação das dimensões de Cidade Destino, Cidade Origem e Calendário

![Processo de Modelagem - 1](https://github.com/damisalves/Analise_Dados/assets/137001435/9fd73df2-4a29-4928-b360-246fbaa27e0a)

![Processo de Modelagem -2](https://github.com/damisalves/Analise_Dados/assets/137001435/9d831fa8-f3c5-40dd-84c8-00adb1f7f692)

# 3. Análise de Dados

![Análise de Dados - 1](https://github.com/damisalves/Analise_Dados/assets/137001435/20f0289b-20bb-4563-bd44-8cdf7b62c64c)

![Análise de Dados - 2](https://github.com/damisalves/Analise_Dados/assets/137001435/f0141d3a-a44d-4438-81bb-f9ce3f5a69fe)

Conforme dados analisados na ferramenta de analítica Power BI, pode se concluir que todas as questões levantadas na etapa 2 (Metodologia) foram possíveis de serem respondidas.

# 3.1. Quais as regiões do Brasil que mais fazem voos? 

`As regiões que mais realizam voos são as regiões do sudeste e nordeste.`

# 3.2. Evolução da quantidade de voos no Brasil? 

`Podemos destacar que houve um crescimento continuo desde o ano de 2000 a 2022.`

# 3.3. Quais meses e anos tivemos mais voos domésticos? 
`Houveram picos nos anos de 2011 a 2015 e um declínio nos anos de 2020 e 2021, devido a pandemia no Covid-19. O mês em que mais são realizados voos, é no mês de janeiro.`

# 3.4. Qual empresa realiza a maior quantidade de voos? 

`A empresa que mais realiza voos é a empresa TAM LINHAS AÉREAS S.A.`

# 3.5. Quais os maiores destinos por região do Brasil? 

`Os maiores destinos por regiões são respectivamente: Centro-Oeste: São Paulo e Guarulhos, Sudeste: Rio de Janeiro e São Paulo, Norte: Brasília e Belém, Nordeste: Guarulhos e Recife e Sul: São Paulo e Guarulhos.`

# 3.6. Qual a média de horas voadas por companhia e mês?

`A média de horas voadas é 72 horas mensais. Levando em conta que as maiores companhias áreas TAM LINHAS AÉREAS e GOL LINHAS AÉREAS voam 103 horas mensais, ou seja, 40% a mais que a média geral.`

# REFERÊNCIAS
- https://www.jusbrasil.com.br/artigos/transporte-aereo-domestico-o-que-significa-quais-sao-suas-aplicacoes/376349086
- https://www.anac.gov.br/acesso-a-informacao/dados-abertos/areas-de-atuacao/voos-e-operacoes-aereas/dados-estatisticos-do-transporte-aereo/48-dados-estatisticos-do-transporte-aereo
- https://sistemas.anac.gov.br/dadosabertos/Voos%20e%20opera%C3%A7%C3%B5es%20a%C3%A9reas/Dados%20Estat%C3%ADsticos%20do%20Transporte%20A%C3%A9reo/
