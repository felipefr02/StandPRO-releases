## v2.2.25.120 (2026-10-14) — Estoque só pela Entrada e Saída de material, série e data de fabricação na O.P. e ordem manual no Kanban

### O que muda no jeito de trabalhar

- A Ordem de produção e a Ordem de serviço não dão mais baixa nem entrada no estoque. Quem tira peça do estoque é a Saída de material, e quem põe o produto pronto é a Entrada de material.
- As peças da O.P. e as peças aprovadas da O.S. ficam esperando a Saída de material; o produto da O.P. fica esperando a Entrada de material desde a criação da ordem. Essas pendências aparecem em Pendências › Estoque ("Solicitação OP", "Solicitação OS" e "Entrada OP") e abrem a Saída ou a Entrada já preenchidas com o que falta.
- Na O.P., o número de série do produto virou um campo de digitar (um número por linha) e a data de fabricação virou um campo da ordem. A O.P. não abre mais janelas de lote e número de série ao salvar.
- No Kanban, os cartões podem ser arrastados para cima ou para baixo dentro da mesma etapa e ficam na ordem escolhida, para todos que veem o quadro. Cartão trazido de outra etapa fica no lugar onde foi solto.

### Ordem de produção

- Lista de peças sem as colunas "Qtd. disponível" e "Depósito". O Salvar não confere mais saldo e a quantidade não fica mais vermelha.
- O depósito do produto saiu do painel Produto: quem escolhe o depósito é a Entrada de material.
- "Nº de série do produto": um número por linha. Com 2 ou mais máquinas, o rótulo mostra "(N, um por linha)" e o campo cresce. Em ordem nova de produto controlado por número de série, é preciso informar um número diferente para cada máquina.
- Saiu o botão "Números de série do produto". Ordem antiga com a série só no histórico mostra essa série no campo, e o próximo Salvar a grava na ordem.
- Novo campo "Data de fabricação" em Detalhes, logo depois da data de conclusão.
- As datas de início, conclusão e fabricação podem ficar em branco (caixinha do campo desmarcada). Ordem nova nasce sem data de conclusão e sem data de fabricação.
- Peça repetida agora é o mesmo código na lista. Ordem antiga que tinha a mesma peça duas vezes continua podendo ser salva enquanto ninguém mexer na lista de peças.
- Novo botão "🧾 Gerar pedido de venda": abre um pedido novo com o produto e a quantidade da ordem; salvo o pedido, a ordem se liga a ele sozinha.
- Novo botão "📎 Documentos" (ver "Documentos da ordem e do pedido").
- "Copiar para novo" não leva os números de série nem a data de fabricação, e passa a levar a ligação do produto e do pedido de venda (antes o pedido mostrado na cópia não era gravado).

### Ordem de serviço

- Lista de peças sem "Qtd. disponível" e "Depósito". O Salvar não confere saldo nem pede lote ou número de série, e a quantidade não fica mais vermelha.
- Novas colunas "Valor unit." (pode ser digitado) e "Desc. %". Total da linha = quantidade × valor unitário − desconto.
- A peça nova vem com o preço de venda do cadastro do item (sem preço de venda, vem zero para digitar). Trocar o depósito ou atualizar a linha não volta mais o valor para o preço do cadastro.
- Nova coluna "Descrição apelido", logo depois da Descrição: é o nome da peça que sai nos documentos da O.S. Vem com o apelido do item (ou com a descrição); apagada, volta a ser a descrição.
- O produto da O.S. é escolhido entre os itens do estoque do tipo "Produto acabado", e a ordem grava o código e o nome do item. Produto acabado sem cadastro de produto também pode ser salvo.
- Proprietário: botão "..." ao lado da lista abre uma janela de pesquisa por nome, CPF/CNPJ, telefone ou e-mail.
- O botão "📎 Evidências" passou a se chamar "📎 Documentos".
- A data de conclusão pode ficar em branco; para fechar a ordem ela continua obrigatória. Ordem nova nasce sem data de conclusão.
- O mesmo item não entra duas vezes na lista de peças. Ordem antiga com item repetido continua podendo ser salva enquanto ninguém mexer na lista.
- "Copiar para novo" não leva o número de série nem o status.
- Corrigido: "Copiar para novo" podia travar ou fechar o programa.
- Corrigido: o custo total abria como "R$ 0" e, salvando sem mexer nas peças, o "R$ 0" era gravado por cima do custo da ordem.

