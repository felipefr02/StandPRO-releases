## v2.2.25.118 (2026-10-07) — Pedido de venda com documentos, Kanban de OS e OP, permissões por usuário e produto do modelo pelo estoque

### Pedido de venda

- Botão "👤 Novo cliente" no cabeçalho: cadastra o cliente sem sair do pedido. Ao fechar o cadastro, a lista é recarregada e o cliente criado já fica selecionado, com CPF/CNPJ, telefone e e-mail.
- Botão "📎 Documentos" no cabeçalho (pedido já salvo): anexa contrato, proposta, comprovante e outros arquivos ao pedido, com descrição. A lista mostra arquivo, descrição e data; duplo clique abre o documento em qualquer computador.

### Modelo de novos campos

- Botão "Copiar": abre um modelo novo com os campos, formulários e produtos do modelo aberto, para aproveitar um modelo parecido (por exemplo, o do Ultratone no Ultratone Compact).
- Produtos vinculados passam a vir do estoque: "Vincular produto" abre a lista de itens do estoque já filtrada em Produto acabado, com seleção de vários de uma vez. Os vínculos antigos, feitos pelo cadastro de Modelo do produto, continuam valendo até o modelo ser salvo com os produtos escolhidos no estoque.
- TAG do tipo Lista: as opções são cadastradas item a item, com a escolha entre seleção única e múltipla. O servidor passou a gravar as opções na própria TAG.

### Ordem de produção e Ordem de serviço

- O campo "Situação formal" saiu da tela (OP e OS). O andamento da ordem é o "Status (Kanban)", que também aparece nas listas. O valor antigo continua gravado com a ordem.
- Ordem de produção: o campo do pedido passou a se chamar "Pedido de venda / cliente" e mostra o número do pedido e o nome do cliente.
- Ordem de produção: novo botão "Números de série do produto" no cabeçalho, para definir ou corrigir as séries do produto da ordem. As alterações só são gravadas ao salvar a ordem.
- Lista de peças da OP: ao adicionar a estrutura com itens já na lista, a tela pergunta se é para acrescentar ou substituir.
- Produto sem modelo de campos vinculado: o bloco fica sem modelo, em vez de voltar sozinho para o primeiro da lista.

### Kanban de OS e OP

- O "Quadro de etapas" passou a se chamar "Kanban — OS e OP" e fica dentro das listas de Ordem de serviço e Ordem de produção: os botões "Lista" e "Kanban" alternam a visualização sem sair da tela, mantendo a busca digitada.
- O cartão ficou maior e mostra modelo do produto, número de série, cliente, número da ordem com o Status (Kanban), responsável e quantidade.
- Clique direito no cartão: "Abrir formulário da ordem", "Acompanhamento e comentários" e "Mover para" (lista das etapas). F2 abre o acompanhamento do cartão selecionado.
- Filtro "Todos os produtos" com a contagem de ordens de cada produto; a busca também encontra por lote e código do produto. Nova caixa "Mostrar etapas ocultas".
- Depois de mover um cartão, o quadro é relido sozinho, já com o efeito das automações.

### Acompanhamento e comentários (OS e OP)

- Novo botão "Acompanhamento e comentários" no cabeçalho da Ordem de serviço e da Ordem de produção (a ordem precisa estar salva). A mesma tela abre pelo cartão do Kanban.
- Histórico de observações e etapas em linha do tempo, com autor e data/hora; comentário com menção de pessoas.
- Aba "Atividades e prazos": tarefas com responsável, prazo, andamento e checklist.
- "Observar este cartão" / "Deixar de observar", com a lista de observadores.
- Aba "Conferência da etapa": mostra o que falta para avançar e permite vincular uma foto da ordem a cada requisito de foto.

### Etapas, automações e requisitos do Kanban (quem configura)

- "Automações": ao entrar em uma etapa, notifica usuários ou setores ou encaminha o cartão para outro quadro/etapa.
- "Requisitos da etapa": define o que é exigido antes de sair ou de entrar na etapa (campo preenchido, quantidade mínima de fotos) e quem pode avançar.
- Automações e requisitos aceitam condições E / OU por modelo, código do produto, número de série, quantidade, cliente, número da ordem e Status (Kanban).
- Etapas das ordens: botão "Excluir etapa" (a exclusão só vale ao salvar, o histórico é preservado, e "Desfazer exclusões" recupera antes de salvar) e coluna "Ocultar no quadro". As mensagens de validação indicam a linha.

