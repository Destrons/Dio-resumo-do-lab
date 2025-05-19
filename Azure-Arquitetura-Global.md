---

## 🏗️ Arquitetura do Azure e Estrutura Global

Este conteúdo aprofunda a compreensão sobre a infraestrutura global da Microsoft Azure, abordando **regiões, zonas de disponibilidade, replicação de dados, criação de grupos de recursos**, e aspectos fundamentais para **residência de dados, governança e segurança**.

---

### 🌍 Infraestrutura Global do Azure

- **Mais de 60 regiões Azure** distribuídas globalmente, permitindo implantação estratégica de recursos com menor latência e alta disponibilidade.
- Regiões brasileiras:
  - **Brazil South (São Paulo):** Região principal disponível para todos os clientes.
  - **Brazil Southeast (Rio de Janeiro):** Região voltada a clientes que requerem **disaster recovery com residência de dados no Brasil**, como exige a **LGPD**.
- **Residência de dados:** Alguns recursos em Brazil South são replicados para os EUA por padrão; Brazil Southeast permite replicação **nacional**, mediante solicitação formal à Microsoft.

---

### 🛰️ Replicação e Conformidade

- **Cenário com LGPD:** Dados sensíveis não podem ser replicados automaticamente para fora do Brasil.
- A replicação interna entre regiões (ex: Brazil South ↔ Brazil Southeast) exige **contrato e aprovação da Microsoft**.
- As regiões são conectadas por cabos submarinos e infraestrutura própria que garantem comunicação e replicação segura.

---

### 🏢 Tour Virtual em Data Centers

- A Microsoft disponibiliza um **tour virtual interativo** dos seus data centers, mostrando:
  - **Centro de operações (NOC)**
  - **Salas de servidores**
  - **Áreas mecânicas**
  - **Camadas de segurança**
- Proporciona uma visão clara da **escala, modernização e segurança física** da infraestrutura Azure.

---

### 📦 Grupos de Recursos (Resource Groups)

- São **containers lógicos** que agrupam recursos do Azure com o mesmo ciclo de vida e políticas.
- Permitem:
  - Gerenciar permissões de forma granular.
  - Aplicar políticas e tags para organização e controle de custos.
  - Auditar ações através de logs de atividades.
  - Realizar automações e implantações mais organizadas.

---

### 🔐 Segurança, Permissões e Boas Práticas

- **Permissões baseadas em função (RBAC):** Conceda apenas o acesso necessário para cada usuário.
- **Bloqueios (Locks):** Impedem a exclusão acidental ou maliciosa de recursos críticos.
- Exemplo real citado: Exclusão de todos os recursos por um ex-funcionário causou paralisação de três dias – reforçando a importância de políticas e bloqueios.

---

### 🧠 Implantação via Código e Automação

- Recursos criados via portal geram templates (ARM/JSON) que podem ser baixados e reutilizados para automação.
- Ideal para replicar ambientes, padronizar configurações e realizar **deploys em larga escala**.

---

> **🎯 Objetivo:** Capacitar o profissional a entender a arquitetura física e lógica do Azure, tomando decisões seguras, eficientes e alinhadas à legislação nacional (como LGPD), além de dominar ferramentas de gerenciamento, automação e segurança.
