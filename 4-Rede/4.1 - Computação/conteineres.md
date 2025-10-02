# Serviços do azure - Conteineres
  Os conteinêres do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alterações sob demanda.
  O conteiner foi uma evoluçãao de virtualização de maquinas, pois virtualizar tambem consome de uma maquina fisica. Conteiner não exige um sistema operacional. 

  - Instancias de Conteiner do Azure: uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure.
  - Aplicativos de Coneiner do Azure: uma oferta de PaaS, como instâncias de conteineres, que pode balancear a carga e escalar.
  - Serviço de Kubernetes do Azure: um serviço de orquestração para conteineres com arquiteturas distribuidas e grandes volumes de conteineres.

Contêineres são uma tecnologia de virtualização leve que permite empacotar e isolar aplicações junto com suas dependências, sem precisar de um sistema operacional completo. Isso facilita a portabilidade, consistência e eficiência no uso dos recursos.

Benefícios dos Contêineres:
Leveza: Compartilham o kernel do sistema operacional, usando menos recursos que VMs.
Portabilidade: Podem ser executados em qualquer ambiente que suporte contêineres.
Escalabilidade: Facilitam a escalabilidade horizontal de aplicações.
Serviços de Contêineres no Azure:
Azure Container Instances (ACI):

Descrição: Serviço PaaS que permite executar contêineres sob demanda sem gerenciar a infraestrutura subjacente.
Uso: Rápida implantação de contêineres, execuções curtas e cargas de trabalho que não requerem um ambiente complexo.
Azure Kubernetes Service (AKS):

Descrição: Serviço gerenciado que simplifica a implantação, gerenciamento e operações de clusters Kubernetes.
Uso: Orquestração de contêineres em grande escala, gestão de múltiplos contêineres, balanceamento de carga e escalabilidade automatizada.
Azure Container Registry (ACR):

Descrição: Repositório privado para armazenar e gerenciar imagens de contêiner.
Uso: Armazenar, gerenciar e implantar imagens de contêiner de forma segura.
Exemplos de Uso:
Desenvolvimento e Teste: Criar ambientes de desenvolvimento consistentes.
Microserviços: Implementar aplicações em arquitetura de microserviços.
Computação em Nuvem: Executar cargas de trabalho distribuídas e escaláveis.

Para mais detalhes, consulte a documentação oficial do Azure sobre contêineres.
  
  
