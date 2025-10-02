# DNS do AZure

O **DNS do Azure** é um serviço de hospedagem para domínios DNS, permitindo que você gerencie e resolva nomes de domínio em infraestrutura do Azure. Ele fornece alta disponibilidade e desempenho, juntamente com a capacidade de gerenciar registros DNS de forma fácil e segura.

## Características Principais
- **Alta Disponibilidade:** O serviço é distribuído globalmente, garantindo alta disponibilidade.
- **Desempenho Rápido:** Resolução de nomes rápida utilizando a infraestrutura global da Microsoft.
- **Segurança:** Integração com o Azure Active Directory para controle de acesso baseado em funções.
- **Facilidade de Gerenciamento:** Gerenciamento de registros DNS através do portal do Azure, CLI, ou API REST.

## Tipos de Zonas DNS
- **Zona DNS Privada:** Usada para gerenciar e resolver nomes de domínio dentro de uma rede virtual.
- **Zona DNS Pública:** Usada para gerenciar e resolver nomes de domínio acessíveis pela Internet.

## Casos de Uso Comuns
- **Gerenciamento de Nomes de Domínio:** Hospedar domínios DNS e gerenciar registros.
- **Integração com Outros Serviços do Azure:** Configurar registros DNS para serviços como Web Apps, VMs, e outros recursos do Azure.
- **Resolução de Nomes Privados:** Gerenciar nomes de domínio dentro de uma rede virtual, sem expô-los à Internet.

