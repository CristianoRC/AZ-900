# Pontos de Extremidade Públicos do Serviço de Armazenamento do Azure

Os **Pontos de Extremidade Públicos** do serviço de armazenamento do Azure permitem que você acesse seus recursos de armazenamento (Blobs, Tabelas, Filas e Arquivos) através da internet usando URLs públicos.

## Características Principais

- **Acesso Público:** Permite acessar os dados diretamente via HTTP/HTTPS.
- **Controle de Acesso:** Gerenciamento detalhado através de SAS (Shared Access Signatures) e políticas de acesso.
- **Segurança:** Criptografia de dados em trânsito e em repouso para proteger os dados.

## Casos de Uso Comuns

- **Distribuição de Conteúdo:** Hospedar arquivos públicos como imagens, vídeos e documentos para distribuição global.
- **Aplicações Web:** Fornecer armazenamento de backend para aplicações web acessíveis pela internet.
- **Integração com Serviços Externos:** Compartilhar dados com aplicações e serviços externos de forma segura.

![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/be90b722-9227-4660-b9fa-add3758e7178)

## Exemplo de Uso

### Acessando um Blob Público

1. **Criar um Blob Público:**
   - No Portal do Azure, crie um contêiner e defina suas permissões para público.
2. **Obter a URL do Blob:**
   - Use o URL fornecido pelo Azure para acessar o blob publicamente.

```python
from azure.storage.blob import BlobServiceClient

# Conectar ao serviço de blob
blob_service_client = BlobServiceClient.from_connection_string("sua_connection_string")
container_client = blob_service_client.get_container_client("meuContainer")

# Obter a URL do blob
blob_url = container_client.url + "/meuBlob.txt"
print(blob_url)



