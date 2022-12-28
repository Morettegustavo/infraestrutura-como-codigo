# Infraestrutura como código
 Infraestrutura como código: preparando máquinas na AWS com Ansible e Terraform
 
![1-14](https://user-images.githubusercontent.com/88351614/209815821-56aca32c-0c74-403f-a70d-e109cacc7577.png)

***
## Preparando o ambiente
> Terraform: O Terraform é uma ferramenta de software de infraestrutura como código de código aberto criada pela HashiCorp. Os usuários definem e fornecem infraestrutura de data center usando uma linguagem de configuração declarativa conhecida como HashiCorp Configuration Language ou, opcionalmente, JSON

### Instalação Ubuntu
```
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=$(dpkg --print-architecture)] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt install terraform
```

***
> Ansible: Ansible é uma ferramenta de TI de código aberto para gerenciar, automatizar, configurar servidores e, implantar aplicativos, a partir de uma localização central. Ele inclui sua própria linguagem declarativa para descrever a configuração do sistema

### Instalação Ubuntu
```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt-get install ansible
```

***
## AWS CLI
Caso você ainda não tenha instalado a AWS CLI, basta ir a [página da AWS CLI](https://docs.aws.amazon.com/pt_br/cli/latest/userguide/getting-started-install.html) e seguir os procedimentos para o seu sistema operacional.

Depois de instalado você pode configurar a AWS usando o comando aws configure onde será requisitado a chave secreta (secret key) que pode ser criada [nessa pagina](https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fus-east-1.console.aws.amazon.com%2Fiam%2Fhome%3Fregion%3Dus-east-1%26skipRegion%3Dtrue%26state%3DhashArgs%2523%252Fsecurity_credentials%26isauthcode%3Dtrue&client_id=arn%3Aaws%3Aiam%3A%3A015428540659%3Auser%2Fiam&forceMobileApp=0&code_challenge=MOKhfr4ggOkCeths_jQs4elTWJWhy1Bc0NnOxn1jA6w&code_challenge_method=SHA-256) clicando em “criar chave de acesso” na aba “credenciais do AWS IAM”.

***