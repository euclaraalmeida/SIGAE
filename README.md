# Visão do Produto
## SIGAE - Sistema de Gerenciamento e Agendamento de Espaços Esportivos 🏐
Versão 1

## Histórico de revisões

| Data       | Versão | Descrição                      | Autor             |
|------------|--------|--------------------------------|-------------------|
| 14/10/2025 | 1.0    | Criação do documento           | Clara Almeida     |


# Introdução

O Documento de Visão do Produto (DVP) é um documento que descreve o produto de software que será desenvolvido. Ele descreve o problema que será resolvido, as principais necessidades dos stakeholders, as principais funcionalidades do sistema, as restrições do projeto, etc.

## Propósito

O objetivo deste documento é coletar, analisar e definir características e as necessidades de alto nível do **Sistema de Gerenciamento e Agendamento de Espaços Esportivos (SIGAE)**

Ele se concentra nos recursos necessários aos stakeholders e aos usuários, e nas razões que levam a essas necessidades.

Os detalhes de como o **Sistema de Gerenciamento e Agendamento de Espaços Esportivos (SIGAE)** atingem essas necessidades são descritos nas _especificações de casos de uso_ e nos _requisitos funcionais_.

### Abreviações

| Termo | Definição                                    |
| :---: | -------------------------------------------- |
|  DCE  | Diretório Central dos Estudantes                 |
|  CEF  | Coordenação de Educação Física         |


### Definições

|    Termo    | Definição                                                                                                                       |
| :---------: | ------------------------------------------------------------------------------------------------------------------------------- |
|   Diretório Central dos Estudantes | Setor que faz a intermediação da CEF para os estudantes|
|  Coordenação de Educação Física  | Setor responsável pela gestão pedagógica e das atividades que utilizaram os espaços esportivos  |
| Aluno | Estudante do IFPB  |



## Escopo do produto

O **Sistema de Gerenciamento e Agendamento de Espaços Esportivos (SIGAE)** é um sistema que tem como objetivo substituir o método informal e descentralizado (WhatsApp) por uma plataforma centralizada, transparente e automatizada para solicitação, aprovação e consulta de horários de uso das quadras e outros espaços esportivos do campus, utilizando o SUAP como base para autenticação e identificação dos usuários.

---

# Posicionamento

## Oportunidade de negócios

1.**Centralizar e Formalizar os Pedidos**: Substituir o caos do grupo de WhatsApp e o trabalho manual por um sistema oficial, organizado e justo.

2. **Garantir a Disponibilidade Real**: Mostrar no calendário apenas os horários que estão realmente livres, já descontando as aulas e atividades prioritárias.

3.**Vizualização**: Criar um calendário público onde qualquer aluno ou servidor possa consultar o que está livre ou ocupado em tempo real, acabando com a confusão de informações.

4.**Criar um Registro Digital e de Responsabilidade** : Saber exatamente quem (nome e matrícula) reservou e usou cada horário, permitindo a criação de termos de responsabilidade digitais e tirando o risco das costas do DCE.

## Descrição dos benefícios para os clientes e dos problemas resolvidos

| Benefícios | Problemas Resolvidos | Afetados |
| :--- | :--- | :--- |
| **Automação e Otimização do Tempo** | Processo manual de intermediação, consolidação e distribuição de horários feito pelo DCE, que depende de WhatsApp. | Moderadores/Gestores (DCE e CEF) |
| **Comunicação Eficiente e Clara** | Falta de notificações automáticas sobre o status dos agendamentos (pendente, aprovado, negado). | Solicitantes (Representantes de curso, servidores) |
| **Transparência e Centralização** | Desorganização e "confusão" causadas por informações descentralizadas (Google Agenda e WhatsApp). Professores bloqueiam espaços que acabam não utilizando. | Todos os usuários (Estudantes, Servidores, DCE, CEF) |
| **Responsabilização e Auditoria** | Falta de registro formal de qual indivíduo utilizou o espaço. A responsabilidade por danos recai inteiramente sobre o DCE, que assina termos físicos. | Gestores (DCE, CEF) e Solicitantes |
| **Acesso Justo (Democratização)** | A regra atual de "quem pediu primeiro" no WhatsApp não garante a hierarquia oficial de prioridades (Aulas > Projetos > Alunos), limitando a "democratização" do espaço. | Solicitantes (Representantes de curso) e Gestores/Moderadores (CEF) |

---
# Descrição dos stakeholders e dos usuários
Esta seção descreve os stakeholders e os usuários do Sistema de Controle de Garantias de Produtos (SCGP).

## Stakeholders
Segue abaixo a lista de stakeholders.

