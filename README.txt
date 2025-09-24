
# 📌 README – Sistema de Gestão de Projetos (Java)

### **Descrição**
Este é um sistema de gestão de projetos desenvolvido em **Java (console-based)**.  
Permite gerenciar usuários, projetos, equipes e tarefas, com exportação de relatórios em **CSV**.

---

### **Fase 1 – Usuários**
- Cadastro com: Nome completo, CPF, e-mail, cargo.  
- **Login automático**: Nome + Sobrenome + 3 últimos dígitos do CPF.  
- **Senha**: precisa ter pelo menos uma letra maiúscula e um número.  
- Perfis:  
  - **Administrador (PO)** → acesso total e edição.  
  - **Gerente** → visualiza, edita apenas com liberação do Admin.  
  - **Colaborador** → visualiza, pede liberação para editar.  
- Simulação de envio de e-mail com login e senha.  
- Usuários pré-cadastrados:  
  - Lucas Silva (Admin)  
  - Carol Cavalcante (Gerente)  
  - Thamiris Marie (Colaboradora)  
  - Rodrigo Bat (Colaborador)  

---

### **Fase 2 – Projetos e Equipes**
- Criar Projeto: Nome, Descrição, Atuação.  
- Definir prazos: Data de início e data de término prevista.  
- Status do Projeto: Planejando, Em andamento, Concluído, Cancelado.  
- Regras:  
  - Cada usuário pode ter no máximo **4 projetos simultâneos**.  
  - Cada projeto deve ter um **gerente responsável**.  
- Equipes:  
  - Gerente pode adicionar/remover membros.  
  - Colaboradores apenas visualizam.  
  - Observações visíveis a todos no projeto.  

---

### **Fase 3 – Tarefas e Relatórios**
- Cadastro de Tarefas: Título, Descrição, Responsável, Prioridade, Status.  
- Status da Tarefas: Pendente, Concluída, Cancelada.  
- **Conclusão** → Notificação ao Admin/Gerente + agradecimento ao colaborador.  
- **Cancelamento** → Solicita motivo.  
- **Atraso** → Solicita justificativa.  
- Exportação de dados em **CSV** com:  
  - Projeto, Administrador, Gerente, Colaboradores.  
  - Prazos (início e fim).  
  - Situação da entrega (em dia, atrasada ou cancelada).  

---

### **Como Rodar no NetBeans**
1. **Baixe o arquivo ZIP** e **extraia**.  
2. No **NetBeans**: File → Open Project.  
3. Selecione a pasta do projeto extraído (onde está o `pom.xml`).  
4. Abra `SistemaFinal.java` em `src/main/java`.  
5. Clique com o botão direito em `SistemaFinal.java` → **Run File**.  
   *(ou Run no projeto inteiro)*  
6. O sistema inicia no console do NetBeans.  

---

### **Limitações e Observações**
- Aplicação é **console-based** (não tem interface gráfica).  
- **Notificações por e-mail são simuladas no console**.  
- **Recomendado JDK 17+** (necessário para `switch ->` e configuração Maven).  
- O projeto não possui banco de dados real: os dados são armazenados em memória.  
- Relatórios exportados em **CSV simples** (podem ser abertos no Excel).  
- Estrutura preparada para evolução futura: banco de dados, interface gráfica, envio real de e-mails.  
