## Banco de dados

### Amazon RDS
- Fornece plataforma para criação de instâncias de banco de dados relacionais
- ***Tipos:***
  - ***Amazon Aurora:***
     - Banco de dados relacional
     - Compatível com MySQL e PostgreSQL
     - Combina velocidade e disponibilidade de BDs comerciais com simplicidade e economia de BDs de código aberto.
     - 5x melhor desempenho do que o MySQL
     - Baixo custo
  - ***Oracle***
     - Permite implantar várias edições do Oracle Database
     - Permite trazer licenças Oracle existentes ou pagar pelo uso da licença por horas
  - ***Microsoft SQL Server***
     - Permite implantar instâncias do SQL Server
     - Permite utilizar recursos nativos da plataforma SQL Server
  - ***MySQL***
     -  Permite implantar instâncias do MySQL

### DynamoDB
- Fornece plataforma para criação de instâncias do banco DynamoDB não relacional
- Trabalha com dados não estruturados ou semiestruturado


### Estratégias de backup e recuperação de dados
- ***Avaliação e planejamento***
   - Identificar dados críticos
   - Definição de RPO (Objetivos de Ponto de Recuperação)
   - Definição de RTO (Objetivos de Tempo de Recuperação)
   > [!NOTE]
   > RPO determina a margem que ***pode ser perdida*** entre os clicos de backup realizados diariamente, semanalmente e mensalmente.
   > [!NOTE]
   > RTO determina o limite de ***tempo de indisponibilidade do sistema***. O tempo máximo que o sistema pode ficar parado até a recuperação do ambiente.

- ***Serviços disponibilizados pela AWS***
   - ***Amazon S3*** pode ser utilizado para armazenar os backups
   - ***AWS Backup*** que gerencia e automatiza os backups de serviços da AWS
   - ***Amazon RDS Automated Backups e Snapshots*** permite a configuração de bakcups automatizados para BDs em RDS e snapshots para bakcups manuais e restaurações pontuais.
   - ***Amazon DynamoDB On-Demand Backup*** permite bakcups sob demanda e contínuos (PITR) para tabelas do DynamoDB

- ***Implementação da estratégia de backup***
   - ***Backup regulares diários*** para dados críticos
   - ***Backup incrementais*** para otimizar tempo e armazenamento
   - Cópias de segurança em ***múltiplas regiões***, por exemplo utilização do amazon S3 com replicação entre regiões.
   - Utilizar AWS Lambda e/ou AWS CloudWatch para ***automatizar e monitorar*** a ***integridade e o status do bakcup***

- ***Recuperação e teste***
   - Documentação e implementação de planos detalhados para diferentes cenários de falha.
   - Realização regular de testes de recuperação de backups ***(Backup Drill)***

- ***Segurança e conformidade***
   - Utilização de ***criprografia em trânsito (TLS)*** e em ***repouso (S# Server-Side Encryption, RDS Encryption)***
   - Configuração de políticas do IAM para ***restrição de acesso*** aos backups
   - Utilizar registros e auditoria para garantir conformidade com requisitos regulatórios. ***(AWS CloudTrail)***

- ***Custo e otimização***
   - Utilização de ferramentas para análise de custos para monitorar e otimizar gastos com backup ***(AWS Cost Explorer)***
   - Gerenciamento de ciclo de vida através de políticas de movimentação de dados entre classes de armazenamento.
