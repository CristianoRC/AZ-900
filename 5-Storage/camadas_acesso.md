# Camadas de Acesso de Armazenamento do Azure

No Azure Storage, as camadas de acesso se referem aos diferentes níveis de acesso e políticas de armazenamento que você pode configurar para seus dados. O Azure oferece várias camadas de acesso para otimizar custos e desempenho com base na frequência de acesso aos dados. As principais camadas de acesso de armazenamento no Azure são:

## Hot (Quente)
- **Definição**: Projetada para dados que são acessados com frequência.
- **Custo de Armazenamento**: Mais alto.
- **Custo de Acesso**: Mais baixo.
- **Uso Comum**: Dados em uso ativo, como arquivos de trabalho em andamento, logs recentes, backups frequentes, etc.

## Cool (Fria)
- **Definição**: Projetada para dados que são acessados com menos frequência, mas que ainda precisam ser acessados rapidamente quando necessário.
- **Custo de Armazenamento**: Mais baixo que a camada Hot.
- **Custo de Acesso**: Mais alto que a camada Hot.
- **Uso Comum**: Dados de longo prazo que são raramente acessados, como backups mensais, arquivos antigos de projetos, etc.

## Archive (Arquivo)
- **Definição**: Projetada para dados que são raramente acessados e que podem tolerar latência maior ao serem recuperados.
- **Custo de Armazenamento**: Mais baixo de todos.
- **Custo de Acesso**: Mais alto de todos e também inclui uma taxa de recuperação (ingress/egress).
- **Uso Comum**: Dados de arquivamento de longo prazo, como backups anuais, registros históricos que precisam ser mantidos por razões de conformidade, etc.

## Comparação das Camadas

- **Hot**:
  - **Latência de Acesso**: Baixa.
  - **Tempo de Recuperação**: Imediato.
  - **Exemplo de Uso**: Aplicativos em tempo real, bancos de dados em produção.

- **Cool**:
  - **Latência de Acesso**: Média.
  - **Tempo de Recuperação**: Imediato.
  - **Exemplo de Uso**: Dados de backup, dados de teste, armazenamento de longo prazo para dados de acesso esporádico.

- **Archive**:
  - **Latência de Acesso**: Alta (horas para recuperar).
  - **Tempo de Recuperação**: Lento (várias horas).
  - **Exemplo de Uso**: Arquivamento de dados de longo prazo, dados de conformidade.

![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/a8c42a01-fb76-4983-85b4-d8da061009e0)


## Mudança entre Camadas

Os dados no Azure Storage podem ser movidos entre essas camadas de acesso conforme necessário. Isso permite otimizar os custos de armazenamento com base na frequência de acesso aos dados. As transições entre camadas podem ser gerenciadas automaticamente usando políticas de gerenciamento de ciclo de vida do Azure Storage.

Essas camadas de acesso permitem que as empresas equilibrem custo e desempenho de acordo com as necessidades específicas de seus dados, proporcionando flexibilidade na gestão de armazenamento em nuvem.

Para mais detalhes, consulte a [documentação oficial do Azure Storage](https://learn.microsoft.com/pt-br/azure/storage/blobs/access-tiers-overview).