### Ordem de produção e Ordem de serviço

- Ordem nova: o número que aparece ao abrir é uma prévia; o número definitivo é reservado na hora de salvar. Se não der para reservar, nada é gravado e a tela avisa.
- Ordem concluída, fechada ou cancelada: "Documentos", "Gerar documento" e "Acompanhamento e comentários" continuam disponíveis, e a lista de peças pode ser rolada e consultada (sem editar).
- Se as peças ou os itens da ordem não puderem ser lidos ao abrir, a tela avisa e não deixa salvar (salvar assim apagaria a lista gravada).
- Data gravada que não pode ser lida não vira mais "hoje" sem aviso: a tela pede para conferir antes de salvar.
- Excluir uma linha da lista conta como alteração: o Salvar acende e fechar pergunta.
- Ordem que já está aberta vem para a frente quando é aberta de novo pelo Kanban ou por um aviso, em vez de abrir outra janela.
- Depois de salvar uma ordem nova, o "Novo" da lista volta a abrir uma janela em branco.
- Ao concluir, liberar ou fechar a ordem, se faltar requisito da etapa, o aviso lista o que falta.

### Registro da ordem (tela do técnico)

- Registro da O.P.: saiu a aba "2". O que se digitava nela não era gravado; os Novos campos são preenchidos na tela da ordem.
- Corrigido: no Registro da O.P. a caixa "Conforme" não podia ser marcada, e toda conclusão pelo programa saía como não conforme.
- "Liberação bloqueada" lista o que falta quando o motivo é requisito da etapa.
- Registro da O.S.: depois de salvar aparece "✓ Alterações salvas" (ou "✓ Ordem de serviço concluída"), e a ordem concluída ou cancelada abre só para consulta.
- Registro da O.S.: o campo "Observações" aceita digitação.
- Corrigido: no Registro da O.S., o técnico gravado na ordem era trocado pelo nome de quem abria a tela.
- Registro da O.S. de produto sem cadastro de produto mostra o nome do produto gravado na ordem.

### Pendências (Estoque)

- Nova linha "Entrada OP": toda O.P. com produto ainda não recebido, desde a criação, com o produto e quanto falta receber ("Aguardando entrada" ou "Recebido em parte"). Abre a Entrada de material já preenchida.
- "Solicitação OP" mostra só a O.P. aberta com peça que ainda não saiu, e abre a Saída de material com o que falta.
- "Solicitação OS" mostra só a O.S. aberta com peça aprovada ainda não entregue (antes aparecia toda O.S. não cancelada), com a situação: "Aguardando entrega", "Entregue em parte" ou "Conferir saídas".

### Entrada de material

- Aberta pela linha "Entrada OP", traz um item só (o produto da ordem), na quantidade que falta receber e no depósito padrão do item. O título da janela mostra o número da ordem.
- Fornecedor, pedido de compra, nota fiscal e valor não se aplicam a essa entrada e ficam desligados. Número de série e lote são pedidos ao salvar, como em toda entrada.
- Se a ordem já registrou a série (ou o lote) do produto, a entrada só confirma a quantidade, no depósito desse registro, sem pedir a série de novo.
- A entrada do produto de uma ordem, depois de gravada, reabre com as mesmas travas.

### Saída de material

- Aberta pela linha "Solicitação OP" ou "Solicitação OS", traz só as peças que ainda faltam entregar (da O.S., só as aprovadas), na quantidade que falta, com o saldo e o depósito padrão do item. Antes vinham todas as peças, com disponível "0".
- Ordem fechada, cancelada ou sem nada a entregar: a tela avisa.
- Corrigido: a saída feita a partir de solicitação criada no portal não puxava o modelo do produto.

### Solicitação do estoque

- Solicitação atendida em parte pode ser editada: item que já teve saída não pode ser tirado nem trocado, e a quantidade não pode ficar abaixo do que já saiu. A tela mostra "Atendida em parte: o que já saiu não pode ser tirado nem diminuído".
- Depois de salvar, a tela relê a situação; se a solicitação ficou atendida por inteiro, passa a só consulta.

### Kanban

