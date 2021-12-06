## Airbnb - Estimando os preços de listagens de Airbnb da cidade do Rio de Janeiro
Com os dados disponibilizados pelo [Inside Airbnb](http://insideairbnb.com/get-the-data.html) -"[...] um conjunto independente e não comercial de ferramentas e dados que permitem que você explore como o Airbnb está realmente sendo usado em cidades ao redor do mundo" - foi realizado um estudo que visa analisar como está sendo utilizado o Airbnb na cidade do Rio de Janeiro.

## Tabela de conteúdo
<a id='Tabela de conteúdo'></a>

### <a href='#1. Introdução'> 1. Introdução </a>
### <a href='#2. O Dataset'> 2. O Dataset </a>
### <a href='#3. Hipóteses iniciais'> 3. Hipóteses iniciais </a>
### <a href='#4. Modelo'> 4. Modelo </a>
### <a href='#5. Resultados'> 5. Resultados </a>

### 1. Introdução
<a id='1. Introdução'></a>

Este estudo tem como objetivo analisar como o Airbnb está sendo utilizado na cidade do Rio de Janeiro através de dados fornecido pela própria organização. Como resultado, temos a criação de um modelo de predição de preços baseado nas features mais relevantes. Além disto, o projeto reforça a importância dos dados nas decisões dos negócios e como podemos tirar insights a partir dos mesmos para termos o melhor resultado possível na resolução de problemas.

O relatório irá conter tanto as característica do Airbnb na cidade do Rio de Janeiro quanto os resultados obtidos a partir do Modelo de Machine Learning desenvolvido - através da Regressão Linear e Árvore de decisão - com a finalidade de prever os preços baseados nas features de cada Airbnb.


### 2. O Dataset
<a id='2. O Dataset'></a>

No primeiro notebook, será performado uma análise dos dados de listagens da cidade do Rio de Janeiro. O dataset foi nomeado como sendo `listings.csv.gz` e são referente aos dados de Julho de 2021. Para auxiliar na interpretação dos dados, o dicionário - que também é disponibilizado pelo Inside Airbbv - está disponibilizado no arquivo `Inside Airbnb Data Dictionary - listings.csv detail v4.csv`.


> Este projeto foi desenvolvido utilizando PySpark na plataforma do Databricks. <br>


### 3. Hipóteses iniciais 
<a id='3. Hipóteses iniciais'></a>

No início do estudo foram levantadas algumas hipóteses que serão investigadas durante este estudo. Elas são:

 1. **Preço**
<br>	Considerando que o Estado do Rio de Janeiro é litorâneo, supõe-se que os preços da diária dos Airbnb são maiores quanto mais próximos estão localizados mais próximos do mar. 
 2. **Features**
 <br>	As features mais determinantes para o preço de um Airbnb se darão pela cidade no qual está localizado e com uma boa avaliação da locação e do anfitrião.

### 4. Modelo
<a id='4. Modelo'></a>

Para este problema, será utilizado diferentes modelos de Aprendizado Supervisionado a fim de prever os preços do Airbnb baseado nas diferentes features encontradas nos dados. Para este projeto, regressão será o método focal. 

Dentre a infinidade de métodos de regressão que existem, foi utilizado a **Regressão Linear**, por ser um modelo simples e, em alguns cenários, muito eficaz, e **Árvore Aleatória - Random Forest** , por ser um modelo mais robusto, mas que entrega uma boa precisão. Serão utilizado esses dois modelos a fim de comparar a acurácia entre cada modelo e entender qual é mais eficiente em solucionar ao problema proposto. 


### Resultados
<a id='5. Resultados'></a>
Como podemos perceber, o modelo de Regressão Linear em comparação com o modelo de Random Forest gerado é um bom modelo para predição de preços da diária de Airbnbs na cidade do Rio de Janeiro. Além disso, as features *bathrooms, bedrooms,accommodates, latitude e longitude* são as features mais importantes para o nosso modelo. 

Com o desenvolvimento foi percebido que os modelos de regressão utilizados são altamente influenciados por outliers, uma informação que ajudaria a resolver este problema seria o tamanho da locação, pois algumas locações possuem a mesma quantidade de banheiros, quartos, cama e localização porém se diferem no tamanho da propriedade o que acaba gerando uma grande discrepância nos preços - informação que não é repassada diretamente no dataset - entretando, quando limitados os preços para até R$2.000 reais temos um desempenho melhor na generalização do modelo. 

Vale ressaltar que, de fato, bairros mais próximo ao literal tendem a ter um maior valor médio e a maioria dos Airbnb se enquadram em um Cluster de preço que vão até o máximo R$ 1.000 o valor da diária. 

Estas análises tem muito valor tanto para quem quer viajar e encontrar um bom lugar com o melhor preço e para pessoas que pretendem colocar seu apartamento ou casa para locação no Airbnb saber a média de preço que ele pode cobrar de acordo com as características da locação. 
<div align="center">Work in progress</div>
