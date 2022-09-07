# Express Route

Se você precisa trafegar uma quantidade muito grande de dados emtre sua infra local e o Azure(ou qualquer outro cloud), você pode estar fazendo o uso do Express Route, que basicamente é uma forma de fazer um link direto do seu ponto até o data center do Azure, esse passo custa um pouco caro, mas é mais fácil que trafegar pela internet. Ponsto importante é que essas configurações são feitas do lado do Azure e do seu provedor de inetrnet.

![-](https://docs.microsoft.com/pt-br/azure/architecture/reference-architectures/hybrid-networking/images/expressroute.png)

# V-NET

É uma forma de segregar o acesso as seus serviços(via rede). Basicamente você pode ter várias sub-redes dentro da sua infra, e dentro delas você colocar apenas os apps que precisam se comunicar, para ter uma menor chance de ter falhas de segurança ou um serviço chamando o outro sem poder. Além de bloquear as chamadas de forma interna, você pdoe definir quais dessas v-nets tem acesso via internet, gatway ou VPN.

![-](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/_images/azure-best-practices/network-hub-spoke-high-level.png)

# Load Balancer

Para saber mais sobre o assunto da uma olhada nesse vídeo aqui

[![-](http://i3.ytimg.com/vi/ODcQC0_RyH0/hqdefault.jpg)](https://www.youtube.com/watch?v=ODcQC0_RyH0)
