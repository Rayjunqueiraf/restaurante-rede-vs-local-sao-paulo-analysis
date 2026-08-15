# restaurante-rede-vs-local-sao-paulo-analysis
Análise estatística comparando restaurantes de rede e locais em São Paulo, com foco em preço, avaliação, popularidade, percepção de valor e desempenho de delivery.

# 🍽️ Restaurantes de Rede vs. Locais em São Paulo

## Uma análise estatística de preço, avaliação, popularidade, percepção de valor e delivery

## 📌 Sobre o projeto

Este projeto investiga se **restaurantes de rede e restaurantes locais na cidade de São Paulo** apresentam diferenças significativas em características comerciais, percepção dos consumidores e indicadores operacionais de delivery.

A análise combina **estatística descritiva, visualização de dados, testes estatísticos e regressão linear múltipla** para avaliar se o modelo de negócio — rede ou local — está associado a diferenças nos indicadores analisados.

O objetivo não é apenas comparar médias, mas verificar se as diferenças observadas nos dados possuem **evidência estatística suficiente** para sustentar as hipóteses formuladas.

---

## 🎯 Pergunta de negócio

> **Restaurantes de rede e restaurantes locais apresentam diferenças significativas em preço, avaliação, popularidade, percepção de valor e desempenho de delivery na cidade de São Paulo?**

A partir dessa pergunta, foram formuladas seis hipóteses relacionadas às principais dimensões analisadas.

---

## 📍 Escopo da análise

* **Localização:** cidade de São Paulo, Brasil
* **Unidades analisadas:** restaurantes
* **Modelos de negócio:** restaurantes de rede vs. restaurantes locais
* **Observações:** 305 restaurantes
* **Restaurantes de rede:** 80
* **Restaurantes locais:** 225

> **Nota:** os grupos possuem tamanhos diferentes, portanto essa característica foi considerada na interpretação dos resultados estatísticos.

---

## 🔎 Hipóteses

O estudo foi estruturado em seis hipóteses principais:

| Hipótese | Pergunta                                                                                                      |
| -------- | ------------------------------------------------------------------------------------------------------------- |
| **H1**   | O modelo de negócio está associado a diferenças de preço?                                                     |
| **H2**   | Restaurantes de rede e locais apresentam diferenças nas avaliações dos consumidores?                          |
| **H3**   | O modelo de negócio está associado a diferenças de popularidade?                                              |
| **H4**   | Restaurantes de rede e locais apresentam diferenças na percepção de valor?                                    |
| **H5**   | Existem diferenças entre os modelos de negócio nos indicadores de delivery?                                   |
| **H6**   | O modelo de negócio permanece associado à avaliação após controlar por outras características do restaurante? |

---

# 📊 Metodologia

A análise foi desenvolvida em Python utilizando um fluxo composto por diferentes etapas.

### 1. Preparação dos dados

Foram realizadas etapas de:

* inspeção da base;
* tratamento e organização das variáveis;
* identificação dos grupos de restaurantes;
* verificação das características das variáveis;
* preparação dos dados para as análises estatísticas.

### 2. Estatística descritiva

Foram calculadas medidas como:

* média;
* mediana;
* diferenças entre grupos;
* tamanho das amostras;
* distribuição das variáveis.

As estatísticas descritivas foram utilizadas para identificar padrões iniciais entre restaurantes de rede e locais.

### 3. Visualização

Foram utilizados gráficos para comparar visualmente a distribuição dos indicadores entre os grupos.

Entre as visualizações utilizadas estão:

* boxplots;
* comparações de distribuição;
* gráficos comparativos entre redes e restaurantes locais.

As visualizações foram utilizadas como complemento aos testes estatísticos, e não como substituição da inferência estatística.

### 4. Testes estatísticos

Foram realizados testes para verificar se as diferenças observadas entre restaurantes de rede e locais apresentavam evidência estatística.

Foi adotado:

**Nível de significância: α = 0,05**

Assim:

* `p < 0,05` → evidência estatística de diferença;
* `p ≥ 0,05` → não há evidência estatística suficiente para rejeitar a hipótese nula.

### 5. Modelo multivariado

Foi utilizada uma **regressão linear múltipla** para verificar se o modelo de negócio permanece associado à variável dependente após considerar simultaneamente outras características dos restaurantes.

Foram consideradas variáveis relacionadas a:

* modelo de negócio;
* nível de preço;
* preço médio do menu;
* popularidade;
* percepção de valor;
* tempo médio de entrega;
* taxa de cancelamento;
* custo total do delivery.

### 6. Diagnóstico de multicolinearidade

Também foi realizado o cálculo do **Variance Inflation Factor (VIF)** para avaliar possíveis problemas de multicolinearidade entre as variáveis explicativas.

Foi identificada forte sobreposição entre:

* **Nível de preço — VIF = 10,28**
* **Preço médio do menu — VIF = 10,27**

Esse resultado foi considerado uma limitação metodológica do modelo multivariado.

---

# 📈 Principais resultados

## 💰 Preço

