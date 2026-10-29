## v2.2.25.127 (2026-10-29) — Listas sem perder o lugar, janelas que não somem, vínculos certos e O.P. só com produtos acabados

### Listas

- Depois de salvar, de "↻ Atualizar", de "Colunas" e de importar, a lista volta com a mesma linha marcada, na mesma rolagem e na mesma ordem.
- O Salvar não deixa mais a janela parada esperando a lista inteira recarregar: o "… salvo" aparece na hora e a lista se atualiza sozinha.
- Se só a atualização da lista falhar, não aparece mais "Erro" com o registro já salvo.
- Excluir ou cancelar não apaga mais a busca digitada nem desmarca o "Filtrar período". Depois de excluir, nenhuma linha fica marcada sozinha.
- Com "Filtrar período" marcado, o registro novo aparece na lista depois de salvar.

### Janelas

- Ordem ou ficha aberta pelo Kanban ou por um aviso ganha aba na barra de tarefas e não se perde atrás da janela principal. Abrir de novo o mesmo cartão ou aviso traz a mesma janela.

### Estoque

- A "Lista de itens do estoque" avisa quando não consegue carregar, com o botão "Tentar de novo", em vez de abrir vazia.
- No pedido de venda gerado pela O.P., uma falha de leitura não aparece mais como "produto não encontrado".

### Qualidade e vínculos

- Reclamação e O.S.: os botões abrem o registro já ligado em vez de criar outro. A O.S. cancelada não conta como ligada, e aí a reclamação pode ganhar uma O.S. nova.
- Inspeção de recebimento: "Abrir não conformidade" abre a NC já ligada. Se a inspeção ainda não foi decidida e a NC ligada já está fechada, dá para abrir outra.

### Ordem de produção

- A escolha do produto da O.P. nova mostra só os produtos acabados ("04 - Produto acabado"), como no site. Produto sem Estrutura do produto abre sem lista de peças inicial e sem DMR, e a ordem pode ser salva assim.
