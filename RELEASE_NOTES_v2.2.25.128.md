## v2.2.25.128 (2026-11-22) — Qualidade pelas normas, vínculos entre os registros, Compras, Kanban do pedido e documentos numa janela só

### Ordens de serviço e produção

- O.S.: a tabela de peças ganhou a coluna "Observações"; a peça escolhida no estoque já vem com a observação do cadastro do item.
- O.S. e O.P.: botão "🔗 Vínculos" no alto mostra peças (pedido, entregue e falta), saídas de material, não conformidades e, na O.P., a entrada do produto, com "Abrir" em cada linha.
- O.P.: o "↗" ao lado do "Pedido de venda" abre o pedido, e o "↗" depois do produto abre a estrutura do produto.
- O.P.: o aviso "Estrutura diferente do DMR" ganhou o botão "Ver DMR"; ao fechar o DMR, a pergunta volta.
- O.S.: o "↗" ao lado do Modelo do produto abre o modelo (depois de salvar a ordem).
- O.S. cancelada e O.P. concluída ou cancelada: o "🔗 Vínculos" e o "↗" continuam funcionando, mesmo só para consulta.
- O.P. com estrutura sem DMR aprovado: o Salvar abre a janela "Resolver DMR", com "Abrir o DMR desta estrutura", "Conferir de novo" e, para o Master, "Não exigir DMR nesta empresa"; o que foi preenchido continua na ordem.
- O.S. e O.P.: o "Mover" do "Status (Kanban)" de dentro da ordem, quando falta campo, abre a mesma janela "O que falta para mover" do Kanban, com "Salvar e mover".
- O.S. e O.P.: com alteração por salvar, o "Mover" avisa para salvar a ordem e mover de novo; nada do que foi digitado se perde.
- O.S. e O.P.: ao escolher a etapa no "Status (Kanban)", antes de mover, a ordem já marca os campos que essa etapa vai pedir.
- Fotos da O.S. e da O.P.: ao escolher várias fotos de uma vez, elas sobem uma por vez, para nenhuma se perder quando a conexão está fraca.

### Kanban

- Setas "‹" e "›" na borda do quadro quando há etapas escondidas; clicar rola quase uma tela (O.S., O.P. e pedido de venda).
- Cada etapa pode ter um "O que significa" (em Configurar etapas, até 300 letras); no quadro, um "?" ao lado do nome mostra a frase.
- Ao recusar a troca de etapa, o quadro diz o que falta e qual etapa pede ("Preencha X — pedido pela etapa Y para avançar").
- Janela "O que falta para mover": cada campo diz qual etapa o pede.
- Requisitos da etapa: o que já é obrigatório sempre aparece como "Sempre — regra do campo" ou "Sempre — fixo do sistema".
- Textos do quadro mais claros: rodapé explica como mudar a etapa, filtro "Semana da ordem: todas" / "Semana do pedido: todas", e a recusa com a sigla ("PV 118/26 voltou para a etapa anterior").
- Kanban da O.S.: clicar no selo da proposta ("Proposta enviada · esperando", "aprovada", "reprovada"…) abre a janela "Resumo da proposta".
- Resumo da proposta: situação, o que o cliente pediu para mudar, quando e por quem foi enviada, o PDF ("Ver"), "Copiar link" e os pedidos anteriores.
- Automações (O.S., O.P., pedido de venda e proposta) e lembrete do prazo: botão "🏷 TAGs disponíveis" embaixo do texto, com busca, mostra TAG e campo e põe a TAG onde está o cursor.
- Quadro da O.P.: o botão direito no cartão que tem pedido mostra "Abrir pedido de venda".
- Quadro da O.P.: "Pedido de venda" como opção (desligada) em "Campos do cartão", "Colunas" e no título do cartão.
- Cada etapa com dois ou mais cartões tem um "⇅" no cabeçalho, ao lado do nome: ele pergunta "Reorganizar os cartões" e põe só aquela etapa em ordem de número, crescente ou decrescente (não aparece em "Pedidos de venda" da O.P. nem em "Sem etapa").
- O quadro que se atualiza sozinho a cada 30 segundos fica mais leve: quando nada mudou, ele não é montado de novo.

### Pedido de venda

