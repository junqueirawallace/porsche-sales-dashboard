# Dashboard Interativa de Vendas Porsche

Dashboard web de arquivo único (`index.html`) criada para o desafio de análise de vendas da Porsche da DIO. Usa HTML, CSS e JavaScript sem bibliotecas externas: filtros e gráficos funcionam direto no navegador.

**Ver dashboard online:** [COLE AQUI O LINK DO GITHUB PAGES]

![Dashboard Porsche](imagens/dashboard-porsche.png)

## Perguntas de negócio

1. **Quais modelos geram mais receita?** Ranking dos dez modelos com maior receita no recorte filtrado.
2. **Quais estados concentram mais vendas?** Os dez estados com maior número de registros.
3. **Quais métodos de pagamento são mais utilizados?** Comparação da quantidade de vendas por método.

Os indicadores de topo mostram quantidade de vendas, receita total, ticket médio e quantidade de estados. Os filtros de modelo, estado, ano do veículo e método de pagamento atualizam todos os indicadores e gráficos.

## Tratamento da base

A base possui 100 registros, com colunas originais e sanitizadas.

- Foram usados apenas os campos sanitizados (modelo, ano, preço, quilometragem, método de pagamento, cidade, estado e status de entrega).
- Preço e ano foram convertidos para valores numéricos.
- As 100 vendas foram mantidas. A data da venda não foi usada porque há valores marcados como `INVALID`; por isso não há análise temporal.
- Nomes de clientes e vendedores não foram incluídos, reduzindo a exposição de dados pessoais.
- Valores em dólares americanos (USD).

## Ferramentas e uso de IA

HTML, CSS e JavaScript. O código foi construído com apoio do ChatGPT, a partir de um prompt que defini com as perguntas de negócio, os indicadores e os filtros. [Descreva aqui, em uma frase, o que você revisou ou validou.]

## Arquivos

- `index.html`: dashboard completa, com os dados necessários para renderização.
- `TRATAMENTO_DOS_DADOS.md`: detalhes do tratamento da base.

## Autor

**Wallace F. Junqueira**
Tecnólogo em Logística | Estudante de Gestão da TI | MBA em Data Warehouse e Business Intelligence
[LinkedIn](https://www.linkedin.com/in/wallace-f-468b7a190)
