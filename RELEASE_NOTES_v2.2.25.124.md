## v2.2.25.124 (2026-10-24) — Telas regulatórias como no site, Kanban com filtro por técnico, lembrete do prazo e campos por etapa, Kanban do pedido de venda completo e um documento vigente por modelo

### Kanban

- Janela "Indicadores": novo "Filtrar por". Escolha um campo da ordem (por exemplo, o técnico) ou um Novo campo em "Novo campo…" e depois o valor, numa janela com busca que mostra quantos cartões do mês têm cada valor ("(em branco)" para os vazios).
- Com um valor escolhido, o tempo por etapa, o "Dentro do prazo" e os "Atrasados agora" passam a contar só esses cartões (pelo valor que a ordem tem hoje). "Escolher…" troca o valor e "Limpar" volta a todos os cartões.
- "Configurar etapas": novo botão "⏰ Lembrete…" e nova coluna "Lembrete do prazo" (dois cliques também abrem). Marcando "Lembrar quando passar do prazo", o aviso sai quando o cartão passa do prazo e se repete a cada intervalo escolhido (de 1 hora a 30 dias) até ele sair da etapa; ordem encerrada não recebe.
- Na janela do lembrete você escolhe "Quem recebe o lembrete" e, se quiser, a mensagem, com {{controle}}, {{cliente}}, {{etapa}}, {{modelo}}, {{serie}} e os Novos campos pela TAG (ex.: {{@W01V}}). Em branco, vai uma mensagem com o prazo e o tempo na etapa. O lembrete só vale em etapa com prazo e depois de salvar as etapas.
- "Requisitos da etapa" ganhou três botões: "Campos nativos", "Campos customizados" e "Seções". Nos dois primeiros, uma tabela "Obrigatório nesta etapa?" com Não ou Sim para cada campo, com "Buscar campo" quando a lista é longa; "Sempre (regra dos campos)" mostra o que já é obrigatório em todas as etapas pela tela "Alterar regras dos campos".
- Na tela da O.S. e da O.P., o campo que a etapa atual pede para avançar fica marcado como obrigatório: rótulo vermelho com "*", a aba com "*" e a frase "A etapa "…" pede este campo para avançar.". Os campos cobrados por uma troca de etapa recusada também ficam marcados. O "Salvar" não cobra esses campos; quem cobra é a troca de etapa.
- O quadro do Pedido de venda agora tem "Indicadores", "Campos do cartão", "Automações" e "Requisitos da etapa", como a O.S. e a O.P., e o "O que falta para mover" também vale para ele. No pedido, a automação só avisa ("Notificar usuários ou setores").
- "Campos do cartão" do pedido: o título do cartão é sempre o número do pedido. Desligado, o cartão mostra o de sempre: cliente, data do pedido, entrega, valor e O.P.
- O tempo do cartão na etapa conta minutos ("25 min"), depois horas e depois dias, também nas etapas sem prazo: o cartão que acabou de entrar não aparece mais como "hoje". A dica diz, por exemplo, "Nesta etapa há 25 minutos".
- "Acompanhamento e comentários": com mais de 12 pessoas, aparece uma busca "Buscar pelo nome" em cima da lista de menções. Quem já foi marcado continua marcado, mesmo quando a busca o esconde.

### Ordens de serviço e de produção

- O.P.: a janela de escolha do pedido de venda ganhou a coluna "Itens" (código — descrição (quantidade), até 8 itens e "e mais N"). O pedido mais novo vem primeiro, e a busca também acha pelos itens.
- O.P.: uma moeda por ordem também ao trazer a estrutura do produto. Ordem sem itens, ou trocando os itens pelos da estrutura, fica na moeda da estrutura; se a moeda for diferente, aparece o aviso "Moedas diferentes no mesmo documento" e nada entra na ordem.
- Novos campos: o botão "Preencher valores iniciais" agora aparece para todos os usuários, não só para o administrador. Ele preenche só os campos vazios que a pessoa pode editar; criar e editar o modelo continua só para quem tem acesso aos modelos.
- Entrada de material do produto de uma O.P.: a janela dos números de série já abre com os números informados na ordem, para conferir, mesmo com tudo preenchido. Só quando a pessoa ainda não digitou nada; se parte já foi recebida, só quando a quantidade de números é a que falta.

### Documentos

- Gerar documento: novo botão "..." ao lado do modelo. Ele abre a janela "Selecionar modelo de documento", com busca por código, nome ou revisão, os modelos ligados ao produto da ordem primeiro e nenhuma linha marcada sozinha.
- Quando é preciso escolher o modelo na hora de gerar, a pergunta passou a ser essa mesma janela com busca (antes era uma lista sem busca, com a primeira linha já marcada). Cancelar continua não gerando nada.
- Um documento vigente por modelo: dá para gerar, por exemplo, o Laudo e o RHP do mesmo registro, e os dois ficam valendo. A pergunta "Gerar de novo?" só aparece quando já existe documento do mesmo modelo: ele vai para as versões anteriores e o novo fica no lugar, sem mexer nos dos outros modelos.
- "🗂 Versões anteriores": novo botão "🗑 Remover", para tirar o documento vigente de outro modelo. O documento do modelo da tela continua saindo por "Remover documento"; com a ordem encerrada, não dá para remover.