| Stakeholder | Descrição | Papel |
| :--- | :--- | :--- |
| **DCE (Diretório Central dos Estudantes)** | Entidade que representa os estudantes e atua como cliente do sistema. Gerencia o agendamento dos horários livres disponíveis para os membros da comunidade acadêmica. | Cliente, Usuário (Moderador) |
| **CEF (Coordenação de Educação Física)** | Órgão responsável pela gestão principal dos espaços esportivos e gerenciamento do calendário de aulas. | Cliente, Usuário (Moderador) |
| **Comunidade Acadêmica (Alunos e Servidores)** | Todos os membros do campus (professores, técnicos, alunos) que precisam consultar a disponibilidade ou solicitar o uso dos espaços. | Usuários (Solicitante, Visualizador) |
| **Gestores (Diretores/Coordenadores)** | Diretores ou coordenadores que não operam o sistema no dia a dia, mas precisam de relatórios e estatísticas de uso dos espaços. | Consumidor de Relatórios |
| **DTI (Diretoria de Tecnologia da Informação)** | Departamento de TI do campus, responsável por fornecer e dar suporte à API de autenticação e dados do SUAP. | Fornecedor de API / Suporte Técnico |
| **Equipe de Desenvolvimento** | Profissionais responsáveis por desenvolver e manter o sistema SIGAE. | Desenvolvedores |


## Usuários e atores
Segue tabela com os usuários e atores do sistema:
| Usuário | Descrição | Responsabilidades | Stakeholders |
| :--- | :--- | :--- | :--- |
| **Solicitante** | **Qualquer membro da comunidade acadêmica** (alunos e servidores) | • Autenticar-se via SUAP.<br>• Consultar horários livres no calendário.<br>• Preencher e enviar formulário de solicitação.<br>• Acompanhar status dos seus pedidos ("Pendente", "Aprovado", "Negado").<br>• Cancelar agendamentos aprovados. | DCE, CEF, Comunidade Acadêmica, Equipe de Desenvolvimento |
| **Moderador / Administrador** | Membros do **DCE** e da **CEF** responsáveis pela operação diária e gestão das solicitações no sistema. | • Gerenciar o painel de solicitações pendentes.<br>• Aprovar ou negar solicitações.<br>• Criar agendamentos recorrentes (ex: aulas).<br>• Bloquear horários para manutenção ou eventos.<br>• Configurar regras de agendamento. | DCE, CEF, Gestores, Equipe de Desenvolvimento |
| **Visualizador** | **Qualquer membro da comunidade acadêmica** (alunos e servidores) que precise consultar a agenda. | • Acessar o sistema para visualizar o calendário público de espaços.<br>• Consultar a disponibilidade (horários livres/ocupados). | Comunidade Acadêmica, DCE, CEF, Equipe de Desenvolvimento |
| **Gestor** | **Diretores ou coordenadores** que não operam o sistema no dia a dia, mas consomem dados gerenciais. | • Acessar um painel (dashboard) com gráficos e estatísticas de uso (ex: taxa de ocupação, horários de pico).<br>• Gerar relatórios de uso dos espaços. | Gestores, DCE, CEF, Equipe de Desenvolvimento |
---

# Descrição do ambiente de uso
## Ambiente de uso

### 1. Ambiente do Usuário (Público e Solicitante):
1.  **Visualizadores** podem acessar publicamente o calendário para consultar a disponibilidade dos espaços.
2.  **Solicitantes (Alunos, servidores)** precisam se autenticar (via SUAP) para submeter pedidos de agendamento.
3.  O acesso será feito através de um navegador web padrão (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari) em dispositivos como computadores, smartphones e tablets.
4.  O sistema será acessado pela internet através de um endereço web (ex: sigae.ifpb.edu.br).
  
### 2. Ambiente de Moderação (Restrito):
5.  **Moderadores** utilizam o sistema para aprovar/negar solicitações, gerenciar o calendário e bloquear horários (ex: aulas).
6.  **Gestores** utilizam o sistema para acessar painéis de estatísticas (dashboards) e gerar relatórios de uso.
7.  Este ambiente é acessado preferencialmente via navegador web em um computador, devido à natureza das tarefas de gerenciamento.
   
### 3. Ambiente de Teste:
8.  O ambiente de teste é acessado através de um navegador web e requer um login de acesso específico para este ambiente.


## Necessidades principais quanto ao ambiente

