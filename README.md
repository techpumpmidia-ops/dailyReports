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
> `• Tudo versionado e enviado ao GitHub (repos pumpCore, prototipes e dailyReports).`
___
