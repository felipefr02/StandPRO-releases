## v2.2.25.114 (2026-10-01) — hotfix: envio de documentos, TAGs do Word e lista de recursos

- Envio de arquivos: nomes com acento (ex.: "38-26 - Reclamação de cliente - … .docx") voltam a ser enviados. O nome vai em UTF-8 no upload e o servidor não recusa mais o envio com "Method not allowed. Must be one of: POST".
- Geração de documentos (Word): TAG seguida de quebra de linha (Shift+Enter), tabulação ou retorno de carro volta a ser substituída (ex.: @RPR na reclamação de cliente).
- Reclamação de cliente: @NRA traz a resposta do próprio formulário ("Necessário o registro da ação corretiva?", SIM/NÃO), e não o nome do cliente vindo de um catálogo antigo. As TAGs do formulário passam a ter prioridade sobre as TAGs de mesmo código do cadastro relacionado.
- Lista de recursos: abrir pela Estrutura do produto ou pela Ordem de produção não mostra mais "Não foi possível concluir a operação".

Build do hotfix: código exato da 2.2.25.113 com apenas estas 4 correções. Como na 113, as verificações de build (alvos Check* e o verificador de campos nativos, que comparam com a API local) ficaram desligadas só neste build.
