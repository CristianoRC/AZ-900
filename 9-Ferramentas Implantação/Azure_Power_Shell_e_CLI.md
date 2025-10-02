# PowerShell e Azure CLI

## PowerShell

### O que é
PowerShell é uma linguagem de script e um shell de linha de comando desenvolvido pela Microsoft. É projetado para automação de tarefas e gerenciamento de configuração.

### Características
- **Cmdlets**: Comandos específicos do PowerShell que realizam tarefas simples. Eles podem ser combinados para criar scripts complexos.
- **Objetos**: PowerShell trabalha com objetos, o que significa que os dados são estruturados em objetos que podem ser facilmente manipulados.
- **Pipeline**: Permite a passagem de saída de um cmdlet como entrada para outro, facilitando a criação de scripts eficientes.

### Uso no Azure
- PowerShell pode ser usado para automatizar a criação, configuração e gerenciamento de recursos do Azure.
- O módulo `Az` é o conjunto de cmdlets do PowerShell para gerenciar o Azure.

## Azure CLI

### O que é
A Azure Command-Line Interface (CLI) é uma ferramenta de linha de comando que proporciona uma experiência de gerenciamento de recursos do Azure através de comandos.

### Características
- **Interoperabilidade**: CLI pode ser usada em várias plataformas, incluindo Windows, macOS e Linux.
- **Simplicidade**: Oferece comandos simples e diretos que podem ser usados de forma interativa ou em scripts para automatização.
- **Flexibilidade**: É baseada em comandos JSON, permitindo integração fácil com outras ferramentas e serviços.

### Uso no Azure
- A CLI é usada para criar, atualizar, excluir e gerenciar recursos do Azure.
- Exemplos de comandos incluem `az vm create` para criar uma máquina virtual e `az storage account create` para criar uma conta de armazenamento.

## Comparação

### Facilidade de Uso
- PowerShell é mais robusto para quem está familiarizado com a linguagem e o ambiente Windows.
- CLI é mais simples e intuitivo para quem prefere comandos de estilo Unix/Linux.

### Automatização
- Ambos suportam scripts, mas PowerShell oferece uma linguagem de script mais rica.

### Compatibilidade
- CLI é mais versátil em termos de compatibilidade com diferentes sistemas operacionais.

## Exemplos de Uso

### PowerShell
```powershell
# Login no Azure
Connect-AzAccount

# Criar um recurso de grupo
New-AzResourceGroup -Name "myResourceGroup" -Location "EastUS"

# Criar uma máquina virtual
New-AzVm -ResourceGroupName "myResourceGroup" -Name "myVM" -Image "Win2019Datacenter"
