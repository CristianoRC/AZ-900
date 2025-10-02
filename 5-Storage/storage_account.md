# Servicos de Armazenamento

### Storage Count (Contas de Armazenamento)
 - Deve ter um nome globalmente exclusivo.
 - Fornecer acesso a internet em todo o mundo
 - determinar os serviços de armazenamento e as opções de redundância.

   

A **Azure Storage Account** fornece serviços de armazenamento duráveis e escaláveis na nuvem. Ele oferece diferentes tipos de armazenamento para diversos cenários, como dados de blobs, filas, tabelas e arquivos.

## Tipos de Serviços de Armazenamento
- **Blob Storage:** Armazenamento de grandes quantidades de dados não estruturados, como documentos, vídeos e backups.
- **File Storage:** Compartilhamentos de arquivos acessíveis via SMB protocol, úteis para migração de aplicativos legados.
- **Queue Storage:** Armazenamento de mensagens para comunicação entre componentes distribuídos de uma aplicação.
- **Table Storage:** Armazenamento de dados semi-estruturados em uma tabela NoSQL, ideal para armazenar grandes volumes de dados.

## Características Principais
- **Alta Disponibilidade e Durabilidade:** Os dados são replicados para garantir alta disponibilidade e resiliência contra falhas.
- **Segurança:** Suporte a criptografia em repouso e em trânsito, além de gerenciamento de acesso granular.
- **Escalabilidade:** Capacidade de armazenamento massiva e escalabilidade automática para atender demandas crescentes.
- **Gerenciamento de Dados:** Ferramentas para gerenciamento de ciclo de vida de dados e políticas de retenção.

## Casos de Uso Comuns
- **Backup e Recuperação de Desastres:** Armazenar backups de dados críticos.
- **Armazenamento de Dados de Aplicativos:** Armazenamento de grandes volumes de dados de aplicações web e móveis.
- **Compartilhamento de Arquivos:** Fornecer acesso a arquivos para aplicações e usuários distribuídos.
- **Processamento de Mensagens:** Implementar filas para processamento assíncrono de tarefas.

## Links Úteis
Para mais informações detalhadas, consulte a [documentação oficial do Azure Storage](https://learn.microsoft.com/pt-br/azure/storage/common/storage-account-overview).




# Configuração de Redundância do Azure Storage Account

A configuração de redundância no Azure Storage Account garante a alta disponibilidade e durabilidade dos dados. Existem várias opções de redundância disponíveis para atender diferentes necessidades de replicação e durabilidade.

## Tipos de Redundância

### Locally Redundant Storage (LRS)
- **Descrição:** Replica dados três vezes dentro de um único datacenter.
- **Uso:** Ideal para cenários onde os dados não precisam ser replicados em várias regiões.

### Zone-Redundant Storage (ZRS)
- **Descrição:** Replica dados em três zonas diferentes dentro de uma região.
- **Uso:** Protege contra falhas de datacenter ou zona dentro de uma região.

### Geo-Redundant Storage (GRS)
- **Descrição:** Replica dados em uma região primária e, em seguida, replica de forma assíncrona para uma segunda região distante.
- **Uso:** Garantia de durabilidade mesmo em desastres regionais.

### Read-Access Geo-Redundant Storage (RA-GRS)
- **Descrição:** Fornece todas as vantagens do GRS, além de permitir leitura dos dados na região secundária.
- **Uso:** Alta disponibilidade de leitura em caso de indisponibilidade da região primária.

### Geo-Zone-Redundant Storage (GZRS)
- **Descrição:** Combina replicação entre zonas e entre regiões, replicando dados em várias zonas na região primária e em uma região secundária.
- **Uso:** Maior resiliência contra falhas de zona e desastres regionais.

### Read-Access Geo-Zone-Redundant Storage (RA-GZRS)
- **Descrição:** Combina as vantagens do GZRS com a capacidade de leitura dos dados na região secundária.
- **Uso:** Alta disponibilidade de leitura e proteção contra falhas de zona e desastres regionais.

## Características
- **Alta Disponibilidade:** Replicação dos dados para garantir acesso contínuo.
- **Durabilidade:** Proteção contra perda de dados em casos de falhas ou desastres.
- **Segurança:** Criptografia dos dados em repouso e em trânsito.

## Links Úteis
Para mais informações detalhadas, consulte a [documentação oficial do Azure Storage Redundancy](https://learn.microsoft.com/pt-br/azure/storage/common/storage-redundancy).

![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/68783416-5b02-4d53-8f0a-c11447c6df82)



![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/e3334847-0e0d-47a1-8bbf-30034d78336a)

