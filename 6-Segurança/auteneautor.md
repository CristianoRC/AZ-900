# Autenticacao e Autorização 

# Comparação entre Autenticação e Autorização no Azure

## Autenticação

A autenticação é o processo de verificar a identidade de um usuário ou dispositivo. No contexto do Azure, a autenticação garante que a pessoa ou serviço que está tentando acessar um recurso é quem diz ser.

### Características da Autenticação no Azure

- **Verificação de Identidade**: Confirma a identidade de usuários e dispositivos.
- **Métodos de Autenticação**:
  - Senhas
  - Autenticação Multifator (MFA)
  - Certificados Digitais
  - Autenticação baseada em biometria
- **Serviços Relacionados**:
  - **Azure Active Directory (Azure AD)**: Principal serviço de gerenciamento de identidades e autenticação no Azure.
  - **Azure AD B2C**: Serviço de autenticação para aplicativos direcionados ao consumidor.
  - **Azure AD B2B**: Permite a colaboração com usuários externos.
- **Experiência do Usuário**: Envolve o processo de login, onde o usuário fornece credenciais (como nome de usuário e senha) e, possivelmente, realiza uma verificação adicional, como um código enviado para um dispositivo móvel.

## Autorização

A autorização é o processo de determinar o nível de acesso que um usuário autenticado possui. No Azure, a autorização define quais recursos e operações um usuário ou serviço pode acessar e realizar.

### Características da Autorização no Azure

- **Controle de Acesso**: Determina as permissões de usuários e serviços.
- **Tipos de Permissões**:
  - Leitura
  - Gravação
  - Modificação
  - Exclusão
- **Serviços Relacionados**:
  - **Role-Based Access Control (RBAC)**: Sistema que usa funções para conceder permissões a usuários, grupos e serviços.
  - **Azure Policy**: Serviço que aplica políticas organizacionais para garantir a conformidade com regras e regulamentos.
- **Níveis de Autorização**:
  - **Nível de Assinatura**: Controle de acesso em toda a assinatura do Azure.
  - **Nível de Recurso**: Controle de acesso a recursos específicos, como máquinas virtuais, bancos de dados, etc.
- **Experiência do Usuário**: Após a autenticação, o usuário tenta acessar um recurso. O sistema verifica as permissões e decide se o acesso será concedido ou negado.

## Diferenças Principais

| Aspecto                  | Autenticação                                             | Autorização                                             |
|--------------------------|----------------------------------------------------------|---------------------------------------------------------|
| **Definição**            | Verifica a identidade do usuário ou dispositivo.         | Determina as permissões e o nível de acesso.             |
| **Objetivo**             | Garantir que o usuário é quem diz ser.                   | Garantir que o usuário tem permissão para acessar um recurso. |
| **Métodos**              | Senhas, MFA, biometria, certificados digitais.           | RBAC, Azure Policy.                                      |
| **Serviços**             | Azure AD, Azure AD B2C, Azure AD B2B.                    | RBAC, Azure Policy.                                      |
| **Foco**                 | Identidade e verificação.                                | Permissões e controle de acesso.                         |
| **Processo**             | Login e verificação de credenciais.                      | Verificação de permissões após a autenticação.           |
| **Experiência do Usuário** | O usuário fornece credenciais e pode passar por MFA. | O sistema verifica se o usuário tem permissão para o recurso desejado. |

## Resumo

Enquanto a autenticação no Azure trata de verificar quem é o usuário ou serviço, a autorização trata do que o usuário ou serviço pode fazer após ser autenticado. Ambos são componentes essenciais para garantir a segurança e o controle de acesso eficazes no ambiente do Azure.