- Kanban do pedido: "Requisitos da etapa" com as abas Campos nativos, Campos customizados e Seções, como na O.P.
- Dentro do pedido: os Novos campos mostram só as seções da etapa atual, e o campo que a etapa pede fica marcado.
- Novo campo obrigatório que está numa seção passa a ser cobrado pela etapa do Kanban, como na O.S. e na O.P. (não trava mais o Salvar).
- Botão "Acompanhamento e comentários" dentro do pedido: atividades e prazos, observar, comentários com @ e até 5 fotos ou PDFs.
- O mesmo "Acompanhamento e comentários" no menu do cartão do quadro do pedido (e na tecla F2).
- Cartão do pedido: uma linha por O.P. com a etapa dela ("O.P. 25/26 · Finalizada ✓") e "✓ Todas as O.P. concluídas" quando todas terminaram (inclusive em "Fechado").
- Cartão do pedido: cada O.P. abre com um clique, e o botão direito tem "Abrir O.P. …" para cada uma.
- Entrega atrasada aparece em vermelho, com "atrasada há N dias".
- Coluna "Entregue": avisa que os entregues ficam escondidos e que é só marcar "Mostrar entregues".
- Dentro do pedido: "Etapa (Kanban)" ao lado do número, só para leitura (a etapa muda pelo Kanban).
- Automações do pedido: novas opções "Quando as O.P. do pedido chegarem numa etapa" e "Quando uma O.P. for ligada ao pedido", que levam o pedido para a coluna escolhida (só para frente).
- Automações do pedido: as condições ficam só com Cliente, Número do pedido e Status (Kanban).
- Botão "Ver cliente" ao lado do cliente: abre o cadastro; quem não tem acesso a Clientes vê os contatos que o pedido já mostra.
- "🔗 Vínculos" do pedido mostra as O.P. dele (número, equipamento, série e etapa).
- "Gerar ordem de produção" num pedido que já tem O.P. pergunta antes: "Abrir O.P. …", "Gerar outra" ou "Voltar".

### Estoque e Compras

- "Sugestão de compra" (no Pedido e na Solicitação): opções "Abaixo do mínimo", "Quantidade" e "Fornecedor", abrindo em "Abaixo do mínimo".
- Sugestão de compra: caixinhas, "☑ Marcar todos", "✓ Incluir marcados" e a quantidade sugerida pode ser mudada antes de incluir.
- Incluir na Sugestão com itens já lançados pergunta: "Substituir os itens", "Juntar aos itens" ou "Voltar".
- No Pedido, a Sugestão mostra os itens de um fornecedor por vez; incluir itens de outro fornecedor pergunta se troca o fornecedor do pedido.
- Itens incluídos pela Sugestão vêm com o último preço em vermelho, até a pessoa confirmar.
- Trocar ou limpar o fornecedor de um pedido que já tem itens pergunta "Trocar fornecedor" ou "Manter fornecedor".
- Indicador "Itens abaixo do mínimo" (antes "Itens sinalizados para compra"), na Tela inicial e no Dashboard do estoque, abre a Solicitação de compra já na Sugestão.
- "Lote mínimo/máximo" agora se chama "Estoque mínimo/máximo" nas telas.
- Aviso "N itens abaixo do mínimo" na Central de notificações para quem tem acesso à Solicitação de compra; o "Abrir" leva à Sugestão.
- Pedido de compra: botão "🖨️ Imprimir para conferência", com a prévia das páginas e impressão na impressora ou em PDF.
- Entrada de material: valor diferente do pedido mostra a caixa "Valor diferente do pedido", com "Salvar assim mesmo" ou "Voltar".
- Pedido de compra: botão "📥 Dar entrada" abre a Entrada de material já com o pedido e o que falta receber.
- Lista de pedidos de compra com as colunas "Recebimento" (Não recebido, Recebido em parte, Recebido) e "Data de entrega".
- Pedido de compra: coluna "Já recebido" e quadro "Entradas deste pedido", que abre cada entrada; a faixa do pedido recebido diz quais entradas.
- Pedido de compra já recebido abre só para consulta: "Gerar documento" e "Imprimir para conferência" funcionam direto, sem pedir para salvar.
- Entrada de material: o "📂" do pedido abre o Pedido de compra só para consulta, e a lupa só mostra pedidos com algo a receber.
- Lista de Solicitações de compra com a coluna "Pedido" (o número do pedido gerado).
- Solicitação de compra nova também tem "🛒 Criar pedido", que pergunta "Salvar e gerar o pedido?".
- Indicador "Pedidos aguardando entrega" (com os atrasados) na área Compras da Tela inicial.
- Menu Compras na ordem do trabalho, agora com "Entrada de material".
- Pedido de compra: "↗" do fornecedor e "↗ Solicitação de origem" no alto; a Entrada de material também tem o "↗" do fornecedor.
- Fornecedor: "🔗 Vínculos" com os pedidos de compra e as entradas dele.
- Item do estoque: "🔗 Vínculos" com entradas, saídas, transferências, lançamentos, lotes e séries, pedidos, solicitações, O.S., O.P., estruturas, listas de peças e DMR.
- Item do estoque: a Classificação fiscal volta a ficar escondida (só aparece se uma regra pedir) e "Observações" fica na Identificação.
- Histórico de lote e de número de série: coluna "Origem" na lista e "↗ Origem" na ficha do movimento.
- Inventário e lançamento ligados: "↗ Lançamento aplicado" e "↗ Inventário de origem".
- Saída de material: mostra de onde veio (O.S. ou O.P., com "↗").
- Saída de material: a mensagem de saldo diz quanto há no depósito, quanto foi pedido e que dá para entregar em parte.
- Solicitação do estoque: "🔗 Vínculos" com todas as saídas que a atenderam.
- Pendências de entradas e saídas: botão "↗ Abrir origem"; a entrada do produto da O.P. tem "↗ Abrir ordem de produção".
- Entrada e Saída: os campos que ficam cinza dizem por quê, e a saída de item em quarentena não pede mais para "retirar a quarentena".
- Lista de itens do estoque mais rápida ao lançar várias peças seguidas.

