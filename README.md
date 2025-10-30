# resumo_cloudformation
Resumo e anotações do laboratório "Implementando sua Primeira Stack com AWS CloudFormation" da DIO. Inclui exemplos de templates YAML, conceitos de IaC e documentação prática.

🏗️ Implementando sua Primeira Stack com AWS CloudFormation

Este arquivo contém meu resumo e anotações sobre o laboratório de implementação da primeira Stack utilizando AWS CloudFormation, proposto no bootcamp da DIO.

📘 O que é AWS CloudFormation
AWS CloudFormation é um serviço de Infraestrutura como Código (IaC) que permite criar, gerenciar e versionar recursos AWS usando arquivos YAML ou JSON.

Ele pode automatizar a criação de:
- S3 Buckets
- EC2 Instances
- VPCs e Subnets
- Security Groups (Firewall)
- IAM Roles e Policies
- Banco de dados (RDS, DynamoDB)
- Lambda Functions
- E muito mais

✅ Benefícios principais
- Padronização da infraestrutura
- Redução de erros humanos
- Infraestrutura versionada (Git)
- Automatização (IaC)
- Rollback automático em falhas
- Essencial para DevOps

🧠 Conceitos importantes
- Stack → conjunto de recursos criados pelo CloudFormation
- Template → arquivo YAML/JSON com definição de recursos
- Resources → serviços AWS a serem criados
- Parameters → variáveis para templates dinâmicos
- Outputs → valores exibidos após criação (ex: IP, bucket name)

-------------------------------------------------------------

🚀 Criando uma Stack simples
