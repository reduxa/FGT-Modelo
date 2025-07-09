# 🧠 FGT Tech – Sistema de Chamados e Tarefas Inteligente

**FGT Tech** é um sistema de **criação e gestão de chamados/tarefas**, focado em **reduzir fluxos operacionais**, automatizar processos e facilitar o dia a dia de equipes técnicas, administrativas ou de atendimento.

> 🔄 Desenvolvido com Vue 3 e Django, o sistema é responsivo, minimalista e pensado para performance e usabilidade.

---

## 📌 Objetivos do Projeto

- Reduzir o tempo de criação e resolução de tarefas  
- Automatizar etapas repetitivas com inteligência simples  
- Fornecer visibilidade de produtividade e prazos  
- Criar um ambiente organizado com foco em agilidade  

---

## 🧱 Estrutura do Projeto

```bash
FGTTech/
├── frontend/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── views/
│   │   ├── router/
│   │   ├── store/
│   │   ├── App.vue
│   │   └── main.js
│   ├── public/
│   └── package.json
├── backend/
│   ├── fgt/
│   ├── manage.py
│   └── pyproject.toml
└── README.md
```

---

## 🛠️ Tecnologias Utilizadas

- Vue 3  
- Vue Router  
- Pinia (ou Vuex)  
- Axios  
- Vite (empacotador frontend)  
- Django (backend REST API)  
- PDM (gerenciador de pacotes Python)

---

## 📦 Instalação Local

### 1. Clone os repositórios

```bash
# Frontend
git clone https://github.com/reduxa/FgtTech_front.git

# Backend
git clone https://github.com/reduxa/fgt_tech_back.git
```

### 2. Instale as dependências

```bash
# Frontend
cd FgtTech_front
npm install

# Backend
cd ../fgt_tech_back
pdm install
```

### 3. Execute o servidor local

```bash
# Frontend
npm run dev

# Backend
pdm run dev
```

- Frontend: http://localhost:5173  
- Backend: http://localhost:8000  

---

## 🧠 Regras de Negócio

### 1. Criação de Tarefas/Chamados
- Toda tarefa deve conter: **título**, **descrição**, **prioridade** e **responsável**.  
- Apenas usuários autenticados podem criar tarefas.  
- O status inicial é sempre `Aberto`.  
- O sistema pode sugerir responsáveis com base na categoria.

### 2. Status das Tarefas
- Status disponíveis: `Aberto`, `Em Progresso`, `Aguardando`, `Concluído`.  
- Alterações de status são registradas com data e autor.  
- Tarefas sem atualização por 7 dias mudam para `Aguardando`.  
- Apenas usuários com permissão podem concluir tarefas.

### 3. Priorização e SLA
- Níveis de prioridade:
  - `Baixa` – 5 dias úteis  
  - `Média` – 3 dias úteis  
  - `Alta` – 2 dias úteis  
  - `Urgente` – 1 dia útil  
- Notificações são enviadas com 12h de antecedência do vencimento do SLA.

### 4. Notificações
- São geradas automaticamente quando:
  - Uma tarefa é atribuída a um usuário  
  - O status da tarefa é alterado  
  - O SLA está próximo do vencimento  
- As notificações podem ser exibidas no sistema e enviadas por e-mail.

### 5. Controle de Acesso
- Perfis de usuário:
  - `Administrador` – controle total  
  - `Gestor` – cria e gerencia tarefas  
  - `Operador` – visualiza e atualiza tarefas atribuídas  
- Apenas administradores podem excluir tarefas.

### 6. Automatizações
- Sugestão de responsáveis com base no histórico  
- Geração automática de tags com base no conteúdo  
- Criação de tarefas recorrentes (ex: manutenção semanal)  
- Integração com e-mail para criar tarefas por palavras-chave

### 7. Relatórios e Auditoria
- Logs com data, hora e autor de cada ação  
- Relatórios semanais por setor e responsável  
- Métricas de produtividade acessíveis no painel

### 8. Restrições
- Cada tarefa deve ter apenas um responsável  
- Tarefas concluídas não podem ser reabertas (apenas duplicadas)  
- Tarefas com histórico de alterações não podem ser excluídas, apenas arquivadas  

---

## 🎨 Layout

O sistema possui uma estética limpa e moderna:

- Interface baseada em cartões  
- Navegação lateral minimalista  
- Painel principal com visão geral + botão de criação rápida  
- Kanban com colunas: `Aberto`, `Em Progresso`, `Aguardando`, `Concluído`

---

## 🚧 Funcionalidades Futuras

- 🔄 Sincronização com Google Agenda  
- 🤖 IA para sugestão de descrição e prazos  
- 🧩 Integrações com Slack, WhatsApp e Discord  
- 📱 Aplicativo mobile  

---

## 👥 Autores

Desenvolvido por:

- **Rafael de França**  
  📧 erfranca.com@gmail.com  
  🔗 [LinkedIn](https://www.linkedin.com/in/rafael-de-fran%C3%A7a-26009b240/)  
  🐙 [GitHub](https://github.com/eoFrancaa)

- **Eduardo Gabriel dos Santos**  
  📧 dudugx05@gmail.com  
  🔗 [LinkedIn](https://www.linkedin.com/in/eduardo-gabriel-dev05/)  
  🐙 [GitHub](https://github.com/dudug05)

---

## 📄 Licença

© 2025 Rafael de França & Eduardo Gabriel dos Santos.  
Todos os direitos reservados.

Este projeto é de uso privado e não está autorizado para cópia, modificação ou redistribuição sem consentimento prévio por escrito dos autores.
