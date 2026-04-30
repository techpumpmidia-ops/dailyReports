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
> `• Processo: incluídas no DEV_PROMPT do pumpCore três regras de trabalho — documentação contínua, fluxo de Git padronizado (branch, commit, PR) e granularidade ágil (Epic → Story → Task → Subtask). Objetivo: padronizar entregas e tornar o histórico mais auditável;`  
>
> `• Padrão visual: removido o template antigo e adicionados dois padrões candidatos (patterDesign1 e patterDesignd2) para escolha do visual oficial do hub. Limpeza no repositório de 130 arquivos de metadados do Windows que poluíam o histórico;`  
>
> `• Protótipo HubPumP: criada a 'casca' do hub (porta de entrada da equipe tech) rodando offline em localhost, mesmo padrão técnico do DevFlow. Inclui cadastro com aprovação por administrador, login com abas separadas (Padrão / Dev) e home listando os 3 apps internos (DevFlow, Demand Manager, Mídia Tracker) — clicáveis e visíveis, ainda sem funcionalidades próprias. Serve de base testável para o hub real que entrará em produção depois;`  
>
> `• Perfil do usuário: tela completa com foto, cargo, edição de dados, troca de senha, preferências de notificações, histórico de acessos (cadastro, último login, apps abertos) e 'Zona de perigo' para desativação da conta com dupla confirmação;`  
>
> `• Acesso rápido e descoberta: campo de busca por nome na home + sistema de favoritos por usuário (estrela no card e seção dedicada de acesso rápido);`  
>
> `• Notificações: feed por usuário com sino e badge no header, criação automática quando o administrador aprova cadastros ou altera permissões. Cada usuário controla quais tipos de notificação quer receber;`  
>
> `• Painel de administrador: tela de Usuários reescrita — cada usuário pode ser expandido para ver cargo, status, último acesso, apps que mais usa e preferências configuradas, mantendo as ações de aprovar e alterar permissão. Acesso restrito a contas dev;`  
>
> `• Login unificado no HubPumP: removida a separação 'login dev x login padrão' — agora todos entram pela mesma tela. Em vez disso, foi criado o conceito de 'tipo de usuário' (administrador, desenvolvedor, usuário padrão), que vai controlar o que cada pessoa enxerga dentro de cada app — base que sustenta a diferenciação de funcionalidades quando os apps reais entrarem no hub. Administrador continua com acesso a tudo;`  
>
> `• README do repositório pumpCore reescrito de ponta a ponta: linguagem acessível para leitores não técnicos (objetivo, funcionalidades, status, segurança em poucas linhas), com explicações breves sempre que aparece um termo técnico (ex.: por que PostgreSQL).`
>
> `• Início da construção do pumpCore (parte da tarde): saímos da fase de protótipos e começamos o projeto real. Estrutura de monorepo montada (um repositório único que comporta todos os apps internos da PumP), com ferramentas de padronização de código e validação automática a cada commit — garante que ninguém suba código fora do padrão;`
>
> `• Infraestrutura na nuvem desenhada em código (AWS CDK): três blocos prontos — rede compartilhada (VPC), banco de dados gerenciado (RDS Postgres 16) e cofre de segredos (chaves JWT). Ainda não foi para o ar — está validado offline, aguardando credenciais AWS para subir;`
>
> `• Banco de dados local funcionando: Postgres 16 rodando em container (docker-compose) com schema 'core' já migrado. Modelos iniciais criados (usuários, apps, permissões, sessões e auditoria) usando SQLAlchemy + Alembic — base que vai sustentar login, controle de acesso e histórico de uso de todos os apps do hub;`
>
> `• Sistema de autenticação reutilizável: pacote 'auth-py' com login por JWT (token assinado com RS256) e senhas protegidas por bcrypt. Pode ser plugado em qualquer app interno da PumP sem reimplementar do zero;`
>
> `• Backend do Hub (FastAPI) no ar localmente: endpoints de login, dados do usuário logado e listagem de apps, com 10 testes de integração passando. Frontend do Hub (Vite + React + Tailwind) também no ar localmente, com tela de login validada, dashboard listando os apps e proteção de rotas (quem não está logado é redirecionado);`
>
> `• Cliente de autenticação compartilhado ('auth-client'): biblioteca em TypeScript que qualquer app frontend da PumP usa para login, sessão e renovação automática de token — evita que cada app reescreva essa lógica;`
>
> `• Pausa estratégica ao final do dia: hub local 100% funcional offline (login → dashboard → listagem de apps contra Postgres real). Próximo passo é deploy em staging na AWS, mas isso depende de credenciais e domínio que ainda preciso receber. Registrado checkpoint detalhado para retomar sem perder contexto;`
>
> `• Tudo versionado e enviado ao GitHub (repos pumpCore, prototipes e dailyReports).`
___
> ***30/04/2026***  
>
> `• Bug no protótipo HubPumP: frontend (Vite, porta 5174) acusava 'ECONNREFUSED 127.0.0.1:4001' a cada tentativa de login. Causa: o backend Node estava morrendo silenciosamente ao iniciar — sem mensagem de erro, sem porta aberta. Diagnóstico rodando o entrypoint direto mostrou exit code 139 (segfault), indicando módulo nativo incompatível com a versão atual do Node;`
>
> `• Correção: 'npm rebuild better-sqlite3' no backend do HubPumP recompilou o módulo nativo contra o Node 20 atual. Backend voltou a escutar em :4001, login respondendo 200 e o frontend funcionando normalmente;`
>
> `• Aprendizado registrado na 'error-memory' (skill de memória persistente de erros): entrada nova em 'dependency/better-sqlite3-segfault-node-mismatch' com sintoma, causa raiz, solução e como diferenciar de causas parecidas — para que esse tempo de diagnóstico não se repita na próxima vez que o erro aparecer.`
>
> `• Protótipo ProjPlan (substituto interno do ClickUp): construída a primeira versão offline em localhost (Node/Express/SQLite no backend, Vite/React/TS no frontend), mesmo padrão visual do HubPumP. Inclui sidebar com árvore Workspace → Space → Folder → List, Inbox com 'minhas tasks' / vencendo hoje / atrasadas, detalhe de task em drawer lateral (assignees, prioridade, tags, custom fields, comentários, subtasks), e quatro views da mesma lista: Board (Kanban), List, Calendar e Table. Funcionalidades complexas (Gantt, Automações, Dashboards, Goals, Sprints, Whiteboards, AI, Integrações) aparecem como 'Em breve' — o foco do protótipo é apresentar a visão do produto, não implementá-lo de ponta a ponta;`
>
> `• Validação prática do protótipo ProjPlan: subi backend e frontend e bati em todas as rotas da API (workspaces, lists, tasks, inbox, docs, criar comentário, alterar task, marcar subtask). Encontrado e corrigido um bug — a saudação da Inbox aparecia como 'Olá, undefined' porque o endpoint /inbox retornava só o ID do usuário; agora devolve nome, e-mail e avatar igual ao /me. Typecheck e build de produção do frontend passam limpos;`
>
> `• Ajuste de UX no ProjPlan: ícone do toggle de tema trocado de raio (Zap) para sol/lua (Sun/Moon), alinhando ao padrão visual já usado no HubPumP — coerência entre os apps internos da PumP;`
>
> `• Tudo versionado e enviado ao GitHub (repos prototipes e dailyReports).`
___
