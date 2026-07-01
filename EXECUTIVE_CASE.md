# Executive Case — Análise de Churn e Priorização de Retenção em Telecom

> Estudo executivo de Business Analytics e Machine Learning aplicado à tomada de decisão em retenção de clientes.

---

## 1. Contexto do projeto

Este projeto foi desenvolvido a partir de uma base pública de churn em telecom, com 7.043 clientes.

O objetivo principal não foi apenas construir um modelo preditivo, mas demonstrar como dados podem apoiar decisões executivas de retenção.

A análise buscou responder uma pergunta de negócio:

> Como identificar clientes com maior risco de cancelamento para priorizar ações de retenção de forma mais eficiente?

---

## 2. Problema de negócio

Churn representa perda de receita, redução de previsibilidade e aumento da pressão por aquisição de novos clientes.

Em muitas empresas, ações de retenção são feitas de forma ampla, tratando clientes com diferentes níveis de risco da mesma maneira.

O problema é que nem todos os clientes têm a mesma probabilidade de cancelar.

Por isso, uma abordagem orientada por dados permite sair de uma atuação reativa para uma estratégia preventiva, priorizando clientes com maior risco e maior potencial de retorno.

---

## 3. Objetivo da análise

A análise foi estruturada para:

- Identificar fatores associados ao churn.
- Estimar a probabilidade de cancelamento por cliente.
- Segmentar a base em faixas de risco.
- Apoiar campanhas de retenção mais direcionadas.
- Simular o impacto financeiro de ações priorizadas.
- Gerar uma base acionável para CRM, Customer Success, Marketing ou áreas de retenção.

---

## 4. Abordagem utilizada

O projeto seguiu um fluxo de ponta a ponta:

```text
Problema de negócio
        ↓
Análise exploratória dos dados
        ↓
Preparação e tratamento da base
        ↓
Seleção de variáveis
        ↓
Modelagem preditiva
        ↓
Score de churn por cliente
        ↓
Segmentação por risco
        ↓
Recomendações executivas
        ↓
Simulação financeira
```

O Machine Learning foi utilizado como ferramenta de priorização, não como fim do projeto.

---

## 5. Principais achados

A taxa geral de churn da base foi de aproximadamente 26,5%.

A análise mostrou que o churn não ocorre de forma aleatória. Ele se concentra em perfis específicos de clientes.

Os principais fatores associados ao risco previsto foram:

- Contrato mensal.
- Menor tempo de relacionamento.
- Serviço de internet por fibra óptica.
- Ausência de segurança online.
- Ausência de suporte técnico.
- Pagamento via electronic check.
- Maior cobrança mensal.

Esses fatores devem ser interpretados como associações estatísticas, não como causalidade direta.

---

## 6. Modelo preditivo

O modelo final escolhido foi Gradient Boosting.

Principais métricas em teste:

| Métrica | Resultado |
|---|---:|
| ROC AUC | 0,8397 |
| PR AUC | 0,6692 |
| F1-score | 0,6266 |
| Recall | 0,6868 |
| Precision | 0,5761 |
| Accuracy | 0,7824 |

O modelo apresentou boa capacidade de separar clientes com maior e menor risco de churn, especialmente quando utilizado como ferramenta de priorização operacional.

---

## 7. Segmentação por risco

A partir da probabilidade estimada pelo modelo, os clientes foram classificados em quatro faixas de risco.

| Faixa de risco | Clientes | Taxa real de churn |
|---|---:|---:|
| Baixo | 3.779 | 7,0% |
| Médio | 1.285 | 28,4% |
| Alto | 1.057 | 52,1% |
| Crítico | 922 | 74,5% |

O principal achado foi a forte separação entre os grupos.

Clientes classificados como críticos apresentaram churn real superior a 74%, enquanto clientes de baixo risco ficaram próximos de 7%.

Isso mostra que a segmentação pode apoiar uma priorização muito mais eficiente das ações de retenção.

---

## 8. Impacto para o negócio

Antes da análise, uma empresa poderia tratar toda a base de clientes da mesma forma em campanhas de retenção.

Com o score de churn, torna-se possível:

- Priorizar clientes com maior probabilidade de cancelamento.
- Direcionar investimentos para grupos com maior risco.
- Reduzir desperdício em campanhas amplas.
- Criar estratégias específicas por faixa de risco.
- Integrar o score ao CRM.
- Apoiar decisões de CRM, Marketing, Customer Success e Revenue Operations.

A principal mudança é sair de uma lógica reativa para uma atuação preventiva.

---

## 9. Simulação financeira

Foi realizada uma simulação para comparar campanhas direcionadas por risco.

Premissas utilizadas:

- Horizonte mensal.
- Margem de 70%.
- Custo unitário de campanha de R$ 10.
- Uplift esperado de 30%.

A simulação indicou que campanhas concentradas nos clientes de maior risco tendem a ser mais eficientes do que campanhas amplas sem priorização.

A recomendação é iniciar com um piloto controlado, especialmente nos grupos de maior risco, antes de escalar a estratégia.

---

## 10. Recomendações executivas

Com base na análise, as principais recomendações são:

- Priorizar clientes classificados como crítico e alto risco.
- Criar campanhas específicas para clientes com contrato mensal.
- Melhorar onboarding nos primeiros meses de relacionamento.
- Investigar a experiência dos clientes com fibra óptica.
- Oferecer suporte técnico e segurança online como ações preventivas.
- Integrar o score de churn ao CRM.
- Medir o impacto real das campanhas com teste A/B ou grupo de controle.
- Monitorar performance do modelo ao longo do tempo.

---

## 11. Limitações

A análise possui algumas limitações importantes:

- A base não possui janela temporal explícita.
- Não há validação out-of-time.
- O ROI é uma simulação, não um resultado financeiro realizado.
- As variáveis indicam associação, não causalidade.
- A implantação exigiria monitoramento contínuo e validação operacional.

Esses pontos não invalidam a análise, mas indicam cuidados necessários antes de uso em produção.

---

## 12. Próximos passos

Para evolução do projeto, os próximos passos recomendados seriam:

- Validação temporal com dados históricos.
- Calibração formal das probabilidades.
- Teste A/B de campanhas de retenção.
- Monitoramento de drift do modelo.
- Integração ao CRM.
- Criação de health score combinado.
- Mensuração de uplift real após campanhas.
- Retreinamento periódico do modelo.

---

## 13. Conclusão

O principal resultado deste projeto não foi apenas prever churn.

Foi transformar probabilidades em prioridades de negócio.

Machine Learning não reduz churn sozinho.

O valor está em usar o modelo para apoiar decisões melhores: quem priorizar, onde investir, quais ações testar e como medir o impacto.

Este projeto demonstra como Business Analytics e Machine Learning podem trabalhar juntos para apoiar uma estratégia de retenção mais eficiente, preventiva e orientada por evidências.
