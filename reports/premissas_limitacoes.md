# Premissas, limitações e cuidados de interpretação

## Validação temporal

A base usada no projeto não traz uma coluna clara de data de extração, data de churn ou janela de observação/previsão. Por isso, a avaliação foi feita com divisão treino, validação e teste estratificada, mas não com validação temporal out-of-time.

Isso significa que o resultado mede a capacidade de separação estatística na base histórica, mas não prova sozinho que o desempenho será idêntico em safras futuras.

## ROI e receita preservada

O ROI apresentado é uma simulação, não um resultado financeiro realizado. A receita preservada foi estimada usando ARPU médio mensal, margem assumida, custo unitário de campanha e uplift esperado.

Premissas usadas na simulação principal:

- Horizonte financeiro: mensal.
- Margem assumida: 70%.
- Custo unitário de campanha: R$ 10.
- Uplift esperado: 30%.

## Interpretação das variáveis

As variáveis importantes indicam associação com o risco previsto de churn. Elas não provam causalidade.

## Próximos passos para produção

- Validação temporal out-of-time.
- Calibração formal das probabilidades.
- Teste controlado com grupo de controle.
- Monitoramento de drift.
- Retreinamento periódico.
- Integração do score ao CRM.
- Medição de uplift real pós-campanha.
