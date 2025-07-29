# Trabalho-de-PAM
Trabalho de PAM com banco de dados 



Dia 05/08:
	apresentação dos repositórios com os requisitos e temas

Dia 12/08:
	Apresentação do protótipo do projeto



Solução: HospiFlow - Sistema Inteligente de Triagem Hospitalar
	📌 Conceito Principal
	Transforme a recepção hospitalar com um sistema de triagem digital e agendamento dinâmico, eliminando filas físicas e acelerando o atendimento. 
	Os pacientes recebem notificações em tempo real sobre seu status na fila e podem agendar horários com base na disponibilidade médica.

⚙️ Arquitetura do Banco de Dados
	Usaremos um banco de dados híbrido para garantir:

	Escalabilidade (para hospitais de pequeno e grande portes)
	Conformidade com LGPD (dados sensíveis de saúde)
	Integração com prontuário eletrônico (Sistema HIS/PEP)



Funcionamento para Pacientes

	Pré-Triagem Digital (via App/WhatsApp)

	Cadastro rápido ou login existente
	Questionário de sintomas (define prioridade)
	Escolha de médico/disponibilidade
	Agendamento

	Recebe confirmação + tempo estimado
	Opção de "chegar quando chamarem"
	Notificação Inteligente

	"Você é o próximo em 15 min" (GPS detecta proximidade)
	"Sua consulta com Dr. Silva está pronta - Sala 12"

🏥 Painel para Recepção Hospitalar

	Priorização automática (emergência > urgência > eletivo)
	Integração com exames/laboratório (evita filas repetidas)

💡 Diferenciais Competitivos
	✅ Redução de 70% no tempo de espera
	✅ Integração com telemedicina (se sintomas forem leves)
	✅ Relatórios para gestão hospitalar (picos de demanda, médicos mais requisitados)

🔹 Pontos a se observar ainda:

	Sistema de priorização (como evitar abusos?)
	App mobile com NFC para check-in automático
	Versão para clínicas pequenas (baixo custo)




📍 Sugestão Prática para TCC
	App Mobile: Flutter + Firestore (mais documentação)
		(Linguagem de programação: Dart ---> Orientada a objeto, parecido com javascript e c#)

	Backend: Firebase Functions (para notificações)
		(banco de dados em tempo real, autenticação de usuário e notificação para dispositivos móveis)

	Banco: Firestore (NoSQL)
		(banco de dados próprio do firebase)
