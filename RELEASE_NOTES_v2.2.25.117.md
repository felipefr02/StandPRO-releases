## v2.2.25.117 (2026-10-03) — Estrutura do produto fase 2, excluir TAG e ajustes de validação

### Estrutura do produto (fase 2 do redesenho)

- A Etapa vira o cabeçalho do grupo: uma faixa com ⚑ "Etapa {nº} · {código} — {descrição}" e, no lugar do "—", a soma do tempo dos recursos e a soma do custo dos itens e recursos do grupo (Σ). As somas só aparecem na tela; nada novo é gravado. As linhas do grupo ficam recuadas, e o título do bloco mostra "{N} linhas · {M} etapas".
- Cada tipo tem um ícone (■ Item, ◷ Recurso, ⚑ Etapa, ¶ Texto) e uma faixa de 4 px na sua cor, que fica vermelha na linha com erro. O Texto ocupa uma faixa só, do Código ao Total, com um editor da mesma largura; uma observação antiga aparece no fim da faixa e sai com "Limpar observação antiga" (botão direito).
- Incluir linha: o "+" (ou Ins) abre um menu por tipo — Item do estoque, Recurso, Etapa de itinerário e Texto da linha (Ctrl+1 a Ctrl+4). A linha entra abaixo da atual; com Shift, entra acima, e "Incluir no fim" leva a linha para o fim. A linha só entra completa: item, recurso ou etapa não escolhido e Texto deixado vazio não ficam na lista.
- A etapa é escolhida numa lista com busca, que ignora acentos e maiúsculas, mostra primeiro o código exato e marca as etapas já usadas ("✓ linha N"). Pelo teclado, Ctrl+1 e Ctrl+2 (ou uma letra digitada no Código) procuram o item ou o recurso pelo código exato; se o código não for achado, ficar vazio ou a pessoa apertar F4, a lista abre.
- O tipo não se troca mais na célula. O botão direito oferece "Substituir por outro tipo" e "Converter em Texto"; numa linha antiga sem tipo, ou com tipo desconhecido, oferece "Definir tipo".
- Item ou recurso que já está na estrutura não entra de novo: a tela pergunta "Somar lá?" e soma 1 no item (ou o tempo-base no recurso) na linha que já existe; uma estrutura antiga com linha repetida só salva depois de juntar as quantidades. Excluir uma etapa com linhas abaixo pergunta "Só a etapa", "Etapa e as N linhas" ou "Cancelar". Ctrl+Z (ou "Desfazer" no botão direito) desfaz inclusões, trocas, exclusões, "Somar lá", mover linha, edições e "Atualizar preços".
- Salvar: a tela confere todas as linhas com as mensagens do site, mostra um resumo ("5 linhas precisam de atenção: 3 (tempo inválido), 9 (repetida)…") e leva o foco para a primeira. Os avisos que não impedem salvar ficam na própria linha: etapa fora do itinerário, etapa sem linhas, linha sem custo e unidade diferente do cadastro.
- Mudança em relação à 2.2.25.116: duas situações de estruturas antigas, que antes eram gravadas como estavam, agora pedem correção antes de salvar: uma linha sem tipo (resolve com "Definir tipo") e um Texto que passa de 255 caracteres depois de juntar Código e Descrição (o Texto aparece inteiro e o Salvar pede para encurtar).
- Teclado completo: Enter ou F2 abrem a busca da linha (ou escrevem no Texto), Del exclui, Alt+Shift+↑/↓ movem a linha, e Tab passa só pelas células que se digitam.
- "Atualizar preços pelo cadastro…": a prévia usa os textos do site, e o botão fica desligado em consulta e quando não há item nem recurso. Mensagens com código ou descrição do cadastro aparecem como escritas; antes, um texto com "não encontrado", "Drive" ou "SQL" virava o aviso genérico "Registro não encontrado…".

### Modelo do produto e TAGs

- O botão Excluir voltou à tela "TAGs disponíveis" e ao seletor de campos do modelo. A TAG customizada agora é excluída pelo servidor, com registro na auditoria.
- O servidor só exclui TAG customizada da própria empresa, sem cadeado e sem uso em modelo de campos (contam também os modelos excluídos e os modelos antigos que citam a TAG nos campos de texto). TAG em uso não sai, e a mensagem diz em quais modelos ela está; TAG nativa ou com cadeado também não sai.
- Ao excluir várias TAGs no seletor, a recusa de uma não impede as outras, e o aviso final diz quantas saíram e por que as outras ficaram.
- TAG que está na lista de um modelo aberto e ainda não salvo não pode ser excluída pela galeria: a tela avisa para tirá-la do modelo antes.

### Engenharia, risco e validação

- RMF: a resposta "Risco residual total aceitável?" fica salva no rascunho e aparece ao reabrir; antes voltava em branco. Depois de aprovado, o RMF continua congelado. Um RMF marcado "Não" não é aprovado enquanto a conclusão não for revista (antes a aprovação trocava por "Sim"), e a tela avisa isso antes de pedir a assinatura eletrônica.
- Validação de software: o pacote VMP/URS/FRS/RA/IQ/OQ/PQ/VSR de um estudo concluído (validado, reprovado ou obsoleto) usa a cópia do software guardada no estudo, não o cadastro atual. Mudar o software depois, por exemplo com nova versão ou outro nome, não altera mais o pacote do estudo antigo. Os documentos têm a linha "Dados do software", que diz de onde vieram os dados. Se a cópia não conferir com o código de verificação, o pacote não é gerado e a tela explica o motivo. Estudo em rascunho continua usando o cadastro atual; estudo antigo sem cópia guardada usa o cadastro atual e o pacote avisa isso.
- Validação de processo: a grade de critérios de aceite, com 24 colunas, rola para o lado (barra de baixo, Shift + roda do mouse ou dois dedos no touchpad). Cada coluna abre numa largura legível e não pode ser estreitada abaixo de um mínimo; antes, o Critério ficava com 49 px e a última coluna era cortada. As outras listas da tela continuam ocupando a largura toda.
- Validação de software e Submissão por mercado: "Origem do software", "Situação" e "Status do ciclo" passam a ser obrigatórios com cadeado em "Alterar regras dos campos". As telas já preenchiam esses campos sempre, então nada muda no uso.

### Ordens de serviço e estoque

- Registro da OS: nas listas Características técnicas e Novos campos, a lixeira aparecia cortada na borda do quadro. Agora cada lista tem altura para todos os botões laterais (+, ×, ▲, ▼ e lixeira).
- Condições de armazenagem: locais que não são depósito (fabricação, laboratório, quarentena etc.) voltam a salvar; "Depósito / área" só é cobrado quando o local é um depósito.

### Servidor (publicado junto com esta versão)

- Rota nova para excluir TAG customizada; RMF grava a conclusão do rascunho e recusa aprovar com "Não"; Condição de armazenagem só cobra o depósito em local que é depósito; catálogo com cadeado em Origem/Situação do Software e Status da Submissão (entra no próximo login de cada empresa).
- Com o servidor ainda antigo, o Desktop avisa que a exclusão de TAG não está disponível e nada é excluído.