- Ao arrastar um cartão, uma linha mostra onde ele vai ficar.
- Arrastando um cartão perto da borda, o quadro rola sozinho.
- Segurar o botão esquerdo no fundo do quadro (fora dos cartões) e arrastar rola o quadro.
- "Mostrar fechadas e canceladas" já vem marcada.
- O quadro se atualiza sozinho a cada 30 segundos quando está parado, e só redesenha se algo mudou.
- Depois de mover, a linha ao lado da busca diz onde a ordem ficou, se os responsáveis foram avisados e se alguma automação da etapa falhou.
- Sem resposta ao mover, o aviso pede para conferir onde a ordem está antes de repetir, e o quadro é relido (antes dizia que a ordem tinha voltado, sem conferir).
- Texto cortado no cartão (vários números de série, cliente comprido) aparece inteiro ao parar o mouse em cima.
- Novo botão "Campos do cartão" (quem configura o Kanban): escolhe os Novos campos e os campos nativos da ordem que aparecem no cartão, na sequência escolhida. Vale para todos da empresa, também no portal. A busca do quadro procura também nesses campos.
- Mudança de etapa recusada por falta de preenchimento: as seções com pendência abrem nos Novos campos e, ao fechar o aviso, a tela vai até o primeiro campo que falta.

### Acompanhamento e comentários

- Saiu a aba "Conferência da etapa": o que falta para avançar aparece no aviso, ao mover o cartão.
- Comentário pode levar foto ou PDF: "Anexar foto ou PDF…" e "Tirar anexos". Até 5 anexos por comentário e PDF de até 5 MB; a foto é reduzida antes de enviar.
- O histórico mostra o nome dos anexos de cada comentário, e o botão "Anexos dos comentários (N)" abre qualquer um deles.
- Corrigido: a segunda menção do dia na mesma ordem não chegava como aviso quando a primeira já tinha sido resolvida.

### Requisitos da etapa e automações (quem configura o Kanban)

- Nova parte "Seções que aparecem na ordem nesta etapa": com "Escolher as seções que aparecem nesta etapa" ligado, a ordem mostra só as seções marcadas enquanto estiver na etapa (nenhuma marcada = nenhuma seção). As outras continuam guardadas.
- A lista das etapas mostra quantas seções cada etapa mostra.
- Ao lado de cada seção aparecem os modelos de campos que a usam, e há o botão "Marcar todas" (com a busca, vale para as encontradas).
- Não dá mais para exigir fotos como requisito da etapa; requisito de fotos antigo aparece indicado para ser retirado.
- Pessoa ou setor marcado que não existe mais aparece com "(não existe mais)".
- Automação "Encaminhar cartão" só oferece quadro do mesmo tipo de ordem da etapa de origem.

### Lista de ordens (O.P. e O.S.)

- Novo botão "Colunas" (quem configura o Kanban): escolhe os campos nativos e os Novos campos que aparecem como coluna. A busca procura neles e clicar no título ordena (números em ordem numérica, datas como data, vazios no fim). Vale para todos da empresa.
- Corrigido: ordenar por uma coluna desfazia a busca (tudo voltava a aparecer com o texto ainda escrito).
- Os botões "Lista", "Kanban" e "Colunas" ganharam o desenho padrão dos botões do programa. Corrigido: no tema Dark o texto deles sumia.

### Novos campos

- Nas ordens, a etapa do Kanban pode mostrar só as seções dela. Uma faixa avisa quantas seções estão à vista, e quem cuida dos modelos tem "Mostrar todas as seções".
- A escolha do modelo e os botões do bloco só aparecem para quem tem acesso a "Modelo dos novos campos"; os demais veem só os campos.
- Campos de Data e de "Data e hora" ganharam o botão do calendário.
- Lista de múltipla escolha com muitas opções mostra todas, em colunas, sem rolar por dentro.
- Digitar "|" num campo mostra o aviso de que ele será gravado como "-".
- Se os campos ou a lista de modelos não puderem ser carregados, o bloco mostra o aviso com "Tentar de novo" e o Salvar é recusado até carregar.
- Modelo gravado no registro que foi excluído ou desligado aparece como "Modelo deste registro (não está mais disponível)", com os campos e os valores; o Salvar mantém o modelo e os valores.
- Bloco vazio diz por quê: registro sem modelo, modelo sem campos ou nenhum modelo para o formulário.
- Corrigido: valores de Novos campos fora do modelo eram descartados ao salvar ordens gravadas sem a lista de números dos campos (por exemplo, vindas de carga de dados).

