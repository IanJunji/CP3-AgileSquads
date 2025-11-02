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
