# Kaggle + Artigo Técnico

Projeto de análise exploratória de dados sobre desempenho de entregas e avaliações de clientes, usando o [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

## Pergunta de análise

O que aparece associado a atrasos nas entregas e à avaliação dos clientes?

Este conjunto descreve pedidos de comércio eletrônico no Brasil, não pedidos de restaurantes. O projeto usa a operação de entrega como tema de análise e não apresenta seus resultados como se fossem dados do iFood.

## Fonte, licença e dados

A Olist disponibilizou dados comerciais anonimizados, referentes a pedidos de 2016 a 2018. A página do Kaggle informa a licença **CC BY-NC-SA 4.0**. Atribua a fonte, respeite o uso não comercial e os termos de compartilhamento indicados pela licença. Este repositório contém código e documentação, mas não redistribui os arquivos CSV.

No Kaggle, crie um notebook, escolha **Add Input**, pesquise por **Brazilian E-Commerce Public Dataset by Olist** e adicione o conjunto de dados. O notebook também aceita os CSVs em `data/raw/` quando executado localmente.

## Conteúdo

- `notebooks/olist_delivery_analysis.ipynb`: carregamento, verificações de qualidade, análise de atrasos e relação descritiva com avaliações.
- `docs/artigo-tecnico.md`: estrutura do artigo. Complete a seção de resultados depois de executar o notebook.
- `requirements.txt`: dependências para execução local.

## Execução local no Windows

Use Python 3.11:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
jupyter notebook
```

Baixe os CSVs pela página do Kaggle e coloque-os em `data/raw/`, mantendo os nomes originais. Não envie os dados brutos ao GitHub.

## Método e limites

O notebook compara a data real de entrega com a data estimada informada ao cliente e relaciona essa diferença às notas de avaliação. A análise é descritiva: associações observadas não demonstram causalidade. O conjunto é histórico, cobre comércio eletrônico e pode não representar operações atuais de delivery de refeições.
