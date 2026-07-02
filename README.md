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
* **População:** Conjunto de todos os elementos de interesse (finito ou infinito).
* **Desvio-padrão:** Medida de variabilidade individual.
* **Erro-padrão:** Medida de variabilidade entre amostras (precisão da estimativa).
* **Erro Tipo I:** Rejeitar a hipótese nula (H0) quando ela é verdadeira. (Ex: Afirmar que uma nova rotina gerou lucro, quando na verdade não gerou).
* **Erro Tipo II:** Não rejeitar H0 quando ela é falsa. (Ex: Não detectar uma falha que realmente está ocorrendo).
* **P-value:** É a probabilidade, calculada sob H0, de se obter uma estatística de teste tão extrema ou mais extrema do que a observada na amostra. 

### 3. Prompts Reutilizáveis
Para sessões de revisão técnica no NotebookLM, utilize os seguintes prompts:
* 💡 *"Baseado no Teorema de Bayes, gere um problema de negócio prático sobre probabilidade de inadimplência em contratos, resolva o cálculo passo a passo e me mostre como estruturar essa lógica matematicamente."*
* 💡 *"Crie uma tabela comparando testes paramétricos e não paramétricos (como t de Student e Wilcoxon), indicando quando eu devo usar cada um em uma análise de viabilidade de projetos no Python."*
* 💡 *"Considerando a diferença entre variabilidade individual e variabilidade entre amostras, elabore 3 perguntas de múltipla escolha com alto nível de dificuldade para testar meus conhecimentos."*
