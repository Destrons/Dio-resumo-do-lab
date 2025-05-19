---

## ☁️ Modelos de Serviço e Responsabilidade na Nuvem Azure

Esta seção detalha os modelos de serviço disponíveis no Microsoft Azure (IaaS, PaaS e SaaS) e o **modelo de responsabilidade compartilhada**, que define os limites entre as obrigações do provedor (Microsoft) e do cliente.

---

### 🏗️ IaaS, PaaS e SaaS na Azure

Explicação dos três principais modelos de serviço em nuvem oferecidos pelo Azure:

#### 🧱 IaaS (Infrastructure as a Service)
- Provedor fornece: infraestrutura básica (máquinas virtuais, rede, armazenamento).
- Cliente gerencia: sistema operacional, aplicativos, tempo de execução e dados.
- Exemplo: **Azure Virtual Machines**.
- Ideal para: migração lift-and-shift, ambientes legados, controle total sobre o sistema.

#### ⚙️ PaaS (Platform as a Service)
- Provedor fornece: infraestrutura + sistema operacional + plataforma de execução.
- Cliente gerencia: apenas os dados e as aplicações.
- Exemplo: **Azure App Services, Azure SQL Database**.
- Ideal para: desenvolvimento rápido de aplicações, sem se preocupar com manutenção da infraestrutura.

#### 🧩 SaaS (Software as a Service)
- Provedor fornece: aplicação completa pronta para uso.
- Cliente usa: via navegador ou app, sem necessidade de gerenciamento técnico.
- Exemplo: **Microsoft 365, Dynamics 365**.
- Ideal para: uso imediato, colaboração, ferramentas de produtividade e CRM/ERP.

---

### 🛡️ Modelo de Responsabilidade Compartilhada

O modelo de responsabilidade compartilhada define quais aspectos da segurança, conformidade e operações são de responsabilidade da Microsoft e quais cabem ao cliente, variando conforme o modelo de serviço.

| Elemento                   | IaaS                  | PaaS                      | SaaS                      |
|----------------------------|-----------------------|---------------------------|---------------------------|
| Físico (data center)       | Microsoft             | Microsoft                 | Microsoft                 |
| Hardware e rede            | Microsoft             | Microsoft                 | Microsoft                 |
| Sistema operacional        | Cliente               | Microsoft                 | Microsoft                 |
| Aplicação                  | Cliente               | Cliente                   | Microsoft                 |
| Dados                      | Cliente               | Cliente                   | Cliente                   |
| Acesso e identidades       | Cliente               | Cliente                   | Cliente                   |
| Monitoramento de segurança | Compartilhado         | Compartilhado             | Compartilhado             |

**Resumo por modelo:**
- **IaaS:** Maior controle → mais responsabilidades do cliente.
- **PaaS:** Equilíbrio entre controle e conveniência.
- **SaaS:** Conveniência máxima → menor responsabilidade técnica do cliente.

---

> **🎯 Objetivo:** Compreender os diferentes modelos de serviço na nuvem Azure e os limites de responsabilidade entre o cliente e a Microsoft, possibilitando decisões informadas sobre arquitetura, segurança e governança.
