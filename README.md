# 🧠 FGT Tech – Sistema de Chamados e Tarefas Inteligente

FGT é um sistema de **criação e gestão de chamados/tarefas**, focado em **reduzir fluxos operacionais**, automatizar processos e facilitar o dia a dia de equipes técnicas, administrativas ou de atendimento.

> 🔄 Desenvolvido com Vue 3, o sistema é responsivo, minimalista e pensado para performance e usabilidade.

---

## 📌 Objetivos do Projeto

- Reduzir o tempo de criação e resolução de tarefas
- Automatizar etapas repetitivas com inteligência simples
- Fornecer visibilidade de produtividade e prazos
- Criar um ambiente organizado com foco em agilidade

---

## 🧱 Estrutura do Projeto

```bash
reduxa/
├── src/
│   ├── assets/
│   ├── components/
│   ├── views/
│   ├── router/
│   ├── store/
│   ├── App.vue
│   └── main.js
├── public/
├── package.json
└── README.md
````
## 🛠️ Tecnologias Utilizadas
Vue 3

-Vue Router
-Pinia (ou Vuex)
-Axios
-Vite para bundling
-Backend sugerido: API REST com Django

## 📦 Instalação Local

# 1. Clone o repositório
Frontend: https://github.com/reduxa/FgtTech_front.git
Backend: https://github.com/reduxa/fgt_tech_back.git

cd FGTTech

# 2. Instale as dependências
npm install (Para o Frontend)
pdm install (Para o Backend)

# 3. Rode o servidor local
npm run dev (Para o Frontend)
pdm dev (Para o Backend)

Acesse: http://localhost:5173
Acesse: http://localhost:8000

## 🧠 Regras de Negócio

1. Criação de Tarefas/Chamados
Toda tarefa deve conter: título, descrição, prioridade e responsável.

Apenas usuários autenticados podem criar tarefas.

O status inicial padrão é Aberto.

O sistema pode sugerir responsáveis com base na categoria escolhida.

2. Status das Tarefas
Status disponíveis: Aberto, Em Progresso, Aguardando, Concluído.

Alterações de status são registradas com data e autor.

Tarefas sem atualização por 7 dias mudam para Aguardando.

Apenas usuários com permissão podem concluir tarefas.

3. Priorização e SLA
Níveis de prioridade:

Baixa – 5 dias úteis

Média – 3 dias úteis

Alta – 2 dias úteis

Urgente – 1 dia útil

Notificações são enviadas com 12h de antecedência do prazo de SLA.

4. Notificações
São geradas automaticamente quando:

Uma tarefa é atribuída a um usuário

O status da tarefa é alterado

O SLA está próximo do vencimento

Podem ser enviadas por e-mail ou exibidas na interface.

5. Controle de Acesso
Perfis de usuário:

Administrador – controle total

Gestor – cria e gerencia tarefas

Operador – apenas visualiza e atualiza tarefas atribuídas

Apenas administradores podem excluir tarefas.

6. Automatizações
Sugestão de responsáveis com base no histórico

Tags automáticas geradas a partir do conteúdo

Criação de tarefas recorrentes (ex: manutenção semanal)

Integração com e-mail para criação automática de tarefas por palavras-chave

7. Relatórios e Auditoria
Logs completos com data, hora e autor de cada ação

Relatórios semanais automáticos por setor e responsável

Métricas de produtividade acessíveis pelo painel

8. Restrições
Cada tarefa pode ter apenas um responsável

Tarefas concluídas não podem ser reabertas (apenas duplicadas)

Tarefas com histórico de alterações não podem ser excluídas, apenas arquivadas

## 🎨 Layout
O sistema segue uma estética limpa e moderna:

Interface baseada em cartões

Navegação lateral minimalista

Painel principal com visão geral + botão de criação rápida

Kanban com colunas: Aberto, Em Progresso, Aguardando, Concluído

##🚧 Funcionalidades Futuras

🔄 Sincronização com Google Agenda

🤖 IA para sugestão de descrição e prazos

🧩 Integrações com Slack, WhatsApp e Discord

📱 Aplicativo mobile

##🧑 Autor
Desenvolvido por Rafael de França & Eduardo Gabriel dos Santos

📧 erfranca.com@gmail.com & dudugx05@gmail.com
🔗 LinkedIn <a href='https://www.linkedin.com/in/rafael-de-fran%C3%A7a-26009b240/'>Rafael<a> <a href='https://www.linkedin.com/in/eduardo-gabriel-dev05/'>Eduardo<a>
🐙 GitHub <a href='https://github.com/eoFrancaa/'>Rafael<a> <a href='https://github.com/dudug05'>Eduardo<a>