### Documentos

- Documentos: o "Anexar" aceita vários arquivos de uma vez; no fim, um aviso diz quantos entraram e quais ficaram de fora.
- Documento gerado: duas marcas no mesmo trecho do Word (como "{ITEM_QTD} {ITEM_UNP}") saem as duas preenchidas.
- Peças da O.S. no documento: a TAG {ITEM_OBS} traz a observação de cada peça; os P17 da O.S. já saem com o "Campo 21: Observações".
- Modelo de documento: dois cliques num produto ligado abrem o item do estoque.
- Toda tela abre a mesma janela "Documentos", com "Gerar documento" e "Anexar documento" juntos; só a O.S. tem a mais a parte da aprovação do cliente.
- Pela lista de Evidências e pelas Pendências, a O.S., a O.P. e o pedido de venda abrem essa mesma janela (antes só o "Gerar documento"), e a avaliação de calibração abre com as evidências.
- Inspeção de recebimento ganhou o "Gerar documento", com as TAGs da inspeção (número, nota fiscal, fornecedor, quem decidiu, data e hora da decisão e os itens).
- Itinerário: o botão de documento saiu.
- "Ver TAGs" do cadastro de modelos mostra as mesmas TAGs da janela do registro.
- "Documentos" (anexar e gerar) também na Não conformidade, Programa de auditoria, Auditoria interna, Análise crítica, Submissão regulatória, Atividade de vigilância, Usabilidade, Histórico de projeto (DHF), Recall, Mudança (ECN) e Arquivo de gestão de risco (RMF).
- Evidências: linha sem arquivo mostra "sem documento atual (ver Versões anteriores)" no lugar de "Não definido".
- Modelo de documento: excluir pede o motivo, e a versão de um modelo que já gerou documento não pode ser trocada.
- Modelo de documento novo ou com revisão nova só entra no "Gerar documento" depois de aprovado com assinatura; os que já existiam continuam gerando, com a marca "Aprovação pendente".
- Dossiê regulatório: mostra a data da assinatura, o código inteiro e o botão "Abrir versão" (só para ver).
- Distribuição de documentos: no alto, "⌕ Selecionar documento", "↗ Documento" e "⌕ Selecionar responsável da linha" escolhem em janela o documento e a pessoa (o texto livre continua valendo).
- Distribuição: recusa revisão como "2.5" com frase clara, mostra "Removido por … em …" e guarda linha por linha (a linha tirada fica marcada).
- Histórico de Auditoria: os filtros "Ação" e "Formulário" não encolhem mais depois de filtrar, e a lista avisa quando parou nos registros mais recentes.
- "Verificar integridade" usa as mesmas frases do site, fica registrado no Histórico e diz quantas linhas ficaram fora da conta; na lista do RMF o botão se chama "Verificar".
- Histórico de Auditoria: botão "⬇ Exportar" para planilha (até 5.000 linhas, com aviso).
- Política de retenção: salvar grava só a linha que mudou e avisa se outra pessoa mexeu na mesma linha.
- Política de retenção: linha nova "Validação de processos" e cartão "Cópia de segurança dos dados", só para ver, com a última cópia e o último teste de restauração (hoje mostra "Sem registro").

