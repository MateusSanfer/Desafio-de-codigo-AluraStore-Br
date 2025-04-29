
# 📊 Desafio de Análise de Lojas - Alura Store

## Descrição
Este projeto é resultado do primeiro desafio de análise de dados do curso da Alura.  
O objetivo é ajudar o Senhor João a decidir qual das quatro lojas fictícias da rede Alura Store ele deve vender para investir em um novo empreendimento.  

A análise foi realizada com base em diversas métricas:
- Faturamento total
- Avaliação dos clientes
- Vendas por categoria
- Produtos mais e menos vendidos
- Frete médio
- Distribuição geográfica de vendas (Latitude e Longitude)

## Objetivos
- Analisar dados de vendas e desempenho das lojas.
- Calcular métricas relevantes como faturamento, avaliação dos clientes, vendas por categoria e frete médio.
- Produzir visualizações gráficas para facilitar a interpretação dos dados.
- Apresentar uma recomendação final baseada nos dados analisados.

## Tecnologias Utilizadas
- **Python 3.11** — Linguagem de programação principal.
- **Pandas** — Manipulação e análise de dados.
- **Matplotlib** — Criação de gráficos e visualizações.


## Etapas da Análise
1. **Carregamento dos dados CSV:**  
   Cada loja possui seu próprio arquivo de dados (loja1.csv, loja2.csv, loja3.csv, loja4.csv).

2. **Análises realizadas:**
   - Faturamento total por loja.
   - Avaliações médias dos clientes.
   - Categorias de produtos mais vendidos.
   - Produtos mais e menos vendidos.
   - Frete médio por loja.
   - Distribuição geográfica das vendas.

3. **Geração de Gráficos:**
   - Gráfico de barras: Comparativo de faturamento entre as lojas.
   - Gráfico de barras percentuais: Distribuição de vendas por categoria.
   - Gráfico de linha: Avaliação média por loja.
   - Gráfico de pizza: Comparativo do frete médio.
   - Gráfico de dispersão: Localização geográfica das vendas.

## Como Executar o Projeto
### 1. Clone o repositório
```bash
git clone https://github.com/MateusSanfer/Desafio-de-codigo-AluraStore-Br.git
```

### 2. Acesse a pasta do projeto
```bash
cd Desafio-de-codigo-AluraStore-Br
```

### 3. Instale as dependências necessárias
```bash
import pandas as pd
import matplotlib.pyplot as plt
```

### 4. Carregue os dados
Os arquivos CSV devem ser carregados utilizando o Pandas:

```python
import pandas as pd
import matplotlib.pyplot as plt

url = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_1.csv"
url2 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_2.csv"
url3 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_3.csv"
url4 = "https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_4.csv"

loja = pd.read_csv(url)
loja2 = pd.read_csv(url2)
loja3 = pd.read_csv(url3)
loja4 = pd.read_csv(url4)

loja.head()
```

Se necessário, baixe os dados originais do repositório da Alura:  
[Challenge 1 Data Science - GitHub](https://github.com/alura-es-cursos/challenge1-data-science.git)

### 5. Execute a análise
O projeto está estruturado em diferentes blocos de código, cada um responsável por calcular métricas específicas e gerar visualizações gráficas.

Exemplo de cálculo de faturamento:
```python
print('Análise do faturamento: ')
faturamento ={
    "Loja 01": loja["Preço"].sum(),
    "Loja 02": loja2["Preço"].sum(),
    "Loja 03": loja3["Preço"].sum(),
    "Loja 04": loja4["Preço"].sum(),
}
for nome_lojas, valor in faturamento.items():
    print(f'{nome_lojas}: R${valor:,.2f}')
```

Exemplo de gráfico:
```python

lojas = list(faturamento.keys())   # ['Loja 01', 'Loja 02', 'Loja 03', 'Loja 04']
valores = list(faturamento.values()) # [1534509.12, 1488459.06, 1464025.03, 1384497.58]

plt.figure(figsize=(8,6))  # Define o tamanho da figura
plt.bar(lojas, valores, color=['skyblue', '#348888', '#FA7F08', '#F24405'])

plt.title("Análise do Faturamento", fontsize=16)
plt.xlabel("Lojas", fontsize=12)
plt.ylabel("Faturamento (R$)", fontsize=12)

for i, valor in enumerate(valores):
    plt.text(i, valor + 10000, f'R${valor:,.0f}', ha='center', va='bottom', fontsize=10)

plt.tight_layout()
plt.show()
```

## Recomendação Final

- Após rodar a análise, interprete os resultados para identificar qual loja apresenta o pior desempenho em termos de faturamento, avaliações e outras métricas. A recomendação final será baseada nesses dados.
- Resultados A análise mostra que a Loja 04 apresenta o menor faturamento, vendas por categoria e avaliações em comparação com as demais lojas.
- Apesar de ter o menor custo de frete, o desempenho inferior em outros pontos faz com que seja a loja mais indicada para ser vendida.

### Portanto:
➡️ A recomendação é que o Senhor João **venda a Loja 04** para focar seus recursos no novo empreendimento, pois ela apresentou o pior desempenho em todas as métricas analisadas.
.

## 📢 Contribuições
Sinta-se à vontade para:
- Fazer fork do projeto
- Abrir pull requests
- Reportar problemas ou melhorias

## 🧑🏾‍💻 Autor
| [<img src="https://avatars.githubusercontent.com/u/126841158?v=4" width=115><br><sub>Mateus Sanfer</sub>](https://github.com/MateusSanfer) |
| :---: |
