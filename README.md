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
| Alunos  | Estudante do IFPB  |



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

| Stakeholder | Descrição | Papel |
| :--- | :--- | :--- |
| **DCE (Diretório Central dos Estudantes)** | Entidade que representa os estudantes e atua como cliente do sistema. Co-gerencia o agendamento dos horários livres. | Cliente, Usuário (Moderador) |
| **CEF (Coordenação de Educação Física)** | Órgão responsável pela gestão principal dos espaços esportivos e gerenciamento do calendário de aulas. | Cliente, Usuário (Moderador) |
| **Comunidade Acadêmica (Alunos e Servidores)** | Todos os membros do campus (professores, técnicos, alunos) que precisam consultar a disponibilidade ou solicitar o uso dos espaços. | Usuários (Solicitante, Visualizador) |
| **Gestores (Diretores/Coordenadores)** | Diretores ou coordenadores que não operam o sistema no dia a dia, mas precisam de relatórios e estatísticas de uso dos espaços. | Consumidor de Relatórios |
| **DTI (Diretoria de Tecnologia da Informação)** | Departamento de TI do campus, responsável por fornecer e dar suporte à API de autenticação e dados do SUAP. | Fornecedor de API / Suporte Técnico |
| **Equipe de Desenvolvimento** | Profissionais responsáveis por desenvolver e manter o sistema SIGAE. | Desenvolvedores |
---
| Usuário | Descrição | Responsabilidades | Stakeholders |
| :--- | :--- | :--- | :--- |
| **Solicitante** | **Qualquer membro da comunidade acadêmica** (alunos e servidores) | • Autenticar-se via SUAP.<br>• Consultar horários livres no calendário.<br>• Preencher e enviar formulário de solicitação.<br>• Acompanhar status dos seus pedidos ("Pendente", "Aprovado", "Negado").<br>• Cancelar agendamentos aprovados. | DCE, CEF, Comunidade Acadêmica, Equipe de Desenvolvimento |
| **Moderador / Administrador** | Membros do **DCE** e da **CEF** responsáveis pela operação diária e gestão das solicitações no sistema. | • Gerenciar o painel de solicitações pendentes.<br>• Aprovar ou negar solicitações.<br>• Criar agendamentos recorrentes (ex: aulas).<br>• Bloquear horários para manutenção ou eventos.<br>• Configurar regras de agendamento. | DCE, CEF, Gestores, Equipe de Desenvolvimento |
| **Visualizador** | **Qualquer membro da comunidade acadêmica** (alunos e servidores) que precise consultar a agenda. | • Acessar o sistema para visualizar o calendário público de espaços.<br>• Consultar a disponibilidade (horários livres/ocupados). | Comunidade Acadêmica, DCE, CEF, Equipe de Desenvolvimento |
| **Gestor** | **Diretores ou coordenadores** que não operam o sistema no dia a dia, mas consomem dados gerenciais. | • Acessar um painel (dashboard) com gráficos e estatísticas de uso (ex: taxa de ocupação, horários de pico).<br>• Gerar relatórios de uso dos espaços. | Gestores, DCE, CEF, Equipe de Desenvolvimento |
---


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

