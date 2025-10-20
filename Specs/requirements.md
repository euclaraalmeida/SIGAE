#### Requisitos funcionais

Os requisitos funcionais são descritos a seguir.

- [RF001] - Como Aluno, eu gostaria de visualizar os horários disponíveis dos espaços esportivos do meu campus, identificando-os claramente como: "Disponível", "Pendente de Aprovação" (para solicitações de outros alunos) ou "Indisponível" (agendamentos já confirmados), entre os horários possíveis (7h às 22h).

- [RF002] - Como Administrador DCE, eu gostaria de alterar todos os horários agendados dentro do período permitido (7h às 22h), exceto aqueles com a flag “aulas curriculares”.

- [RF003] - Como Administrador CEF, eu gostaria de alterar todos os horários agendados dentro do período permitido (7h às 22h).

- [RF004] - Como Administrador DCE, eu gostaria de aplicar flags em todos os horários agendados, sendo elas: aula curricular, projeto de ensino de professores com equipes oficiais do IFPB, aluno do ensino superior e pessoa externa (como federação esportiva).

- [RF005] - Como Administrador CEF, eu gostaria de aplicar flags em todos os horários agendados, sendo elas: aula curricular, projeto de ensino de professores com equipes oficiais do IFPB, aluno do ensino superior e pessoa externa (como federação esportiva).

- [RF006] - Como Administrador CEF, eu gostaria de excluir horários agendados, independentemente da flag, mediante justificativa válida apresentada pelo usuário responsável pelo agendamento.

- [RF007] - Como Administrador DCE, eu gostaria de excluir horários agendados, exceto aqueles com a flag “aula curricular”, mediante justificativa válida apresentada pelo usuário responsável pelo agendamento.

- [RF008] - Como Aluno, eu gostaria de poder solicitar um agendamento em um espaço esportivo do campus dentro de um horário previamente identificado como "Disponível", com antecedência mínima de 24 horas, para que meu pedido fique pendente de aprovação por um administrador (DCE ou CEF).

- [RF009] - Como Aluno, eu gostaria de receber uma notificação por e-mail sobre o status da minha solicitação de agendamento (ex: "Solicitação Recebida", "Agendamento Confirmado", "Agendamento Negado") e também sobre alteração ou cancelamento.

- [RF010] - Como Administrador DCE, eu gostaria de gerar relatórios semanais e mensais sobre a utilização dos espaços esportivos, a fim de realizar análises de uso.

- [RF011] - Como Administrador DCE, eu gostaria de armazenar termos de responsabilidade com a confirmação da entidade solicitante do espaço esportivo, visando prevenir danos ao local ou eventuais acidentes.

- [RF012] - Como Aluno, eu gostaria de poder solicitar o cancelamento do meu agendamento com antecedência mínima de 24 horas, conforme as regras do sistema, apresentando justificativa válida.

- [RF013] - Como Administrador CEF, eu gostaria de gerenciar usuários, incluindo liberar ou suspender permissões de agendamento conforme critérios internos.

- [RF014] - Como Administrador CEF, eu gostaria de aceitar ou negar solicitações de alteração de horário dos alunos, conforme as regras do sistema, se apresentadas justificativas válidas.

- [RF015] - Como Aluno, eu gostaria de poder solicitar a alteração de horário ou do espaço esportivo presentes no meu agendamento com antecedência mínima de 24 horas, conforme as regras do sistema, apresentando justificativa válida.

- [RF016] - Como Usuário (Aluno, ADM DCE, ADM CEF), eu gostaria de poder realizar login no sistema informando meu usuário (matrícula ou SUAP) e senha, para acessar as funcionalidades permitidas para meu perfil.

- [RF017] - Como Usuário, eu gostaria de poder realizar logout (sair) do sistema de forma segura, para encerrar minha sessão.

- [RF018] - Como Usuário, eu gostaria de ter uma opção de "Esqueci minha senha" na tela de login, para que eu possa redefinir meu acesso através de um link enviado ao meu e-mail cadastrado.

- [RF019] - Como Administrador DCE, eu gostaria de visualizar um painel ou lista com todas as solicitações de agendamento pendentes de aprovação.

