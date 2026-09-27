# Porsche Sales Dashboard

Dashboard interativa em HTML criada a partir da planilha sanitizada do desafio da DIO.

## Objetivo

Transformar uma base de 100 registros de vendas Porsche em uma dashboard de Business Intelligence capaz de responder perguntas comerciais por meio de indicadores, gráficos e filtros.

## Perguntas de negócio

### 1. Quais modelos Porsche geram maior receita?

A análise usa um gráfico de barras com a receita por modelo. A pergunta ajuda a identificar quais modelos concentram maior valor financeiro no recorte selecionado.

### 2. Quais estados concentram a maior receita?

A análise agrupa a receita por estado. Com os filtros, é possível investigar como a concentração geográfica muda conforme modelo, ano, pagamento ou status.

### 3. Como a receita se distribui entre os métodos de pagamento?

O gráfico compara a receita registrada por método de pagamento. Isso permite observar a composição financeira das vendas.

## Indicadores

A dashboard apresenta:

- Total de vendas/Registros
- Receita registrada
- Ticket médio
- Quantidade de vendas com status `Delivered`

## Filtros

- Modelo
- Estado
- Ano do modelo
- Método de pagamento
- Status de entrega

Todos os gráficos e indicadores são recalculados conforme os filtros.

## Tratamento da base

O desafio fornece os campos em duas versões: dado cru e dado sanitizado.

Para a dashboard foram utilizadas somente as colunas sanitizadas:

- `PorscheModelSanitized`
- `ModelYearSanitized`
- `SalesPriceSanitized`
- `VehicleMileageSanitized`
- `PayMethodSanitized`
- `CitySanitized`
- `StateSanitized`
- `SaleDateSanitized`
- `DeliveryStatusSanitized`

Preço, ano e quilometragem foram convertidos para tipos numéricos. A data foi interpretada como data quando válida.

Um ponto relevante da base é que 24 registros possuem data sanitizada classificada como `INVALID`. Esses registros foram preservados e documentados. A dashboard não inventa datas nem usa a data como dimensão principal, evitando criar informação artificial.

## Ferramenta e processo

O projeto foi estruturado com:

- HTML5
- CSS3
- JavaScript
- Chart.js
- GitHub Pages para publicação

### Prompt utilizado como ponto de partida

```text
Tenho uma planilha com 100 vendas da Porsche e quero criar uma
dashboard interativa em HTML para um projeto de portfólio de
Análise de Dados.

Use somente as colunas sanitizadas da base.

Quero que a dashboard responda estas três perguntas de negócio:

1. Quais modelos Porsche geram maior receita?
2. Quais estados concentram a maior receita?
3. Como a receita se distribui entre os métodos de pagamento?

Crie filtros para modelo, estado, ano do modelo, método de pagamento
e status de entrega.

Inclua no topo os indicadores de quantidade de vendas, receita,
ticket médio e quantidade de entregas realizadas.

A interface deve ter aparência premium, inspirada no universo visual
automotivo/Porsche, usando fundo escuro, grafite, branco e vermelho
como cor de destaque.

A entrega deve ser um único arquivo index.html, com os dados
embutidos no próprio arquivo e gráficos interativos.

Priorize código organizado, responsivo e fácil de publicar no
GitHub Pages.
```

## Evolução do prompt

Na etapa de refinamento, a preocupação principal foi fazer a dashboard responder perguntas de negócio em vez de apenas apresentar gráficos.

Também foram adicionados:

- filtro por status;
- leitura executiva automática;
- ticket médio;
- quantidade de entregas;
- observação sobre datas `INVALID`;
- layout responsivo;
- gráficos ordenados por receita.

## Estrutura

```text
porsche-sales-dashboard/
├── index.html
└── README.md
```

## Publicação no GitHub Pages

1. Crie um repositório público com nome, por exemplo:
   `porsche-sales-dashboard`
2. Coloque `index.html` e `README.md` na raiz.
3. Vá em **Settings → Pages**.
4. Em **Build and deployment**, selecione:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
5. Salve e aguarde a publicação.
6. O endereço será semelhante a:

```text
https://SEU-USUARIO.github.io/porsche-sales-dashboard/
```

## Evidências recomendadas

Para fortalecer o portfólio, adicione ao README:

- print da dashboard completa;
- print com um estado filtrado;
- print com um modelo filtrado;
- link para a dashboard publicada;
- link para este repositório.

## Observação

A base utilizada no projeto é a versão sanitizada fornecida no desafio. Como os dados ficam incorporados no HTML para permitir a execução da dashboard como arquivo único, verifique sempre se a base disponibilizada pelo desafio continua adequada para publicação pública.
