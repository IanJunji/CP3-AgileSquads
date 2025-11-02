# Declaração de Visão do Produto

**Para:** Gestores e colaboradores do Hospital São Rafael

**Cujo:** Processo de gestão de leads, agendamento e acompanhamento de pacientes é atualmente manual e descentralizado, o que resulta em perda de oportunidades de negócio e baixa eficiência operacional.

**O:** HSR-CRM

**É um(a):** Plataforma de gestão de relacionamento com o cliente (CRM) focada na área da saúde.

**Que:** Centraliza e automatiza a jornada do paciente, desde a captação do lead, passando pelo agendamento e chegando até o pós-atendimento. O objetivo é otimizar a conversão de vendas, aumentar a eficiência da equipe e melhorar a experiência do paciente.

**Diferentemente de:** Soluções genéricas de mercado e processos manuais baseados em planilhas.

**O nosso produto:** Oferece uma solução completa, personalizada para as necessidades do Hospital São Rafael, e integrada com o sistema Tasy. A plataforma inclui funis de venda customizados, automação de comunicação via WhatsApp, e dashboards com indicadores de performance em tempo real para apoiar a tomada de decisão estratégica.

<div style="page-break-after: always;"></div>

# Quadro É/Não é, Faz/Não Faz

## É
- Um sistema de CRM para gestão de vendas e relacionamento com o paciente.
- Uma ferramenta para automação da comunicação e acompanhamento da jornada do paciente.
- Uma plataforma para análise de dados de vendas e performance de atendimento.
- Um sistema focado nos processos específicos do Hospital São Rafael.

## Não é
- Um sistema de gestão hospitalar completo (ERP).
- Um sistema de prontuário eletrônico (apesar de se integrar ao Tasy para buscar informações).
- Um sistema de faturamento ou contabilidade.
- Um aplicativo mobile para uso direto dos pacientes.

## Faz
- Captura e centraliza leads de múltiplas fontes (redes sociais, site, etc.).
- Cadastra pacientes, médicos e colaboradores com seus respectivos dados.
- Gerencia la agenda dos médicos, incluindo bloqueios e horários extras.
- Calcula automaticamente o IMC dos pacientes com base em altura e peso.
- Envia lembretes e confirmações de agendamento via WhatsApp/mensagens.
- Rastreia o histórico de interações do paciente em diferentes áreas (vendas, recepção).
- Distribui leads automaticamente para os operadores logados.
- Gera dashboards e relatórios sobre a performance de vendas e atendimento.
- Permite o registro e acompanhamento de reclamações (SAC).
- Integra-se com o sistema Tasy para troca de informações sobre agendamentos.

## Não Faz
- Processa pagamentos de consultas ou procedimentos cirúrgicos.
- Armazena o prontuário médico detalhado do paciente.
- Gerencia o estoque de insumos e medicamentos do hospital.
- Controla a folha de pagamento ou os recursos humanos do hospital.
- Realiza diagnósticos ou prescrições médicas.

<div style="page-break-after: always;"></div>

# Requisitos

## Requisitos Funcionais (RF)

### Gestão de Leads
- **RF01:** O sistema deve permitir a captura de leads de formulários de redes sociais (Instagram, Facebook, Google, TikTok).
- **RF02:** O sistema deve criar contas de lead contendo: nome, telefone, e-mail, canal de entrada, procedimento de interesse e preferência por médico.

### Cadastros Gerais
- **RF03:** O sistema deve permitir o cadastro de Médicos com: Nome, CRM, telefone, e-mail, procedimentos atendidos, data de nascimento e CFPs.
- **RF04:** O sistema deve permitir o cadastro de Colaboradores com: nome, CPF, e-mail e data de nascimento.
- **RF05:** O sistema deve permitir o cadastro de Pacientes com: Nome, CPF, data de nascimento, Sexo, peso, altura, e-mail, telefone e "por onde nos conheceu".
- **RF06:** O sistema deve calcular e armazenar o IMC do paciente automaticamente durante o cadastro.
- **RF07:** O sistema deve validar e impedir a criação de cadastros duplicados (Médicos, Colaboradores, Pacientes) com base em campos-chave (CPF, CRM, e-mail).

