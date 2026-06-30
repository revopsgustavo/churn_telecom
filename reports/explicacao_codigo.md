# Explicação passo a passo

Este documento explica a lógica do projeto em linguagem simples.

## Problema

Churn significa cancelamento. A empresa quer descobrir quais clientes têm maior propensão estimada ao cancelamento para agir antes que isso aconteça.

## Alvo

A coluna `Churn` informa se o cliente cancelou ou não. No código, `Yes` é convertido para 1 e `No` para 0.

## Features

Features são as colunas usadas para estimar o risco, como contrato, tenure, mensalidade, serviço de internet e método de pagamento.

## Pipeline

O pipeline organiza tratamento de dados e modelo em uma sequência única. Isso evita vazamento porque imputação, escala e encoding são aprendidos apenas no treino.

## Score

O modelo gera uma probabilidade de churn por cliente. Essa probabilidade vira faixa de risco e ajuda a priorizar a fila de retenção.