- [RF020] - Como Administrador CEF, eu gostaria de visualizar um painel ou lista com todas as solicitações de agendamento pendentes de aprovação.

- [RF021] - Como Administrador DCE, eu gostaria de poder aprovar ou negar as solicitações de agendamento pendentes, exceto aquelas que conflitem com "aulas curriculares".

- [RF022] - Como Administrador CEF, eu gostaria de poder aprovar ou negar todas as solicitações de agendamento pendentes.

<br>

#### Requisitos não-funcionais

Os requisitos não-funcionais são descritos a seguir.

**Disponibilidade**

- [RNF001] - O sistema deve estar disponível para consulta e solicitação de agendamentos 24 horas por dia, 7 dias por semana, 365 dias por ano.

- [RNF002] - O sistema deve ser desenvolvido de forma que possa ser escalável, ou seja, deve ser possível aumentar a capacidade de processamento de requisições sem que haja perda de desempenho em períodos de alta demanda (como inícios de semestre).

**Privacidade e segurança**

- [RNF003] - O sistema deve ser desenvolvido de forma que os dados dos usuários (alunos e administradores) sejam protegidos e não sejam acessíveis por terceiros não autorizados.

- [RNF004] - O sistema deve atender aos requisitos de privacidade da LGPD (Lei Geral de Proteção de Dados).

- [RNF005] - O sistema deve possuir controle de permissões por perfil de usuário (Aluno, ADM DCE, ADM CEF) para limitar o acesso às funções.

- [RNF006] - O sistema deve garantir que as senhas dos usuários sejam armazenadas de forma criptografada, impossibilitando a recuperação da senha original.

- [RNF007] - Toda a comunicação entre o cliente (navegador) e o servidor deve ser feita utilizando criptografia de conexão (HTTPS/SSL).

**Usabilidade**

- [RNF008] - O sistema deve ser desenvolvido de forma que seja fácil de usar e de fácil aprendizado, de forma que os usuários não precisem de treinamento extensivo para utilizá-lo.

- [RNF009] - O design da interface do sistema será semelhante ao do HIFPB (https://joaopessoa.ifpb.edu.br/horario/) para reaproveitar o reconhecimento e a familiaridade dos usuários (alunos e funcionários do IFPB).

- [RNF010] - O sistema deve ser desenvolvido de forma que possa ser acessado por pessoas com deficiência, seguindo padrões básicos de acessibilidade web.

**Suportabilidade (Compatibilidade)**

- [RNF011] - O sistema deve ser desenvolvido de forma que possa ser executado nos três principais navegadores da web: Google Chrome, Mozilla Firefox e Microsoft Edge.

- [RNF012] - O sistema deve ser compatível com os sistemas operacionais mais comuns para computadores e notebooks: Windows e Linux.

**Interoperabilidade**

- [RNF013] - O sistema deve ser desenvolvido de forma que possa ser integrado com o sistema de autenticação central do IFPB (ex: SUAP) para validar o login de Alunos e Administradores.

**Manutenibilidade**

- [RNF014] - O sistema deve ser desenvolvido de forma que possa ser facilmente atualizado e mantido.

- [RNF015] - O sistema deve ser desenvolvido de forma que possa ser facilmente testado e validado, de forma manual e automatizada.

- [RNF016] - O sistema deve ser documentado (código-fonte, APIs e arquitetura) de forma que possa ser facilmente compreendido por terceiros e para facilitar a manutenção.

**Desempenho**

- [RNF017] - O sistema deve ter um tempo de resposta de no máximo 5 segundos para carregar o calendário de horários e submeter uma solicitação de agendamento.

- [RNF018] - O sistema deve ser leve e ter bom desempenho em computadores com especificações básicas, conforme o perfil dos equipamentos disponíveis para os usuários.

- [RNF019] - A interface deve ser simples, sem gráficos pesados, e compatível com resoluções comuns de tela.

**Implementação**

- [RNF020] - O sistema deve ser desenvolvido com APIs de acesso aos dados para que o front-end seja desacoplado do back-end.

**Implantação**

- [RNF021] - O sistema deve ser desenvolvido de forma que possa ser implantado em plataformas de servidor padrão (Linux, com hardware x64).
