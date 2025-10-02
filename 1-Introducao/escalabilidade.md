# Escalabilidade
  - Refere-se a capacidade de ajustar recursos para atender a demanda, siginifica que você pode adicionar mais recursos para lidar melhor com o aumento da demanda.
  - Você não esta pagando alem do necessário pelos serviços.
  - Baseado em consumo, vocës só paga pelo que usa.
  - Se a demanda cair vocë poderá reduzir seus recursos e assim reduzir seus custos.

# Elasticidade 
  - Possibilidade de expandir os recursos implantados.
  - Voce pdoe adicionar maquinas virtuais ou conteineres por meio de expansão.
  - Se houver uma queda na demanda, os recursos poderão ser reduzidos horizontalmente ( manual ou automatioc ) 

##### Vertical X Horizontal 
  - Escala vertical, se você estivesse desenvolvendo um aplicativo e precisasse de amsi capacidade de processamento, poderia escalar verticalmente para adicionar mais CPUs ou RAM a VM.
  - Escala horizontal, se seu aplicativo web estiver recebendo mais tráfego do que uma única VM pode lidar, você pode escalar horizontalmente adicionando mais VMs para balancear a carga e melhorar o desempenho e a resiliência.


# Modelos de Nuvem
Aqui podemos diferencair alguns tipos de nuvens. 

#### Nuvem privada
Vamos começar com uma nuvem privada. Uma nuvem privada é, de certa forma, a evolução natural de um datacenter corporativo. Ela é uma nuvem (que fornece serviços de TI pela Internet) usada por uma única entidade. A nuvem privada fornece um controle muito maior para a empresa e o departamento de TI. No entanto, ela também tem mais custos e menos benefícios em relação a uma implantação de nuvem pública. Por fim, uma nuvem privada pode ser hospedada em seu datacenter local. Ela também pode ser hospedada em um datacenter dedicado externo, até mesmo por terceiros que tenham dedicado esse datacenter à sua empresa.

#### Nuvem pública
Uma nuvem pública é criada, controlada e mantida por um provedor de nuvem de terceiros. Com uma nuvem pública, qualquer pessoa que queira comprar serviços de nuvem pode acessar e usar os recursos. A disponibilidade pública geral é uma diferença fundamental entre nuvens públicas e privadas.

#### Nuvem híbrida
Uma nuvem híbrida é um ambiente de computação que usa nuvens públicas e privadas em um ambiente interconectado. Um ambiente de nuvem híbrida pode ser usado para permitir que uma nuvem privada escale para atender a uma demanda maior temporária implantando recursos de nuvem pública. A nuvem híbrida pode ser usada para fornecer uma camada adicional de segurança. Por exemplo, os usuários podem escolher com flexibilidade quais serviços manter na nuvem pública e quais implantar na infraestrutura de nuvem privada.

#### Várias nuvens
O quarto (e cada vez mais provável) cenário, é um cenário de várias nuvens. Em um cenário de várias nuvens, você usa vários provedores de nuvem pública. Talvez você use recursos diferentes de diferentes provedores de nuvem. Ou você pode ter iniciado seu percurso de nuvem com um provedor e esteja em processo de migração para um provedor diferente. Independentemente disso, em um ambiente de várias nuvens, você lida com dois (ou mais) provedores de nuvem pública e gerencia recursos e segurança em ambos os ambientes.

#### Azure Arc
O Azure Arc é um conjunto de tecnologias que ajuda a gerenciar seu ambiente de nuvem. O Azure Arc pode ajudar a gerenciar o seu ambiente de nuvem, seja uma nuvem pública exclusivamente no Azure, uma nuvem privada em seu datacenter, uma configuração híbrida ou até mesmo um ambiente de várias nuvens em execução em vários provedores de nuvem ao mesmo tempo.

#### Solução VMware no Azure
E se você já estiver estabelecido com o VMware em um ambiente de nuvem privada, mas quiser migrar para uma nuvem pública ou híbrida? A Solução VMware no Azure permite executar suas cargas de trabalho do VMware no Azure com integração e escalabilidade total.