### DMR (Registro Mestre do Produto)

- Em um DMR novo, escolher a Estrutura do produto já traz as peças para os componentes. O botão "Puxar componentes da estrutura" continua disponível para trazer de novo.
- O bloco "Componentes (BoM congelada)" passou a se chamar "Componentes (cópia da Estrutura do produto)".

### Estrutura do produto

- O botão Excluir voltou à tela "Gerenciar Estruturas do Produto". Só é possível excluir a estrutura que nunca foi usada (sem DMR e sem Ordem de produção do produto); a que já foi usada continua protegida e o servidor explica o motivo.

### Permissões

- O menu Permissões abre a tela "Permissões por setor e usuário": escolha Setor ou Usuário, filtre por Módulo e use "Buscar permissão".
- No usuário, cada permissão pode ser SIM, NÃO ou HERDAR (seguir o setor). A coluna ao lado mostra a origem e o valor efetivo.
- Mudanças de permissão passam a valer sem reiniciar: o menu é atualizado a cada minuto e logo após salvar. Se a permissão de uma tela aberta for retirada, a tela é bloqueada com aviso, o rascunho é preservado e ela é liberada se o acesso voltar.
- Telas auxiliares (anexos, históricos de versões, assinatura, importação de Excel, entrada/saída por lote e número de série, gerar documentos) passam a exigir a permissão do módulo de origem.
- Histórico por lote e Histórico por número de série aparecem no menu cada um com a sua permissão. A permissão "Registro" passou a se chamar "Documentos gerados, DHR e avisos ANVISA".

### Sessões e logout da empresa

- Ajustes → Empresa → "Sessões e logout" (para quem tem a permissão de Permissões): define os minutos de inatividade para encerrar a sessão no Desktop e no site, para todos os usuários da empresa; zero significa não encerrar.
- O aviso antes do logout mostra a contagem definida pela empresa.

### Inventário cíclico / anual

- Tela refeita no padrão das demais, com "Salvar rascunho" no rodapé.
- "Fechar inventário" virou "Concluir inventário", com o aviso de que concluir não altera o saldo do estoque (a correção é feita no Lançamento de estoque).
- "Iniciar nova contagem": abre outra sessão com o mesmo planejamento e os saldos atuais, quando o estoque mudou durante a contagem. A tela explica o motivo em vez de mostrar erro genérico.
- Justificativa de divergência com tamanho mínimo (a tela aponta a linha); contagem negativa ou incompatível com a unidade é recusada com mensagem clara; item contado como zero mantém o zero ao reabrir o rascunho.
- Inventário fechado mostra quando e por quem, e permite consultar a contagem por lote/número de série em modo somente leitura.
- Gerenciamento: botão "Excluir selecionado" (só inventário ainda não fechado). Falha ao carregar a lista é avisada.

### Registros (tela removida)

- A tela "Novo Registro" e o "Gerenciamento dos Registros" saíram do menu Qualidade; os atalhos passam a apontar para Modelos de documento. Os registros antigos e seus documentos continuam guardados.
- Modelo de documento que já gerou documento não pode ter o arquivo alterado: a tela pede uma nova revisão.
- Especificação técnica (Pedido de compra): gerar o documento não depende mais do "registro padrão".

### Qualidade e regulatório

- Tecnovigilância: novo item no menu Qualidade e no Mapa do software; bloco "Reportabilidade FDA" reorganizado.
- Submissão regulatória por mercado e Tags do problema: telas no padrão novo; "Abrir / editar" e "Excluir" só habilitam com linha selecionada; falha de carga é avisada com opção de tentar de novo.

### Dashboards

- Menu lateral dos painéis redesenhado (recolhido mostra só ícones). Cada painel só aparece para quem tem a permissão do módulo.
- Gráficos mensais em ordem cronológica, com anos separados, números no formato brasileiro e valor ao passar o mouse.

### Servidor (já publicado)

- Documentos do pedido de venda; exclusão de estrutura sem uso; opções da Lista na TAG; vínculo do modelo de novos campos com o item do estoque.
