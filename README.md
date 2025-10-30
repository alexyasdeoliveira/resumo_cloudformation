# resumo_cloudformation
Resumo e anotações do laboratório "Implementando sua Primeira Stack com AWS CloudFormation" da DIO.
"""
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

🚀 Criando uma Stack simples com S3

Template exemplo (YAML):

AWSTemplateFormatVersion: "2010-09-09"
Description: Criando um bucket S3 com CloudFormation

Resources:
  MeuBucketExemplo:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-bucket-exemplo-cloudformation-123

-------------------------------------------------------------

🔥 Criando Firewall (Security Group) via template

AWSTemplateFormatVersion: "2010-09-09"
Description: Security Group liberando HTTP e SSH

Resources:
  FirewallSecurityGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: Libera portas HTTP e SSH
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 22
          ToPort: 22
          CidrIp: 0.0.0.0/0
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0

⚠️ Observação: Em produção, o acesso à porta 22 deve ser limitado ao seu IP.

-------------------------------------------------------------

📎 Como criar a Stack no Console AWS
1. Acesse AWS CloudFormation
2. Clique em **Create Stack**
3. Escolha seu arquivo YAML
4. Confirme e crie

📎 Criando Stack via CLI

aws cloudformation create-stack \
  --stack-name MinhaPrimeiraStack \
  --template-body file://s3-bucket.yml

-------------------------------------------------------------

🎯 Objetivo do Desafio
- Aplicar conceitos de CloudFormation
- Criar primeira stack AWS
- Documentar aprendizados
- Publicar projeto no GitHub

-------------------------------------------------------------

✅ Aprendizados principais
- Infraestrutura como Código = padronização + automação
- YAML facilita reutilização e clareza
- CloudFormation gerencia recursos em blocos (stacks)
- Essencial em pipelines DevOps e CI/CD

-------------------------------------------------------------

📸 Evidências (caso tenha prints)
Crie uma pasta /images

/images
 ├─ stack-created.png
 ├─ cloudformation-events.png
 └─ s3-bucket-console.png

-------------------------------------------------------------

🎉 Conclusão
Esse projeto reforçou conceitos importantes de IaC, automação e boas práticas DevOps na AWS com CloudFormation.

"Infraestrutura como código não é tendência — é o padrão da computação moderna."
"""

