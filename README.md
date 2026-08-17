# IC - Estudo comparativo de câncer em diferentes regiões do Brasil via regra de associação

Este repositório contém os códigos e rotinas de análise de dados desenvolvidos para o projeto de Iniciação Científica (PIBIC/CNPq) intitulado Estudo comparativo de casos de câncer em diferentes regiões do Brasil via regras de associação, vinculado à Universidade Estadual de Campinas (UNICAMP).

O foco principal do estudo é a aplicação de técnicas de mineração de dados, especificamente o algoritmo Apriori, para identificar padrões e regras de associação na incidência de casos oncológicos, considerando variáveis demográficas e regionais (como dados de Porto Alegre e Belém, que foram obtidos dos RCBPs das respectivas cidades).

O projeto foi originalmente produzido inteiramente no google colab, por esse motivo as bases de dados utilizadas não estão aqui pois ultrapassam o limite que o Github permite, porém em próximas atualizações deste repositório será colocado um .gitignore para fazer o upload das bases que realmente foram o foco da análise.

**Estrutura do Repositório**

A análise está dividida em módulos sequenciais que refletem as etapas de desenvolvimento do projeto:

**ic_parte1.py (Pré-processamento e AED):** Responsável pela leitura das bases de dados, limpeza estrutural e mapeamento dos Códigos da Topografia (ex: conversão de códigos C73 para descrições legíveis). Além disso, também realiza a segmentação dos dados por gênero, isolando os conjuntos para análises mais precisas e removendo inconsistências na base.A base de dados original está disponível para download no link: **https://www.inca.gov.br/BasePopIncidencias/Home.action **

**ic_parte2_algoritmo_de_associacao.py (Mineração de Dados e Regras de Associação):** Focado na extração de regras no subconjunto de dados. O código segmenta a base por Raça/Cor (Branca, Parda e Preta) e aplica o algoritmo Apriori para encontrar padrões frequentes. O modelo foca em métricas rigorosas, filtrando apenas regras que apresentem um valor de Lift superior a 1.0, garantindo a relevância estatística das associações encontradas.

**Tecnologias e Bibliotecas Utilizadas**

Python  
Pandas e NumPy (Manipulação e limpeza de dados)  
Efficient-Apriori (Geração das regras de associação)  
Matplotlib e Seaborn (Visualização gráfica e análise exploratória)

**Como executar o projeto:**

1. Clone este repositório para o seu ambiente local.  
2. Certifique-se de instalar as dependências necessárias executando: pip install pandas numpy efficient-apriori matplotlib seaborn.  
3. Ajuste os caminhos de leitura dos ficheiros CSV nos blocos de código para refletir os diretórios corretos do seu ambiente.
4. Execute os ficheiros de forma sequencial: inicie pela parte 1 para o pré-processamento, seguido da parte 2 para a extração das métricas e regras de associação.
