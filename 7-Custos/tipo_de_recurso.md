## Fatores que Afetam os Custos no Azure: Tipos de Recursos

### 1. **Máquinas Virtuais (VMs)**
As VMs são um dos recursos mais comuns no Azure e incluem custos baseados em:
- **Tipo de VM**: VMs variam em tamanho, capacidade de CPU, memória, e características adicionais, como armazenamento SSD ou GPU.
- **Sistema Operacional**: Custos podem variar entre VMs com Windows e Linux.
- **Tempo de Uso**: Cobrança geralmente é por hora ou minuto, dependendo do tempo em que a VM está em execução.
- **Região**: Preços podem variar de acordo com a região geográfica onde a VM está hospedada.

### 2. **Armazenamento**
O Azure oferece vários tipos de serviços de armazenamento, cada um com sua estrutura de custo:
- **Armazenamento de Blobs**: Utilizado para armazenar grandes quantidades de dados não estruturados.
  - **Tipo de Acesso**: Hot, Cool e Archive; cada um com diferentes custos de armazenamento e acesso.
- **Discos Gerenciados**: Utilizados por VMs.
  - **Tipo de Disco**: Standard HDD, Standard SSD, Premium SSD, Ultra SSD.
  - **Tamanho do Disco**: Custos aumentam com a capacidade do disco.
- **Armazenamento de Arquivos**: Serviço de arquivos compartilhados.
- **Armazenamento de Filas e Tabelas**: Para armazenamento de mensagens e dados NoSQL.

### 3. **Banco de Dados**
Serviços de banco de dados no Azure também possuem diferentes estruturas de custo:
- **Azure SQL Database**: Custos baseados em DTUs (Database Transaction Units) ou vCores, espaço de armazenamento e backup.
- **Cosmos DB**: Banco de dados multimodelo, com cobrança baseada em unidades de solicitação (RU/s) e armazenamento.
- **MySQL, PostgreSQL, MariaDB**: Serviços gerenciados com preços baseados em instâncias, armazenamento e backup.

### 4. **Rede**
Serviços de rede podem incluir custos como:
- **Bandwidth (Largura de Banda)**: Transferência de dados entre diferentes regiões ou fora da nuvem Azure.
- **Azure Virtual Network**: Custos por uso de VPNs, gateways de rede e endereços IP públicos.
- **Load Balancer e Application Gateway**: Custos por instância e volume de tráfego processado.

### 5. **Serviços de Identidade e Segurança**
- **Azure Active Directory**: Pode ter custos baseados em edições (Free, Basic, Premium P1, Premium P2).
- **Azure Key Vault**: Custos por operações de armazenamento e uso de chaves e segredos.
- **Azure Security Center**: Planos de segurança com diferentes níveis de proteção e custos.

### 6. **Serviços de Aplicação**
- **Azure App Service**: Hospedagem de aplicações web, APIs e mobile, com custos baseados em planos de serviço (Free, Shared, Basic, Standard, Premium, Isolated).
- **Azure Functions**: Cobrança baseada em número de execuções, tempo de execução e recursos consumidos.
- **Azure Logic Apps**: Custos por execução de workflows e conectores utilizados.

### 7. **Serviços de IA e Machine Learning**
- **Azure Cognitive Services**: Serviços de IA com cobrança baseada em chamadas de API e uso de recursos.
- **Azure Machine Learning**: Custos por instância de computação, armazenamento e outros recursos utilizados para treinamentos e inferências.

### 8. **Serviços de Contêineres**
- **Azure Kubernetes Service (AKS)**: Custos baseados em VMs usadas para o cluster e recursos adicionais.
- **Azure Container Instances (ACI)**: Custos baseados em memória e CPU consumidas por segundo.

### 9. **Serviços de Backup e Recuperação**
- **Azure Backup**: Cobrança baseada em volume de dados protegidos, instâncias e políticas de backup.
- **Azure Site Recovery**: Custos para replicação de VMs e dados para fins de recuperação de desastres.

---

Para mais informações, você pode consultar a [documentação oficial do Azure em português](https://docs.microsoft.com/pt-br/azure/?product=popular).
