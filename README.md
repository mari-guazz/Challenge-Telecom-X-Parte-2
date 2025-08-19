**Desafio TelecomX: Análise e Modelagem Preditiva de Evasão de Clientes**

Este projeto busca analisar a base de clientes e desenvolver modelos preditivos capazes de identificar clientes com alta probabilidade de evasão (churn). O objetivo final é fornecer insights valiosos e propor estratégias de retenção eficazes.

**Estrutura do Repositório**

O projeto é composto pelo seguinte arquivo principal:

"Challenge_TelecomX_Parte2.ipynb", um notebook Jupyter que documenta todo o processo de análise, desde a preparação dos dados até a modelagem preditiva e a análise dos resultados.

**Metodologia**

A análise e a modelagem foram divididas nas seguintes etapas:

1. Preparação dos Dados
Carregamento e Limpeza: Os dados foram carregados do arquivo dados_tratados.csv. A coluna customerID foi removida, pois não tem valor preditivo.

Análise de Variáveis Categóricas: A técnica de one-hot encoding foi aplicada para transformar as variáveis categóricas em um formato adequado para os modelos de machine learning.

Detecção de Desequilíbrio de Classes: Uma análise inicial da variável alvo (Churn) revelou um desequilíbrio significativo, com a maioria dos clientes não evadindo.

2. Análise de Correlação e Seleção de Variáveis
Matriz de Correlação: Foi gerada uma matriz de correlação para visualizar as relações entre as variáveis e a variável alvo (Churn).

Boxplots: Gráficos boxplot foram utilizados para explorar a relação entre variáveis-chave como tenure e Charges.Total com a evasão. A análise visual mostrou que clientes com menor tempo de contrato (tenure) e menor valor total gasto (Charges.Total) tendem a ter maior taxa de evasão.

3. Modelagem Preditiva
Foram desenvolvidos dois modelos de machine learning para prever a evasão:

Regressão Logística: Escolhida por sua eficiência e alta interpretabilidade. Os dados numéricos foram padronizados usando StandardScaler para garantir que todas as features tivessem a mesma escala, o que é uma prática recomendada para este tipo de modelo.

Resultados: O modelo alcançou uma acurácia de aproximadamente 81.1%. O recall para a classe Churn (evasão) foi de 54%, indicando que o modelo identificou cerca de metade dos clientes que de fato evadiriam.

Random Forest: Selecionado por sua robustez e capacidade de lidar com relações não lineares e o desequilíbrio de classes. A normalização dos dados não foi necessária para este modelo.

Resultados: A acurácia foi de 79.8%. O recall para a classe Churn foi de 49%, um pouco inferior ao da Regressão Logística.

4. Interpretação dos Modelos e Conclusões
A análise dos modelos permitiu a identificação das variáveis com maior impacto na evasão de clientes.

**Principais Fatores de Evasão:**

Tempo de Contrato (tenure) e Tipo de Contrato: Clientes com menor tempo de contrato e aqueles com contratos mensais são significativamente mais propensos a evadir.

Serviços Adicionais: A ausência de serviços como OnlineSecurity e TechSupport aumenta a probabilidade de evasão.

Serviço de Internet: Clientes com Fiber optic têm uma propensão maior a evadir.

Métodos de Pagamento: O uso de electronic check como forma de pagamento está associado a uma maior taxa de evasão.

**Estratégias de Retenção Propostas:**

Foco nos Clientes Iniciais: Implementar programas de boas-vindas e descontos nos primeiros meses para clientes com tenure baixo.

Incentivo a Contratos de Longa Duração: Criar campanhas para migrar clientes de contratos mensais para contratos de 1 ou 2 anos, oferecendo benefícios como preços mais baixos ou serviços adicionais gratuitos.

Melhoria na Qualidade de Serviço: Investigar a alta taxa de evasão entre clientes de internet de fibra óptica e de cheque eletrônico para identificar e resolver problemas de satisfação.

Promoção de Serviços de Valor Agregado: Oferecer pacotes promocionais de segurança e suporte técnico, destacando os benefícios para o cliente, para aumentar a fidelidade.
