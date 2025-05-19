---

## 💻 Computação e Serviços de Rede no Microsoft Azure

Este material explora com profundidade os conceitos e práticas de **computação em nuvem** e **serviços de rede** no Microsoft Azure. São abordados os principais recursos, como máquinas virtuais, dimensionamento automático, área de trabalho virtual, Azure Functions, entre outros, com foco na implementação prática e boas práticas de gestão e segurança.

---

### ⚙️ Máquinas Virtuais (VMs)

- **Criação de VMs via portal Azure**, com opções de pré-configuração para diferentes cenários (teste, produção, otimização de memória/CPU).
- **Modelos prontos com aplicações integradas**, como WordPress, Redis, MySQL.
- **Escolha da região** (ex: East US, Brazil South) impacta em preço e latência.
- **Zonas de disponibilidade** garantem alta disponibilidade ao distribuir recursos entre data centers distintos.
- **Dimensionamento automático (scale sets)** permite que a VM aumente ou reduza sua capacidade com base em métricas (ex: CPU > 80%).
- **Instâncias Spot:** VMs temporárias com desconto, ideais para ambientes de teste, pois podem ser desligadas a qualquer momento se houver demanda de outro cliente.

---

### 📊 Dimensionamento e Performance

- **Escalabilidade horizontal**: Adição automática de instâncias com base na utilização de CPU.
- **Configuração de escalonamento automático**, com número mínimo, máximo e políticas de crescimento/redução.
- **Séries de VMs**: Cada série (D, B, E, H, etc.) tem foco em cargas específicas — uso geral, memória otimizada, segurança, etc.

---

### 🧹 Boas Práticas e Otimizações

- **Excluir recursos com a VM**: Evita a geração de custos com discos órfãos, IPs públicos e NICs esquecidos.
- **Permissões mínimas**: Evite deixar portas como 3389 (RDP) abertas na internet.
- **Regiões diferentes não compartilham redes virtuais** — é necessário criar uma rede para cada região.

---

### 🖥️ Área de Trabalho Virtual do Azure (AVD)

- Alternativa moderna à entrega de máquinas físicas a colaboradores.
- **Host pessoal**: Sessão dedicada a um único usuário (para software licenciado ou personalizado).
- **Host em pool**: Compartilhamento entre múltiplos usuários, com balanceamento de carga (ex: 5 usuários por host).
- Integração com Microsoft 365 e configuração baseada em imagem personalizada.

---

### ⚡ Azure Functions (Aplicativos de Função)

- Permite executar código sob demanda de forma **serverless**.
- **Suporte a várias linguagens**: Python, Node.js, .NET, Java, entre outras.
- **Ambiente influencia na escolha da linguagem**: ex. Python → Linux, .NET → Windows.
- **Importância na prova**: Entender que funções com linguagens diferentes podem exigir ambientes separados.

---

### 🛡️ Segurança, Monitoramento e Backup

- **Regras de acesso por IP**, alertas de segurança e exposição de portas públicas devem ser evitados em produção.
- **Monitoramento e alertas personalizados** podem ser configurados via métricas (CPU, disco, memória).
- **Backup opcional com múltiplas execuções diárias**, ideal para ambientes críticos. Exige criação de um "cofre" (vault).

---

### 🔁 Automatização e Agendamentos

- **Desligamento automático programado** disponível no portal.
- **Ligamento automático** não está disponível por padrão — recomenda-se uso de **Automation Account** para scripts de start/stop.
- **Extensões e agentes** podem ser instalados automaticamente ao criar a VM (ex: Application Insights, antivírus, etc.).

---

> **🎯 Objetivo:** Capacitar a operar máquinas virtuais, automatizar operações, criar ambientes de trabalho virtualizados e utilizar funções serverless no Azure, sempre com foco em escalabilidade, segurança e conformidade com boas práticas.
