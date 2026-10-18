# Dashboard de Vendas — Xbox Game Pass

## Visão geral

Este projeto apresenta um dashboard desenvolvido em Excel para organizar e visualizar dados de assinaturas do Xbox Game Pass. A proposta é transformar a base tabular em indicadores e gráficos que facilitem a leitura dos resultados e apoiem análises baseadas em dados.

O dashboard utiliza uma identidade visual escura, com destaques em verde, e reúne indicadores gerais e comparações por plano e tipo de assinatura.

> **Importante:** a base utilizada no arquivo original é de assinaturas do Xbox Game Pass. Portanto, o projeto demonstra técnicas de análise e visualização de dados em um contexto de assinaturas; não representa uma base genérica de vendas de produtos.

## Objetivo

- Organizar os dados em uma visão resumida.
- Facilitar a análise do faturamento registrado na base.
- Comparar o faturamento entre planos e tipos de assinatura.
- Apresentar uma visão mensal baseada na data de início das assinaturas.
- Demonstrar o uso do Excel para criação de indicadores e gráficos.

## Dados utilizados

Os cálculos são feitos a partir da aba **`B̳ases`** do arquivo Excel original, que contém registros de assinaturas. Entre os campos utilizados pelo dashboard estão:

- **`Customer ID`** (coluna A): identificação do registro/assinante, utilizada para contar os assinantes.
- **`Subscription Type`** (coluna G): tipo de assinatura, agrupado em `Monthly`, `Quarterly` e `Annual`.
- **`Subscription Plan`** (coluna C): plano, agrupado em `Core`, `Standard` e `Ultimate`.
- **`Start Date`** (coluna D): data de início usada para agrupar o faturamento por mês.
- **`Auto Renewal`** (coluna E): indicador de renovação automática.
- **`Total Value`** (coluna M): valor utilizado como faturamento nos indicadores e gráficos.

Os valores, nomes de campos e categorias dependem da base original. Antes de substituir ou ampliar a base, confirme se as colunas continuam nas mesmas posições e se os nomes/categorias permanecem compatíveis com as fórmulas.

## Indicadores e visualizações

### Indicadores principais

- **Faturamento total:** soma dos valores do campo `Total Value`.
- **Assinantes:** contagem dos registros preenchidos na coluna `Customer ID`.
- **Ticket médio por assinante:** faturamento total dividido pela quantidade de registros/assinantes contados.
- **Taxa de renovação automática:** proporção de registros com `Auto Renewal` igual a `Yes`.

### Gráficos

- **Faturamento por plano:** compara o faturamento de `Core`, `Standard` e `Ultimate`.
- **Faturamento por tipo de assinatura:** compara `Monthly`, `Quarterly` e `Annual`.
- **Evolução mensal:** soma o valor de `Total Value` conforme o mês da coluna `Start Date`, para o ano de 2024.

## Estrutura do arquivo

O arquivo `dashboard_vendas_modelo.xlsx` contém as seguintes abas:

- **`Dashboard de Vendas`**: painel visual com indicadores e gráficos.
- **`B̳ases`**: base de dados utilizada nas fórmulas.
- **`C̳álculos`**: aba original de cálculos.
- **`D̳ashboard`**: dashboard original preservado como referência.
- **`A̳ssets`**: aba original de recursos preservada.

A aba **`Dashboard de Vendas`** foi adicionada ao arquivo, mantendo as abas originais.

## Como abrir e utilizar

1. Baixe o arquivo `dashboard_vendas_modelo.xlsx`.
2. Abra-o no Microsoft Excel. Aplicativos compatíveis podem exibir alguns elementos de maneira diferente.
3. Acesse a aba **`Dashboard de Vendas`** para consultar os indicadores e gráficos.
4. Para conferir os registros de origem, abra a aba **`B̳ases`**.
5. Se alterar a base, confira se as fórmulas e os gráficos continuam cobrindo todas as linhas e categorias relevantes.
6. Se o Excel solicitar, habilite o recálculo das fórmulas para atualizar os resultados.

## Como reproduzir o projeto

Para reconstruir um dashboard semelhante usando a base disponível:

1. **Prepare os dados:** mantenha os registros organizados em formato tabular, com cabeçalhos e tipos de dados consistentes.
2. **Identifique os campos:** localize o identificador do assinante, plano, tipo de assinatura, data de início, renovação automática e valor total.
3. **Crie os indicadores:** use fórmulas equivalentes a `SUM`, `COUNTA`, `IFERROR`, `COUNTIF` e `SUMIF`/`SUMIFS` para calcular os totais e agrupamentos.
4. **Agrupe os valores:** calcule o faturamento por plano e tipo de assinatura e consolide o valor por mês da data de início.
5. **Insira os gráficos:** crie um gráfico de barras para comparar planos, um gráfico de rosca para a participação por tipo de assinatura e um gráfico de linhas para a evolução mensal.
6. **Monte o layout:** organize os indicadores no topo, os gráficos de comparação no centro e a evolução mensal na parte inferior. Use títulos claros, formatação numérica consistente e cores com bom contraste.
7. **Valide os resultados:** compare o faturamento total do painel com a soma do campo `Total Value` na base e confira alguns agrupamentos manualmente.

As fórmulas e os gráficos existentes no arquivo foram preparados para a estrutura atual da planilha. A reprodução em outra base pode exigir ajustes de nomes de colunas, intervalos, categorias e período analisado.

## Premissas e limitações

- O campo `Total Value` é tratado como valor de faturamento para fins de análise do projeto; a interpretação comercial exata depende do significado atribuído a esse campo na base de origem.
- O indicador **Assinantes** conta valores preenchidos em `Customer ID`; não é necessariamente uma contagem de clientes únicos caso existam registros repetidos.
- A taxa de renovação automática considera `Yes` como resposta afirmativa. Verifique os valores possíveis na base antes de reutilizar a fórmula em outro conjunto de dados.
- O gráfico mensal está configurado para **2024** e utiliza a data de início da assinatura. Ele não deve ser interpretado como uma série histórica de vendas realizadas por data de pagamento.
- A planilha utiliza fórmulas e gráficos nativos do Excel. A aparência e o recálculo podem variar em outros aplicativos de planilhas.

## Tecnologias e recursos

- Microsoft Excel / planilha `.xlsx`
- Fórmulas de agregação e contagem
- Gráficos de barras, rosca e linhas
- Formatação de células e organização visual de indicadores

## Arquivo do projeto

O principal arquivo é `dashboard_vendas_modelo.xlsx`, que contém o dashboard e a base utilizada na análise.

---

Projeto desenvolvido com foco em organização de dados, visualização de indicadores e prática de análise de dados no Excel.
