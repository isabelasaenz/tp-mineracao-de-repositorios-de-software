# Engenharia de Software II - Ferramenta CodeThermometer – Mineração de Repositórios de Software

## Membros do Grupo

- Deborah Vieira Vilas Boas de Almeida 
- Isabela Saenz Cardoso
- Lucas Almeida Santos de Souza
- Rodrigo Sales Nascimento

---

## Explicação do Sistema

O **CodeThermometer** será uma ferramenta de linha de comando para identificar hotspots de manutenção em projetos de software.  

A ideia central é analisar o **histórico de commits de um repositório Git** para localizar arquivos que passam por muitas modificações ao longo do tempo, o que pode indicar potenciais problemas de manutenção, dívida técnica ou risco de falhas.  

### Funcionalidades esperadas
- Extrair número de commits por arquivo em um período definido.  
- Calcular o Code Churn (linhas adicionadas/removidas).  
- Medir a complexidade ciclomática do código.  
- Identificar autores mais frequentes em cada hotspot (avaliar concentração de conhecimento / bus factor).  
- Gerar relatórios e gráficos para auxiliar na tomada de decisão.

---

## Tecnologias Utilizadas

### Origem dos Dados
- **Git**: análise do histórico de commits.
  - [PyDriller](https://github.com/ishepard/pydriller): framework para mineração de repositórios Git.  
  - Alternativa: [GitPython](https://github.com/gitpython-developers/GitPython).

### Artefatos Analisados
- Commits (frequência, autores, churn de linhas).  
- Arquivos de código-fonte (complexidade).  
- Metadados de autoria (bus factor).

### Métricas de Código
- [lizard](https://github.com/terryyin/lizard): cálculo da complexidade ciclomática.  

### CLI
- [typer](https://github.com/tiangolo/typer): criação de interface de linha de comando intuitiva.  
- Alternativas: `argparse` (biblioteca padrão do Python).

### Visualizações e Relatórios
- [pandas](https://pandas.pydata.org/): manipulação de dados e exportação para CSV/Excel.  
- [matplotlib](https://matplotlib.org/) e [seaborn](https://seaborn.pydata.org/): geração de gráficos