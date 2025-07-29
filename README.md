Projeto de PAM – HospiFlow

Sistema Inteligente de Triagem Hospitalar com Banco de Dados Relacional
📅 Cronograma

	Dia 05/08: Apresentação dos repositórios com os requisitos e definição dos temas
	Dia 12/08: Apresentação do protótipo funcional do projeto

💡 Solução Proposta: HospiFlow

	HospiFlow é um sistema digital de triagem hospitalar e agendamento inteligente. Ele visa transformar o atendimento na recepção de hospitais e clínicas ao:

		Eliminar filas físicas
		Acelerar a triagem com base em sintomas
		Otimizar o agendamento conforme a disponibilidade dos médicos
		Informar os pacientes em tempo real sobre sua posição na fila e o status da consulta

⚙️ Arquitetura Técnica: Banco de Dados com MySQL/MariaDB

	🔧 Banco de Dados Relacional
		Utilizaremos o MySQL (ou MariaDB, dependendo da hospedagem), por oferecer:
			Alta performance em consultas estruturadas
			Confiabilidade e integridade relacional
			Facilidade na geração de relatórios para gestão hospitalar
			Amplo suporte a ORMs e linguagens modernas de backend
			Conformidade com a LGPD, desde que usada com boas práticas de segurança

🧩 Estrutura do Banco (principais tabelas):

	paciente – cadastro com dados pessoais
	medico – nome, especialidade, CRM
	triagem – sintomas, prioridade, data/hora
	consulta – vínculo paciente ↔ médico, status, agendamento
	notificacao – envio de alertas em tempo real
	sala – controle de salas ocupadas ou disponíveis
	usuario – login, senha e permissões

🏥 Fluxo de Funcionamento para Pacientes

	1. Pré-Triagem Digital (via app ou WhatsApp)
 
		Cadastro rápido ou login
		Preenchimento de questionário com sintomas
		Algoritmo define prioridade (emergência > urgência > eletivo)
		Escolha de médico (caso eletivo) com base na disponibilidade
		Confirmação do horário + tempo estimado de atendimento

	2. Check-in Inteligente
 
		Sistema envia notificações como:
		“Você é o próximo em 15 minutos”
		“Sua consulta com Dr. Silva está pronta – Sala 12”
		Possibilidade de chegada com base na chamada (modelo flexível)

📊 Painel Administrativo da Recepção

	Atualiza automaticamente as prioridades com base nas triagens
	Integração com laboratórios para evitar repetição de filas
	Visualização em tempo real da ocupação das salas
	Acompanhamento do fluxo por especialidade ou horário

🧠 Diferenciais Técnicos e Funcionais

	✅ Redução estimada de até 70% no tempo de espera
	✅ Integração futura com telemedicina para casos leves
	✅ Relatórios detalhados:

		Picos de demanda por horário
		Médicos mais requisitados
		Tempo médio por atendimento

⚠️ Pontos de Atenção e Melhorias Futuras

	Criar mecanismo robusto de validação de triagem (evitar fraudes)
		Ex: triagens muito frequentes podem exigir validação manual

	App mobile com NFC para check-in por aproximação
		Versão simplificada e de baixo custo para clínicas pequenas

	Auditoria de logs e controle de acesso, visando LGPD

🧪 Tecnologias Sugeridas:

	📱 App Mobile
		Flutter + MySQL (via REST API)
			Linguagem: Dart (orientada a objetos, parecida com JS/C#)
			Autenticação via JWT ou OAuth2

	🌐 Backend
		Node.js + Express ou Python + Flask/FastAPI
		Comunicação via REST (JSON)
		Integração com MySQL usando ORM como Sequelize ou SQLAlchemy

	💾 Banco de Dados
		MySQL ou MariaDB
		Utilização de índices para acelerar buscas
		Procedures e Triggers para lógica de negócios (como fila de prioridade)

🧑‍💻 Fluxo de Trabalho do Grupo

Acesso Total (Filipe e Cauã)

	Commitam diretamente nos branches main ou dev
	Gerenciam merge requests e conflitos

Acesso Limitado (Lucas e João)

	Trabalham por meio de branches temporários
	Utilizam GitHub Web, Codespaces ou GitHub Mobile para editar e revisar
	Soluções para Dispositivos Limitados
	GitHub Codespaces: IDE completa no navegador (60h/mês grátis)
	vscode.dev: Edição leve no navegador, conectando direto ao repositório
	GitHub Mobile: Revisão de PRs, comentários e gerenciamento básico
