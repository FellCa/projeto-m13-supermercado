# Projeto M13 – Fundamentos da Descoberta de Dados (Supermercado)

Análise estatística e visual da base de produtos de um supermercado do Chile (1.107 produtos, 7 categorias).

## O que o notebook faz

1. Média e mediana de `Preco_Normal` por categoria (e quais ficam acima/abaixo da mediana)
2. Desvio padrão por categoria e comportamento de média x mediana
3. Boxplot de `Preco_Normal` da categoria com maior desvio (`lacteos`) e identificação dos outliers
4. Gráfico de barras com a média de desconto por categoria
5. Mapa interativo (treemap) por categoria e marca, colorido pela média de desconto

## Principais resultados

- `lacteos` tem o maior desvio padrão (~3.926) e a média (2.385) é ~2,4x a mediana (989): distribuição assimétrica à direita.
- Única categoria com média abaixo da mediana: `comidas-preparadas` (efeito dos 10 produtos com `Preco_Normal = 0`).
- 43 outliers em `lacteos` (> 6.119): 33 packs de 6/12 unidades e 10 leites em pó em embalagem grande.
- Maiores descontos médios: `congelados` (~154) e `belleza-y-cuidado-personal` (~123).

> 294 produtos têm `Preco_Normal = 0`. As análises seguem o enunciado (coluna como está); o notebook mostra também a versão sem esses zeros.

## Estrutura

```
projeto_supermercado.ipynb               # código + interpretações
MODULO7_PROJETOFINAL_BASE_SUPERMERCADO.csv
imagens/                                 # boxplot, barras e mapa (png/html)
requirements.txt
```

## Como rodar

```bash
pip install -r requirements.txt
jupyter notebook projeto_supermercado.ipynb
```

(`kaleido` é necessário só para salvar o PNG do mapa interativo; o HTML é gerado sempre.)
