# **Clustering e Análise RFM para Segmentação de Clientes e implementação de medidas estratégicas de marketing**
## Descrição do Projeto
Este projeto tem como objetivo realizar a segmentação de clientes utilizando dados de transações de um varejo online. A segmentação foi feita com base na análise RFM (Recência, Frequência e Valor Monetário), com uma importante adaptação de que ao invés de utilizar o valor total gasto por um cliente, será utilizado o valor médio por transação, que proporciona uma visão mais clara sobre o comportamento de compra, independente da frequência de transações. Junto a isso, foram aplicadas técnicas de clustering para identificar perfis de comportamento, Realizando uma comparação entre dois métodos principais: K-Means e Gaussian Mixture Model (GMM).

Os resultados dessa análise revelaram perfis distintos de clientes, possibilitando a criação de estratégias personalizadas para retenção e fidelização.

## Motivação
A segmentação de clientes com base na análise RFM é uma técnica comum em marketing, permitindo que empresas agrupem clientes com comportamentos semelhantes. Com esse projeto, a intenção foi entender como diferentes abordagens de clustering (K-Means e GMM) podem impactar a qualidade dos grupos formados e, consequentemente, a eficácia das estratégias de retenção.

Em vez de usar o valor total gasto pelos clientes, foi feita uma adaptação importante: o uso do valor médio das transações, proporcionando uma visão mais clara sobre o comportamento de compra, independente da frequência de transações.

## Metodologia
### 1. Transformação de Dados
Criação das variáveis Recência, Frequência e Valor Monetário médio das transações a partir do conjunto de dados de transações.
Aplicação de técnicas de escalonamento com RobustScaler para lidar com outliers e preparar os dados para o clustering.
### 2. Modelos de Clustering
Teste de diferentes números de clusters (2 a 8 clusters) para identificar o número ideal com base no Silhouette Score, elbow method e metodos de teoria da informação com AIC/BIC.
Comparação de dois modelos:
K-Means
Gaussian Mixture Model (GMM)
### 3. Avaliação de Modelos
Avaliação de qualidade dos clusters usando métricas como Silhouette Score e BIC/AIC para o GMM.
Análise das características dos clusters para identificar padrões comportamentais nos grupos formados.
### 4. Visualização
Pairplots: Analisam a relação entre as variáveis e suas distribuições.

Boxplots: Detalham as distribuições das variáveis RFM dentro de cada cluster.

Gráfico 3D: Mostra a distribuição dos clusters no espaço RFM.


## Resultados
**Após comparar os dois modelos de clustering, os principais resultados foram:**

Gaussian Mixture Model (GMM) apresentou uma melhor qualidade de clusters em comparação com K-Means, separando melhor os clientes e identificando um maior número de clientes VIPs.

**Foram gerados os seguintes agrupamentos:**

**Clientes VIP 1**: clientes com altissima frequência e valor de ticket médio.

**Clientes VIP 2:** frequentes: clientes com altissimo ticket medio e boa frequência

**Clientes inativos de alto ticket:** clientes que compraram esporadicamente, mas fazem compras de alto valor.

**Clientes médios ativos:** clientes com ticket baixo-medio, e que compram frequentemente.

**Clientes esporádicos:** aqueles que compraram 1 ou 2 vezes e nunca voltaram.

**Clientes de baixa frequencia:** Clientes que compraram pouco durante o ano e tem em media mais de 30 dias sem comprar


## Conclusão
Este projeto demonstrou a eficácia de técnicas de clustering aplicadas à análise RFM para segmentação de clientes. Com o Gaussian Mixture Model tendo se mostrado mais eficaz do que o K-Means para esse caso. 

Essas segmentações podem ser utilizadas para aplicar estratégias como:

**• Programas de fidelidade exclusivos para clientes VIPs.**

**• Campanhas de reativação para clientes inativos.**

**• Ofertas personalizadas para aumentar o ticket médio de clientes recorrentes.**
