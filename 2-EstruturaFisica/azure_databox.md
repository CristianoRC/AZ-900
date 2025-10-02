# Azure Data Box

O Azure Data Box é uma solução da Microsoft Azure para transferir grandes quantidades de dados para a nuvem Azure. Ele ajuda a mover dados de maneira segura, eficiente e econômica quando a transferência pela rede não é uma opção prática devido ao volume de dados, largura de banda limitada ou custos elevados de transferência de dados. O Azure Data Box oferece várias opções para diferentes necessidades de transferência de dados.

## Opções de Azure Data Box

### Data Box
- **Capacidade**: Até 100 TB.
- **Uso Comum**: Migração de grandes volumes de dados para o Azure, como backups, arquivos de vídeo, bibliotecas de dados, etc.
- **Características**: Dispositivo robusto e seguro, com criptografia AES de 256 bits, resistência a impactos e temperatura.
- **Conectividade**: Suporta interfaces de conexão como SMB e NFS.

### Data Box Disk
- **Capacidade**: Até 8 TB por disco, com até 5 discos por pedido, totalizando até 40 TB.
- **Uso Comum**: Transferência de dados de menor volume ou necessidades de transferência distribuídas.
- **Características**: Pequeno, leve e fácil de transportar, criptografia AES de 128 bits.
- **Conectividade**: USB/SATA.

### Data Box Heavy
- **Capacidade**: Até 1 PB (1.000 TB).
- **Uso Comum**: Migração de grandes volumes de dados, ideal para datacenters ou grandes infraestruturas de TI.
- **Características**: Dispositivo robusto, criptografia AES de 256 bits, projetado para grandes transferências de dados.
- **Conectividade**: Interfaces de alta velocidade, como 40 Gbps.

## Fluxo de Trabalho

1. **Pedido**: Faça o pedido do dispositivo Data Box apropriado através do portal do Azure.
2. **Carregamento**: Receba o dispositivo e carregue os dados nele usando as interfaces de conexão disponíveis.
3. **Envio de Volta**: Envie o dispositivo de volta para a Microsoft, onde os dados serão carregados de forma segura para o armazenamento do Azure.
4. **Disponibilidade dos Dados**: Após o upload, os dados estarão disponíveis na sua conta do Azure.

## Casos de Uso

- **Migração de Dados**: Transferência de grandes volumes de dados para o Azure durante a migração de datacenters.
- **Backup e Arquivamento**: Envio de backups e dados de arquivamento para a nuvem para armazenamento seguro e de longo prazo.
- **Computação de Alto Desempenho**: Transferência de grandes conjuntos de dados para análise e processamento no Azure.

## Segurança

O Azure Data Box oferece segurança robusta para garantir que os dados sejam protegidos durante todo o processo de transferência:
- **Criptografia**: Dados são criptografados no dispositivo usando AES de 128 bits ou 256 bits.
- **Cadeia de Custódia**: Rastreamento completo do dispositivo desde o envio até o recebimento pela Microsoft.
- **Apagamento de Dados**: Após o upload, os dados no dispositivo são apagados de acordo com os padrões de segurança da Microsoft.

 ![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/00ec6166-9480-4fae-a373-c92e43ff07a2)


Para mais detalhes, consulte a [documentação oficial do Azure Data Box](https://learn.microsoft.com/pt-br/azure/databox/data-box-overview).
