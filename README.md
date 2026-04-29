# dailyReports
Relatórios diários sobre atualizações e informações importantes.
___
> ***27/04/2026***  
>
> `• Preparação de ambiente;`  
>
> `• Contas: Gmail: tech.pumpmidia@gmail.com - Github: Gmail. - AWS: Aguardando;`  
>
> `• Criação do repositório pumpCore - Será o monorepo do hub de apps da área tech da PumP;`  
>
> `• Implmentação das regras de negócio e de segurança - Aprovado pelo João (beezz);`  
>
> `• Implementação do prompt de construção do projeto;`
___
> ***28/04/2026***  
>
> `• Construção de 13 agentes para o desenvolvimento do PumPCore: auth-specialist/backend-dev/code-rev/database-rev/devops-hub-eng/doc-writer/frontend-dev/infra-rev/makerting-hub-arch/security-auditor/task-planner/test-writer/ui-reviewer;`  
>
> `• Construção da skill error-memory. Um log de memória persistente de erros evitando o gasto de tokens em encontrar soluções para problemas que já foram resolvidos;`  
>
> `• INDEX para o Error Memory;`  
>
> `• Enquanto não posso iniciar o projeto da HUB, comecei a ajustar as demandas que o Caio mencionou para o app de demandas. Usando um modelo offline, apliquei um sistema de Tasks que ajudam na organização das demandas. Apliquei um sistema de perguntas claude-style (aparecem algumas opções + uma extra 'outras' para respostas por fora). Certifiquei de receber o título de acordo com o que o usuário enviou como foi observado pelo Pedro;`  
>
> `• Adicionei um sistema de histórico de chat para contexto ao dev no momento do desenvolvimento.`
>
> `• Adicionado no app de demandas: atribuição de demandas por nome para devs | filtro "minha demandas" | filtro por complexidade | adicionado opção de anexar arquivos ao chat | taxa de recusa | demandas paradas | top solicitantes (mostra o usuário que mais tem demandas, isso facilita um fluxo de conversas caso seja necessário) | troca de comentários entre DEV e SOLICITANTE na aba da demanda`
>
> `• Reestruturação da arquitetura: trocada a ideia de vários subdomínios para cada app (sugestão do João) por 1 subdomínio único com os apps adicionados diretamente no site, em formato de barra de menu;`
>
> `• Alteração de nome/domínio do hub para hub.pumpmidia.com/;`
>
> `• Criação de um novo repositório para protótipos de projetos que serão acrescentados no hub da PumP.`
___
> ***29/04/2026***  
>
> `• Adicionadas ao DEV_PROMPT.md três novas regras de processo: documentação contínua (gatilhos automáticos por subtask/task/story), gatilhos de Git (branch, commit, push e PR seguindo Conventional Commits) e granularidade ágil (Epic → Story → Task → Subtask);`  
>
> `• Substituído o app _template por dois padrões de design candidatos: patterDesign1 e patterDesignd2. Servirão de base para escolher o padrão visual oficial do hub;`  
>
> `• Adicionada regra ao .gitignore para *:Zone.Identifier (metadados ADS criados pelo Windows ao copiar arquivos para o WSL) e removidos os 130 arquivos desse tipo que estavam versionados no repo;`  
>
> `• Três commits enviados ao origin/main do pumpCore: docs(dev-prompt), chore(template) e chore (limpeza dos Zone.Identifier).`
>
> `• Refatoração do prototipes/hubpump: arquivos do Figma movidos para visualReference/ e criado protótipo HubPumP nos moldes do DevFlow (backend Express+SQLite+JWT na porta 4001, frontend React+Vite+Tailwind na porta 5174). Apenas casca do hub: cadastro com aprovação por dev, login JWT, home com 3 cards de apps placeholder (DevFlow, Demand Manager, Mídia Tracker) clicáveis mas não funcionais, e tela /users só para dev. Tudo offline/localhost, sem deploy;`  
>
> `• Adicionadas tabs de login Padrão/Dev: a aba 'Dev' bloqueia contas sem role 'dev' e desfaz a sessão se a verificação falhar;`  
>
> `• Adicionada coluna avatar_url em users + endpoint PUT /api/auth/me para edição de perfil (nome, e-mail, foto e troca de senha com verificação da senha atual). JWT é reemitido quando nome/e-mail mudam;`  
>
> `• Criada página /profile com upload de foto via file input (data URL ≤ 1.5MB salvo direto no SQLite) e troca de senha em formulário separado;`  
>
> `• Novo componente Avatar (foto ou iniciais) clicável no header do hub, posicionado entre o toggle de tema e o botão Sair, levando ao perfil;`  
>
> `• Permissão da tela /users segue restrita a dev — usuário padrão não vê o link nem consegue acessar a rota.`
___
