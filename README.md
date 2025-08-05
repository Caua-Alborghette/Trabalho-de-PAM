

🏥 Projeto de PAM – HospiFlow

Sistema Inteligente de Triagem Hospitalar com Banco de Dados Relacional

📅 Cronograma

05/08 – Apresentação dos repositórios com os requisitos e definição dos temas

12/08 – Apresentação do protótipo funcional do projeto



---

💡 Solução Proposta: HospiFlow

O HospiFlow é um sistema digital que busca facilitar a triagem hospitalar e o agendamento de consultas. Ele vai ser criado para melhorar o atendimento nas recepções de hospitais e clínicas, com os seguintes objetivos:

Eliminar filas físicas 

Acelerar a triagem (com base nos sintomas informados)

Otimizar o agendamento (conforme a disponibilidade médica)

Manter o paciente informado em tempo real sobre sua posição na fila e o andamento da consulta



---

⚙️ Arquitetura Técnica: Banco de Dados com MySQL/MariaDB

🔧 Banco de Dados Relacional

Será utilizado MySQL (ou MariaDB, dependendo da hospedagem), por oferecer:

Alta performance em consultas

Segurança e integridade dos dados

Facilidade na geração de relatórios gerenciais

Suporte a sistemas modernos de backend

Conformidade com a LGPD (quando usado com boas práticas de segurança)



---

🧩 Estrutura do Banco de Dados (principais tabelas)

paciente – dados pessoais dos pacientes

medico – nome, especialidade e CRM

triagem – sintomas, prioridade, data e hora

consulta – vínculo entre paciente e médico, status e horário

notificacao – mensagens enviadas para o paciente

sala – controle de salas disponíveis ou ocupadas

usuario – login, senha e permissões de acesso



---

🧍‍♂️ Fluxo de Funcionamento para Pacientes

1. Pré-Triagem Digital (via aplicativo em React Native com Expo)

Cadastro ou login rápido

Questionário simples com sintomas

O sistema define a prioridade (emergência, urgência ou eletivo)

Escolha de médico (em caso eletivo) com base em horários disponíveis

Confirmação do horário e estimativa de atendimento


2. Check-in Inteligente

Notificações como:

“Você é o próximo em 15 minutos”

“Sua consulta com Dr. Silva está pronta – Sala 12”


Possibilidade de chegada flexível, com base nas chamadas



---

📊 Painel Administrativo da Recepção

Atualização automática das prioridades da fila

Integração com laboratórios para evitar filas repetidas

Visualização em tempo real da ocupação das salas

Acompanhamento do fluxo de atendimento por horário e especialidade



---

🧠 Diferenciais Técnicos e Funcionais

✅ Redução de mais de 70% nos tempos de filas

✅ Planejamento para futura integração com telemedicina

✅ Geração de relatórios como:

Picos de demanda por horário

Médicos mais procurados

Tempo médio por atendimento




---

⚠️ Pontos de Atenção e Melhorias Futuras

Criar validação para evitar fraudes na triagem
(ex: se um mesmo paciente preencher muitos formulários, exigir revisão manual)

Criar funcionalidade de check-in por aproximação (NFC), se suportado no futuro pelo Expo ou nativamente

Adicionar registro de logs e controle de acessos para seguir a LGPD



---

🧪 Tecnologias Sugeridas

📱 App Mobile

React Native com Expo + MySQL (via REST API)

Desenvolvimento rápido e compatível com Android/iOS

Utiliza JavaScript ou TypeScript

Interface moderna e responsiva

Autenticação com JWT ou OAuth2



🌐 Backend

Node.js + Express ou Python + Flask/FastAPI

APIs REST para comunicação com o app

Integração com banco de dados via ORM (Sequelize, SQLAlchemy etc.)



💾 Banco de Dados

MySQL ou MariaDB

Índices para acelerar buscas

Procedures e Triggers para organizar a lógica de prioridade da fila




---

👥 Fluxo de Trabalho do Grupo

Acesso Total (Filipe e Cauã)

Enviam código diretamente para os branches principais (main ou dev)

Gerenciam conflitos e organizam o repositório


Acesso Limitado (Lucas e João)

Trabalham em branches separados

Utilizam ferramentas online como:

GitHub Codespaces – IDE completa no navegador (60h/mês grátis)

vscode.dev – Editor leve direto do navegador

GitHub Mobile – Revisão e comentários via celular
---





















✅ Requisitos Funcionais

(O que o sistema precisa fazer)

1. Cadastro e login de pacientes
– O paciente pode criar uma conta ou entrar com seu 
  
    2.Definição de prioridade
– O sistema vai colocar o paciente em uma fila de espera dependendo da resposta


3. Agendamento de consulta
– O paciente escolhe o horário 


4. Envio de notificações
– O paciente recebe mensagens como “Você será atendido em 15 minutos” ou “Sua consulta começou”.


5. Painel da recepção e médicos
– Os funcionários veem a lista de pacientes com prioridade atualizada em tempo

6. Gerenciamento de consultas
– As consultas podem ser marcadas, realizadas, canceladas ou reagendadas.

9. Controle de usuários
– Cada pessoa tem um tipo de acesso (paciente, médico, recepção, admin).




---

🔒 Requisitos Não Funcionais

(Como o sistema deve funcionar)

1. Aplicativo leve e rápido feito com React Native + Expo
– Funciona em Android e iOS, com visual moderno e fácil de usar.


2. Sistema seguro
– Login protegido com senha e dados pessoais bem guardados.


3. Banco de dados confiável (MySQL ou MariaDB)
– Rápido e estruturado, ideal para muitos dados e múltiplos usuários.


4. Segurança de dados (LGPD)
– Os dados dos pacientes devem ser protegidos e acessados apenas por quem tem permissão.


5. API separada (backend)
– O app se comunica com o servidor via API, o que facilita manutenção e atualizações.