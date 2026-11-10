# Atrasos de entrega e avaliação dos clientes: análise exploratória dos dados da Olist

> **Status:** rascunho. Preencha os resultados somente depois de executar o notebook. Não publique números estimados ou inventados.

## Resumo

Este artigo analisa a relação descritiva entre atrasos de entrega e avaliações dos clientes no Brazilian E-Commerce Public Dataset by Olist. O objetivo é verificar como a diferença entre a data real e a data estimada se distribui e como as notas variam entre pedidos entregues no prazo e pedidos atrasados.

## Pergunta

O que aparece associado a atrasos nas entregas e à avaliação dos clientes?

## Fonte e contexto

A fonte é o [Brazilian E-Commerce Public Dataset by Olist no Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), com dados comerciais anonimizados de pedidos feitos no Brasil entre 2016 e 2018. A página do conjunto informa a licença CC BY-NC-SA 4.0.

O conjunto representa comércio eletrônico em geral, não pedidos de restaurantes. As conclusões ficam restritas a essa fonte e não são atribuídas ao iFood nem a uma operação de delivery de refeições.

## Preparação e método

O notebook usa os arquivos de pedidos, avaliações e clientes. São considerados pedidos com status de entrega concluída e datas real e estimada disponíveis. A diferença em dias é calculada como data real menos data estimada; valores positivos representam atraso. Avaliações são agregadas por pedido antes das junções para evitar duplicar pedidos.

A análise inclui verificações de duplicidade, valores ausentes, distribuição dos atrasos, proporção de pedidos atrasados e comparação descritiva das notas por situação de entrega. Gráficos com limites de eixo ajustados são identificados como visualizações limitadas para facilitar a leitura, sem remover observações dos resumos numéricos.

## Resultados

**A preencher após executar o notebook.** Registre aqui os números exibidos pelo notebook, o tamanho da amostra analisada e os principais padrões observados. Explique também valores ausentes e eventuais limitações de cobertura.

## Interpretação

Descreva quais padrões são compatíveis com os resultados. Diferencie claramente associação de causalidade: a análise observacional não prova que o atraso causou uma nota específica.

## Limitações

- Dados históricos de 2016 a 2018.
- Comércio eletrônico geral, não delivery de refeições.
- Dados anonimizados e sujeitos à cobertura e qualidade da fonte original.
- Uma associação entre atraso e nota não identifica, por si só, causa ou efeito.
- A análise não mede desempenho atual de uma empresa específica.

## Reprodutibilidade e atribuição

Notebook: `notebooks/olist_delivery_analysis.ipynb`.

Fonte: [Olist, Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). Consulte a página da fonte para atribuição e termos da licença CC BY-NC-SA 4.0.