As análises não encontraram evidência estatística suficiente para afirmar que restaurantes de rede e restaurantes locais apresentam diferenças significativas nos indicadores de preço analisados.

Embora possam existir diferenças numéricas entre as médias dos grupos, elas não foram estatisticamente significativas ao nível de 5%.

**Resultado da H1: ❌ Não apoiada**

---

## ⭐ Avaliação

Não foi identificada diferença estatisticamente significativa entre restaurantes de rede e locais em relação à avaliação média dos consumidores.

Isso indica que, dentro da amostra analisada, não há evidência suficiente para afirmar que um dos modelos de negócio apresente avaliações sistematicamente superiores ao outro.

**Resultado da H2: ❌ Não apoiada**

---

## 📈 Popularidade

As análises também não identificaram diferença estatisticamente significativa no índice de popularidade entre restaurantes de rede e restaurantes locais.

Portanto, o fato de um restaurante pertencer a uma rede não apresentou associação estatisticamente comprovada com maior ou menor popularidade na amostra.

**Resultado da H3: ❌ Não apoiada**

---

## 💎 Percepção de valor

Não foram encontradas evidências estatísticas suficientes de diferença na percepção de valor entre os dois modelos de negócio.

Assim, os resultados não sustentam a hipótese de que restaurantes de rede e restaurantes locais sejam percebidos de maneira significativamente diferente em relação ao valor oferecido.

**Resultado da H4: ❌ Não apoiada**

---

# 🚴 Delivery

A dimensão de delivery apresentou o resultado mais interessante da análise.

Foram comparados:

* tempo estimado de entrega;
* tempo médio de entrega;
* atraso na entrega;
* taxa de cancelamento;
* taxa de entrega;
* taxa de serviço;
* taxa de embalagem;
* custo total do delivery.

De forma geral, os restaurantes de rede apresentaram médias superiores aos restaurantes locais nos indicadores analisados.

Entretanto, **a maior parte dessas diferenças não foi estatisticamente significativa**.

### Principal diferença encontrada

| Indicador                   |     Rede |    Local | Diferença |    p-valor |
| --------------------------- | -------: | -------: | --------: | ---------: |
| **Custo total do delivery** | **9,31** | **8,45** | **+0,87** | **0,0214** |

Como `p = 0,0214 < 0,05`, existe evidência estatística de diferença no custo total do delivery entre os grupos.

Os restaurantes de rede apresentaram custo médio aproximadamente **0,87 unidade maior** que os restaurantes locais.

Por outro lado, não foram encontradas diferenças estatisticamente significativas nos demais indicadores de delivery.

**Resultado da H5: 🟡 Parcialmente apoiada**

---

# 📊 Modelo multivariado

A regressão linear múltipla foi utilizada para verificar se o modelo de negócio permanece associado à avaliação após controlar simultaneamente por outras características dos restaurantes.

A variável **Restaurante local** apresentou:

| Métrica         |   Resultado |
| --------------- | ----------: |
| Coeficiente     | **-0,1055** |
| p-valor         |  **0,3590** |
| IC 95% inferior | **-0,3315** |
| IC 95% superior |  **0,1205** |

Como `p = 0,3590 > 0,05`, não foi encontrada evidência estatisticamente significativa de associação entre o modelo de negócio e a variável dependente após o controle pelas demais variáveis.

Além disso, o intervalo de confiança inclui zero.

**Resultado da H6: ❌ Não apoiada**

### ⚠️ Limitação do modelo

O diagnóstico de multicolinearidade identificou VIF elevado para:

* Nível de preço: **10,28**
* Preço médio do menu: **10,27**

Isso indica forte sobreposição entre essas duas variáveis.

Por esse motivo, os resultados do modelo multivariado devem ser interpretados com cautela. Uma análise de robustez retirando uma dessas variáveis pode ser utilizada para verificar a estabilidade dos resultados.

---

# 🧠 Principais insights

Os resultados sugerem que as diferenças entre restaurantes de rede e locais **não são generalizadas para todas as dimensões analisadas**.

Os principais insights foram:

1. **Preço:** não houve evidência estatística suficiente de diferença entre os grupos.

2. **Avaliação:** não houve diferença estatisticamente significativa entre redes e locais.

3. **Popularidade:** não houve evidência de associação significativa com o modelo de negócio.

4. **Percepção de valor:** não foram identificadas diferenças estatisticamente significativas.

5. **Delivery:** a principal diferença encontrada foi no **custo total**, significativamente maior entre restaurantes de rede.

6. **Modelo multivariado:** o tipo de restaurante não apresentou associação estatisticamente significativa com a variável dependente após o controle pelas demais características.

Em outras palavras, os resultados indicam que **ser uma rede ou um restaurante local não parece, por si só, determinar diferenças generalizadas de desempenho** nas dimensões analisadas.

A principal exceção encontrada foi o **custo total do delivery**.

---

# 📋 Síntese das hipóteses

