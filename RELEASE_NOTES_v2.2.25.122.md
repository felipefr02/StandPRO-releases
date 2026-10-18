## v2.2.25.122 (2026-10-18) — Plano de fundo, Kanban com pedidos de venda, prazos e indicadores, colunas das listas, convite do ambiente e fornecedor com CPF e CNPJ

### Kanban

- Novo Kanban do Pedido de venda: na lista de Pedidos de venda aparece "Lista | Kanban". As etapas do pedido se configuram em "Configurar etapas", como as da O.S. e da O.P.; a caixa "Mostrar entregues" mostra ou esconde a última etapa.
- Kanban da O.P.: nova coluna "Pedidos de venda" antes da primeira etapa, só para consulta, com os pedidos ainda não entregues. O cartão mostra a etapa do pedido, o cliente, o produto vendido e as O.P. ligadas. Clicar numa O.P. abre a O.P.; clicar no cartão abre o pedido. Só aparece para quem tem acesso aos pedidos de venda.
- Novo botão "Indicadores" no quadro da O.S. e da O.P. (só consulta): escolhendo o mês, mostra o tempo médio e o maior tempo por etapa, quantos cartões ficaram dentro do prazo e os "Atrasados agora". Dois cliques num atrasado abre a ordem.
- "Configurar etapas": nova coluna "Tempo máximo (prazo)", em dias ou horas (de 1 hora a 365 dias). Em branco, a etapa fica sem prazo.
- Etapa com prazo: o tempo do cartão na etapa vira uma etiqueta verde (dentro do prazo), amarela (a partir de 75% do prazo) ou vermelha (passou do prazo). Passando o mouse aparece há quanto tempo o cartão está na etapa e qual é o prazo.
- O tempo na etapa soma todas as vezes que o cartão passou por ela: se ele sai e volta, a contagem não zera (vale também para o histórico antigo). A dica mostra "somando N entradas".
- Novo filtro da semana, na O.S. e na O.P.: "Todas as semanas", "Esta semana", "Semana passada" ou "Escolher a semana…". Vale a semana (de segunda a domingo) da data da ordem.
- Barra de rolagem fina embaixo do quadro e nas colunas; as colunas agora vão só até o último cartão. A roda do mouse em cima do fundo do quadro não rola mais para o lado: para o lado, use Shift, a roda de lado ou a barra de baixo.
- Configuração do Kanban › Automações: novo campo "Quando acontece". Além de "Ao entrar numa etapa", na O.S. há "Quando o cliente aprovar a proposta" e "Quando o cliente reprovar a proposta", que avisam as pessoas escolhidas.
- A mensagem das automações aceita campos dos Novos campos pela TAG, por exemplo {{@W01V}}.
- "O que falta para mover": o nome da seção aparece como título maior, e o nome do campo não repete mais o nome da seção.

### Plano de fundo e aparência

- Novo botão "Plano de fundo" ao lado da lua, no alto da tela principal. A janela tem 37 imagens (Natureza, Abstratos, Técnico e Cores), "Sem fundo", "Usar uma imagem minha…" e "Tirar minha imagem".
- Quatro réguas ajustam o visual: "Força da imagem", "Painéis opacos", "Desfoque atrás dos painéis" e "Menu e cabeçalho opacos". Cada mudança aparece na hora e é guardada sozinha.
- A escolha é de cada pessoa e vale em qualquer computador e também no site.
- A imagem aparece atrás do menu, do cabeçalho, da tela inicial, do Kanban, das listas e de todas as telas abertas dentro da janela principal. Janelinhas e avisos continuam como antes.
- Com imagem escolhida, painéis, colunas e cartões ficam arredondados e translúcidos, as faixas de cima e de baixo vão de ponta a ponta e os botões ficam na cor de cartão. Sem imagem, nada muda.
- O título do cabeçalho fica no meio do espaço livre da barra, mesmo com o menu aberto.

### Listas

- Novo botão "Colunas" no alto de todas as listas (menos as da O.P. e da O.S., que já tinham o "Colunas" da empresa). Cada pessoa escolhe, só para ela, quais colunas aparecem; "▲ Subir" e "▼ Descer" mudam a sequência e "Voltar ao padrão" desfaz tudo. A largura muda arrastando a borda do título na própria lista. O ID aparece sempre, e a busca procura nas colunas que aparecem.
- O "Status" das listas de O.S., O.P. e Pedidos de venda ganhou a cor da etapa do Kanban: o selo inteiro na cor, com letra preta ou branca para ler bem.
- A lista de Pedidos de venda ganhou a coluna "Status", e a busca também acha pelo Status.

### Aprovação do cliente (O.S.)

