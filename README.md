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

O Fato é a coluna de interesse que representa o ponto focal da análise. Nesse caso, a coluna "Booking Status" mostra se a corrida foi concluida ou nao.

# Passo 4: Identificação das Dimensões

As colunas foram agrupadas em dimensões comuns que fornecem mais detalhes sobre o Fato que será analisado. Foram organizadas as seguintes dimensões:

Tempo e Data (Contexto Temporal): Date, Time. (Fornece a base cronológica para análise de sazonalidade, picos de demanda e horários de pico).

Localização e Veículo (Logística e Percurso): Vehicle Type, Pickup Location, Drop Location. (Detalha a estrutura operacional da viagem, incluindo o modal utilizado e os pontos de origem e destino).

Valores e Distância (Métricas Quantitativas da Corrida): Avg VTAT, Avg CTAT, Booking Value, Ride Distance. (Reúne as principais medidas numéricas que servirão como base para os cálculos de performance, faturamento e eficiência de tempo).

Avaliações e Pagamento (Experiência e Quitação): Driver Ratings, Customer Rating, Payment Method. (Agrupa as percepções de qualidade tanto do motorista quanto do cliente, além da forma de pagamento utilizada).

Cancelamentos e Incompletude (Motivos de Falha): Reason for cancelling by Customer, Driver Cancellation Reason, Incomplete Rides Reason. (Centraliza os fatores qualitativos e categóricos que explicam as interrupções e insucessos na operação).

Controle e Identificação do Registro: Booking ID, Customer ID, Booking Status, Cancelled Rides by Customer, Cancelled Rides by Driver, Incomplete Rides. (Aqui estão os identificadores únicos para rastreabilidade, as contagens de eventos críticos e o Booking Status, que funciona como a variável de desfecho (alvo) para classificação do resultado final da reserva).


# Passo 5: Hipóteses Analíticas

H1:Cliente tem uma taxa de cancelamento de corrida de 4%

H2:motoristas tem uma taxa de cancelamento na corrida de 20%

H3: os motorista que tem a maior taxa de cancelamento trabalham de carro

H4: os passageiros de moto tem maior taxa de cancelamento em comparação com os que pedem carro

H5: Os clientes que mais cancelam e porque mudaram de ideia

H6: Os clientes que menos cancelam e porque o motorista forcou o cancelamento

H7: As corridas que tem mais cancelamentos sao as mais baratas

H8: Os motoristas cancelam porque a corrida e longa e o retorno e baixo para ele

H9: Motoristas com baixa avaliação cancelam mais

# Passo 6: Critérios de Priorização

- **Critério 1:** Dados disponíveis.
- **Critério 2:** Insights acionáveis.

# Passo 7: Priorização das Hipóteses Analíticas

H1:Cliente tem uma taxa de cancelamento de corrida de 4%

H2:motoristas tem uma taxa de cancelamento na corrida de 20%

H3: os motorista que tem a maior taxa de cancelamento trabalham de carro

H4: os passageiros de moto tem maior taxa de cancelamento em comparação com os que pedem carro

H5: Os clientes que mais cancelam e porque mudaram de ideia

H6: Os clientes que menos cancelam e porque o motorista forcou o cancelamento

H7: As corridas que tem mais cancelamentos sao as mais baratas

H8: Os motoristas cancelam porque a corrida e longa e o retorno e baixo para ele

H9: Motoristas com baixa avaliação cancelam mais

# Insights da análise

# Resultados

**📥 Baixe a apresentação em PowerPoint (clique no link e, em seguida, em "Download" ou "View raw"):**  
  [https://docs.google.com/presentation/d/1ZAYDpxq3G5c3JzxRrJV63NLcst2hbMUj/edit?slide=id.p1#slide=id.p1](https://docs.google.com/presentation/d/1ZAYDpxq3G5c3JzxRrJV63NLcst2hbMUj/edit?slide=id.p1#slide=id.p1)

# Próximos passos

Fazer uma análise preditiva para saber o Turnover da IBM para o próximo ano.

(não é possível fazer essa análise porque esse dataset não tem dimensão de data)