### Qualidade

- "Não conformidade" / "⚠ Abrir NC" na O.S., na O.P. e na unidade DHR, com NC já aberta, pergunta "Abrir NC …", "Nova não conformidade" ou "Voltar".
- O.S. e Reclamação mostram o número ligado no botão ("⚠ Reclamação 2/26" e "🔧 O.S. 12/26").
- NC aberta pela reclamação mostra "Reclamação de cliente 1/26" e o botão "Abrir registro".
- CAPA: "↗" no "Nº Ação corretiva" da Reclamação e da Avaliação de calibração; "Abrir CAPA" no alto da NC; achado da auditoria com CAPA pergunta "Abrir a CAPA?".
- Reclamação: "A situação X pede: …" com um aviso só; NC, CAPA e Recall dizem "Pedido para encerrar."; a trava do instrumento e o erro da avaliação de calibração ficam escritos na janela.
- Histórico de Auditoria: a coluna "Campo" mostra o nome do campo e a "Origem" vem por extenso ("Portal Web", "Aplicativo Windows", "Outro sistema").
- Nomes por extenso: "DMR (registro mestre do produto)", "Histórico de projeto (DHF)" e "Arquivo de gestão de risco (RMF)".

### Geral

- Alterar regras dos campos: trocar SIM por NÃO avisa que o campo deixa de ser obrigatório em todas as etapas.
- O "Salvar" não acende mais sozinho ao abrir uma tela sem mexer (vale para todas as telas de cadastro).
- Pedido de venda, O.P. e O.S.: "🗑 Excluir" na lista, só para administrador; sem nada ligado exclui com motivo, com algo ligado só arquiva.
- "Mostrar arquivados e excluídos" na lista; "↩ Desarquivar" e "↩ Restaurar" trazem o registro de volta, com os itens e o financeiro do pedido.
- Central de notificações em janela própria: ao fechar, a pessoa volta para onde estava; clicar no balão do Windows abre o aviso.
- "Abrir" do aviso de Treinamento, CAPA, PMS, Auditoria e POP abre o próprio registro; ao abrir pelo Kanban ou aviso aparece "Aguarde, carregando os dados...".
- Salvar não fecha mais o Pedido de venda, a Entrada, a Saída e a Solicitação ("✓ … salvo(a)."); o que foi aberto pelas Pendências volta para elas, atualizadas.
- Estrutura do produto, Recurso e Modelo do produto: botão "🔗 Vínculos"; no Itinerário, "🔗 Vínculos da etapa".
- DMR: "↗ Estrutura do produto" no alto; Característica técnica, Lista de peças e Solicitação do estoque: "↗" ao lado do Modelo do produto.
- Mensagens sem termo técnico: as falhas dizem o que houve e o que fazer; "Download", "Upload" e "Logout" em português; acentos corrigidos.
- "CEP não encontrado. Preencha manualmente." e outras frases certas não viram mais "Registro não encontrado"; recusa aparece com o título "Atenção".
- Central de notificações: prioridade "Crítica / Alta / Média / Baixa", "Visto", "Há 1 dia" e o texto do "Adiar" corrigido.
- "Filtrar período" das listas não trava mais enquanto as datas mudam.
- Programa mais leve: com tudo funcionando, confere a conexão a cada minuto (era a cada 15 s) e não consulta nada com todas as janelas minimizadas.
- Pedido de venda, O.S. e O.P.: depois de alterar o cliente pelo "Ver cliente" e fechar o cadastro, o pedido/ordem já mostra o nome, CPF, CNPJ, telefone e e-mail novos, sem sair da tela e sem ficar com alteração por salvar.
- Avaliação do certificado de calibração: com o critério PERCENTUAL ou ABSOLUTA, as colunas "Limite mínimo" e "Limite máximo" aparecem com a faixa calculada pela tolerância (ex.: 4,9 com 10% → 4,41 a 5,39), só para ver, com o fundo do Erro; no critério LIMITES continuam digitadas.
- Dossiê regulatório: o "Abrir" de cada peça (Modelo do produto, DMR, RMF, DHF, Validação de processos e de software, Usabilidade, Submissão regulatória, PMS) e o "+ Cadastrar modelo" abrem numa janela própria, por cima do dossiê; ao fechar, o dossiê continua no mesmo modelo e o índice é atualizado (antes o dossiê fechava e, ao fechar a peça, ia para a tela inicial).
- Saídas e Entradas de material → "Pendências" → "Abrir solicitação": ao fechar a solicitação, a janela Pendências volta sozinha, atualizada, no mesmo ponto (antes ela não voltava).
- "🔗 Vínculos": o "Abrir" abre o registro por cima e a janela Vínculos continua aberta embaixo; ao fechar o registro, a pessoa volta para a lista de vínculos (antes a janela Vínculos fechava).
- Menu: trocar de tela com alterações não salvas e escolher continuar editando agora deixa a pessoa na tela de antes, com o que foi digitado (antes a tela nova abria mesmo assim e a de antes ficava escondida atrás, sem como voltar).
- Recurso de outro plano (conta Grátis): todo botão barrado pelo plano abre o mesmo aviso, "Este recurso faz parte do plano X" (o plano certo, da tabela de planos do Stand PRO), com "Fazer upgrade" e "Fechar" — no "✚ Novo" das listas, na ordem nova (O.S./O.P.) e nos atalhos que criam ordem, no limite do plano Grátis e nas telas que exigem um plano mínimo. Quem ainda pode testar o Profissional lê a oferta dos 7 dias grátis; colaborador lê para pedir ao responsável e só tem "Fechar" (antes: "Conheça o módulo" e "Criar ordens no plano Profissional", com nomes de plano escritos no programa — alguns ainda diziam "Básico", que saiu da venda).
- "Fazer upgrade" abre a Assinatura por cima da tela, numa janela própria com "✕ Fechar" (e Esc); a tela de baixo fica como estava. O "Ver planos" da faixa "Limite de colaboradores excedido" também abre por cima.
- Plano de fundo: a janela "Escolha o seu plano de fundo" (a mesma do site: 8 destaques, "Ver todos os fundos", "Pular" e "Usar este fundo") aparece uma vez por pessoa depois de entrar, só para quem nunca a viu em nenhum aparelho (site, celular ou outro computador); fechar guarda isso no Stand PRO e ela não aparece mais até a próxima novidade da galeria.
- O responsável pela conta entra mesmo sem ter confirmado o e-mail; fica o aviso "Confirme o seu e-mail" nas notificações até o código ser digitado.
- O "Abrir" desse aviso abre a janela do código, e a janela do código depois do cadastro ganhou "Entrar agora e confirmar depois".
- "Centro de Atenção" agora se chama "Avisos e pendências" (tela inicial, menu e mensagens).
- Textos: "Log de Importação" virou "Relatório da importação", as datas aparecem como "dd/mm/aaaa", "UTC" virou "horário universal" e a Assinatura fala em "troca de plano".
- Duas pessoas no mesmo registro: quem salva por último recebe "Este registro foi alterado por outra pessoa…" em Competência, Treinamento, Matriz, Atividades e Relatórios de vigilância, Equipamento e Avaliação de calibração, Distribuição, Especificação, unidades do Recall, Histórico de lote e de série, Programa de auditoria, Política e Itinerário.
- Quando a leitura falha, a tela mostra o aviso de falha em vez de "vazio" ou "não encontrado" (Competência, Matriz, DHR, Recall e Histórico de versões).
- Senha errada na janela de assinatura fica registrada no Histórico como "Assinatura rejeitada"; na terceira a janela fecha.
- Lista que parou no limite avisa no contador ("mostrando os 1.000 mais recentes — use o Filtrar período para ver os mais antigos"), e o "Filtrar período" passa a existir em Competências, Treinamentos, vigilância, Tecnovigilância, Revisão de risco, Inspeção de recebimento, Histórico de lote e de série e DHR.
- A busca das Saídas acha por destino e por número de série, e a do Histórico de série acha pela série.
- Os avisos de auditoria, treinamento e vigilância chegam para quem tem a permissão da própria tela (antes só para quem tinha a da CAPA); auditoria "Em execução" atrasada também avisa.
- Permissões: a Política aparece para quem tem a da Análise crítica, as evidências da calibração aceitam a permissão da Avaliação, e o botão "Assinaturas" diz "Você não tem permissão para consultar este registro." quando é o caso.

