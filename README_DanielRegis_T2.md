# Análise de Vendas do Varejo 🛒

Este projeto mostra o passo a passo de limpeza e análise de uma base de vendas de supermercado.
A ideia principal é transformar dados brutos em gráficos e informações que façam sentido.

## O que tem aqui

- `Miniprojeto_Varejo_AED.ipynb`: notebook principal com todo o fluxo de trabalho.
- `database/Base Varejo.csv`: arquivo original com as vendas.
- `database/df_limpo.csv`: versão limpa dos dados que o notebook gera.

## O que o notebook faz

1. Importa os dados do CSV original.
2. Remove colunas completamente vazias.
3. Converte a coluna `DATA` para um tipo de data que o pandas entende.
4. Substitui valores inválidos em `PR_CAT` por `Sem Categoria`.
5. Traduz os códigos de `CL_EC` para palavras, deixando o gráfico mais claro.
6. Remove duplicatas e salva o resultado limpo em `database/df_limpo.csv`.

## Por que isso é importante

No começo, a coluna `DATA` está como texto. Isso dá problema quando o código tenta usar `df_limpo['DATA'].dt.month` ou `df_limpo['DATA'].dt.year`.
Por isso, a parte de limpeza é a que resolve o principal erro do notebook.

Também é melhor trocar `CL_EC` de número para palavra, porque isso torna o gráfico mais fácil de entender e interpretar.

## O que você encontra no notebook

- limpeza geral do dataset
- transformação de datas
- substituição de códigos de estado civil por rótulos legíveis
- análise de categoria de produtos
- gráficos separados para gênero e estado civil
- agrupamento temporal por mês e por dia da semana

## Como usar

1. Abra `Miniprojeto_Varejo_AED.ipynb` no VS Code ou Jupyter.
2. Execute as células na sequência:
   - limpeza e transformação
   - leitura do arquivo limpo
   - estatísticas e gráficos
3. Se der erro na parte de tempo, execute de novo a célula que lê `df_limpo.csv` e verifica o dtype de `DATA`.

## Resultado esperado

- `DATA` deve ficar como `datetime64[ns]`.
- os gráficos de `CL_GENERO` e `CL_EC` devem aparecer separadamente.
- as vendas por dia da semana mostram o comportamento da base ao longo da semana.

## Principais insights

- A maior parte das vendas está nas categorias do dia a dia, o que mostra que esse público busca produtos essenciais.
- O perfil de compra muda de acordo com o estado civil, então usar `CL_EC` com rótulo ajuda a interpretar melhor os dados.
- Mulheres e homens têm padrões de compra diferentes, o que ajuda a pensar em campanhas mais específicas.
- O volume de vendas varia ao longo da semana: dias úteis são mais fortes que fim de semana.

## Observações finais

O objetivo aqui não é só gerar números, mas deixar os dados prontos para análise.
Quando a base está limpa, a parte de visualização funciona melhor e os resultados ficam mais confiáveis.
