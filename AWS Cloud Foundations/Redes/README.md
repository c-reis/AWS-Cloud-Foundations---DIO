## Redes AWS

### VPC - Virtual Private Cloud
- Rede lógica isolada
- Permite várias sub-redes em diferentes zonas de disponibilidade em uma mesma região
- Fornece gateway para internet

### Serviços públicos x Serviços privados
- Serviço público é qualquer serviço que não esteja implantando eu uma VPC
- Serviço privado requer configuração de VPC para o funcionamento

### SubNet
- Sub-rede lógica criada dentro da VPC
- Permite segregação da rede
- Os grupos de segurança são criados dentro das subnets

### Security Group
- Nível da placa de rede da intância
- Cria as regras de port forwarding

> [!NOTE]
> Em ambientes híbridos (cloud e on-premise), as mesmas regras aplicadas no security group devem ser refletidas no firewall on-premise.

### Route 53
- Serviço DNS da AWS
- Gestão de domínios
- Permite transferêcia de domínios
- Fornece políticas e fluxo de tráfego

### Cloudfront
- Oferece serviço de CDN
- Entrega de conteúdo global, através do edge location

### EBL - Elastic Load Balancer
- Balanceador de carga
- Distribui a carga de forma eficiente e automática para um grupo de servidores
- Ganho de velocidade e desempenho
- Permite uma melhor escalabilidade
- Fornece alta disponibilidade
- Distribuir e equilibrar recursos
  - Tipos:
    - ***Application Load Balancer:***
      - Gerencia tráfego de aplicação HTTP/HTTPS
      - Baseado em regras como URL e cabeçalhos
      - ***Utilização:*** Balancear tráfegos de aplicativos web que demandem roteamento avançado e suporte a WebSockets.
    - ***Network Load Balancer:***
      - Gerencia o tráfego TCP/UDP a nível de rede
      - Fornece baixa latência e alta taxa de transferência
      - ***Utilização:*** Balancear tráfego de aplicativos que exigem alta performance, baixa latência, como serviços financeiros e jogos.
    - ***Gateway Load Balancer***
      - Funções de load balacing com serviço de rede em única aplicação
      - Fornece firewalls e detecção de instrusões
      - ***Utilização:*** Balancear o tráfego adicionando funcionalidades de segurança. Permitindo uma simplificando a arquitetura de segurança.
    - ***Classic Load Balancer***
      - Load balancer legado que distribui tráfego HTTP/HTTPS e TCP entre instâncias EC2
      - ***Utilização:*** Adequado para aplicativos anteriores ao balanceadores ALB e NLB. Por exemplo aplicativos monolíticos.
    