### Novos campos

- O bloco "Novos campos" é o mesmo em todas as telas, e no registro novo o modelo já vem escolhido quando a empresa só tem um.
- Análise crítica, Solicitação do estoque e Avaliação de fornecedor ganharam o bloco "Novos campos".
- Não conformidade, Programa de auditoria, Auditoria interna, Submissão regulatória, Risco, Tecnovigilância, Recall e Mudança (ECN) também ganharam o bloco "Novos campos".
- Dentro do bloco aparece a seção "Campos padrão", com campos que já vêm prontos (não obrigatórios, com TAG): 10 na NC, 4 na CAPA (verificação da eficácia), 3 no Programa de auditoria, 2 na Auditoria interna, 8 na Tecnovigilância, 5 no Risco, 7 no Recall, 3 na ECN e "Responder até" na Submissão.
- TAG customizada: o "Se vazio, usar" vale em todos os formulários (fora do pedido de venda, O.P. e O.S., escolhe-se outro campo do mesmo documento).

### Qualidade — não conformidade, CAPA e reclamação

- Depois de criar, a tela mostra o número definitivo (NC, CAPA, Reclamação, Atividade e Relatório de vigilância, Revisão de risco, Competência, DHF, RMF, ECN e Recall) e usa esse número nos Documentos.
- NC fechada, CAPA encerrada, auditoria concluída e análise crítica concluída abrem só para consulta.
- Salvar a reclamação não troca mais o número por "Não aplicável", salvar a NC não apaga o número da CAPA ligada, e as datas antigas da NC e da CAPA aparecem (data vazia fica vazia, não vira hoje).
- CAPA: o Salvar logo depois de "Gerar CAPA" funciona, abrir a CAPA não troca o Emitente, e a lista de ações corretivas é ordenada pela data de verdade.
- "📋 Copiar dados" só aparece com o registro salvo (NC, CAPA, Programa, Auditoria interna, Competência e POP), e o "Gerar CAPA" fica apagado quando a NC já tem CAPA.
- Listas de NC, Auditoria interna e Análise crítica com a caixa "Todos os status"; a "Lista de ações corretivas" com o desenho acertado.
- Reclamação: a "Reportabilidade" começa em branco e é pedida para concluir ("Informe a reportabilidade antes de concluir.").
- Reclamação: o botão mostra o que está ligado ("🛡️ Tecnovigilância 4/26", "⚠️ NC 8/26"), e "Gerar Tecnovigilância" pergunta "Abrir …", "Nova tecnovigilância" ou "Voltar" quando já existe uma.
- Reclamação concluída só oferece "Em investigação" e "Concluída"; o Cancelar ao lado do "Nº Ação corretiva" virou o sinal "⊘".
- Reclamação: marcar ou desmarcar "Reportável" pede a assinatura.
- Reclamação ganhou "🔗 Vínculos" e "Ver cliente"; o cadastro do Cliente ganhou "🔗 Vínculos".
- "Preparar recall" na NC e na CAPA pergunta "Abrir …", "Novo recall" ou "Voltar" quando já existe recall.
- CAPA: "🔗 Vínculos" mostra as reclamações que apontam para ela, e a tela avisa (sem impedir) quando a única ação é treinamento.
- NC: a disposição "Concessão" ou "Usar como está" pede justificativa e assinatura de quem autorizou; nova disposição "Devolver ao fornecedor".
- NC: o rótulo virou "Quarentena?", e a quarentena vale também por número de série (a Saída de material recusa a série em quarentena).
- Reclamação: o botão "Recall" confere a permissão do Recall.

