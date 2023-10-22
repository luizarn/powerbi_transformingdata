# Processando e Transformando Dados com Power BI

Este projeto envolveu a criação de uma instância no Azure para MySQL e um banco de dados a partir de scripts presentes no arquivo 'script_para_database_azure.txt'. A integração do Power BI com o MySQL no Azure também foi realizada. Após esses primeiros passos, iniciou-se a verificação na base de dados para realizar a transformação dos dados.

**Transformações Realizadas**
- Tabela "employee"
Na coluna "salary," o tipo de dado foi alterado para "Número Decimal Fixo" ao invés de "Número Decimal, para melhor representação de valores financeiros.
- Tabela "works_on"
Na coluna "hours," o tipo de dado foi alterado para "Inteiro," uma vez que horas não fazem sentido serem decimais.
- Tabela "project"
Um projeto que tinha 0 horas foi alterado para 10 horas, considerando uma situação real em que possivelmente houve um erro de digitação.
- Algumas colunas foram renomeada para maior clareza.
- Um dos colaboradores na tabela "employee" não tinha um supervisor (Super_ssn), e isso foi mantido, supondo que ele é o gerente do departamento, e ele foi adicionado como gerente do seu departamento, o quanto não possuia valor.
- Os endereços dos colaboradores foram divididos em colunas de "street," "number," "city," e "state" separando com base na localização do caractere "-."
- Mesclagem de Consultas:
Consultas da tabela "employee" e "departament" foram mescladas para criar uma tabela "employee" com os nomes dos departamentos associados a cada colaborador.
- Análise de Dados
Colunas desnecessárias foram eliminadas nas tabelas resultantes das mesclagens.

Tabelas e artifícios visuais foram criados no relatório para demonstrar a proporção de colaboradores para cada gerente, a média salarial de cada departamento, a quantidade de colaboradores em cada departamento, os gerentes de cada departamento, a proporção de horas trabalhadas por cada colaborador e seu departamento, e onde cada colaborador mora.

**Motivação**

Essas transformações e análises visaram avaliar a distribuição de colaboradores entre projetos e departamentos, verificar a carga de trabalho de cada colaborador, identificar quem está contribuindo mais em termos de horas de trabalho, e analisar a possibilidade de colaboradores sobrecarregados. Essas análises são úteis para otimizar processos na equipe, distribuir equitativamente o trabalho entre os colaboradores, diminuir a pressão e melhorar os resultados.

O Power BI foi utilizado para criar visualizações e relatórios que facilitam a análise dos dados e a tomada de decisões informadas.
