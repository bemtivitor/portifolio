# Auditoria do portfólio — 12/10/2026

Base revisada: `a1f0ec0efb2c94862d3d18334558e6c82cfeefb1` (main).
Escopo: estrutura completa do repositório e código de index.html; renderização e interação da proposta local. Não foram auditados os sistemas ELO4 nem os conteúdos do currículo, LinkedIn ou Drive. Nenhum resultado de negócio foi inferido.

## Diagnóstico e prioridades

| Prioridade | Área | Evidência na versão original | Consequência | Ação |
| --- | --- | --- | --- | --- |
| P1 | Conteúdo e posicionamento | ELO4 não aparece; projetos de bypass, produtos gamer, anime, hardware e nível ocupam grande parte da página | A experiência recente com sistemas não fica evidente para recrutadores | Implementado: ELO4 no primeiro bloco e biblioteca, contato profissional e narrativa focada em sistemas |
| P1 | Conteúdo dos cases | Não há descrição dos sistemas ELO4 no repositório | Não é possível avaliar complexidade, autoria ou impacto | Pendente: validar problema, contribuição, tecnologias e resultados de cada case antes da publicação |
| P1 | Performance e robustez | Loading fixo ocultado por setTimeout de 3500ms; GIF externo, vídeo aleatório autoplay e Tailwind carregado via script remoto | Acesso ao conteúdo atrasado e dependente de rede/JavaScript; maior tráfego e movimento | Implementado: HTML/CSS locais, sem loading, vídeo, GIF, fontes ou scripts externos |
| P1 | Acessibilidade | Serviços são divs com evento click; popups sem semântica de diálogo, Escape, gestão ou devolução de foco | Navegação por teclado e leitura assistiva prejudicadas | Implementado: conteúdo aberto e details/summary nativo, foco visível e link para pular conteúdo |
| P1 | UI/UX mobile | Nav com hidden md:flex e sem alternativa mobile | Contatos desaparecem em telas pequenas | Implementado: navegação visível em todas as larguras, links profissionais e botões com área mínima de 48px |
| P2 | Estrutura | HTML, CSS e JS em um index de 42.465 bytes; styles.css referenciado mas ausente; sem README | Manutenção e entrada de novos colaboradores difíceis; requisição de CSS inválida | Implementado: CSS separado em assets/styles.css, README e auditoria |
| P2 | Hierarquia visual | Painéis densos com rolagem interna e texto de 10–12px; várias categorias competindo | Projetos e valor profissional difíceis de localizar | Implementado: tipografia maior, seções sequenciais, capas conceituais e foco nos dois sistemas; identidade inspirada na Steam preservada |
| P2 | Responsividade | overflow-x:hidden no body mascara possíveis excessos; popups w-full sem margem mobile | Falhas de layout podem ficar ocultas | Implementado: grids adaptativos e containers fluidos sem esconder overflow; verificar também aparelhos reais |
| P2 | Acessibilidade e movimento | Imagens sem alt; vídeo e animações sem reduced-motion | Conteúdo visual sem descrição e movimento permanente | Implementado: imagens externas removidas, arte CSS decorativa aria-hidden e preferência de movimento reduzido |
| P2 | SEO e compartilhamento | Sem meta description; título usa nome diferente do h1 | Apresentação em busca pouco consistente | Implementado: título e descrição coerentes; pendente domínio canônico e imagem social quando URL final for confirmada |
| P2 | Credibilidade | Status estáticos rotulados Live Feed; números de certificações/repositórios sem evidência | Pode sugerir monitoramento ou provas que a página não fornece | Implementado: remoção dos status e contagens não comprovados |
| P2 | Privacidade | Links para pasta Drive e currículo público | Conteúdo externo pode conter informações pessoais ou internas não avaliadas | Removido link genérico para pasta; currículo existente preservado. Revisar PDF e permissões externas antes de divulgar |
| P3 | Evolução | Sem automação de validação ou instruções de contribuição | Regressões podem passar despercebidas | README com checklist; considerar CI de links/HTML e métricas Lighthouse após consolidar conteúdo |

P1 = alto impacto na apresentação/acesso; P2 = qualidade e manutenção; P3 = evolução. Não foram encontrados segredos no HTML revisado; isso não substitui uma análise do histórico Git ou do PDF.

## Proposta editorial para cada ELO4

Preencher somente com informações autorizadas:
1. Contexto e problema, sem identificar clientes.
2. Sua contribuição específica, período e trabalho individual/equipe.
3. Tecnologias realmente utilizadas e uma decisão técnica com justificativa.
4. Resultado verificável; se não houver métricas, descrever uma entrega concreta.
5. Evidência sanitizada: diagrama genérico ou demonstração com dados sintéticos. Não publicar telas internas sem autorização.

As capas da proposta são arte abstrata em CSS, explicitamente identificadas como conceituais. O texto atual usa apenas os nomes e a participação em desenvolvimento confirmados pelo proprietário. Os cases ainda precisam de conteúdo para atingir o objetivo de convencer recrutadores. As experiências antigas não foram reafirmadas nem descartadas como falsas; saíram do destaque por decisão de foco editorial.

## Validação da proposta

- Microsoft Edge headless: larguras 320, 390, 768 e 1440px, altura de viewport 1000px.
- Sem overflow horizontal nas quatro larguras; um h1 e dois artigos de projeto.
- Nenhum erro JavaScript ou resposta HTTP >=400 durante o carregamento local.
- Primeiro Tab foca Pular para o conteúdo; Enter abre o details do projeto.
- Inspeção visual das capturas desktop e mobile: hierarquia e cartões sem sobreposição.
- git diff --check sem erros de whitespace.
- Página sem JavaScript por construção; uma única dependência local de CSS.

Limites: sem pontuação Lighthouse/Core Web Vitals, teste com leitor de tela, auditoria formal WCAG, aparelhos reais ou verificação de links externos. Não declarar conformidade WCAG ou ganhos percentuais de performance. O CSS não foi minificado; priorizou-se simplicidade e manutenção.

## Publicação

Proposta publicada na branch feat/portfolio-elo4. A criação do PR em rascunho pelo GitHub conectado retornou HTTP 403 (Resource not accessible by integration); abrir o PR pela interface do GitHub. Não fazer merge enquanto os cases e o currículo não forem revisados. Nenhuma mudança deve ser enviada diretamente à main. Confirmar a configuração de hospedagem antes de promover o PR; serviços externos podem gerar previews automaticamente.
