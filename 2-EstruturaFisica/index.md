# Estrutura do Azure

O Azure tem data centers espalhados por varías partes dos mundo, mas não são todas elas que oferecem todos os serviços. Além de não  disponibilizar alguns serviços dependendo do data center, os valores entre eles também podem mudar bastante.

[Visão geral da estrutura](https://azure.microsoft.com/pt-br/global-infrastructure/geographies/)
[Visão geral dos Data Centers](https://infrastructuremap.microsoft.com/)

## Region

Cada região do Azure apresenta data centers implantados dentro de um perímetro definido por latência. Eles são conectados por uma rede regional de baixa latência dedicada. Esse design garante que os serviços do Azure em qualquer região ofereçam o melhor desempenho e segurança possíveis. - Fonte: Doc. do Azure.

![-](https://www.azureexperts.com.br/wp-content/uploads/2020/03/infra-azure2.png)

## Availability Zones

Em sua grande maria, cada região tem mais de uma zona de disponibilidade, que servem como backup caso algum de problema de conexão, energia, ou qualquer outro detalhe. Basicamente o Azure faz uma replica do seu serviço em outro local, e se uma das zonas "cairem" dentro da região, a outra assume e você nem percebe.
Essas zonas são conectadas com links diretos de alta velocidade, com uma latência de ida e volta de menos de 2ms.

![-](https://docs.microsoft.com/pt-br/azure/availability-zones/media/availability-zones.png)

## Replicação geografica

Quando você precisa realmente garantir que sua aplicaçao não vai cair, ou você tem uma aplicação de nível global que precisa de performance(baixa latência) em várias partes dos mundo, você pode partir para uma replicação geográfica. Funciona bem parecido com as zonas de desponobilidade, só que agora você ta replicando para servidores em outras regiões.

![-](https://docs.microsoft.com/pt-br/azure/availability-zones/media/availability-zones-region-geography.png)