### Qualidade — auditoria, análise crítica e Política

- Auditoria interna nova começa com a "Data execução" vazia, e a CAPA do achado aparece na grade como "CAPA 22/26", sem ser criada em dobro num segundo clique.
- Programa de auditoria: "🔗 Vínculos" e "Auditorias internas" mostram as auditorias do programa, e a auditoria mostra o programa.
- Auditoria interna: a área auditada vem da lista de setores, a tela avisa quando o auditor líder é do setor auditado, a CAPA gerada pelo achado leva descrição, requisito e evidência, e a grade de achados mostra a situação da CAPA.
- Análise crítica: os indicadores usam a mesma conta do site e são recusados se forem de outro período ("Puxe os KPIs novamente para o período informado.").
- Análise crítica: "Anual / Semestre / Trimestre" e "Programada / Em andamento / Concluída" por extenso (também na ata em PDF), dois cliques no indicador abrem os registros contados, pauta "Notificações às autoridades" com dois indicadores novos e atalho para a análise anterior.
- Análise crítica: objetivo da qualidade ligado ao indicador pelo nome, com quadro de andamento, e aviso de análise próxima ou atrasada na Central, com "Abrir".
- Política da Qualidade: com rascunho aberto dá para ver a versão vigente e a lista de versões, e a tela diz qual versão vale; a data antiga do Representante volta a aparecer.

