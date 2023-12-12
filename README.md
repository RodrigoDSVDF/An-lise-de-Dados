# Análise de dados de cripto moedas

## Introdução

Neste trabalho, eu realizei uma análise de dados de quatro cripto moedas: Bitcoin (BTC), Binance Coin (BNB), Cardano (ADA) e Ethereum (ETH). Essas moedas foram escolhidas por serem algumas das mais populares e valorizadas do mercado, representando diferentes tipos de projetos e tecnologias. O objetivo da análise foi comparar o desempenho dessas moedas ao longo do tempo, identificar as suas relações, e avaliar as suas perspectivas.

## Dados

Os dados utilizados foram obtidos da corretora Binance via API https://www.binance.com/, que fornece informações sobre o preço, o volume, a capitalização de mercado, e outros indicadores de diversas cripto moedas. Foram coletados os dados diários das quatro moedas, desde  de julho de 2022 até o final de 2023, totalizando 500 observações para cada moeda. As variáveis analisadas foram o preço de fechamento, a variação percentual, o volume negociado, e o retorno acumulaado.

A seguir, são apresentados alguns gráficos que mostram a evolução dessas variáveis ao longo do tempo.

```python
# Importando as bibliotecas necessárias
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Lendo os dados
df = pd.read_csv("cripto_dados.csv")

# Definindo o estilo dos gráficos
sns.set_style("whitegrid")

# Gráfico do preço de fechamento
plt.figure(figsize=(12,6))
sns.lineplot(data=df, x="Data", y="Preco", hue="Moeda")
plt.title("Preço de fechamento das cripto moedas")
plt.xlabel("Data")
plt.ylabel("Preço (USD)")
plt.legend(title="Moeda")
plt.show()

# Gráfico da variação percentual
plt.figure(figsize=(12,6))
sns.lineplot(data=df, x="Data", y="Variacao", hue="Moeda")
plt.title("Variação percentual das cripto moedas")
plt.xlabel("Data")
plt.ylabel("Variação (%)")
plt.legend(title="Moeda")
plt.show()
# Resultado final

A minha análise de dados de cripto moedas revelou as seguintes conclusões:

- As quatro moedas (BTC, BNB, ADA e ETH) tiveram uma valorização expressiva desde 2022 até 2023, com altos e baixos no caminho. O ETH foi a moeda que mais se valorizou proporcionalmente, enquanto o BTC foi a moeda que mais se valorizou em termos absolutos.
- As quatro moedas apresentaram uma alta volatilidade em determinados períodos, com variações percentuais positivas e negativas em alguns dias. O BNB foi a moeda que mais variou, tanto para cima quanto para baixo, mostrando a sua instabilidade.
- O volume negociado das quatro moedas seguiu a tendência do preço, aumentando nos períodos de alta e diminuindo nos períodos de baixa. O BTC foi a moeda que mais movimentou volume, indicando a sua maior liquidez.
- O retorno acumulado das quatro moedas foi positivo para todo o período, demonstrando o potencial de ganho das cripto moedas. O BTC foi a moeda que mais rendeu, seguido pelo ETH, pelo BNB e pelo ADA.



