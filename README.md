# Dashboard Interativa de Vendas Porsche

Dashboard web de arquivo único (`index.html`) criada para o desafio de análise de vendas da Porsche da DIO. A página usa HTML, CSS e JavaScript sem bibliotecas externas: os filtros e gráficos funcionam diretamente no navegador.

## Perguntas de negócio

1. **Quais modelos geram mais receita?** O gráfico ranqueia os dez modelos com maior receita no recorte filtrado. Ajuda a identificar modelos com maior contribuição financeira.
2. **Quais estados concentram mais vendas?** O gráfico mostra os dez estados com maior número de registros. Ajuda a visualizar a distribuição geográfica do volume.
3. **Quais métodos de pagamento são mais utilizados?** O gráfico compara a quantidade de vendas por método de pagamento, ajudando a entender as preferências registradas na base.

Os indicadores de topo mostram quantidade de vendas, receita total, ticket médio e quantidade de estados no recorte. Os filtros de modelo, estado, ano do veículo e método de pagamento atualizam os indicadores e os três gráficos.

## Prompt usado para orientar a construção

> Crie uma dashboard de vendas Porsche em um único arquivo HTML, responsiva e sem dependências externas, usando apenas os campos sanitizados da planilha. O público é alguém que precisa entender o desempenho comercial de forma rápida. Inclua os indicadores quantidade de vendas, receita total, ticket médio e estados atendidos; filtros de modelo, estado, ano do veículo e método de pagamento; e três gráficos que respondam a estas perguntas: quais modelos geram mais receita, quais estados concentram mais vendas e quais métodos de pagamento são mais utilizados. Todos os filtros devem atualizar todos os indicadores e gráficos. Use uma identidade visual premium inspirada em automóveis de luxo, com fundo escuro, branco e vermelho como cor de destaque. Não inclua nomes de clientes nem vendedores. Não invente nem altere os valores da planilha. Entregue tudo em `index.html`, com HTML, CSS e JavaScript no mesmo arquivo.

### Refinamentos aplicados

- Definimos as perguntas de negócio antes de selecionar os gráficos.
- Mantivemos a página em um único HTML, sem bibliotecas externas, para simplificar a publicação.
- Adicionamos filtros sincronizados para modelo, estado, ano do veículo e método de pagamento.
- Incluímos estados vazios para combinações de filtros sem resultados e um botão para limpar os filtros.
- Registramos no painel que a análise não usa a data da venda, pois existem datas sanitizadas como `INVALID`.

## Tratamento da base

A base recebida possui 100 registros e colunas originais e sanitizadas. Para construir o HTML:

- Foram usados os campos sanitizados `PorscheModelSanitized`, `ModelYearSanitized`, `SalesPriceSanitized`, `VehicleMileageSanitized`, `PayMethodSanitized`, `CitySanitized`, `StateSanitized` e `DeliveryStatusSanitized`.
- Preço e ano foram convertidos para valores numéricos; quilometragem também foi convertida quando disponível.
- As 100 vendas foram mantidas. A data da venda não é usada nos gráficos porque alguns valores sanitizados estão marcados como `INVALID`; por isso, não é feita uma análise temporal.
- Nomes de clientes e vendedores e os campos crus não foram incluídos no HTML. Isso reduz a exposição de dados pessoais e segue o princípio de incluir apenas os campos necessários.
- Os valores monetários são exibidos em dólares americanos (USD), conforme a indicação de moeda presente nos valores sanitizados da base.

## Ferramenta utilizada

O HTML foi construído com auxílio do ChatGPT nesta conversa. O processo descrito aqui não depende de Canvas nem de um agente com skill própria.

## Arquivos

- `index.html` — dashboard interativa completa, incluindo os dados necessários para renderização.

## Publicação no GitHub Pages

1. Crie um repositório **público** com nome simples, por exemplo `porsche-sales-dashboard`.
2. Envie `index.html` e `README.md` para a raiz do repositório.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**; selecione a branch `main` e a pasta `/ (root)`, depois salve.
5. Aguarde a publicação e abra o endereço apresentado pelo GitHub Pages. Normalmente, o formato será `https://SEU-USUARIO.github.io/porsche-sales-dashboard/`.
6. Teste os quatro filtros, o botão de limpar filtros e os indicadores em desktop e celular.
7. Na plataforma do curso, envie o **link do repositório**, conforme solicitado. Coloque o link publicado da dashboard no README.

> Substitua no README o endereço de exemplo pelo endereço real do GitHub Pages depois que o GitHub o publicar. O link público só fica disponível após concluir a configuração no GitHub.

## Validação sugerida antes da entrega

- [ ] O repositório está público e contém `index.html` e `README.md`.
- [ ] O GitHub Pages abre a dashboard sem erro.
- [ ] Cada filtro atualiza os quatro indicadores e todos os gráficos.
- [ ] O botão “Limpar filtros” restaura a visão completa.
- [ ] O README contém o link real da dashboard publicada.
- [ ] A entrega na DIO aponta para o repositório, não apenas para a página publicada.

## Autor

### Wallace F. Junqueira

Graduado em Tecnologia em Logística. Estudante de Gestão da Tecnologia da Informação. Pós Graduado em MBA Data Warehouse e Business Intelligence