- A janela foi reorganizada em blocos: "1 · Proposta em PDF", "2 · Link para o cliente" e "Histórico dos pedidos". No alto, uma etiqueta colorida diz a situação: Esperando o cliente (amarela), Aprovada (verde), Reprovada (vermelha) ou cinza (Link vencido, Proposta mudou, Sem pedido, Sem proposta).
- Novo botão "🔄 Atualizar proposta" no passo 2: gera o PDF de novo com o modelo escolhido e renova o pedido num clique. O cliente usa o mesmo link e já vê a proposta nova.
- Uma frase no passo 2 diz o que fazer agora (mandar o link, atualizar a proposta ou pedir a aprovação).
- Ao gerar a proposta ou pedir de novo, a janela confere antes a situação mais recente: se o cliente acabou de reprovar, ela já sabe.
- "Pedir aprovação do cliente" só liga quando já existe o PDF da proposta.

### Fornecedor

- CPF e CNPJ agora são dois campos separados no cadastro do fornecedor, como no cadastro de clientes. Os dois ficam guardados.
- Trocar a Natureza (física ou jurídica) não apaga mais nada: ela só decide qual dos dois aparece primeiro e é cobrado; o outro aparece ao lado, com "(fica guardado)", quando já tem número.
- Novo bloco "Documento do exterior" (tipo e número do documento), só para fornecedor de fora do Brasil; o padrão é "Nenhum (fornecedor do Brasil)". Preenchido, é esse documento que sai no pedido de compra, e o CPF/CNPJ deixa de ser cobrado.
- O documento principal do fornecedor (o das listas e dos documentos gerados) é montado sozinho: o do exterior, se houver; senão o CPF (pessoa física) ou o CNPJ (pessoa jurídica).
- Ao salvar, os avisos dizem o que falta, por exemplo "Confira o CPF do fornecedor." ou "Escolha o tipo do documento do exterior, ou apague o número."
- Fornecedores antigos: o número que estava no campo único passa para o CPF ou para o CNPJ certo. Zeros, traços e campos vazios contam como sem documento.

### Convite para o ambiente

- Novo botão "Convidar para o ambiente", no alto da tela principal, à esquerda do plano de fundo. Ele dá um link para mandar a quem vai começar a usar o Stand PRO: a pessoa só cria a conta, sem digitar o nome do ambiente, e espera o Master liberar o acesso.
- "Copiar link" copia o link. O Master pode "Gerar outro link"; o anterior para de funcionar.
- Link com função: escolha a função de quem vai entrar, digite a sua senha para confirmar e clique em "Gerar link". O link vale para 1 pessoa, vence em 7 dias e a pessoa já entra liberada. Em "Escolher depois (o Master libera)" vale o link de sempre.
- Se o plano estiver sem vaga para mais uma pessoa, a janela avisa antes de mandar o link. No plano Grátis ela só explica que é preciso mudar o plano.
- O Master recebe o aviso "Conta nova esperando liberação"; clicar nele abre o cadastro da pessoa, para escolher o setor e liberar o acesso.

### Documentos

- Nova TAG @DFO nos modelos Word do pedido de compra: escreve o documento do fornecedor já com o nome na frente ("CNPJ: …", "CPF: …" ou o do exterior). O modelo não precisa mais ter "CNPJ:" digitado antes da TAG.
- A TAG @CPF continua saindo como antes (só o número). A @DFO aparece na lista de TAGs do pedido de compra.

### Estoque e histórico

- Histórico de lote e de número de série de uma O.P. ou O.S.: o "Abrir" mostra só para consulta. Lote e série de ordem não se corrigem por ali, como no site.
- Lote ou série que já teve saída: a mensagem agora diz "Já existe saída desses itens. A rastreabilidade da entrada só pode ser corrigida enquanto nenhum item tiver sido baixado." A frase antiga sugeria corrigir datas e garantia, o que não era permitido.

### Treinamento

- Alertas de treinamento: o resumo (vencidos, a vencer em até 30 dias e pendências de ação) e a lista agora usam o mesmo cálculo do site, então os números e as linhas são iguais nos dois lugares.
- Quem ainda não tem um treinamento obrigatório da matriz de competência aparece na lista como "Sem treinamento obrigatório".
- Sem alertas, a lista diz "Nenhum alerta encontrado nesta consulta."; se os números não fecharem com a lista, a tela pede para atualizar.

### Conta e planos

- Na conta Grátis (plano sem O.S. e O.P.), o "Novo" das listas de O.S. e O.P., o "Copiar para novo", o "Gerar ordem de produção" do Pedido de venda e o botão da O.S. na Reclamação de clientes avisam antes de abrir o formulário.
- O Master que ainda pode testar vê "Ativar 7 dias grátis" do plano Profissional (sem cartão e sem renovação automática); quem já testou vê "Ver planos"; os outros usuários são orientados a pedir ao responsável pela conta.

### Correções

- Faixas das seções dos Novos campos (por exemplo na O.P.) agora acompanham a troca de tema; no tema escuro apareciam brancas.
- Central de notificações: no tema escuro a lista abria com faixas claras.
- Item do estoque: as dicas dos botões de copiar estavam trocadas ("para dados de venda" e "para dados da compra").
- O aviso de cópia mostra "✓ Dados copiados para um novo registro" (antes aparecia um "?").
