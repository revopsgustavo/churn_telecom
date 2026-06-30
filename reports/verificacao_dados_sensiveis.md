# Verificação de dados sensíveis

Foi feita uma revisão simples dos nomes de colunas da base antes da publicação.

## Resultado

Nenhuma coluna com dado pessoal sensível evidente foi identificada, como CPF, e-mail, endereço, data de nascimento ou telefone do cliente.

A coluna `customerID` foi mantida apenas como identificador técnico da base. A coluna `PhoneService` indica contratação de serviço telefônico e não representa um número de telefone pessoal.

## Cuidados mantidos

- Não publicar credenciais, tokens, senhas ou arquivos `.env`.
- Não incluir arquivos temporários, logs ou modelos serializados sem necessidade.
- Manter o README claro de que o projeto usa base pública/sintética de telecom para fins analíticos.
