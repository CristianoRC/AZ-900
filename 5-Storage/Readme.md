# Storage

Em uma conta de armazenamento no Azure temos alguns recursos: Blob Sotrage, Queue Storage, Table Storage e File Storage

![-](https://wakeupandcode.com/wp-content/uploads/2019/08/storage-icons.png)

## Blob Storage(Binary Large OBject)

Serve para a gente gerenciar arquivos de uma forma fácil e muito barata no Azure, ao invés de guardar os arquivos na VM, ou no seu banco de dados(pf não faça isso), com o Blob Storage você controla tudo de maneira fácil, via HTTP, SDK ou até mesmo interface gráfica [Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer/). Tem três camadas de acesso, a HOT, para leitura super rápida, arquivos que são sempre usados, Cool para arquivos que não precisam de tanta performance, e o Archive, que veremos mais sobre no final deste arquivo.


Sua organização é feita por conta(storage account), container(como se fossem os diretórios) e os blobs(os arquivos).

![-](https://docs.microsoft.com/sv-se/azure/storage/blobs/media/storage-quickstart-blobs-dotnet/blob1.png)


## Queue Storage

É uma fila básica que permite trafegar dados bem pequenos, mas que em situações mais tranquilas podem ajudar bastante. 

![-](https://docs.microsoft.com/pt-br/azure/includes/media/storage-queue-concepts-include/azure-queue-service-components.png)

## Table Storage

É um banco de dados de tablea, não relacional, muito bom quando tu queres guardar dados temporário, ou dados que não vão ter consultas super complexas.

![-](https://docs.microsoft.com/pt-br/azure/includes/media/storage-table-concepts-include/table1.png)

## Disc Storage

Forma de armazenar os discos de suas VMs, basicamente um disco rigido virtual, com backup e uma série de coisas. É existe uma serie de possíveis configurações, HDD "normal", Ultra Disk(super SSD)...

![-](https://novacontext.com/images/e/ee62508759fbd1341efe1007d0cc2387.jpg)

## File Storage

Também mais focado em VMS, compartilhamento de arquivos entre sistemas operacionais ou armazenamentos dos arquivos de sua empresa de forma segura, com backup e garantia de disponibilidade.
Trafega os dados entre os sistemas operacionais usando o protocolo SMB


![-](https://sameeraman.files.wordpress.com/2017/10/filesync-overview.png)

## Archive Storage

Se você precisa manter os arquivos de sua empresa armazenado por um grande tempo, de forma segura e muito barato, você pode usar a solução do Archive Storage. É super barato armazenar esses dados, eles ficam armazenados de forma criptografada e uma séria de outras feature. Só não é indicado se você usa muito esses arquivos(grande quantidade de leitura). Ele é basicamente um blob storage, então todas as ferramentas usadas lá também funcionarão aqui.