### Agendamento
- **RF08:** O sistema deve permitir o agendamento de consultas, associando paciente, data, hora, procedimento e médico.
- **RF09:** O sistema deve permitir a alteração de status de um agendamento (ex: agendado, atendido, falta, cancelado).
- **RF10:** O sistema deve permitir o bloqueio de horários na agenda de um médico, com a inclusão de um motivo.
- **RF11:** O sistema deve permitir a criação de agendas extras para os médicos.

### Jornada do Paciente
- **RF12:** O sistema deve apresentar um histórico completo do paciente, agrupado por áreas (agendamento, vendas, pós-vendas, recepção, mensagens).
- **RF13:** O sistema deve permitir o envio de mensagens manuais e automáticas (confirmações de agendamento) para os pacientes.

### Performance e Atendimento
- **RF14:** O sistema deve registrar e exibir o tempo de entrada do lead até o primeiro atendimento.
- **RF15:** O sistema deve acionar um alerta de tempo mínimo de atendimento não atingido.
- **RF16:** O sistema deve realizar a distribuição automática de leads para os operadores logados.
- **RF17:** O sistema deve redistribuir automaticamente os leads de um operador que fez logout.

### Vendas e Orçamentos
- **RF18:** O sistema deve permitir o registro e acompanhamento de orçamentos de vendas, incluindo status (aberto, em andamento, fechado).

### SAC
- **RF19:** O sistema deve permitir o cadastro de reclamações, com área envolvida, prazo de resposta e motivo.
- **RF20:** O sistema deve permitir anexar documentos a uma reclamação.
- **RF21:** O sistema deve emitir alertas com base no tempo de resposta das reclamações.

### Relatórios e Dashboards
- **RF22:** O sistema deve gerar um dashboard com relatórios de login/logout de colaboradores, atendimentos, mensagens enviadas e ociosidade das agendas.
- **RF23:** O sistema deve permitir a exportação e importação de bases de dados em formato Excel.

### Integração
- **RF24:** O sistema deve realizar integração com o sistema Tasy para agendamentos e troca de informações.

## Requisitos Não Funcionais (RNF)

- **RNF01 (Usabilidade):** A interface deve ser intuitiva, permitindo que um novo usuário realize as operações básicas após um treinamento de no máximo 2 horas.
- **RNF02 (Responsividade):** O sistema deve ser acessível e funcional em navegadores web modernos (Chrome, Firefox, Edge) em desktops e tablets.
- **RNF03 (Performance):** As principais telas de consulta e cadastro devem carregar em menos de 3 segundos.
- **RNF04 (Segurança):** O sistema deve estar em conformidade com a LGPD, garantindo a proteção dos dados sensíveis dos pacientes.
- **RNF05 (Segurança):** O acesso deve ser controlado por perfis de usuário (ex: Administrador, Colaborador, Médico), com diferentes níveis de permissão.
- **RNF06 (Disponibilidade):** O sistema deve garantir uma disponibilidade de 99.5% durante o horário comercial (8h às 18h, de segunda a sexta).

## Regras de Negócio (RN)

- **RN01:** Um lead de um operador que fez logout deve ser reatribuído a um operador ativo em até 5 minutos.
- **RN02:** Não é possível agendar duas consultas para o mesmo médico no mesmo horário.
- **RN03:** O cálculo do IMC (Índice de Massa Corporal) deve seguir a fórmula padrão: `peso / (altura * altura)`.
- **RN04:** Um colaborador do tipo "operador" só pode visualizar os leads e pacientes que estão sob sua responsabilidade.
- **RN05:** Um médico não pode ser descadastrado se possuir agendamentos futuros.

## Requisitos Técnicos (RT)