| Necessidade | Prioridade | Interesse | Solução Atual | Soluções Propostas |
| :--- | :--- | :--- | :--- | :--- |
| **Qualidade:** O sistema deve ser confiável, livre de erros e falhas, garantindo que os agendamentos sejam registrados corretamente sem duplicidade. | **Alta** | A comunidade espera que o sistema seja justo e confiável. Uma falha pode gerar conflitos de horário, como ocorre hoje. | O controle é manual (WhatsApp/Google Agenda) e pode ter erros humanos, desorganização e falhas de comunicação. | Implementar testes automatizados (unitários, integração) e um processo de QA. Realizar Testes de Aceitação do Usuário com o DCE e a CEF. |
| **Desempenho:** O sistema deve ter um tempo de resposta rápido, especialmente na visualização do calendário. | **Alta** | Sendo um recurso de "alta demanda" ("super lotada"), o sistema precisa ser rápido para muitos usuários consultando horários simultaneamente. | O WhatsApp é instantâneo, mas caótico. O Google Agenda é lento para atualizar e consultar. | Otimização de consultas ao banco de dados (especialmente para o calendário), uso de cache para o calendário público e otimizações de front-end. |
| **Escalabilidade:** O sistema deve suportar picos de acesso (ex: início de semestre, abertura de agenda) sem lentidão. | **Moderada** | A base de usuários é o campus), mas os picos de acesso simultâneo podem ser altos. | (O sistema atual não é escalável e gera sobrecarga de trabalho manual nos moderadores). | Arquitetura de aplicação e banco de dados otimizada para consultas, hospedada em infraestrutura robusta. |
| **Segurança:** O sistema deve garantir que apenas usuários autorizados possam pedir horários e que apenas Moderadores possam aprovar/negar. | **Alta** | A segurança garante a legitimidade dos pedidos e a integridade do calendário. | Inexistente. O controle de acesso no WhatsApp é frágil e a edição do Google Agenda é centralizada em uma pessoa. | Integração com SUAP para autenticação. Implementar Controle de Acesso para os diferentes perfis (Solicitante, Moderador, Gestor). |
| **Usabilidade:** O sistema deve ser fácil de usar e intuitivo, tanto para solicitar quanto para gerenciar horários. | **Alta** | O sistema precisa ser mais fácil de usar do que o processo atual (WhatsApp) para garantir a adoção pelos usuários. | O WhatsApp é "fácil" de enviar mensagem, mas "difícil" de gerenciar. O Google Agenda não é intuitivo para esse fim. | Prototipação e realização de testes de usabilidade com alunos, DCE e CEF.|
| **Tempo de resposta:** O sistema deve atualizar o calendário (ex: de "livre" para "ocupado") imediatamente após uma aprovação. | **Alta** | A informação precisa ser em tempo real para evitar que dois usuários tentem agendar o mesmo horário vago. | Lento. O processo manual de atualizar o Google Agenda após um pedido no WhatsApp não é em tempo real. | Otimizações de performance  e uso de tecnologias que permitam atualização em tempo real se necessário. |
| **Confidencialidade:** O sistema deve proteger os dados pessoais (nome, matrícula) dos usuários e o histórico de agendamentos. | **Moderada** | Os dados (nome, matrícula) vêm do SUAP e devem ser protegidos. O histórico de uso deve ser acessível apenas por gestores/moderadores. | Insegura. Grupos de WhatsApp expõem números de telefone e informações de todos os membros. | Armazenar o mínimo de dados necessários do SUAP. Garantir que apenas usuários autorizados possam ver os registros. |

### Alunas Responsáveis pelo projeto 
<table>
  <tr>
    <td align="center">
      <a href="https://github.com/clarabalcantara">
        <img src="https://github.com/clarabalcantara.png" width="120" height="120" style="border-radius: 50%; border: 3px solid #4CAF50;"/>
      </a>
      <br>
      <strong><a href="https://github.com/oiclai" style="text-decoration: none; color: #4CAF50;">Clara Alcantara</a></strong>
    </td>
    <td align="center">
      <a href="https://github.com/euclaraalmeida">
        <img src="https://github.com/euclaraalmeida.png" width="120" height="120" style="border-radius: 50%; border: 3px solid #4CAF50;"/>
      </a>
      <br>
      <strong><a href="https://github.com/euclaraalmeida" style="text-decoration: none; color: #4CAF50;">Maria Clara Almeida</a></strong>
    </td>
    <td align="center">
      <a href="https://github.com/marisarinho">
        <img src="https://github.com/marisarinho.png" width="120" height="120" style="border-radius: 50%; border: 3px solid #4CAF50;"/>
      </a>
      <br>
      <strong><a href="https://github.com/marisarinho" style="text-decoration: none; color: #4CAF50;">Mariana Sarinho</a></strong>
    </td>
  </tr>
</table>