### Fotos da ordem

- Cada painel (Entrada e Saída) ganhou "Selecionar", "Baixar todas" e "Excluir todas". No modo de seleção, clicar marca a foto e os botões viram "Baixar (N)" e "Excluir (N)"; Ctrl+A marca todas e Esc sai.
- "Baixar" salva cópias numa pasta escolhida, sem sobrescrever arquivo com o mesmo nome. Funciona também com a ordem encerrada.
- Excluir foto agora é só do Master e de quem é do setor Administração. Pede só a confirmação (sem motivo) e tira a foto também da pasta da ordem no computador. "Remover foto…" passou a se chamar "Excluir foto…".
- Fotos que não foram enviadas: ao fechar a ordem, a tela pergunta antes de descartá-las ("Descartar fotos e fechar" ou "Continuar editando").
- As fotos são reduzidas ao enviar (lado maior até 1600 px) e ficam em torno de 150 a 300 KB.
- No computador, as fotos e os documentos ficam numa pasta própria de cada ordem (por exemplo "Ordens de Produção\OP 1-26", com Entrada, Saída e Documentos).
- A galeria só começa a buscar as fotos depois que a tela da ordem termina de abrir, e as miniaturas são montadas sem travar a tela.

### Visualizador de fotos

- Trocar de foto não fica mais parado em "Carregando foto…": a miniatura aparece na hora, ampliada, enquanto a foto completa carrega.
- As últimas fotos abertas ficam guardadas (voltar e avançar é instantâneo) e a próxima e a anterior já são adiantadas.
- Contador "3 de 71" entre "Anterior" e "Próxima"; abaixo da foto, nome, data e tamanho.
- Teclas novas: Home e End (primeira e última foto), F5 (tentar de novo) e Esc (fechar). A roda do mouse dá zoom sem precisar clicar antes.
- Fundo escuro em volta da foto, nos dois temas; em janela estreita os botões descem para uma segunda linha.

### Documentos da ordem e do pedido

- Tela única "Documentos" na Ordem de produção, na Ordem de serviço e no Pedido de venda: o que foi anexado e o que foi gerado pelo "Gerar documento", numa lista só, mais novo em cima.
- "+ Anexar" com descrição: PDF, imagem (JPG ou PNG), Word ou Excel, até 50 MB. Duplo clique ou "👁 Abrir" abre o arquivo.
- Fotos de entrada e saída e anexos de comentário não entram nessa lista: ficam na galeria e no acompanhamento.
- O documento gerado e o PDF de O.P. e O.S. também aparecem, por atalho, na pasta Documentos da ordem no computador.
- Em ordem encerrada, documento e PDF continuam podendo ser gerados e carregados; só remover fica bloqueado.

### Gerar documento

- Os modelos ligados ao produto da ordem vêm primeiro na lista e o primeiro já vem escolhido. Sem modelo do produto, a lista da O.P. e da O.S. abre sem modelo escolhido e pergunta qual usar ao gerar.
- Modelo sem arquivo Word não aparece na lista.
- "Gerenciar modelos" só aparece para quem tem acesso aos modelos de documento. Em "Ver TAGs", Nova, Editar e Excluir só aparecem para quem tem acesso aos modelos de campos.
- Com documento já gerado, "Gerar documento" continua disponível e pergunta "Gerar de novo?". O documento atual fica em "Gerados" como versão anterior; se a geração não chegar ao fim, ele continua valendo.
- Ao clicar em gerar, se a ordem foi alterada e não salva, a tela pede para salvar antes.
- "Abrir PDF" refaz o PDF quando o documento foi gerado de novo (antes abria o PDF antigo).
- "Abrir documento" confere a cópia do computador com o documento registrado; se for diferente, abre o registrado e guarda a cópia antiga com outro nome, sem apagar.
- O documento sai sempre do Word guardado do modelo escolhido: Word trocado em outro computador ou pelo portal passa a valer, e modelos com o mesmo nome de arquivo não se misturam.
- Modelo que já gerou documento abre numa cópia só de leitura.
- Ordem de produção: novas TAGs @NSP (número de série do produto) e dados do cliente do pedido de venda (@IDP, @PRO, @CPF, @CNP, @TEL, @EML, @END).
- Ordem de serviço: {ITEM_DES} sai com a descrição apelido da peça; novas TAGs {ITEM_VLU} (valor unitário) e {ITEM_DSC} (desconto em %).
- Registro sem itens: a linha da tabela de itens sai em branco (antes saía com as TAGs escritas).
- Corrigido: a TAG @PRI (problema informado) da O.S. saía sempre vazia.
- Corrigido: quando o documento não chegava a ser registrado na ordem, a janela o marcava como gerado mesmo assim.

