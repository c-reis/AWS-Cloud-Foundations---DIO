## Conceitos AWS - EC2/EBS/S3

### EC2 - Amazon Elastic Compute Cloud
- IAAS
> [!TIP]
> A infraestrtura é gerenciada pela AWS, mas o SO, atualizações, aplicação e segurança são gerenciadas pelo usuário.

- Fornece computação em núvem escalável (Servidor virtual na nuvem)
- Instâncias separadas por família
  - Uso geral: t2, t3, t4...
  - Otimizado para computação: c5, c6, c8...
  - Memória otimizada: r5, r6, x2...
  - Amrazenamento otimizado: d2, d3, h1...
  - Computação acelerada: dl1, f2, g7...
  - Alta performance: hpc6, hpc7, hpc8...

- Volume temporário: Excluído quando a instância é interrompida, hibernação ou encerrada
- Volume persistente: EBS

### AMI - Amazon Machine Images
- Imagem modelo de instâncias EC2
- Modela tanto as configurações da intância quanto o modelo de persistência
- Devem estar na mesma Region que a instância

### EBS - Elastic Block Store
- Fornece recurso para armazenamento em bloco
- Escalável e de alto desempenho
- Oferece criação de Snapshots(backup)
- Oferece criptografia

### S3 - Simple Storage Service
- Fornece recursos para armazenamento de objetos
- Escalável e de alto desempenho
- Não é global
- Classes:
  - S3 Express One Zone: Acesso frequente, única zona de disponibilidade (Baixo custo) 
  - S3 Standard: Acesso frequente, múltiplas zonas de disponibildade
  - S3 Glacier: Baixa frequência de acesso, múltiplas zonas, baixo custo
- Fornece recurso para versionamento

### - OUs - Organizational Units
- Agrupar contas
- Unificar controle de políticas
- Recomendado pela AWS a configuração de várias contas:
  - Benefícios:
    - Faturamento simplificado
    - Controle de segurança flexíveis
    - Adpatação a necessidade do negócio
- Deve ser criadas baseadas em funções ou conjunto de controles
> [!TIP]
> Recomenda-se a criação de OUs de Segurança e Infraestrutura
> Internamente seprando ambiente produtivo de não produtivo




