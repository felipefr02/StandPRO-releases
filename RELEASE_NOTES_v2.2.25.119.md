## v2.2.25.119 (2026-10-08) — Seções nos Novos campos, obrigatório cobrado pela etapa do Kanban e valor inicial

### Novos campos em seções (todos os formulários)

- Os campos do modelo aparecem agrupados em seções, com o título de cada seção, na ordem definida no modelo (por exemplo: Geração de O.P, Fabricação (Montagem), Ensaio de processo… Liberação final).
- A TAG deixou de aparecer ao lado de cada campo: ela só interessa na criação do modelo de documento, onde continua visível.
- Lista de escolha única ganhou uma linha em branco, para voltar o campo a vazio.

### Ordem de produção e Ordem de serviço: obrigatório cobrado pela etapa

- Campo obrigatório que está dentro de uma seção não impede mais o Salvar da ordem. Ele continua com o "*" e o destaque, e quem cobra o preenchimento é a etapa do Kanban.
- Campo obrigatório fora de seção continua impedindo o Salvar. Nos outros formulários nada muda: obrigatório impede o Salvar como sempre.
- Ao mover a ordem de etapa (pelo "Status (Kanban)" da ordem ou arrastando o cartão), se faltar algo o aviso passa a listar o que falta, por seção e campo, em vez de só dizer que há requisitos pendentes.
- Se as seções do modelo não puderem ser lidas (rede), a tela avisa e o Salvar não fica preso por isso.

### Requisitos da etapa (quem configura o Kanban)

- Tela refeita, mais simples: a lista da esquerda traz todas as etapas (com ✔ e a quantidade de requisitos) e, para a etapa escolhida, basta marcar as seções que precisam estar concluídas. Seção concluída = campos obrigatórios da seção preenchidos, no modelo da própria ordem.
- Aberta no Kanban da Ordem de produção, mostra só as etapas e as seções de produção; no de Ordem de serviço, só as de serviço. O que está configurado para o outro tipo de ordem é preservado ao salvar.
- As seções aparecem na ordem do trabalho (a ordem em que estão nos modelos) e há busca pelo nome, sem diferenciar maiúsculas nem acentos.
- "Quando conferir": para o cartão ENTRAR na etapa (padrão) ou para SAIR dela.
- Campo específico, fotos e "quem pode avançar" ficam em "Mais opções".
- Salvar não fecha a tela: ela relê o que ficou gravado e continua na mesma etapa.
- Corrigido: seções marcadas, campo específico e fotos não eram gravados por esta tela.
- Corrigido: condição por "ID do modelo" fazia o servidor recusar o salvar.

### Modelo de novos campos (cadastro)

- Coluna "Seção": digite a seção no primeiro campo de cada grupo e use "Preencher seções para baixo" (clique direito). "Limpar a seção de todas as linhas" desfaz.
- Coluna "Valor inicial": valor que o campo já traz preenchido em registro novo.
- Salvar não fecha a tela, para continuar editando; a TAG customizada também permanece aberta depois de salvar e relê as opções gravadas.
- A lista de campos acompanha o tamanho da janela; clicar no título das colunas não reordena mais a lista (a ordem é a do modelo); duplo clique em qualquer linha abre a TAG.
- "Copiar" voltou a funcionar (dava "Não foi possível copiar o modelo agora").
- Se os campos ou as seções do modelo não puderem ser lidos, a tela avisa e não deixa salvar o modelo vazio.
- O valor inicial só é enviado nas linhas em que foi alterado nesta tela, para não desfazer mudança feita no portal com a tela aberta.

### Valor inicial nos formulários

- Em registro novo, os campos nascem com o valor inicial do modelo. Em registro que já tinha Novos campos gravados nada é alterado sozinho.
- Novo botão "Preencher valores iniciais" no bloco de Novos campos: preenche só os campos vazios; nada é gravado até salvar.
- Ordem nova: trocar o produto volta a trocar o modelo sugerido, mesmo quando o modelo anterior tinha valor inicial (o que a pessoa digitou continua valendo).
- "Editar modelo" dentro da ordem não apaga mais o que foi digitado e ainda não salvo.

### Ordem de produção

- Cabeçalho reorganizado em uma linha, com o botão para cancelar o vínculo com o pedido de venda.
- Número de série do produto aparece na tela (como no portal), inclusive em ordem concluída.
- "Copiar para novo" logo depois de criar a ordem (ou de trocar o modelo) leva o modelo de Novos campos; antes a cópia abria sem modelo e os valores ficavam escondidos.

### Ordem de serviço

- "Copiar para novo" leva o vínculo do produto e, logo depois de criar a ordem, os Novos campos.

### Gerar documento

- Novo botão "🗂 Gerados": histórico dos documentos gerados para o registro, com quem gerou e quando.

### Kanban

- Quadro de etapas: rolagem horizontal pela roda inclinada do mouse, Shift + roda e arrasto com o dedo em tela de toque.
- Aba "Conferência da etapa": o texto deixa claro que ela confere o que é pedido para SAIR da etapa atual.

### Correções gerais

- "Salvar e sair": se o Salvar falhar, a tela avisa e não fecha mais sem gravar.
