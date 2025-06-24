# Certificação AZ-104 – Resumo Completo

## Alguns temas abordados:
- Implementar, gerenciar e monitorar ambiente Azure.
- Ferramentas: Azure CLI, PowerShell, ARM/Bicep, portal, MS Entra ID.

## 1. Identidades & Governança
O gerenciamento de identidades no Azure começa com o Azure Active Directory (Azure AD), onde administramos usuários, grupos e permissões. É fundamental configurar adequadamente recursos como SSPR (Self-Service Password Reset), permitir o uso de identidades externas (usuários convidados) e aplicar boas práticas de segurança. O uso estratégico de grupos permite gerenciar acessos de forma mais eficiente, enquanto o controle granular com roles simplifica a administração em ambientes maiores.

A governança é mantida por meio de RBAC (Role-Based Access Control), que define quem pode fazer o quê, em qual escopo — seja assinatura, grupo de recursos ou recurso específico. Além disso, o Azure fornece mecanismos como Resource Locks, Tags, Policies e Management Groups, que ajudam na padronização e prevenção de ações indesejadas. Esses recursos também colaboram com a gestão de custos, permitindo segmentar orçamentos e aplicar alertas sobre gastos excessivos, promovendo ambientes mais organizados e seguros.

## 2. Armazenamento
O Azure oferece diversas contas de armazenamento, que podem ser configuradas com diferentes níveis de redundância (como LRS, GRS), tipos de acesso (Hot, Cool, Archive) e regras de segurança (como SAS tokens, firewalls e VNet integration). Esse serviço é fundamental para hospedar desde dados estruturados até arquivos não estruturados, e oferece controle preciso de permissões e políticas de ciclo de vida.

Além disso, o armazenamento de dados pode ser gerenciado com ferramentas como AzCopy, Storage Explorer e serviços de Import/Export. Recursos como Azure Files e Blob Storage possibilitam criar compartilhamentos de rede ou armazenar arquivos de maneira escalável e econômica. Funcionalidades como snapshots, versionamento e políticas de retenção aumentam a segurança e a resiliência dos dados.

## 3. Computação
A base da computação no Azure são as Máquinas Virtuais (VMs), que podem ser implantadas com diferentes tamanhos, discos e estratégias de alta disponibilidade como Availability Sets ou Zones. É possível automatizar a criação dessas máquinas com templates ARM ou Bicep, permitindo reuso, padronização e controle de infraestrutura como código (IaC). Recursos como Azure Disk Encryption (ADE) oferecem mais segurança aos dados em repouso.

Além das VMs, o Azure permite a execução de cargas em contêineres, via Azure Container Instances (ACI) ou Azure Kubernetes Service (AKS), fornecendo elasticidade e escalabilidade. Também é possível hospedar aplicações web em App Services, que simplificam a gestão de deploy, certificados, escalonamento automático e ambientes de staging. Essa flexibilidade permite que o administrador escolha a abordagem ideal para cada cenário de negócio.

## 4. Rede
As redes virtuais (VNets) são a fundação da comunicação no Azure. Com elas, podemos segmentar ambientes em sub-redes, interligá-los por meio de peering, e aplicar rotas personalizadas (UDRs) para controle avançado de tráfego. A integração com DNS personalizados e regras de acesso garante uma comunicação segura e eficiente entre recursos.

No quesito segurança, o Azure oferece NSGs (Network Security Groups) e ASGs (Application Security Groups) para controlar o tráfego de entrada e saída com regras específicas. Recursos como Azure Bastion e Private Endpoints asseguram conexões seguras, sem exposição pública. Para cenários híbridos ou inter-regionais, serviços como VPN Gateway, ExpressRoute e Virtual WAN possibilitam conexões robustas. Já para balanceamento de tráfego, o Azure oferece Load Balancer e Application Gateway (com ou sem WAF), garantindo disponibilidade e distribuição inteligente das cargas.

## 5. Monitoramento & Backup
O Azure Monitor é a principal ferramenta para obter visibilidade do ambiente em nuvem. Ele reúne métricas, logs, alertas, dashboards e integrações com ferramentas externas. Utilizando o Log Analytics, é possível realizar consultas avançadas para investigar eventos e tendências. Com alertas customizados e action groups, é possível configurar respostas automáticas, como envio de e-mails ou execução de scripts.

A continuidade dos serviços é garantida com Azure Backup e Azure Site Recovery (ASR). O Backup permite políticas automatizadas de retenção e recuperação, com suporte a VMs, arquivos, bancos e muito mais. Já o ASR atua como ferramenta de disaster recovery, replicando cargas críticas para outra região ou ambiente, assegurando que o sistema possa continuar operando mesmo diante de falhas graves.
## 6. Monitoramento
No módulo prático final, aplicamos os conceitos aprendidos em um cenário real de monitoramento. Começamos com o deploy de um template ARM, que provisionou os recursos automaticamente. Em seguida, habilitamos o VM Insights para monitorar o desempenho da máquina virtual em tempo real, coletando métricas e logs detalhados através do Azure Monitor.

Com a infraestrutura pronta, criamos uma regra de alerta para notificar a exclusão da VM. Utilizamos action groups para enviar alertas por e-mail, garantindo que eventos críticos fossem rapidamente detectados. Ao excluir propositalmente a máquina, validamos o workflow completo: da detecção automática até o envio do alerta. Essa experiência consolidou a importância da observabilidade contínua em ambientes de produção na nuvem.
