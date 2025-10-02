# Azure Files

O **Azure Files** é um serviço de compartilhamento de arquivos totalmente gerenciado que permite acessar arquivos via protocolos SMB e NFS. Ele oferece uma experiência de compartilhamento de arquivos semelhante à dos servidores de arquivos tradicionais, com a escalabilidade e segurança do Azure.

## Características Principais

- **Compatibilidade com SMB e NFS:** Suporte para os protocolos de compartilhamento de arquivos SMB (Server Message Block) e NFS (Network File System).
- **Gerenciamento Simples:** Fácil de configurar e gerenciar via Portal do Azure, CLI ou PowerShell.
- **Alta Disponibilidade:** Compartilhamentos de arquivos são replicados para garantir alta disponibilidade.
- **Segurança:** Integração com Azure Active Directory (AD) para controle de acesso baseado em identidade e criptografia em repouso.

## Casos de Uso Comuns

- **Migração de Aplicações:** Facilita a migração de aplicações que dependem de compartilhamentos de arquivos.
- **Ambientes de Desenvolvimento e Teste:** Compartilhamento de arquivos para equipes de desenvolvimento e teste.
- **Armazenamento de Dados de Aplicativos:** Armazenamento centralizado de arquivos para acesso por múltiplas instâncias de aplicativos.

## Funcionalidades Adicionais

- **Snapshots:** Captura de snapshots de compartilhamentos de arquivos para recuperação de dados.
- **Redimensionamento Dinâmico:** Ajuste de capacidade de armazenamento conforme necessário.
- **Híbrido com Azure File Sync:** Sincronização de compartilhamentos de arquivos do Azure com servidores on-premises.

## Exemplo de Configuração

### Criar um Compartilhamento de Arquivos

1. **Crie uma Conta de Armazenamento:**
   - No Portal do Azure, vá para "Contas de Armazenamento" e crie uma nova conta.
2. **Crie um Compartilhamento de Arquivos:**
   - Dentro da conta de armazenamento, vá para "Arquivos" e crie um novo compartilhamento.
3. **Conecte-se ao Compartilhamento de Arquivos:**
   - Siga as instruções fornecidas pelo Azure para conectar-se ao compartilhamento usando o protocolo SMB ou NFS.

### Exemplo em PowerShell

```powershell
# Autenticar no Azure
Connect-AzAccount

# Criar uma nova conta de armazenamento
$storageAccount = New-AzStorageAccount -ResourceGroupName "MeuResourceGroup" `
  -Name "minhaContaDeArmazenamento" -Location "EastUS" `
  -SkuName "Standard_LRS"

# Criar um novo compartilhamento de arquivos
$context = $storageAccount.Context
New-AzStorageShare -Name "meuCompartilhamento" -Context $context
