# Sistema de Análise Automatizada de Dados

## Visão Geral
Este projeto tem como finalidade a criação de um sistema que realiza a análise automática de dados, gerando relatórios HTML personalizados com estilo Bootstrap. A ferramenta foi desenvolvida para facilitar a análise exploratória de datasets, mostrando informações estatísticas e gráficos de maneira visual e acessível. O desenvolvimento utiliza Python com o auxílio de bibliotecas amplamente conhecidas, como `pandas`, `matplotlib`, `seaborn` e `jinja2`.

## Equipe de Desenvolvimento
- **Nikolas Rodrigues Moura dos Santos** - RM: 551566
- **Rodrigo Brasileiro** - RM: 98952
- **Thiago Jardim de Oliveira** - RM: 551624

## Principais Funcionalidades
- Geração automática de relatórios em formato HTML a partir de um dataset.
- Estatísticas incluídas no relatório:
  - Quantidade de linhas e colunas.
  - Contagem de variáveis e observações.
  - Células com dados ausentes e linhas duplicadas.
  - Classificação das variáveis em numéricas e categóricas.
- Visualização gráfica:
  - Histogramas para variáveis numéricas.
  - Gráficos de barras para variáveis categóricas.
- Layout do relatório otimizado com Bootstrap, garantindo uma interface responsiva.

## Estrutura do Sistema
1. **Template HTML**: Utiliza um layout com Bootstrap para organizar as estatísticas e gráficos de maneira visualmente agradável.
2. **Funções principais**:
   - `summarize_df(df)`: Calcula e retorna as principais estatísticas do dataset.
   - `plot_64(fig)`: Converte gráficos em strings Base64 para inclusão direta no HTML.
   - `create_plot(df)`: Cria gráficos para variáveis categóricas e numéricas.
   - `to_html(df)`: Usa o template HTML para renderizar os gráficos e estatísticas no relatório.

## Como Utilizar

### Requisitos
- Python 3.x
- Recomenda-se usar Google Colab para uma experiência mais rápida e visual.
- adicionar o dataset (arquivo .csv do repositório) a /content no colab
- Instale as seguintes bibliotecas: `pandas`, `matplotlib`, `seaborn`, `jinja2`, `base64`, `io`, `os`

### Etapas de Execução
1. Carregue o dataset no Google Colab.
2. Verifique se as bibliotecas necessárias estão instaladas com o comando:
   ```python
   !pip install pandas matplotlib seaborn jinja2
   ```
3. Execute o código e carregue o dataset desejado, como por exemplo:
   ```python
   df = pd.read_csv('/content/pokemonDB_dataset.csv')
   ```
4. O relatório HTML será gerado automaticamente e exibido no Colab por meio de um `IFrame`.

## Estrutura do Relatório
O relatório HTML gerado possui as seguintes seções:
- **Sumário**: Traz informações como o número total de registros, variáveis, células ausentes e duplicadas.
- **Tipos de Dados**: Apresenta a lista de colunas e seus respectivos tipos de dados.
- **Classificação das Variáveis**: Exibe a quantidade de variáveis numéricas e categóricas.
- **Células Ausentes**: Informa a quantidade de valores faltantes em cada coluna.
- **Visualização Gráfica**: Inclui histogramas e gráficos de contagem organizados de forma responsiva.

## Exemplo de Uso
Caso queira rodar um teste rápido, utilize o seguinte exemplo de dataset:
```python
df = pd.read_csv('/content/pokemonDB_dataset.csv')
report_path = to_html(df)
```

O arquivo HTML será salvo no diretório `/content/relatorio.html`. Para visualizá-lo no Colab, utilize o código:
```python
from IPython.display import IFrame
IFrame(report_path, width=800, height=600)
```

## Tecnologias Utilizadas
- **Python**
- **Google Colab** como plataforma recomendada
- **Bootstrap** para estilização dos relatórios
- **pandas**, **matplotlib**, **seaborn** para manipulação e visualização dos dados
- **jinja2** para a renderização do template HTML

## Possíveis Melhorias
- Implementação de interatividade nos gráficos e filtros dinâmicos.
- Adicionar exportação do relatório em outros formatos, como PDF.
- Desenvolver uma interface web para que os usuários possam carregar datasets e gerar relatórios diretamente.

## Contato
Para dúvidas ou sugestões, entre em contato com os integrantes do projeto:
- Nikolas Rodrigues Moura dos Santos - [LinkedIn](https://www.linkedin.com/in/nikolas-dos-santos)
- Rodrigo Brasileiro - [LinkedIn](https://www.linkedin.com/in/rodrigo-brasileiro-54031b249/)
- Thiago Jardim de Oliveira - [LinkedIn](https://www.linkedin.com/in/thiago-jardim-490164298/)