### Janelas de escolha

- "Selecionar proprietário" (O.S. e Reclamação de clientes) e "Selecionar cliente" (Pedido de venda): nenhuma linha fica marcada sozinha, nem ao abrir nem depois da busca. Vale a linha que a pessoa marcar (ou o cliente que a tela já tinha), que continua marcada depois da busca; "Selecionar" fica apagado sem linha marcada, e Enter com um único resultado escolhe ele.
- As outras janelas de escolha de registro, como a do pedido de venda na O.P., seguem a mesma regra: nada marcado sozinho e "Selecionar" só com uma linha marcada.

### Dossiê Regulatório

- O índice das peças passou a ser calculado pela mesma conta do site, e os dois mostram sempre o mesmo índice. Com isso, a peça PMS não dá mais erro, quem só tem acesso ao Dossiê não vê mais GSPR, Rotulagem e UDI com erro, e os resumos ficaram sem termos técnicos.
- "Histórico de snapshots" passou a se chamar "Histórico de versões". Cada versão mostra a situação (Rascunho, Assinada, Cancelada ou Expirada) e a data na hora local.
- Quando "Gerar versão" é recusado, a mensagem explica o motivo, por exemplo "O dossiê só pode ser preservado quando todas as peças estiverem vigentes ou formalmente não aplicáveis.". Depois de "Gerar versão" e de "Histórico de versões", a linha de prontidão volta ao resumo.
- "Copiar índice": a situação geral sai como "PRONTO", "NÃO PRONTO" ou "BLOQUEADO", como na tela, com a mesma hora de avaliação e o mesmo código de verificação do site.
- "Abrir" na linha do DHF abre o DHF aprovado do modelo; sem ele, abre um DHF novo já com o modelo do Dossiê.

### Modelo do produto

- "Data da validade do registro" fica vazia até alguém preencher, com uma caixa de marcar, como a data de liberação da rotulagem. Antes o "Novo" gravava a data de hoje sem ninguém escolher.

### DHF (Histórico de Projeto)

- Lista de DHF: o modelo aparece como "#id — código (modelo)", e "Versão" e "Não declarado" ganharam acento, como no site. A mensagem de exclusão ficou "DHF aprovado ou obsoleto não pode ser excluído."
- Num DHF já salvo, o modelo não pode mais ser trocado, porque a versão é do modelo. Para outro modelo, crie outro DHF.
- "Registrar N/A": o aviso da justificativa N/A vigente mostra a justificativa, a base legal/norma e quem aprovou e quando. Modelo que já tem DHF aprovado não recebe N/A: "Este modelo já tem DHF aprovado. A justificativa N/A é só para modelo sem DHF aprovado."
- Revisões formais: revisão já registrada não pode ser excluída da lista ("Revisão formal já registrada não pode ser excluída. Registre uma nova revisão.").
- Exportar: DHF obsoleto sai como "VERSÃO OBSOLETA — SUBSTITUÍDA POR VERSÃO MAIS NOVA", com a aprovação que teve, e não mais como rascunho.

### Gestão de risco (RMF)

- Os indicadores do RMF (total, alto, médio, baixo e residuais inaceitáveis) passaram a vir da mesma conta do site e da aprovação: o nível de cada risco é o residual, quando houver, senão o inicial. Antes o risco "Pendente de aprovação" ficava fora de Alto, Médio e Baixo. Se não der para calcular, a tela avisa e pede para tentar de novo.
- Revisão de risco pós-mercado: "Abrir RMF do modelo (§10.4)", quando o modelo ainda não tem RMF aprovado, abre um RMF novo já com o modelo da revisão.

### Validação de Processos

- Textos legíveis, como no site: Tipo, Resultado, Causa da revalidação, Papel, Conforme? e Ponto OQ mostram o nome com acento (por exemplo "Revalidação", "Não conforme", "Periódica", "Pior caso"). As listas mostram "Ativo/Inativo", "Validação/Revalidação" e "Conforme/Não conforme".
- A fase da evidência controlada (IQ, OQ ou PQ) agora é escolhida numa lista, em vez de digitada.
- "+ Novo processo" aberto pelo Dossiê já vem com o modelo.

### Validação de Software

- Textos legíveis, como no site: Contexto regulatório ("Software de dispositivo médico", "SGQ / produção / medição"), Abordagem, Tipo, Status, Resultado (agora com "Em avaliação"), Risco do processo, Método de assurance e Conforme?. No cadastro do software, Origem ("Personalizado", "Comercial (COTS)", "SOUP (terceiros)") e Situação; as listas mostram os mesmos nomes.
- "+ Novo software" aberto pelo Dossiê já vem com o modelo.