## Links Úteis
Para mais informações detalhadas, consulte a [documentação oficial do Azure DNS](https://learn.microsoft.com/pt-br/azure/dns/dns-overview).


# Gateway VPN

O gateway de VPN é usado para enviar trafego criptografado entre uma rede virtual do Azure e uma no local pela internet publica. 

O **Gateway VPN do Azure** permite que você configure uma conexão segura entre sua rede local e a rede virtual do Azure. Ele suporta dois tipos de VPN:

## Tipos de VPN

### VPN Point-to-Site (P2S)
- **Descrição:** Permite conexões individuais de clientes para a rede do Azure.
- **Uso:** Ideal para funcionários remotos que precisam acessar recursos no Azure.

### VPN Site-to-Site (S2S)
- **Descrição:** Cria uma conexão segura entre sua rede local e a rede do Azure.
- **Uso:** Perfeito para conexões persistentes entre sua infraestrutura local e o Azure.

## Características
- **Segurança:** Criptografia IPsec/IKE.
- **Alta Disponibilidade:** Pode ser configurado em uma arquitetura de alta disponibilidade.
- **Gerenciamento:** Fácil configuração e gerenciamento via Portal do Azure.

## Tipos de Gateways VPN
- **Basic, Standard, HighPerformance, VpnGw1, VpnGw2, VpnGw3:** Diferentes níveis de desempenho e custo.

## Passos Básicos para Configuração
1. **Criar um gateway de rede virtual no Azure.**
2. **Configurar a conexão VPN no dispositivo local.**
3. **Estabelecer a conexão entre a rede local e a VNet do Azure.**

Para mais informações detalhadas, consulte a [documentação oficial do Azure VPN Gateway](https://learn.microsoft.com/pt-br/azure/vpn-gateway/vpn-gateway-about-vpngateways).


![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/d1bf457e-d595-4868-8118-f1c3bda353d8)



# Express Route

Se você precisa trafegar uma quantidade muito grande de dados emtre sua infra local e o Azure(ou qualquer outro cloud), você pode estar fazendo o uso do Express Route, que basicamente é uma forma de fazer um link direto do seu ponto até o data center do Azure, esse passo custa um pouco caro, mas é mais fácil que trafegar pela internet. Ponsto importante é que essas configurações são feitas do lado do Azure e do seu provedor de inetrnet.

![-](https://docs.microsoft.com/pt-br/azure/architecture/reference-architectures/hybrid-networking/images/expressroute.png)

![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/2b86b8a1-727f-4757-abfb-024244327917)

# V-NET

É uma forma de segregar o acesso as seus serviços(via rede). Basicamente você pode ter várias sub-redes dentro da sua infra, e dentro delas você colocar apenas os apps que precisam se comunicar, para ter uma menor chance de ter falhas de segurança ou um serviço chamando o outro sem poder. Além de bloquear as chamadas de forma interna, você pdoe definir quais dessas v-nets tem acesso via internet, gatway ou VPN.

Permite que os recursos do Azure se comuniquem uns com os outros, com a internet e com as redes locais.

Pontos de exetremidade públicos, acessiveis de qualquer lugar na internet.

Pontos de extremidades privados, acessiveis somente de dentro da sua rede.

![-](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/_images/azure-best-practices/network-hub-spoke-high-level.png)

## Estrutura da Rede Virtual no Azure

### Hub Virtual Network
- **PIP:** Public IP para proteção DDoS.
- **Application Gateway (com WAF):** Gateway de aplicação com firewall de aplicativo web.
- **Azure Firewall:** Firewall para proteção e controle de tráfego.
- **Virtual Network Peering:** Conexões de emparelhamento de rede virtual entre redes virtuais (VNets).

### Virtual WAN
- **ExpressRoute e VPN:** Conexões WAN virtuais para integrar redes on-premises (sede e filiais) com a nuvem.
- **vWAN Hub:** Hub central para gerenciar conexões WAN.

### Estrutura de Spokes (Projetos)
- **Spokes (ex. Spoke1, Spoke2, Spoke3, etc.):**
  - **Load Balancer:** Balanceamento de carga para distribuir tráfego entre várias instâncias.
  - **Virtual Networks:** Redes virtuais individuais para cada spoke, contendo VMs, SQL, e outros recursos.
  - **NSG:** Network Security Groups para controlar o tráfego de entrada e saída.
  - **Dev and Test, UAT, PROD:** Ambientes de desenvolvimento/teste, User Acceptance Testing (UAT), e produção.

### Serviços Transversais
- **Cross Subscription Services:** Serviços que abrangem várias assinaturas, como Azure Active Directory e DNS (Público e Privado).

### Descrição por Elemento
1. **Azure Front Door:** Gestão de tráfego global com proteção DDoS.
2. **Remote Hub:** Hub remoto não detalhado na imagem.
3. **Hub Virtual Network:** Rede central que conecta múltiplos spokes.
4. **Virtual WAN:** Conexão WAN virtual integrando redes on-premises com Azure.
5. **Spokes:** Redes virtuais conectadas ao hub, cada uma com suas próprias cargas de trabalho e ambientes (desenvolvimento, teste, produção).

### Fluxo de Tráfego
1. **Internet -> Azure Front Door -> Hub Virtual Network:** Tráfego entra pela Azure Front Door, passa pela proteção DDoS, e é roteado através do Application Gateway e Azure Firewall.
2. **Hub Virtual Network -> Spokes:** Tráfego é distribuído para várias redes virtuais (spokes) via Virtual Network Peering.
3. **Virtual WAN -> On-Premises:** Integração de redes on-premises via VPN/ExpressRoute para comunicação segura e eficiente.

### Funções e Benefícios
- **Segurança:** Proteção DDoS, Azure Firewall, NSGs.
- **Escalabilidade:** Balanceamento de carga e Virtual Network Peering.
- **Conectividade:** ExpressRoute e VPN para integração on-premises.
- **Gerenciamento:** Estrutura de hub-and-spoke para facilitar a administração e a segmentação de redes e ambientes.


# Load Balancer

Para saber mais sobre o assunto da uma olhada nesse vídeo aqui

[![-](http://i3.ytimg.com/vi/ODcQC0_RyH0/hqdefault.jpg)](https://www.youtube.com/watch?v=ODcQC0_RyH0)
