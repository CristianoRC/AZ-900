# Bloqueio de Recursos no Azure

## Visão Geral

O bloqueio de recursos no Azure é uma funcionalidade que oferece proteção adicional aos recursos críticos, evitando alterações ou exclusões acidentais. Os bloqueios são aplicáveis a diversos níveis, como recursos individuais, grupos de recursos e assinaturas inteiras.

## Tipos de Bloqueio

Existem dois tipos principais de bloqueio no Azure:

- **ReadOnly (Somente Leitura)**: Impede qualquer modificação no recurso. Os usuários podem visualizar o recurso, mas não podem realizar ações de exclusão ou atualização.
- **Delete (Exclusão)**: Impede a exclusão do recurso. Os usuários podem visualizar e modificar o recurso, mas a exclusão é bloqueada.

## Níveis de Aplicação de Bloqueio

Os bloqueios podem ser aplicados em diferentes níveis hierárquicos, oferecendo flexibilidade e controle sobre a proteção dos recursos:

- **Recurso Individual**: Protege um recurso específico contra exclusão ou modificação.
- **Grupo de Recursos**: Aplica o bloqueio a todos os recursos dentro de um grupo de recursos.
- **Assinatura**: Aplica o bloqueio a todos os recursos em uma assinatura, abrangendo todas as regiões.

## Benefícios do Bloqueio de Recursos

- **Proteção Contra Exclusões Acidentais**: Evita que recursos críticos sejam excluídos por engano.
- **Controle de Modificações**: Garante que somente alterações intencionais e autorizadas sejam realizadas nos recursos protegidos.
- **Governança**: Facilita a implementação de políticas de governança, assegurando que recursos essenciais permaneçam intactos e conformes com os padrões organizacionais.

## Considerações Importantes

- **Hierarquia de Bloqueios**: Bloqueios aplicados em níveis mais altos (como assinaturas ou grupos de recursos) afetam todos os recursos subordinados.
- **Documentação e Descrição**: É recomendável documentar e fornecer descrições claras para os bloqueios, facilitando o entendimento e gerenciamento pelos administradores.
- **Revisão Periódica**: Bloqueios devem ser revisados periodicamente para garantir que ainda são necessários e estão alinhados com os objetivos da organização.

O bloqueio de recursos é uma prática essencial para garantir a segurança e integridade dos recursos no Azure, proporcionando uma camada adicional de controle e proteção.

![image](https://github.com/user-attachments/assets/bd83a3dc-25d8-4d3a-b371-634bd9d8aa2d)

