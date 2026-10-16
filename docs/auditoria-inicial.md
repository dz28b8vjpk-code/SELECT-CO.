# Auditoria inicial — Select Co.

## Estado do repositório

- Branch de trabalho: `estrutura-selectco`
- Branch principal preservada: `main`
- Arquivos existentes: `index.html` (~4,76 MB) e `README.md`
- O arquivo HTML parece ser uma captura/exportação do site renderizado, não o código-fonte original da aplicação.
- Há marcações de captura (`data-savepage-*`), scripts convertidos para `type="text/plain"` e referências a assets da Emergent. Portanto, abrir esse HTML isoladamente não garante que a aplicação funcione como no preview original.
- A captura inclui a estrutura visual renderizada, mas a análise inicial não encontrou código de interação suficiente para confirmar pesquisa, filtros, carrinho ou estilista IA operacionais.

## Decisão de segurança

Não alterar nem substituir o `index.html` original nesta etapa. A branch de trabalho é separada para que qualquer reorganização possa ser revisada antes de integrar à `main`.

## Próximos passos técnicos

1. Recuperar o código-fonte editável da Emergent, se houver exportação ou sincronização disponível.
2. Se o código-fonte não estiver acessível, extrair da captura os textos, imagens, estilos e estrutura visual que possam ser reaproveitados.
3. Criar uma aplicação organizada por componentes, páginas, dados e serviços apenas depois de mapear os recursos recuperáveis.
4. Implementar e testar pesquisa, filtros, navegação, detalhes de produto, carrinho e estilista IA.
5. Não declarar um recurso funcional até ser testado em execução.

## Limitação atual

Uma captura HTML sozinha não equivale a um projeto React/Vite completo. Ela pode preservar a aparência, mas não necessariamente a lógica, os dados, as rotas e as integrações de backend.
