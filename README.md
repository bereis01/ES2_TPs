# **Trabalho Prático:** Mineração de Repositórios de Software

**Universidade Federal de Minas Gerais | Departamento de Ciência da Computação | 2025/02**

**Aluno:** Bernardo Reis de Almeida

**Professor:** André Cavalcante Hora

**Disciplina:** DCC072 - Engenharia de Software II

## Ideia do Sistema

Este trabalho prático tem por objetivo o desenvolvimento de uma ferramenta de linha de comando (CLI) para a mineração de repositórios Git/GitHub. A ideia é que uma URL que aponte para um repositório seja fornecida no terminal e a ferramenta produza alguma forma de análise acerca de panoramas de manutenção e evolução de software, tais como métricas de qualidade de código.

Em particular, propõe-se uma ferramenta que avalia a evolução do repositório quanto a diferentes quesitos de qualidade ao longo do tempo (em uma granularidade de, por exemplo, anos). De maneira preliminar, estabelece-se três quesitos: complexidade, acoplamento e responsabilidade. Em cada um, heurísticas serão levantadas para a formulação de uma *score* de qualidade. Em termos de complexidade, pode-se utilizar a média da quantidade de linhas por função. Em termos de acoplamento, uma métrica interessante talvez seja a quantidade média de referências a outras classes por classe. Por fim, em termos de responsabilidade, a distribuição de contribuições ao código entre os colaboradores do repositório e quantos concentram a maior parte delas. Tais heurísticas, como mencionado, serão agregadas em uma *score* atribuída a cada quesito, indicando se o respectivo sistema tem evoluído ou tem decaído em termos de sua qualidade em cada um deles.

Para isso, informações extraídas do repositório GitHub do sistema serão utilizadas. Isto é, a ferramenta receberá como entrada uma URL do GitHub. Elementos a serem analisados potencialmente incluem o histórico de commits, as diferentes versões do código ao longo do tempo, dentre outros, os quais deverão ser devidamente parseados e agregados.

## Tecnologias

De maneira preliminar, a ferramenta deve ser elaborada inteiramente com a linguagem de programação Python. A biblioteca **argparse** oferece recursos interessantes para a elaboração de uma interface em linha de comando, como processamento automático de *flags*. A biblioteca **requests**, juntamente com a API fornecida pelo próprio GitHub, podem ser utilizadas para a extração das informações. Código deverá ser escrito para o parsing e para a análise das informações extraídas, enquanto os resultados finais provavelmente serão exportados em algum formato gráfico de arquivo, incluindo tanto texto, quanto visualizações.
