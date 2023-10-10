# ProjetoIntegrado
Diretório destinado ao projeto integrado do MBA Inteligência Artificial e Aprendizado de Máquinas -  PUC Minas


## Uso de Séries Temporais para Análise Beneficiários Ativos da Saúde Suplementar


### Introdução

A inteligência artificial (IA) tem se estabelecido como uma área de pesquisa e desenvolvimento com aplicações cada vez mais relevantes e abrangentes em diversos setores da sociedade. Com o avanço da tecnologia e o crescente poder computacional, a IA tem se mostrado capaz de lidar com problemas complexos e oferecer soluções inovadoras em áreas como reconhecimento de padrões, processamento de linguagem natural e tomada de decisões autônomas.
Um campo fundamental dentro da inteligência artificial é o estudo de séries temporais, que são dados organizados em função do tempo. As séries temporais referem-se a observações realizadas em diferentes momentos ao longo do tempo, onde cada observação é registrada em sequência cronológica. Esses dados podem ser encontrados em diversas áreas, como finanças, meteorologia, medicina, energia, entre outras.<br>
A importância das séries temporais reside no fato de que elas refletem a natureza dinâmica e evolutiva dos fenômenos do mundo real. Compreender e analisar padrões, tendências e comportamentos subjacentes às séries temporais pode fornecer informações valiosas para a tomada de decisões estratégicas e previsões futuras. No entanto, a análise de séries temporais apresenta desafios específicos, como a presença de ruídos, sazonalidades, tendências não lineares e dependências temporais complexas.<br>
Diante desses desafios, a inteligência artificial surge como uma ferramenta poderosa para lidar com a complexidade das séries temporais. Os algoritmos de IA podem identificar padrões ocultos, capturar relações não lineares e aprender com a evolução temporal dos dados. A combinação de técnicas como aprendizado de máquina, redes neurais e processamento de linguagem natural tem impulsionado avanços significativos na análise de séries temporais.<br>
Assim, o objetivo deste trabalho é explorar o potencial da inteligência artificial na análise de séries temporais, investigando seus métodos, técnicas e aplicações em diferentes domínios. Serão abordados algoritmos de aprendizado de máquina, redes neurais recorrentes, modelos de séries temporais e outras abordagens relevantes para a compreensão e previsão de dados temporais. <br>


### Descrição do Problema e da Solução Proposta

Em um mercado altamente competitivo como o da saúde suplementar, a capacidade de se preparar adequadamente para as mudanças e tendências do mercado pode se tornar um diferencial crucial para as operadoras de planos de saúde. Nesse contexto, a aplicação efetiva da inteligência artificial (IA) emerge como um fator determinante para o setor de saúde, ganhando cada vez mais destaque e gerando impactos positivos em diversos departamentos e processos.<br>
Com o objetivo de explorar e aproveitar o potencial da IA, este estudo visa analisar a série temporal dos dados relacionados à evolução mensal do SIB (Sistema de Informações de Beneficiários), um sistema informatizado que contém informações cadastrais dos beneficiários de planos privados de saúde no Brasil. O escopo dessa análise abrange tanto uma perspectiva preditiva quanto uma abordagem descritiva, permitindo a identificação de tendências, sazonalidades e outras características relevantes.<br>
Ao realizar uma análise preditiva, pretendemos utilizar técnicas avançadas de IA para fazer previsões com base nas séries temporais disponíveis no SIB. Essas previsões podem auxiliar as operadoras de planos de saúde na tomada de decisões estratégicas, como alocação de recursos, planejamento de demanda e elaboração de estratégias de marketing mais eficientes.<br>
Além disso, por meio de uma análise descritiva, pretendemos explorar as características intrínsecas das séries temporais, identificando tendências de longo prazo, padrões sazonais, flutuações periódicas e outros aspectos relevantes. Essa análise nos permitirá compreender melhor os dados e fornecer insights valiosos para a gestão da saúde suplementar, ajudando a identificar possíveis áreas de melhoria, antecipar demandas e otimizar processos operacionais.
Para alcançar tais objetivos, este estudo utilizará três algoritmos distintos de aprendizado de máquina: SARIMAX, XGBoost e Redes Neurais Tradicionais (MLP).
O algoritmo SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous regressors) é uma extensão do modelo ARIMA (AutoRegressive Integrated Moving Average) que incorpora componentes sazonais. Ele é amplamente utilizado na análise de séries temporais, permitindo capturar padrões sazonais e tendências ao considerar tanto a ordem das diferenças (determinada pela integração) quanto a autocorrelação e médias móveis.<br>
O XGBoost (Extreme Gradient Boosting) é um algoritmo de aprendizado de máquina baseado em árvores de decisão, conhecido por sua eficiência e precisão. Ele utiliza o método de boosting para criar um modelo preditivo poderoso, que combina várias árvores de decisão fracas para formar um modelo mais robusto e geralmente mais preciso. O XGBoost é amplamente aplicado em problemas de regressão e classificação, e sua capacidade de lidar com grandes conjuntos de dados e variáveis complexas o torna uma escolha popular para análise de séries temporais.<br>
As Redes Neurais Tradicionais, também conhecidas como Multilayer Perceptrons (MLP), são um tipo de modelo de aprendizado de máquina inspirado no funcionamento do cérebro humano. Elas consistem em várias camadas de neurônios artificiais, cada um dos quais recebe entradas, processa-as e transmite os resultados para a próxima camada. As MLPs são capazes de aprender relações complexas entre as variáveis de entrada e saída, tornando-as adequadas para a análise de séries temporais, onde podem identificar padrões e tendências não lineares.<br>
Ao usar esses três algoritmos distintos, SARIMAX, XGBoost e Redes Neurais Tradicionais (MLP), este estudo se beneficiará de abordagens variadas e complementares. O SARIMAX explorará a estrutura temporal e sazonal dos dados, o XGBoost aproveitará as vantagens do boosting e das árvores de decisão, enquanto as Redes Neurais Tradicionais (MLP) utilizarão sua capacidade de aprender representações complexas. Essa combinação de algoritmos permitirá uma análise abrangente e robusta das séries temporais relacionadas ao SIB, fornecendo insights valiosos para a gestão da saúde suplementar.


