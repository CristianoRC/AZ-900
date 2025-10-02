# Serviços de Computação 
 A Computação do Azure é um serviço sob demanda que fornece recursos de computação, como discos, processadores, memória, rede e sistemas operacionais. 

 ![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/52be27c7-e361-4170-9562-8085c64d4c33)

 ### MAquinas Virtuais 
  - Pode ser Linux ou Windows, controle sobre o sistema operacional
  - São emulações de software d computadores fisicos.
  - incluir processador virtual, memória, armazenamento e rede.
  - Oferta de IaaS que oferece personalização e controle total.

    #### Conjunto de dimensionamento de VMs.
    - Escalar horizontalmente quando o recurso precisar aumentar.
    - Reduzir horizontalmente quando o recurso precisar diminuir. 
    - Um conjunto de VMs identiicas, escalonamento horizontal. 
    - Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar recursos automaticamente. 

    #### Conjunto de disponibilidae de VM
    Domínios de Falha (Fault Domains): Cada rack é considerado um domínio de falha. No diagrama, temos três racks:

    Fault Domain 1
    Fault Domain 2
    Fault Domain 3
    Domínios de Atualização (Update Domains): Cada camada horizontal é um domínio de atualização. Isso significa que durante as atualizações planejadas, os recursos em diferentes domínios de atualização são atualizados em 
    horários diferentes para minimizar a indisponibilidade:
    
    Update Domain 1
    Update Domain 2
    Update Domain 3 

    ![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/4e4368d8-fbfd-4fea-8582-d0288682ebac)
 

 
 
