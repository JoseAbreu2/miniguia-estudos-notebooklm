# 📊 Miniguia de Estudos: Análise de Dados com Python e NotebookLM

## 🎯 Contexto e Objetivos
O objetivo deste repositório é servir como base estruturada para o estudo aprofundado de **Análise de Dados com Python**. O foco é aplicar a estatística (descritiva, probabilidade e inferencial) à resolução de problemas complexos na área de negócios, como otimização de rotinas operacionais, gestão e auditoria de contratos, e dimensionamento de viabilidade em projetos. 

A proposta é utilizar a Inteligência Artificial (NotebookLM) não apenas como um buscador, mas como uma ferramenta de curadoria técnica e aprendizagem ativa, traduzindo teoria matemática em código e inteligência de negócios.

**Objetivos de Estudo:**
* Traduzir conceitos estatísticos puros em análises exploratórias viáveis com Python (Pandas/SciPy).
* Compreender e diferenciar métodos descritivos de processos inferenciais (Testes de Hipóteses e Intervalos de Confiança) para tomada de decisão com base em dados.
* Documentar a evolução da engenharia de prompts aplicada à extração de conhecimento técnico.

## 📚 Curadoria de Fontes
A base de conhecimento fornecida ao NotebookLM consistiu em materiais focados no rigor estatístico:
1. *Introdução*: População x Amostra, Descritiva vs. Inferencial.
2. *Probabilidade Básica*: Teoria dos Conjuntos e Axiomas.
3. *Probabilidade Avançada*: Teorema de Bayes e Probabilidade Condicional.
4. *Representação Gráfica*: Histogramas e Medidas de Centralidade.
5. *Medidas de Dispersão*: Variância, Amplitude e Boxplots.
6. *Análise Bivariada*: Covariância, Coeficiente de Pearson e Associação.
7. *Distribuições de Variáveis Discretas*: Binomial, Hipergeométrica e Poisson.
8. *Distribuições de Variáveis Contínuas*: Distribuição Normal.
9. *Inferência Estatística I*: Estimadores e Intervalos de Confiança.
10. *Inferência Estatística II*: Teste de Hipóteses, P-valor e Erros.

## 🛠️ Engenharia de Prompts e "Cicatrizes"
O processo de extração de valor da IA exige refinamento crítico. Abaixo, o *troubleshooting* documentado durante a interação com o NotebookLM:

* **Tentativa 1 (Prompt Ingênuo):** *"Faça um resumo dos PDFs sobre estatística descritiva e inferencial para a área de negócios."*
  * ❌ **O que deu errado:** O resultado foi demasiadamente teórico e raso. A IA apenas listou conceitos e algumas pacotes e bibliotecas em Python sem fazer uma conexão forte com a teoria além de não relacionar com situações práticas do mundo dos negócios. Faltou direcionamento analítico. Também é importante criticar que a falta de aprofundamento no conceitos pode levar o estudante a cometer erros nas análises de dados como por exemplo: 
(a) usar média quando existe outlier gerando uma medida de centralidade irreal; 
(b) não citou os tipos de variáveis, assunto que eu julgo importante pois no momento de escolher os métodos estatísticos para fazer inferência é crítico saber o tipo de variável.
* **Tentativa 2 (Focando no ferramental):** *"Explique a diferença entre estatística descritiva e inferencial. Dê exemplos de como eu calcularia isso em Python usando a base das aulas fornecidas."*
  * ⚠️ **O que deu errado:** Melhorou na parte técnica, mas sem exemplos práticos de casos de negócios. Faltou rigor na aplicação corporativa pesada, além de só apresentar exemplos de códigos em python para inferência estatística. Não apresentou nenhum código para gerar gráficos ou tabelas.
* **Tentativa 3 (Prompt focado e com detalhes - Sucesso):** *"Aja como um Cientista de Dados sênior. Com base nos documentos fornecidos, crie um guia prático diferenciando Estatística Descritiva e Inferencial aplicadas a um cenário de negócios técnico (ex: análise de eficiência de automações operacionais ou consumo/viabilidade de sistemas de energia). Extraia as definições matemáticas exatas dos textos para 'covariância' e 'p-valor', e sugira como o Python entra nesse fluxo."*
  * ✅ **Resultado:** Cenário adotado: Análise de consumo e viabilidade de sistemas de energia
  * ✅ **Resumo da Resposta: (Análise Descritiva)** Foi capaz de indicar problemas ao usar a média e sugeriu dar preferência para a mediana do consumo de energia (kWh); Sugeriu criar um histograma com a quantidade de classes extraindo a raiz quadrada do número total de observações; Finalizou com a importância de identificar anomalias com o Boxplot.
  * ✅ **Resumo da Resposta: (Análise Inferencial)** Previsão de Demanda (Intervalos de Confiança): sugere criar um Intervalo de Confiança (IC) para afirmar que, por exemplo, com 95% de confiança, a verdadeira média de consumo da população inteira está entre um limite inferior e superior, baseando-nos no erro-padrão da amostra.
  * ✅ **Resumo da Resposta: (Análise Inferencial)** Testes de Viabilidade (Testes de Hipóteses): Trouxe um cenário real de negócio (implantar medidores inteligentes para reduzir o consumo) e traçou testes de hipóteses a partir da instalação e observação de 100 medidores e a partir desses dados confrontar as hipóteses H0 e H1. Por fim, finaliza trazendo as definições matemáticas e o fluxo de trabalho no Python.

## 📘 Miniguia de Estudo