### Coleta de Dados


Os dados utilizados neste estudo serão coletados do portal Dados Abertos do Governo Federal, especificamente do conjunto de dados intitulado "Informações Consolidadas de Beneficiários". Os dados podem ser acessados por meio do seguinte link: https://dados.gov.br/dados/conjuntos-dados/informacoes-consolidadas-de-beneficiarios.<br>
Esses dados estão organizados por Ano/Mês e estão divididos em 28 arquivos distintos. Cada arquivo representa um estado brasileiro, além de um arquivo adicional chamado "XX", que contém os registros de cadastro nos quais o estado de residência do beneficiário não foi identificado.<br><br>

\begin{flushleft} Figura 1 - Volumetria da base de dados \end{flushleft} 
<img src="image/Volumetria_BeneficiariosConsolidadosANS.png">

A Extração dos dados ocorreu no dia 15/05/2023.<br><br>

**Nome do dataset:** Informações consolidadas de Beneficiários <br>
**Descrição:** Informações consolidadas de beneficiários por competência, extraídas dos arquivos SIB.<br>
Link: https://dados.gov.br/dados/conjuntos-dados/informacoes-cosolidadas-de-benficiarios <br>

| **Nome do Atributo** | **Descrição** | **Tipo** |
| --- | --- | --- |
| ID_TEMPO_COMPETENCIA | Competência dos dados no formato AAAAMM | CHAR |
| CD_OPERADORA | Código de registro da operadora de plano de saúde na ANS | CHAR |
| RAZAO_SOCIAL | Razão Social da Operadora | VARCHAR |
| CNPJ | CNPJ da Operadora | NUMBER |
| MODALIDADE_OPERADORA | Classificação das operadoras de planos privados de assistência à saúde de acordo com seu estatuto jurídico | VARCHAR
| SG_UF | Sigla da unidade da federação de residência do beneficiário | CHAR |
| CD_MUNICIPIO | Código IBGE do munícipio de residência do beneficiário, sem o dígito verificador | NUMBER |
| NM_MUNICIPIO | Nome do munícipio de residência do beneficiário | VARCHAR |
| SEXO | Identificação do sexo do beneficiário | CHAR |
| FAIXA_ETARIA | Faixa etária do beneficiário | VARCHAR|
| FAIXA_ETARIA_REAJUSTE | Faixa etária do beneficiário utilizada para o reajuste do plano | VARCHAR |
| CD_PLANO | Código do plano registrado ou cadastrado na ANS no qual o beneficiário possui vínculo | CHAR|
| VIGENCIA_PLANO | Início da vigência do plano para comercialização | CHAR |
| CONTRATACAO_PLANO | Tipo de contratação do plano do beneficiário | VARCHAR |
| SEGMENTACAO_PLANO | Tipo de segmentação assistencial do plano do beneficiário | VARCHAR |
| ABRANGENCIA_PLANO | Tipo de abrangência do plano do beneficiário | VARCHAR |
| COBERTURA_ASSISTENCIAL _PLANO | Tipo de cobertura de plano do beneficiário | VARCHAR |
| TIPO_VINCULO | Tipo de vínculo do beneficiário | VARCHAR |
| QTD_BENEF_ATIVOS | Quantidade de beneficiários ativos na competência | NUMBER |
| QTD_BENEF_ADERIDOS | Quantidade de beneficiários aderidos na competência | NUMBER |
| QTD_BENEF_CANCELADOS | Quantidade de beneficiários aderidos na competência | NUMBER |

