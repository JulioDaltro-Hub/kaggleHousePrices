# kaggleHousePrices

Utilizando o dataset de Ames, Iowa, este projeto busca solucionar um dos desafios no site Kaggle aplicando técnicas avançadas de Regressão com Machine Learning para prever o preço de venda de casas.

O modelo analisa 80 variáveis explicativas para estimar o valor final de mercado com alta precisão. 
O dataset original possuía muitos valores ausentes e redundantes. Dentre outras soluções, o processo de limpeza incluiu principalmente:

  1. Remoção de colunas com baixa variabilidade (ex: Utilities, Street).
  2. Tratamento de nulos em garagens e piscinas, transformando-os em categorias "NoGarage" ou "NoPool".
  3. Conversão de escalas qualitativas (Ex, Gd, TA, Fa, Po) em valores numéricos (5, 4, 3, 2, 1).
  4. Transformar colunas em colunas binárias.

Além dos Drops, também foram criadas variáveis estratégicas, alguns exemplos são:

  1. lifetime: Idade do imóvel no momento da venda (YrSold - YearBuilt).
  2. TotalOutdoorSF: Consolidação de todas as áreas externas (varandas, decks, porches).
  3. TotalBathrooms & TotalWashrooms: Unificação de banheiros do porão e andares superiores.
  4. Mapeamento de Vizinhança: Bairros categorizados por faixas de preço mediano, transformando localização em força preditiva numérica.

Aqui estão as colunas que foram mais significativas para o modelo

<img width="1109" height="644" alt="image" src="https://github.com/user-attachments/assets/9e8be3b9-3f0d-4efc-9940-e0c76aee0400" />

Em relação a performance do Modelo, temos:

  O modelo explica quase 90% da variação dos preços! Alcançando impressionantes 88.94%
  Acurácia Média: 89.29% baseada no erro percentual.
  Erro Médio Absoluto (MAE): $17,797.58

Tendo em vista a amplitude dos preços, uma média de erros de aproximadamente 18 mil reais é aceitável devido a quantidade de dados sobre imóveis mais caros.

Ao traçar uma linha imaginando os valores do imóvel, notamos que os erros acontecem justamente nas casas mais caras.
Portanto, concluímos que as principais falhas do modelo estão vinculadas a falta de dados para imóveis de maior custo.
<img width="1094" height="683" alt="image" src="https://github.com/user-attachments/assets/a0d7fce3-67a8-4118-8c8d-31af9c45ea5d" />