### 1. Resumos Estruturados Aplicados a Negócios
* **Estatística Descritiva:** Tem como objetivo organizar e resumir os dados. Em Python, usamos bibliotecas para gerar histogramas e boxplots (para identificar *outliers* que afetam a média). Essencial para gerar relatórios gerenciais e entender o comportamento de variáveis financeiras ou operacionais (ex: tempo médio de execução de um processo sistêmico).
* **Análise Bivariada e Probabilidade:** O objetivo de estabelecer a distribuição conjunta de duas variáveis é compreender a existência de alguma associação entre elas. A covariância mede o afastamento simultâneo das respectivas médias. Já a probabilidade condicional (como o Teorema de Bayes) ajusta a chance de um evento com base em uma informação prévia, sendo vital para modelos de risco de crédito ou análise de quebra de contratos.
* **Estatística Inferencial (Testes de Hipóteses):** Permite extrair conclusões sobre uma população a partir de informações de uma amostra. Ferramenta crítica para testes A/B no desenvolvimento de *features* corporativas. Compara-se a Hipótese Nula (H0) com a Alternativa (Ha). Se o p-valor for menor ou igual ao nível de significância, rejeitamos H0, validando estatisticamente o ganho de eficiência de um novo fluxo implantado.

### 2. Glossário Técnico
* **População:** É o conjunto de todos os objetos ou elementos de interesse envolvidos em uma investigação, que pode ser finito ou infinito.
* **Amostra:** É um subconjunto representativo selecionado a partir da população, utilizado porque restrições de tempo e recursos geralmente tornam inviável analisar o universo inteiro (censo).
* **Estatística Descritiva:** Ramo da estatística focado em organizar, resumir e visualizar um conjunto de dados numéricos ou categóricos por meio de gráficos e medidas-resumo.
* **Estatística Inferencial:** Ramo que utiliza o raciocínio indutivo para extrair conclusões e generalizar os resultados obtidos em uma amostra para toda a população, quantificando a incerteza desse processo.
* **Variável Aleatória:** É uma regra matemática que associa um valor numérico a cada resultado de um espaço amostral, podendo ser discreta (valores contáveis) ou contínua (valores em um intervalo da reta real).
* **Média Amostral:** É uma medida de centralidade obtida pela soma de todas as observações do conjunto dividida pelo número total de elementos (n).
* **Mediana:** É a medida que representa o valor central de um conjunto de dados quando as observações estão ordenadas da menor para a maior.
* **Desvio-Padrão:** É a principal medida de variabilidade individual dos dados, calculada como a raiz quadrada positiva da variância.
* **Variância:** Medida de dispersão baseada na média dos quadrados dos desvios em relação à média geral; em amostras, divide-se por (n-1) para corrigir subestimativas (correção de Bessel).
* **Erro-Padrão:** É a medida da variabilidade entre amostras, utilizada especificamente para avaliar a precisão do cálculo da estimativa da média populacional.
* **Coeficiente de Variação (CV):** Mede a variação relativa à média, geralmente expressa em porcentagem (%), sendo ideal para comparar a volatilidade de diferentes séries de dados que possuem unidades ou proporções distintas.
* **Intervalo de Confiança (IC):** É uma estimativa que fornece um intervalo completo de valores plausíveis para um parâmetro populacional desconhecido, acompanhado de um grau quantificável de confiança (ex: 95%).
* **Teste de Hipóteses:** É um procedimento formal de tomada de decisão que avalia evidências amostrais contra uma afirmação prévia (a hipótese nula), decidindo por rejeitá-la ou não.
* **P-valor (p-value):** É a probabilidade, calculada sob a suposição de que a hipótese nula (H0) é verdadeira, de se obter uma estatística de teste tão ou mais extrema do que a que foi observada na amostra. O p-valor não é a probabilidade de a hipótese estar certa ou errada.
* **Erro Tipo I:** Ocorre quando o pesquisador decide rejeitar a hipótese nula (H0) quando ela é, na verdade, verdadeira; a probabilidade desse erro é definida pelo nível de significância (α).
* **Erro Tipo II:** Ocorre quando o pesquisador decide não rejeitar a hipótese nula (H0) quando ela é, de fato, falsa.
* **Covariância:** É uma medida estatística bivariada que indica o afastamento simultâneo das respectivas médias de duas variáveis, mostrando se elas tendem a crescer ou diminuir juntas.
* **Coeficiente de Correlação de Pearson:** É um índice sem unidade, limitado entre -1 e 1, que mede a direção e a intensidade da relação linear entre duas variáveis. Valores próximos de 1 ou -1 indicam forte relação positiva ou negativa, enquanto valores próximos a zero indicam ausência de relação linear.
* **Teorema de Bayes:** É uma regra baseada em probabilidade condicional que permite transformar uma crença prévia (distribuição a priori) por meio de novas evidências (verossimilhança) em uma crença refinada (a posteriori).
* **Distribuição Normal:** É o modelo de probabilidade contínua mais importante da estatística, caracterizado por uma curva simétrica em forma de sino centrada na média. Muitas populações e variáveis aleatórias podem ser aproximadas por este modelo através do Teorema do Limite Central.


### 3. Prompts Reutilizáveis
Para sessões de revisão técnica no NotebookLM, utilize os seguintes prompts:
* 💡 *"Baseado no Teorema de Bayes, gere um problema de negócio prático sobre probabilidade de inadimplência em contratos, resolva o cálculo passo a passo e me mostre como estruturar essa lógica matematicamente."*
* 💡 *"Crie uma tabela comparando testes paramétricos e não paramétricos (como t de Student e Wilcoxon), indicando quando eu devo usar cada um em uma análise de viabilidade de projetos no Python."*
* 💡 *"Considerando a diferença entre variabilidade individual e variabilidade entre amostras, elabore 3 perguntas de múltipla escolha com alto nível de dificuldade para testar meus conhecimentos."*
