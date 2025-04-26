Desafio de Análise de Vendas - Alura Store
Descrição
Este projeto tem como objetivo analisar o desempenho de quatro lojas fictícias da rede Alura Store, a fim de ajudar o Senhor João a decidir qual loja vender para iniciar um novo empreendimento. A análise foi realizada com base em métricas de faturamento, avaliação dos clientes, vendas por categoria, produtos mais e menos vendidos e frete médio.

Com isso, foi possível identificar a loja com menor eficiência e gerar uma recomendação para o Senhor João.

Objetivos
Analisar dados de vendas e desempenho das lojas.

Calcular métricas importantes como faturamento, avaliação dos clientes, vendas por categoria, e frete médio.

Visualizar os resultados com gráficos para facilitar a interpretação dos dados.

Apresentar uma recomendação final sobre qual loja o Senhor João deve vender.

Funcionalidades
Análise do Faturamento: Soma do preço de todos os produtos vendidos em cada loja.

Vendas por Categoria: Análise das categorias mais vendidas em cada loja.

Média de Avaliação das Lojas: Cálculo da média das avaliações feitas pelos clientes.

Produtos Mais e Menos Vendidos: Identificação dos produtos com maior e menor número de vendas.

Cálculo do Frete Médio: Determinação do custo médio de frete por loja.

Tecnologias Utilizadas
Python: Linguagem de programação utilizada.

Pandas: Biblioteca para manipulação e análise de dados.

Matplotlib: Biblioteca para criação de gráficos e visualizações.

Jupyter Notebook (opcional): Ambiente de desenvolvimento interativo recomendado para execução do código.

Como Rodar o Projeto
Instale as dependências:

Se ainda não tiver o Python e as bibliotecas necessárias instaladas, você pode instalar as dependências utilizando o pip. Execute o seguinte comando:

bash
Copiar
Editar
pip install pandas matplotlib
Carregue os dados:

O projeto espera que os dados das lojas sejam fornecidos como arquivos CSV (por exemplo, loja.csv, loja2.csv, etc.). Certifique-se de carregar os arquivos corretamente utilizando o Pandas. Exemplo de código para carregar os dados:

python
Copiar
Editar
import pandas as pd

loja = pd.read_csv('loja.csv')
loja2 = pd.read_csv('loja2.csv')
loja3 = pd.read_csv('loja3.csv')
loja4 = pd.read_csv('loja4.csv')
Execute a análise:

Após carregar os dados, execute as funções para calcular as métricas de desempenho e gerar os gráficos. O código está estruturado em diferentes partes, cada uma responsável por uma análise específica.

Exemplo de código para calcular o faturamento:

python
Copiar
Editar
faturamento = {
    "Loja 01": loja["Preço"].sum(),
    "Loja 02": loja2["Preço"].sum(),
    "Loja 03": loja3["Preço"].sum(),
    "Loja 04": loja4["Preço"].sum(),
}

for nome_lojas, valor in faturamento.items():
    print(f'{nome_lojas}: R${valor:,.2f}')
Visualizações:

Utilize o matplotlib para criar gráficos que ajudam a ilustrar melhor os dados analisados. Por exemplo:

python
Copiar
Editar
import matplotlib.pyplot as plt

# Exemplo de gráfico de barras para faturamento
lojas = ["Loja 01", "Loja 02", "Loja 03", "Loja 04"]
faturamento_values = [faturamento["Loja 01"], faturamento["Loja 02"], faturamento["Loja 03"], faturamento["Loja 04"]]

plt.bar(lojas, faturamento_values)
plt.title('Faturamento por Loja')
plt.xlabel('Lojas')
plt.ylabel('Faturamento (R$)')
plt.show()
Leitura e Interpretação dos Resultados:

Após rodar a análise, interprete os resultados para identificar qual loja apresenta o pior desempenho em termos de faturamento, avaliações e outras métricas. A recomendação final será baseada nesses dados.

Resultados
A análise mostra que a Loja 04 apresenta o menor faturamento, vendas por categoria e avaliações em comparação com as demais lojas.

Apesar de ter o menor custo de frete, o desempenho inferior em outros pontos faz com que seja a loja mais indicada para ser vendida.

Conclusão
A recomendação final é que o Senhor João venda a Loja 04, pois ela apresentou o pior desempenho em todas as métricas analisadas.

Contribuições
Se você quiser contribuir com este projeto, sinta-se à vontade para fazer fork, abrir pull requests ou relatar problemas.
