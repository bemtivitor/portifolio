# Portfólio de Vitor Soares

Site estático com identidade inspirada na Steam e foco nas experiências recentes com ELO4 Coletas e ELO4 Financeiro. Sem vínculo com a Valve.

## Estrutura

- index.html: conteúdo e semântica da página.
- assets/styles.css: identidade visual e layouts responsivos.
- Imagens/: acervo existente e currículo PDF; a página nova utiliza somente o PDF.
- docs/AUDITORIA.md: diagnóstico, prioridades, decisões e validação.

## Executar

Abra index.html em um navegador ou sirva a pasta com `python -m http.server 8000` e visite http://localhost:8000. Não há instalação de dependências ou etapa de build.

## Atualizar conteúdo

Edite os dois artigos em index.html. Confirme problema, contribuição, stack e resultados de cada sistema antes de publicar. Use apenas dados públicos autorizados e arte demonstrativa identificada; não inclua clientes, credenciais, valores internos ou código privado. O texto atual é uma base conservadora que ainda precisa de detalhamento dos cases.

Mantenha GitHub, LinkedIn e currículo atualizados. O PDF foi preservado do repositório original e precisa de revisão editorial e de privacidade.

## Verificar alterações

- Abrir em 320, 390, 768 e 1440px e confirmar ausência de rolagem horizontal.
- Usar Tab, Enter e Shift+Tab; verificar foco visível, link de pular conteúdo e detalhes dos projetos.
- Conferir links, acentos, hierarquia dos títulos e carregamento sem JavaScript.
- Verificar preferência de movimento reduzido e zoom de 200%.
- Conferir as mudanças em PR antes de fazer merge; não publicar direto na main.
