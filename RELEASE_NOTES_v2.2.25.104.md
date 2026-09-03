# Stand PRO 2.2.25.104

Correção do catálogo documental e do fluxo de geração de documentos:

- `@NRA` agora significa “Necessário o registro da ação corretiva?” e usa `SIM/NÃO`.
- O contrato vale para reclamações de clientes e avaliações de certificados de calibração.
- `@NRS` identifica Nome/Razão do cliente; `@IDP` identifica o ID do proprietário.
- `@RAC` continua reconhecido como alias de modelos antigos.
- Tenants existentes são normalizados de forma idempotente no bootstrap da API.