### Qualidade — POP, treinamento e competência

- POP: número obrigatório, maior que zero e sem repetir; só aprova com Word ou PDF e, ao aprovar, diz quantos treinamentos abriu ("POP aprovado. 3 treinamentos pendentes abertos.").
- POP: coluna "Situação" na lista, aviso antes de abrir arquivo de revisão obsoleta e "Histórico de versões" com as revisões obsoletas.
- "🔗 Vínculos" no POP e na Competência, "↗ POP" na Competência e "↗ Competência" no Treinamento; a Competência só oferece POP em revisão vigente.
- Treinamento: não aceita data no futuro nem eficácia "Não aplicável" sem evidência, e revogar ou desfazer a revogação pede o motivo.
- Alertas de treinamento: "↗ Abrir treinamento" (e dois cliques), caixa "Buscar" e coluna "Setor".
- Matriz de competência: usa os setores da empresa, pergunta antes de fechar com mudança por salvar, e o "🧩 Matriz" só aparece para quem tem a permissão de Competências.
- Matriz de competência: aba "Pessoas", com Apto / Falta / Vencido de cada um.

### Qualidade — pós-mercado, recall e rastreio

- Tecnovigilância: campo novo "Soube em", prazo em dias corridos contado dele e seis opções de gravidade (a de 72 horas se chama "Óbito").
- Tecnovigilância: situação "Avaliado — não notificável" com justificativa e assinatura; a notificação reportada ou encerrada fica travada.
- Tecnovigilância: não diz mais "gerado" quando a gravação foi recusada e mostra a reclamação de origem certa.
- Atividade de vigilância: "Concluída" pede data de execução e resultado; tipo novo "Assistência técnica (O.S.)".
- Relatório de vigilância: o PDF é gerado de novo antes da assinatura, e a tela avisa quando o conteúdo mudou depois do PDF.
- Revisão de risco pós-mercado: aprovada com a ação "Abrir CAPA", oferece "Gerar CAPA" (a CAPA abre já preenchida) e ganhou o botão "Gerar CAPA" no alto; período e próxima revisão passam a ser datas.
- O "Excluir" sai das listas de Revisão de risco e de Submissão regulatória; no RMF, na Usabilidade e no DMR só sai o rascunho nunca aprovado, com o motivo.
- Recall: unidade sem cliente do cadastro é acompanhada pelo destino escrito na saída; a busca é pelo lote exato e avisa quando o lote existe em mais de um produto.
- Recall: cancelar e reabrir pedem motivo e assinatura; cada unidade abre a saída e o DHR ("↗"); campo "Produto do lote afetado".
- Rastreio reverso: colunas "Cidade" e "Telefone" do cliente, linha "Consumido na O.P. …" com os produtos feitos, "↗ Abrir saída" e "↗ Abrir DHR", e limite de 10.000 linhas.

### Metrologia, inspeção e fornecedor

- Equipamento de medição já avaliado abre com as datas gravadas (antes mostrava hoje), e "Equipamento utilizado" devolve o número do instrumento.
- Equipamento de medição: "🔗 Vínculos" (O.P., O.S. e avaliações), motivo para retirar de uso, próxima calibração recalculada ao mudar a periodicidade, e instrumento obsoleto não recebe avaliação nova.
- Avaliação de calibração: pede assinatura, a coluna que não é do tipo do ponto vira "não se aplica", "↗ Equipamento" no alto e os títulos "Tolerância absoluta" e "Necessário o registro da ação corretiva?".
- Registrar leitura de armazenagem: coluna "Não conformidade" na grade e botão "🔗 Vincular não conformidade"; a NC da leitura fora da faixa já nasce com a leitura de origem.
- Inspeção de recebimento: trocar NQA, nível ou regime refaz o plano de amostragem, e a inspeção de entrada antiga abre com a entrada.
- Inspeção de recebimento: número dado na gravação, regime trocado à mão pede justificativa, "⌕ Escolher não conformidade" (entre as NCs em quarentena), "↗ Entrada" e "↗ Fornecedor".
- Avaliação de fornecedor: conclui num passo só (classe pela nota certa e próxima reavaliação pela classe nova); o Master aprova a aprovação condicional; "📊 Avaliações" abre pelo fornecedor certo.
- Fornecedor: "Em observação" por extenso, telefone em branco grava vazio, classe de risco só muda pela Avaliação de fornecedor, e documento que vence não aceita "Sem validade"; a Avaliação ganhou "↗ Fornecedor".
- Entrada de material sem pedido e Pedido de compra novo: fornecedor inativo é recusado, e fornecedor com pendência (bloqueio, reavaliação ou documento vencido) abre a janela do motivo.

