
# Projeto de Visualização de Dados

Nome: Marcos Vinicius Bhering Schork de Sousa
Turma QA VDBI
Curso: Visualização de Dados e Business Intelligence.

# Objetivo do projeto:
    Analisar a base enviada do RH para obter informações relevantes sobre a empresa, como quantidade de funcionários por cidade, 
    departamento e região, além de identificar possíveis inconsistências nos dados.
    Eles gostariam de entender melhor a distribuição dos salários em relação dos cargos, departamentos e padrões de remuneração por região.

# Coleta dos Dados
    Os dados foram coletados no banco de dados freesql.
    Foram feitas duas queries para responder às perguntas de negócio.

    • query1: EMPLOYEES com LEFT JOIN em DEPARTMENTS e JOBS.
    • query2: EMPLOYEES com LEFT JOIN em DEPARTMENTS, LOCATIONS, COUNTRIES e REGIONS.
    
# Tratamento da Base de Dados:
    Para responder ás perguntas de negócio, foram realizadas duas consultas SQL DISTINTAS, cada uma trazendo informações complementares:
        • Query1: Retorna dados de departamentos, cargos(JOB_ID) e estatísticas de salário (média, máximo e mínimo).
        • Foi utilizaada para entender a distribuição Salárial por cargo e departamento .

        • Query2: Retorna dados de cidades, regiões e estatísticas de salário.
        • Foi utilizada para analisar a distribuição salarial por localização geográfica.

    # Etapas de tratamento:
        • Exportação: Cada query foi exportada para um arquivo csv e .sql
        • Carregamento: Os arquivos foram carregados em python utilizando a biblioteca Pandas.
        • Integração:  As tabelas foram unidas em um LEFT JOIN utilizando as chaves em comum, assim permitindo os relacionamentos entre elas.
        • Filtragem: Foram aplicados filtros para indentificar as cidades dos funcionários por continente, tanto para Americas quanto para Europa.


# Tabelas utilizadas:
    • COUNTRIES
    • DEPARTMENTS
    • EMPLOYEES
    • JOBS
    • LOCATIONS
    • REGIONS


# Observações da Análise:

    * Salários por Departamento:
        • A maior média de salário é do departamento Executivo com $:20.500,00
        • A menos média de salário é do departamento Administrativo com $:4.400,00

    * Quantidade de funcionário por continente:
        • Américas: 17 funcionários.
        • Europa: 12 funcionários.

    * Gráfico de Média Salárial por Continente
        • Américas $:6895.22
        • Europa €:8485.29

    * Distribuição de funcionários na Américas:
        • Maior concentração em São Francisco (EUA): 45 funcionários.
        • Menor concentração em Toronto (Canadá): 2 funcionários.
        • Outros: Seattle (18), Southlake (5).

    * Grafico Quantidade de funcionários por cidade da Europa:
        • Nota-se uma grande discrepância na Europa pois 94% dos funcionarios moram em Oxford na Inglatera com 34 funcionários.
        • os outros 2 moram: 1 londres Inglatera e 1 Monich (monique) na alemanha.

    * Gráfico para media salarial por cidades na América:
     • Maiores médias Salariais Torronto (Canadá) $9.500,00 e Seattle (EUA) $8.845,33 .
     • Menosres médias Salariais Southlake (eua) $5.760,00 e San Francisco (EUA) $3.475,56 . 
    
    * Gráfico para media salarial por cidades na Europa:
        • Monique (Alemanha) €10.000,00, apenas 1 funcionário.
        • Oxford (Inglaterra) €8.955,88.
        • Londres (Inglaterra) €6.500,00, apenas 1 funcionário.

# Insights da Análise
    • A concentração de funcionários em Oxford (94% da Europa) sugere forte centralização, o que pode gerar riscos de dependência de uma única localidade.
    • O departamento Executivo apresenta a maior média salarial, reforçando o peso estratégico da liderança na empresa.
    • A discrepância entre cidades americanas mostra que São Francisco é um polo dominante, enquanto outras localidades têm baixa representatividade.
    • A média salarial na Europa é superior à das Américas, indicando possível diferença de custo de mão de obra entre continentes.