### Modelos de documento (cadastro)

- Novo bloco "Produtos vinculados (opcional)": escolha produtos acabados do estoque; ao gerar documento numa O.P. ou O.S. desses produtos, o modelo aparece primeiro e já escolhido.
- Modelo que já gerou documento: mudar só o cadastro (Ativo, Observações, produtos) não trava mais. A alteração feita no Word neste computador é guardada à parte, com outro nome, e o arquivo do modelo volta ao guardado. Para mudar o texto, crie uma nova revisão. O mesmo vale ao atualizar os modelos editados.
- Depois de salvar um modelo novo, a tela passa a ser a do modelo gravado: o segundo Salvar não é mais recusado como duplicado.
- Código e versão repetidos são conferidos antes de enviar o Word. Na edição, trocar para o código e a versão de outro modelo é recusado.
- Modelo salvo sem arquivo Word: aviso de que ele só aparece para gerar documento depois de ter o Word.
- Se o modelo não puder ser lido por inteiro ao abrir, a tela avisa e fecha, sem deixar salvar por cima.
- Corrigido: se o Salvar falhasse depois de "Substituir" o Word, o modelo podia ficar sem arquivo.

### Modelo de novos campos e TAGs

- A lista de campos mostra o texto completo: título, conteúdo padrão, valor inicial, seção e opções quebram a linha.
- Fechar com alterações não salvas pergunta (Sair sem salvar / Salvar e sair / Voltar). Antes fechava e perdia o que foi digitado.
- A lixeira diz qual campo ou produto vai sair do modelo e que isso vale depois de salvar.
- Na escolha de campos, as TAGs de outros formulários aparecem no fim, apagadas, com "só em …", e não podem ser marcadas.
- Excluir um modelo de campos pela lista: a pergunta diz qual modelo.
- TAG customizada: novo "Copiar dados" cria uma TAG nova com o mesmo título, tipo, aplicação e opções; só o código fica para preencher.

### Pedido de venda

- Novo botão "🏭 Gerar ordem de produção": abre uma O.P. nova já com este pedido (e o cliente dele).
- Pedido gerado pela O.P. vem com o produto e a quantidade da ordem (o valor de venda fica para informar). Salvo, a janela fecha e a ordem se liga ao pedido.
- Cliente: botão "..." abre a janela de pesquisa por nome, CPF/CNPJ, telefone ou e-mail.
- "📎 Documentos" usa a tela única de Documentos.

### Clientes

- Cliente que não é pessoa física: campo "Nome fantasia" e novo card "Pessoa responsável" (nome da pessoa, CPF e RG). O CPF da pessoa responsável é conferido.
- Novo campo "RG", ao lado do CPF; quando só tem números, ganha o formato 00.000.000-0.
- Pessoa física que já tem CNPJ mostra o CNPJ numa linha à parte.
- Corrigido: ao salvar, o documento (CPF ou CNPJ) que não aparecia na tela era apagado.

### Reclamação de clientes

- Proprietário: botão "..." abre a janela de pesquisa de clientes.

### Estoque

- Item do estoque: novo campo "Descrição apelido", o nome da peça que vai para o cliente nos documentos da O.S.
- A lista de itens abre sem item marcado; a busca não marca linha sozinha, e "Selecionar" leva só o que a pessoa marcou ou clicou.

### Assinatura eletrônica

- Se a sessão não vale mais (por exemplo, a senha foi trocada com o programa aberto), o aviso pede para sair e entrar de novo no Stand PRO, e nada é assinado.
