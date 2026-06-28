# Análise de  "Driver asked to cancel" da Uber

# Problema de Negócio

**Cancelamentos Causados por Falhas Operacionais**

Uma parcela relevante dos cancelamentos ocorre porque o motorista solicita que o cliente cancele a corrida ou porque permanece parado sem seguir para o local de embarque após aceitar a viagem. Em ambos os casos, o cliente percebe que a corrida provavelmente não será realizada e opta pelo cancelamento.

**Impacto:** Aumento da taxa de cancelamento, perda de receita, piora da experiência do usuário e redução da confiança na plataforma, o que pode levar clientes a utilizar serviços concorrentes.
# Premissas da análise

Só analisei o Fenômeno:
Driver asked to cancel (Motorista pediu para cancelar)
Driver is not moving towards pickup location (O motorista está parado)

Foram analisados 150.002 mil corridas da uber
os dados da uber são referentes ao ano de (2024)

# Estratégia da solução

O método Fato-Dimensão foi usado para desenvolver a análise de dados.

# Passo 1: Resumir o contexto em uma pergunta aberta

As perguntas abertas são um tipo de demanda muito comum em análise de dados nas quais a demanda possui N possíveis soluções e cabe ao analista de dados avaliar as possibilidades e escolher a alternativa com o maior retorno e o menor esforço possível. Para essa análise, foi definida a seguinte pergunta aberta:

**como a Uber pode resolver o problema de "Driver asked to cancel" (Motorista pediu para cancelar)**

# Passo 2: Transformar pergunta aberta em fechada

As perguntas fechadas são um tipo de demanda muito comum na área de análise de dados. Essa demanda contém todos os detalhes da análise de dados e direciona o analista exatamente para o que precisa ser feito. Geralmente, a pergunta fechada é a escolha de uma solução entre todas as alternativas possíveis, feita por um profissional mais sênior da área.

Para essa análise, foi definida a seguinte pergunta fechada:

**Pergunta Fechada: **Calcule a taxa de cancelamento dos motoristas em comparação com a dos clientes nos últimos 30 dias, considerando todo o país.**

**Como se trata de uma comparação entre motoristas e clientes, considero aceitável que as taxas percentuais sejam semelhantes. Caso exista uma discrepância significativa entre as taxas de cancelamento, medidas mais diretas devem ser adotadas.**

# Passo 3: Definição da Coluna Fato

O Fato é a coluna de interesse que representa o ponto focal da análise. Nesse caso, a coluna "Attrition" mostra se o funcionário está na empresa ou se já saiu.

# Passo 4: Identificação das Dimensões

As colunas foram agrupadas em dimensões comuns que fornecem mais detalhes sobre o Fato que será analisado. Foram organizadas as seguintes dimensões:

Perfil Pessoal e Demográfico: Age, Gender, MaritalStatus, Education, EducationField, DistanceFromHome, Over18.

Remuneração e Cargo: Department, JobRole, JobLevel, MonthlyIncome, Média_Cargo, Comparativo_Salarial, HourlyRate, DailyRate, MonthlyRate, StockOptionLevel, PercentSalaryHike.

Carreira, Tempo de Casa e Mobilidade: YearsAtCompany, YearsAtCompany_Blocks, YearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager, TotalWorkingYears, NumCompaniesWorked, BusinessTravel.

Satisfação, Engajamento e Desempenho: JobSatisfaction, EnvironmentSatisfaction, RelationshipSatisfaction, WorkLifeBalance, JobInvolvement, PerformanceRating, OverTime, TrainingTimesLastYear.

Controle e Identificação do Registro: EmployeeNumber, EmployeeCount, StandardHours, Attrition (variável alvo).

# Passo 5: Hipóteses Analíticas

H1: Profissionais casados têm uma rotatividade menor.

H2: Profissionais que trabalham em muitas empresas têm alta rotatividade.

H3: Profissionais com baixa qualidade de vida têm rotatividade maior.

H4: Profissionais que fazem hora extra têm alta rotatividade.

H5: Profissionais que recebem menos que os colegas estando no mesmo cargo têm alta rotatividade.

H6: Profissionais com menos de 3 anos de trabalho na IBM têm rotatividade maior.

H7: Profissionais Jrs e Estagiários têm uma rotatividade maior.

# Passo 6: Critérios de Priorização

- **Critério 1:** Dados disponíveis.
- **Critério 2:** Insights acionáveis.

# Passo 7: Priorização das Hipóteses Analíticas

H1: Profissionais casados têm uma rotatividade menor.

H2: Profissionais que trabalham em muitas empresas têm alta rotatividade.

H3: Profissionais com baixa qualidade de vida têm rotatividade maior.

H4: Profissionais que fazem hora extra têm alta rotatividade.

H5: Profissionais que recebem menos que os colegas estando no mesmo cargo têm alta rotatividade.

H6: Profissionais com menos de 3 anos de trabalho na IBM têm rotatividade maior.

H7: Profissionais Jrs e Estagiários têm uma rotatividade maior.

# Insights da análise

# Resultados

**📥 Baixe a apresentação em PowerPoint (clique no link e, em seguida, em "Download" ou "View raw"):**  
  [https://docs.google.com/presentation/d/1ZAYDpxq3G5c3JzxRrJV63NLcst2hbMUj/edit?slide=id.p1#slide=id.p1](https://docs.google.com/presentation/d/1ZAYDpxq3G5c3JzxRrJV63NLcst2hbMUj/edit?slide=id.p1#slide=id.p1)

# Próximos passos

Fazer uma análise preditiva para saber o Turnover da IBM para o próximo ano.

(não é possível fazer essa análise porque esse dataset não tem dimensão de data)
