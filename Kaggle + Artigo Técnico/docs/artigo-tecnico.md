# Atrasos de entrega e avaliação dos clientes: análise exploratória dos dados da Olist

> **Status:** análise executada no Kaggle; resultados registrados a partir da execução da versão 4 do notebook.

## Resumo

Este artigo analisa a relação descritiva entre atrasos de entrega e avaliações dos clientes no Brazilian E-Commerce Public Dataset by Olist. Na amostra analisada, pedidos entregues após a data estimada tiveram nota média inferior à dos pedidos entregues no prazo ou antes. O resultado descreve uma associação na amostra; não demonstra causalidade.

## Pergunta

O que aparece associado a atrasos nas entregas e à avaliação dos clientes?

## Fonte e contexto

A fonte é o [Brazilian E-Commerce Public Dataset by Olist no Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), com dados comerciais anonimizados de pedidos feitos no Brasil entre 2016 e 2018. A página do conjunto informa a licença CC BY-NC-SA 4.0.

O conjunto representa comércio eletrônico em geral, não pedidos de restaurantes. As conclusões ficam restritas a essa fonte e não são atribuídas ao iFood nem a uma operação de delivery de refeições.

## Preparação e método

O notebook usa os arquivos de pedidos, avaliações e clientes. Foram considerados pedidos com status de entrega concluída e datas real e estimada disponíveis. A diferença em dias foi calculada como data real menos data estimada; valores positivos representam atraso. Avaliações foram agregadas por pedido antes das junções para evitar duplicar pedidos.

A taxa de atraso usa somente pedidos que atendem a esses critérios. As notas foram comparadas entre pedidos entregues atrasados e pedidos entregues no prazo ou adiantados. Como algumas avaliações estão ausentes, a contagem de avaliações por grupo é menor que a contagem de pedidos.

## Resultados

A execução analisou **96.470 pedidos entregues** com as datas real e estimada disponíveis. Desses, **7.826 (8,11%)** chegaram após a data estimada. Considerando todos os pedidos da amostra, a mediana da diferença entre entrega real e estimativa foi **−11,95 dias**, indicando que a entrega típica ocorreu antes da estimativa. Entre os pedidos atrasados, a mediana do atraso foi **5,81 dias**.

A avaliação estava disponível para **99,33%** dos pedidos analisados. Na comparação por nota:

| Situação da entrega | Avaliações | Nota média | Mediana |
| --- | ---: | ---: | ---: |
| No prazo ou adiantado | 88.163 | 4,29 | 5 |
| Atrasado | 7.661 | 2,57 | 2 |

Na amostra, os pedidos atrasados tiveram notas médias e medianas menores. O número de avaliações de pedidos atrasados (7.661) é inferior ao número total de pedidos atrasados (7.826) por causa de avaliações ausentes.

## Interpretação

Os resultados mostram uma associação entre atraso e notas menores nesta amostra: pedidos entregues depois da estimativa receberam avaliações médias inferiores às dos pedidos no prazo ou adiantados. A análise não prova que o atraso, sozinho, causou a diferença. Outros fatores — como produto, vendedor, região ou experiência geral de compra — também podem estar relacionados às notas.

## Limitações

- Dados históricos de 2016 a 2018.
- Comércio eletrônico geral, não delivery de refeições.
- A taxa de atraso foi calculada apenas para pedidos marcados como entregues e com as duas datas necessárias.
- Há avaliações ausentes; por isso, a quantidade de avaliações não coincide com a quantidade de pedidos.
- Dados anonimizados e sujeitos à cobertura e qualidade da fonte original.
- Uma associação entre atraso e nota não identifica, por si só, causa ou efeito.
- A análise não mede desempenho atual de uma empresa específica.

## Reprodutibilidade e atribuição

Notebook: `notebooks/olist_delivery_analysis.ipynb`.

Fonte: [Olist, Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). Consulte a página da fonte para atribuição e termos da licença CC BY-NC-SA 4.0.