| Hipótese                                          | Resultado                   |
| ------------------------------------------------- | --------------------------- |
| H1 — Modelo de negócio × preço                    | ❌ **Não apoiada**           |
| H2 — Modelo de negócio × avaliação                | ❌ **Não apoiada**           |
| H3 — Modelo de negócio × popularidade             | ❌ **Não apoiada**           |
| H4 — Modelo de negócio × percepção de valor       | ❌ **Não apoiada**           |
| H5 — Modelo de negócio × delivery                 | 🟡 **Parcialmente apoiada** |
| H6 — Modelo de negócio × avaliação após controles | ❌ **Não apoiada**           |

---

# 💼 Relevância para negócio

Os resultados podem ser relevantes para gestores e operadores do setor de restaurantes.

A ausência de diferenças estatisticamente significativas em preço, avaliação, popularidade e percepção de valor sugere que **o simples fato de pertencer a uma rede não garante vantagem clara nessas dimensões**.

Por outro lado, o maior custo total de delivery observado nas redes pode indicar uma dimensão operacional que merece investigação adicional.

É importante destacar que o estudo não permite identificar a causa dessa diferença. O maior custo pode estar relacionado a diferentes estruturas operacionais, estratégias comerciais, taxas ou características dos restaurantes e dos pedidos.

Portanto, o resultado deve ser interpretado como um **sinal para investigação**, e não como evidência de causalidade.

---

# ⚠️ Limitações

Algumas limitações devem ser consideradas:

### 1. Recorte geográfico

A análise contempla exclusivamente restaurantes localizados na **cidade de São Paulo**.

Portanto, os resultados não devem ser automaticamente generalizados para outras cidades, estados ou países.

### 2. Tamanho desigual dos grupos

A amostra contém:

* 80 restaurantes de rede;
* 225 restaurantes locais.

Essa diferença deve ser considerada na interpretação das comparações.

### 3. Associação não implica causalidade

Os resultados identificam associações estatísticas observadas na amostra.

Não é possível concluir que o modelo de negócio seja a causa direta das diferenças encontradas.

### 4. Multicolinearidade

O modelo multivariado apresentou VIF elevado entre nível de preço e preço médio do menu.

Isso pode dificultar a interpretação dos efeitos individuais dessas variáveis.

### 5. Variáveis não observadas

Outros fatores que não estão presentes na base podem influenciar os resultados, como localização específica dentro da cidade, tipo de culinária, tamanho do restaurante, número de pedidos, estrutura operacional e perfil dos consumidores.

---

# 🚀 Possíveis extensões

Algumas análises futuras poderiam aprofundar os resultados:

* ampliar a amostra para outras cidades;
* utilizar dados ao longo do tempo;
* analisar dados no nível do pedido;
* controlar por tipo de culinária;
* controlar por localização/bairro;
* investigar diferenças de delivery por faixa de preço;
* analisar o impacto de avaliações sobre popularidade;
* testar modelos alternativos de regressão;
* realizar análise de robustez do modelo multivariado;
* investigar especificamente os fatores associados ao maior custo de delivery nas redes.

---

# 🛠️ Tecnologias utilizadas

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **SciPy**
* **Statsmodels**
* **Jupyter Notebook / Google Colab**

---

# 📂 Estrutura do projeto

```text
restaurant-chain-vs-local-sao-paulo-analysis/
│
├── README.md
├── restaurant_analysis.ipynb
│
├── data/
│   └── README.md
│
├── images/
│   ├── price_comparison.png
│   ├── rating_comparison.png
│   ├── popularity_comparison.png
│   ├── value_perception.png
│   └── delivery_distribution.png
│
└── requirements.txt
```

---

# ▶️ Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/restaurant-chain-vs-local-sao-paulo-analysis.git
```

### 2. Instale as dependências

```bash
pip install -r requirements.txt
```

### 3. Abra o notebook

O projeto pode ser executado utilizando:

* Jupyter Notebook;
* JupyterLab;
* Google Colab;
* ou outro ambiente compatível com notebooks Python.

---

# 📌 Conclusão

Este projeto investigou se restaurantes de rede e restaurantes locais na cidade de São Paulo apresentam diferenças em preço, avaliação, popularidade, percepção de valor e operação de delivery.

De forma geral, os resultados **não sustentaram diferenças estatisticamente significativas generalizadas entre os modelos de negócio**.

A principal evidência encontrada esteve relacionada ao **custo total do delivery**, que foi significativamente maior entre restaurantes de rede.

O estudo também demonstra a importância de combinar **análise descritiva e inferencial**: uma diferença observada nas médias não necessariamente representa uma diferença estatisticamente comprovada.

Por fim, o modelo multivariado não encontrou associação significativa entre o modelo de negócio e a variável dependente após os controles considerados, embora a presença de multicolinearidade entre variáveis de preço indique a necessidade de cautela e possíveis análises de robustez.

> **Principal takeaway:** as diferenças entre restaurantes de rede e locais parecem ser mais específicas do que generalizadas, com o custo de delivery surgindo como o principal indicador em que foi encontrada evidência estatística de diferença.

---

## 👤 Autor

**Ray Junqueira**

Projeto desenvolvido como parte do portfólio de **Data Analytics / Data Science**.


