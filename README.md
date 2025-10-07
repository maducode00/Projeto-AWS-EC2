# Projeto-AWS-EC2
Este repositório documenta um laboratório prático realizado na AWS.
🎯 Objetivo do desafio

O desafio proposto consistiu em:

- Criar uma instância EC2 com sistema operacional Windows
- Acessar a instância via Session Manager (sem SSH)
- Preparar o ambiente com arquivos e configurações
- Criar uma AMI personalizada da instância
- Criar um Snapshot do volume EBS
- Lançar uma nova instância a partir da AMI
- Validar o funcionamento da nova instância
- Representar toda a arquitetura em um diagrama técnico

📁 Conteúdo do repositório
aws-ec2-ami-snapshot/ 
├── diagrama-arquitetura.png # Diagrama visual da arquitetura AWS
├── comandos-session-manager.txt # Comandos executados via PowerShell 
├── README.md # Documentação completa do projeto 
└── relatorio-final.pdf # Relatório técnico do laboratório


---

## 🧠 Principais conceitos utilizados

### 🔹 Amazon EC2
Serviço de computação elástica que permite criar máquinas virtuais na nuvem. Neste projeto, foi usada uma instância Windows com acesso via Systems Manager.

### 🔹 Session Manager
Ferramenta do AWS Systems Manager que permite acesso seguro à instância EC2 sem necessidade de abrir portas ou usar chaves SSH. Requer uma IAM Role com a política `AmazonSSMManagedInstanceCore`.

### 🔹 IAM (Identity and Access Management)
Sistema de controle de acesso da AWS. Foi criada uma Role específica para permitir que a instância EC2 fosse gerenciada via Session Manager.

### 🔹 AMI (Amazon Machine Image)
Imagem que contém o sistema operacional, configurações e dados da instância. Permite criar novas instâncias idênticas à original.

### 🔹 Snapshot EBS
Backup incremental do volume de armazenamento da instância. Pode ser usado para restaurar dados ou criar novos volumes.

### 🔹 Security Group
Conjunto de regras de firewall que controla o tráfego de rede para a instância EC2.

---

## 🗂️ Diagrama da arquitetura

![Diagrama da arquitetura](diagrama-arquitetura.png)

### 🔍 Descrição do diagrama

O diagrama representa os principais componentes da arquitetura AWS utilizados no projeto:

- **INSTANCIA EC2**: Máquina virtual criada e configurada
- **EBS**: Volume de armazenamento persistente da instância
- **SNAPSHOT**: Backup do volume EBS
- **SECURITY GROUP**: Regras de acesso à instância
- **USUARIO/ADM**: Usuário que acessa e gerencia os recursos
- **IAM**: Controle de permissões e políticas
- **Session Manager**: Canal seguro de acesso à instância via terminal

As conexões entre os blocos representam o fluxo de criação, acesso e backup dos recursos.

---

## 📚 Referências técnicas

- [Documentação oficial do Amazon EC2](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/concepts.html)
- [Session Manager – AWS Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html)
- [Guia de criação de AMIs](https://docs.aws.amazon.com/pt_br/AWSEC2/latest/UserGuide/creating-an-ami-ebs.html)
- [Snapshots EBS](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)
- [IAM Roles para EC2](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html)

---

## 👩‍💻 Autora

**Maria**  
Estudante de Cloud Computing | Exploradora de Arquiteturas AWS  
Paulista – PE, Brasil
