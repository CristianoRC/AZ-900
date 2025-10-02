# Regiões 
60 Regioes em 140 paises. Onde tem dizponiblidade de data center e onde o recurso vai ficar guardado. Posso criar os recursos onde fica mais proximo a empresa. 
Porquer deixar perto da empresa? Cada local paga um valor, impacta impostos por exemplo. 
Nem todos os recursos estao disopniveis em todas as regiões. 

As Regioes são compostas de um ou mais datacenters muito próximos. 
- Comunicam-se entre si, possui disaster recover, reduzem a latencia em uma disponiblidade de escala.

Eles fornecem flexibilidade e escala para reduzir a latencia do cliente. 
- reduzir o tempo de cada transação.
  
As regiões preservam a residência dos dados com uma oferta abrangente de conformidade. 
- determiados dados nao podem sair do Brasil, aqui inclue questoes de LGPD

# Níveis de Disponibilidade no Azure

Os conjuntos de disponibilidade são compostos por domnios de atualização e domninios de falhas.

## Disponibilidade Local
- **Descrição:** Proteção dentro de um único datacenter, utilizando servidores diferentes.
- **Uso:** Proteção contra falhas de hardware no mesmo datacenter.
- **Custo:** Menor.

## Disponibilidade Zonal
- **Descrição:** Utilização de Zonas de Disponibilidade, que são datacenters fisicamente separados dentro da mesma região.
- **Uso:** Proteção contra falhas de datacenter dentro da mesma região.
- **Custo:** Moderado a alto.

## Disponibilidade Regional
- **Descrição:** Proteção usando datacenters em diferentes regiões.
- **Uso:** Proteção contra desastres que afetam uma região inteira.
- **Custo:** Maior.

## Disponibilidade Geográfica
- **Descrição:** Replicação de dados entre várias regiões geográficas.
- **Uso:** Proteção contra desastres que afetam várias regiões, garantindo a continuidade do negócio.
- **Custo:** Maior.

### Resumo
- **Disponibilidade Local:** Servidores diferentes no mesmo datacenter.
- **Disponibilidade Zonal:** Datacenters separados fisicamente na mesma região.
- **Disponibilidade Regional:** Datacenters em diferentes regiões.
- **Disponibilidade Geográfica:** Replicação entre várias regiões geográficas.



# Pares de Região. ( para onde o disaster recover sera direcionado.) 
- No mninimo 300 milhas de separação entre pares de regiões.
- replicação automática em seu par, para alguns serviços.
- Recuperação de região priorizada em cas de interrupção.
- As atualizações são distribuidas sequencialmente.

![image](https://github.com/ftaveira-data/AZ-900/assets/115483835/802cbd89-4d2c-449c-ab7e-357e6ceda927)


# Regiões Soberanas (são exclusivas)
  AZURE GOVERNAMENTAL - EUA
 - Regiao soberana dos EUA é apenas para as necessidade de segurança e conformidade das agencias federais, governos estaduais e locais dos EUA e seus provedores de soluções.
 - Instancia separada do Azure.
 - Fisicamente isolada de implantações que não sejam do governo dos EUA.
 - Acessivel somente a pessoal verificado e autorizado. 

  AZURE GOVERNAMENTAL - CHINA
  - Primeiro provedor para a china.
  - Instancia fisicamente separada dos serviços de nuvem do AZure operados pela 21Vianet.
  - Todos os dados permanecem dentro da China para garantir conformidade. 