### Engenharia e produção

- Modelo do produto: a rotulagem só vira "Vigente" ou "Obsoleta" com a assinatura.
- RMF: o modelo de um RMF já salvo não muda, a lista ganhou busca e "Colunas", e a ficha mostra a grade "Riscos deste RMF", com "↗" em cada risco.
- Risco: "🔗 Vínculos" (diz em qual RMF entrou), e o risco "Pendente de aprovação" aprova sem precisar mexer em campo.
- DHF: o que foi digitado não some ao abrir Entradas, Saídas ou Revisões; a liberação e o PDF vêm iguais aos do site.
- DHF: "⌕" e "↗" ao lado dos campos de ligação (a fonte da entrada é escolhida em janela), aprovar entrada de projeto pede assinatura, aprovar o DHF lista o que falta, e a ficha ganhou "Verificar integridade".
- Validação de processo e de software: "⌕" e "↗" nos campos de ligação, "🔗 Vínculos" no Processo, aviso "Revalidação necessária" quando o software validado muda, e a validação reprovada pode ser concluída, com assinatura.
- Usabilidade: botão "Assinaturas".
- Mudança (ECN): o Solicitante já vem com quem está usando, e o impacto ganhou o "⌕" que aponta o registro afetado, com "Abrir".
- Mudança (ECN): rejeitar pede motivo e assinatura, o impacto aceita as áreas DMR, Especificação e Estrutura, e a ficha ganhou "🔗 Vínculos".
- DMR: "⌕ Selecionar documento" e "↗ Documento" para a linha marcada, "🔗 Vínculos" e "🗑 Excluir" do rascunho nunca aprovado, com motivo.
- Especificação técnica: situação ("Em uso", Vigente, Obsoleta, Rascunho), "✅ Aprovar (tornar vigente)", "✍️ Assinaturas", "📜 Versões", "🔗 Vínculos" e colunas "Revisão" e "Situação" na lista; a aprovada fica travada.
- Estrutura do produto: rótulo "Produto (item do estoque) *"; Recurso: campo "Equipamento (manutenção)" com a próxima manutenção ou "Manutenção vencida desde…", e aviso de manutenção vencida na Central.
- Itinerário: ao salvar com etapa em uso excluída ou renomeada, pergunta "A etapa X está em N estrutura(s). Salvar mesmo assim?"; se outra pessoa salvou antes, avisa e nada é apagado.
- Lista de peças: a linha em branco é pulada e a "Baixa de estoque" é mantida.
- DHR: "Aguardando Liberação" em amarelo e "Em Quarentena" em vermelho, "🔗 Vínculos", "↗" para a O.P., dois cliques no componente abrem o histórico do lote ou da série, e o DHR de lote mostra lote e quantidade.
- O.P.: botão "✍️ Assinaturas" (igual ao da O.S.).
- O.P.: a liberação da Qualidade passa a ser por unidade — libera as sem pendência, marca "Sucateada" a de NC fechada como sucata e deixa retida a que tem pendência.

### Estoque

- Pendências de Saídas e de Entradas: caixa de busca no alto, e a seta para baixo/para cima marca a linha.
- Pendências da Saída mostram "falta entregar" por item (O.S. e O.P.); Pendências da Entrada mostram os pedidos de compra a receber, com "↗ Abrir origem".
- Saída de material: o "..." do destino abre a pesquisa de clientes e o "↗" abre o cliente (o texto livre continua valendo).
- Saída de material: "↗" da origem do lote; os Vínculos do item mostram "falta entregar N".
- A janela do produto na Reclamação, na Solicitação do estoque, na Saída de material e na Saída de máquina nova lista só os itens "04 - Produto acabado" (as peças continuam todas).
- Histórico de lote e de série: a ficha do movimento ganhou "🔗 Vínculos", e a NC do lote ou da série aparece no histórico.