### Engenharia de Usabilidade

- "+ Novo" com um modelo no filtro (inclusive vindo do Dossiê) abre o arquivo novo já com esse modelo.
- As colunas "Risco vinculado (ISO 14971)" das tarefas e dos cenários oferecem só as análises de risco do modelo escolhido, e trocar o modelo refaz a lista. Uma análise de outro modelo já usada numa linha continua visível, marcada "(de outro modelo)".

### Submissão Regulatória

- "Aprovar (assinar)": antes de pedir a assinatura, a tela confere o que falta no produto e, se faltar algo, mostra "Ainda não dá para aprovar" com a lista ("Antes de aprovar a submissão, resolva: …"). Assim não fica assinatura gravada de uma aprovação recusada.
- "Status do ciclo" com nomes legíveis (Rascunho, Submetido, Exigência, Indeferido); a submissão aprovada mostra "Aprovado (deferido)", e não mais "RASCUNHO".
- Na lista, as colunas de status e de vencimento mostram os nomes legíveis ("Vencido", "A vencer", "Em dia"), com as mesmas cores de antes.
- "+ Nova submissão" com um modelo no filtro (inclusive vindo do Dossiê) já vem com esse modelo.

### Política da Qualidade

- Status legível: "Status: Vigente (versão N, aprovada por …)" ou, por exemplo, "Status: Rascunho (versão N) — não aprovada". O status dos objetivos aparece como "Em andamento", "Atingido", "Não atingido" ou "Suspenso".
- "Aprovar política (assinar)" na versão vigente sem nenhuma mudança agora avisa "Esta versão da Política já está vigente." e não cria uma versão nova igual.

### Criar conta

- Quem começou a criar a conta e parou no código do e-mail pode se cadastrar de novo com o mesmo e-mail e a mesma senha: o cadastro é retomado, o código é enviado de novo e a janela avisa "Você já tinha começado o cadastro com este e-mail. Falta só confirmar: enviamos o código de novo.". Vale o usuário do primeiro cadastro.
- Código errado na confirmação do e-mail: a mensagem agora é "Código incorreto. Confira o código do e-mail mais recente e tente de novo.", porque um código novo pode substituir o anterior.

### Correções

- Controle de distribuição: nenhuma distribuição salvava, porque a data era recusada. Ao abrir uma distribuição, a tela mostrava a data de hoje no lugar da gravada (e um "Salvar" gravaria hoje por cima); agora mostra a data guardada e, se não conseguir lê-la, pede para carregar de novo.
- Gerar planilhas: "Planilha gerada com sucesso." só aparece quando a planilha foi guardada; antes bastava existir uma cópia antiga no computador. Numa falha aparece um aviso só.
- Gerar planilhas: "Abrir" sempre abre a planilha guardada mais recente, também a gerada em outro computador; antes podia abrir uma cópia velha deste computador. Se a planilha já estiver aberta, mostra a mesma; se não der para baixar, avisa em vez de abrir a cópia antiga.
- O.S. e O.P. gravadas voltam na moeda em que foram feitas; antes reabriam em Real (o custo total saía em R$ e a O.S. aceitava peça de outra moeda). "Copiar para novo" também leva a moeda.
- Kanban: "Mostrar etapas ocultas" agora mostra também as etapas que a pessoa escondeu em "Minhas etapas".
- Armazenagem: cores legíveis, iguais às do site. O painel "Alertas" fica vermelho de verdade, e "Dentro da faixa" (que sumia no fundo branco) e "vencido" (rosa-claro) ganharam cor de texto.
- Aviso de vencimento de submissão regulatória: o "Abrir" dava erro; agora abre o cadastro da submissão.
- Modelo do produto: "Copiar para novo" não leva mais o DI (UDI) nem o status da rotulagem; antes a cópia não podia ser salva. A validade do registro é copiada junto com a caixa marcada.
- DHF: em "Saídas de projeto", "Revisões formais" e "Transferência para produção", o aviso de DHF congelado voltou a aparecer (era apagado ao abrir).
- DHF, Revisões formais: a linha já gravada fica travada; se uma linha seguinte for barrada no "Salvar", a primeira não é gravada de novo.
- Validação de Processos: etapa com amostra em branco era recusada no rascunho; agora vai vazia.
- Validação de Software: modelo ou análise de risco que não aparece na lista (apagado ou sem acesso) sumia da tela e o "Salvar" apagava o vínculo; agora aparece como "(não disponível)" e fica guardado.
- Validação de Software: no PDF do FRS, a seta do título "Matriz requisito → função → teste" sumia.
- Dossiê, aba Inspeções: "Fornecedor · NF" não fica mais com " · NF " solto quando falta um dos dois; o duplo clique numa pendência de Entrada de material sem acesso agora avisa (antes não fazia nada); e um pacote exportado com problema mostra uma frase simples, como "O pacote recebido está incompleto. Tente de novo.".