- **RT01:** A aplicação deve ser desenvolvida com arquitetura web.
- **RT02:** A integração com o sistema Tasy deve ser realizada preferencialmente via API REST.
- **RT03:** O sistema de banco de dados deve ser relacional (ex: PostgreSQL, MySQL ou SQL Server).
- **RT04:** O backend da aplicação deve ser construído em uma tecnologia robusta (ex: Java com Spring, C# com .NET, Python com Django/FastAPI ou Node.js com Express).
- **RT05:** O frontend deve ser desenvolvido utilizando um framework moderno (ex: React, Angular ou Vue.js).
- **RT06:** O sistema deve registrar logs de erros e de operações críticas para fins de auditoria e depuração.

<div style="page-break-after: always;"></div>

# Personas

## Persona 1: Colaborador (Atendimento/Vendas)

**Nome:** Carla Almeida

**Idade:** 28 anos

**Ocupação:** Analista de Atendimento no Hospital São Rafael

**Perfil:**
Carla é comunicativa, organizada e ágil. Ela é a linha de frente no contato com os pacientes, desde o primeiro interesse (lead) até o agendamento da consulta. Ela lida com um grande volume de informações diariamente e precisa de ferramentas que otimizem seu tempo e a ajudem a não perder nenhuma oportunidade de negócio para o hospital.

**Frustrações (Dores):**
- "Perco muito tempo alternando entre planilhas, WhatsApp e o sistema de agendamento."
- "Às vezes, dois colaboradores entram em contato com o mesmo lead, causando uma má impressão."
- "É difícil ter uma visão clara de todo o histórico do paciente para oferecer um atendimento personalizado."
- "Sinto que algumas oportunidades são perdidas por falta de um acompanhamento (follow-up) sistemático."

**Objetivos (Ganhos):**
- "Gostaria de ter todas as informações e interações do paciente em um único lugar."
- "Quero um sistema que me ajude a saber qual lead devo priorizar."
- "Preciso de mais agilidade para consultar a agenda dos médicos e marcar procedimentos."
- "Seria ótimo ter lembretes automáticos para fazer o follow-up com os pacientes na data certa."

**Habilidades com Tecnologia:**
Usuária intermediária. Sente-se confortável usando softwares de gestão, planilhas e ferramentas de comunicação online, mas não possui conhecimento técnico em programação.

---

## Persona 2: Médico

**Nome:** Dr. Ricardo Oliveira

**Idade:** 45 anos

**Ocupação:** Cirurgião Ortopedista no Hospital São Rafael

**Perfil:**
Dr. Ricardo é um médico muito respeitado e com uma agenda cheia. Sua prioridade máxima é o bem-estar de seus pacientes. Ele não tem muito tempo para lidar com sistemas complexos, mas precisa que sua agenda de consultas e cirurgias esteja perfeitamente organizada para evitar conflitos e garantir que ele possa atender a todos.

**Frustrações (Dores):**
- "Recebo informações desencontradas sobre o status dos meus pacientes agendados."
- "Às vezes ocorrem falhas de comunicação e minha agenda fica com buracos ou sobreposições."
- "Gostaria de ter uma visão rápida dos procedimentos agendados para a semana, sem precisar pedir para a recepção."
- "A falta de um paciente sem aviso prévio atrapalha todo o meu planejamento do dia."

**Objetivos (Ganhos):**
- "Quero ter acesso fácil e rápido à minha agenda, de qualquer lugar."
- "Preciso que o sistema me notifique sobre cancelamentos o mais rápido possível para otimizar meu tempo."
- "Gostaria de poder bloquear horários na minha agenda para compromissos pessoais de forma simples."
- "Ter um relatório de quantos atendimentos realizei e quais procedimentos foram mais comuns seria útil para meu controle."

**Habilidades com Tecnologia:**
Usuário básico. Utiliza smartphones e computadores para tarefas do dia a dia (e-mail, prontuário eletrônico), mas prefere sistemas que sejam extremamente simples e diretos ao ponto.

---

## Persona 3: Gestor

**Nome:** Fernando Lima

**Idade:** 52 anos

**Ocupação:** Diretor de Operações do Hospital São Rafael

**Perfil:**
Fernando é o responsável por garantir a eficiência e a rentabilidade do hospital. Ele tem um perfil analítico e está constantemente buscando maneiras de otimizar processos e aumentar a receita. Ele não opera o sistema no dia a dia, mas consome os dados e relatórios gerados para tomar decisões estratégicas.

**Frustrações (Dores):**
- "Não temos dados confiáveis sobre nosso funil de vendas e taxa de conversão."
- "É difícil medir a produtividade da equipe de atendimento e identificar gargalos no processo."
- "Tomamos muitas decisões com base na intuição, e não em dados concretos."
- "Perdemos receita por causa da ociosidade não gerenciada na agenda de alguns médicos."

**Objetivos (Ganhos):**
- "Quero um dashboard em tempo real com os principais KPIs: taxa de conversão, tempo médio de atendimento, leads por canal, etc."
- "Preciso de relatórios que me mostrem quais canais de marketing trazem os leads mais qualificados."
- "Gostaria de entender a taxa de conversão por procedimento e por médico para otimizar a oferta."
- "Quero ter a capacidade de exportar dados para fazer análises mais profundas no Excel ou em nossa ferramenta de BI."

**Habilidades com Tecnologia:**
Usuário avançado. Tem familiaridade com planilhas complexas (tabelas dinâmicas, PROCV) e sistemas de BI (Business Intelligence) para análise de dados.

<div style="page-break-after: always;"></div>

# Mapa de Empatia

## Mapa de Empatia 1: Carla Almeida (Colaboradora)

### O que ela PENSA e SENTE?
- **Pensa:** "Preciso ser mais produtiva para bater minhas metas." "Será que estou dando a devida atenção a todos os leads?" "Esse paciente parece ansioso, preciso tranquilizá-lo e ser eficiente."
- **Sente:** Ansiedade para não perder informações importantes. Satisfação ao conseguir ajudar um paciente e fechar um agendamento. Frustração quando o sistema é lento ou falha. Pressão para ser multitarefa.

### O que ela VÊ?
- Telas de computador com múltiplas abas abertas (planilhas, sistema antigo, WhatsApp Web).
- Listas de pacientes para contatar, muitas vezes em papéis ou arquivos desorganizados.
- Agendas dos médicos, com informações que nem sempre estão atualizadas em tempo real.
- Colegas de trabalho também sobrecarregados, fazendo as mesmas perguntas repetidamente.

### O que ela FALA e FAZ?
- **Fala:** "Só um momento, estou verificando a agenda do Dr. Ricardo." "Qual o melhor horário para o senhor(a)?" "Vou confirmar seus dados, um instante." "Sistema caiu de novo!"
- **Faz:** Passa a maior parte do dia no telefone ou respondendo mensagens. Alimenta planilhas manualmente. Tenta manter um registro próprio das suas interações. Conversa com médicos e outros colaboradores para confirmar informações.

### Quais são suas DORES (Frustrações)?
- Falta de uma fonte única e confiável de informação.
- Retrabalho ao ter que inserir a mesma informação em lugares diferentes.
- Risco de cometer erros por causa de processos manuais e desorganizados.
- Dificuldade em priorizar qual lead contatar primeiro.
- Comunicação ineficiente com o resto da equipe.

### Quais são suas NECESSIDADES (Ganhos)?
- Agilidade e eficiência no processo de atendimento.
- Ter uma visão 360º do paciente em uma única tela.
- Automação de tarefas repetitivas (como o envio de lembretes de consulta).
- Confiança nos dados apresentados pelo sistema (agenda, status do paciente).
- Metas claras e uma forma de medir seu próprio desempenho e comissões.

---

## Mapa de Empatia 2: Dr. Ricardo Oliveira (Médico)

### O que ele PENSA e SENTE?
- **Pensa:** "Preciso focar 100% no paciente que está na minha frente." "Será que a recepção me avisou sobre aquele cancelamento?" "Tenho um compromisso pessoal às 18h, não posso me atrasar hoje." "Qual é o próximo procedimento?"
- **Sente:** Pressão constante do tempo. Preocupação com o bem-estar dos pacientes. Irritação com desorganização e falhas de comunicação. Satisfação ao realizar um procedimento bem-sucedido.

### O que ele VÊ?
- A agenda do dia, seja em um tablet, computador ou impressa pela equipe.
- Pacientes na sala de espera.
- O prontuário eletrônico do paciente durante a consulta.
- Notificações no celular sobre a agenda (ou a falta delas).
- Corredores movimentados do hospital.

### O que ele FALA e FAZ?
- **Fala:** "Qual o próximo paciente?" "Por favor, confirme o agendamento da cirurgia para sexta-feira." "Preciso de 15 minutos livres entre as 10h e as 11h para uma ligação." "Esse paciente das 14h faltou?"
- **Faz:** Realiza consultas e cirurgias. Acessa o sistema para visualizar sua agenda. Pede para a equipe da recepção fazer ajustes nos horários. Tenta organizar seu dia em meio aos imprevistos.

### Quais são suas DORES (Frustrações)?
- Agenda desorganizada com furos ou agendamentos sobrepostos.
- Falta de visibilidade e autonomia sobre o que foi agendado para ele.
- Ser interrompido durante o atendimento por questões administrativas que poderiam ser resolvidas pelo sistema.
- Não ser notificado a tempo sobre cancelamentos, gerando tempo ocioso e perda de receita.

### Quais são suas NECESSIDADES (Ganhos)?
- Uma agenda clara, confiável e acessível de qualquer lugar (principalmente do celular).
- Autonomia para realizar pequenos ajustes e bloqueios em sua própria agenda.
- Notificações automáticas e em tempo real sobre eventos importantes (cancelamentos, novos agendamentos).
- Minimizar o tempo gasto com tarefas administrativas para focar no atendimento ao paciente.

---

## Mapa de Empatia 3: Fernando Lima (Gestor)

### O que ele PENSA e SENTE?
- **Pensa:** "Precisamos aumentar nossa taxa de conversão em 15% este semestre." "Qual canal de marketing está nos dando o melhor ROI?" "A equipe de atendimento está sendo produtiva o suficiente?" "A ociosidade na agenda dos médicos está nos custando caro."
- **Sente:** Preocupação com as metas e a saúde financeira do hospital. Confiança quando vê os números melhorando. Frustração com a falta de dados precisos para tomar decisões. Pressão do conselho administrativo por resultados.

### O que ele VÊ?
- Dashboards de BI (Business Intelligence) com gráficos e KPIs.
- Relatórios financeiros e de performance em planilhas e apresentações.
- Gráficos de tendências e projeções de receita.
- Reuniões com as equipes para entender os desafios operacionais e cobrar resultados.

### O que ele FALA e FAZ?
- **Fala:** "Qual a nossa taxa de conversão de leads este mês?" "Preciso de um relatório de atendimentos por médico e por procedimento." "Vamos investir mais no canal que está trazendo mais pacientes qualificados." "Precisamos otimizar a ocupação das agendas para aumentar a receita."
- **Faz:** Analisa dados e relatórios. Define metas para as equipes. Cobra resultados. Participa de reuniões estratégicas. Aprova investimentos em novas ferramentas e tecnologias que comprovem seu valor.

### Quais são suas DORES (Frustrações)?
- Dados pouco confiáveis, descentralizados ou desatualizados.
- Incapacidade de medir o desempenho da equipe e do funil de vendas de forma objetiva.
- Dificuldade em identificar os gargalos e as principais causas da perda de receita.
- Tomar decisões estratégicas importantes com base em "achismos" ou intuição.

### Quais são suas NECESSIDADES (Ganhos)?
- Acesso a dados consolidados e confiáveis em tempo real.
- Dashboards visuais e fáceis de interpretar com os principais KPIs do negócio.
- Relatórios customizáveis para analisar diferentes cenários e responder a perguntas de negócio.
- Ter uma visão clara e completa do funil de vendas, desde a aquisição do lead até a conversão final.
