# Day 3

## Terraform

### Resumo

**Terraform** é uma ferramenta de automação de infraestrutura como código (IaC) que permite provisionar, gerenciar e versionar recursos de nuvem de forma segura e eficiente. Ademais, o Terraform é uma ferramenta de linha de comando que permite que você crie, altere e destroe recursos de nuvem de forma segura e eficiente. Terraform pode gerenciar tanto recursos existentes quanto recursos que ainda não foram criados.

**Terraform provider** é um plugin que permite que o Terraform se comunique com um serviço de nuvem específico. Por exemplo, o provedor AWS permite que o Terraform se comunique com os serviços AWS.

**Terraform module** é um agrupamento de recursos que podem ser reutilizados. Por exemplo, um módulo pode conter um conjunto de recursos que são usados para criar um ambiente de desenvolvimento.

**Terraform vs Ansible :** O Terraform é uma ferramenta de automação de infraestrutura , já o Ansible é uma ferramenta de gerenciamento de configuração. Eles e complementam na construção de uma infraestrutura.

**Hashicorp configuration language (HCL)**

- É a linguagem de configuração declarativa usada pelo Terraform. O HCL é baseado em JSON e é compatível com YAML.

  - ```
    <BLOCK TYPE> "<BLOCK LABEL>" "<BLOCK LABEL>" {
    <IDENTIFIER> = <EXPRESSION>
    <IDENTIFIER> = <EXPRESSION>
    <IDENTIFIER> = <EXPRESSION>
    }
    ```

- Resources

  - ```
      resource "aws_instance" "example" {
        ami           = "ami-2757f631"
        instance_type = "t2.micro"
      }
    ```

- Data Sources

  - ```
      data "aws_instance" "example" {
        name = "example"
      }
    ```

- Providers

  - ```
      provider "aws_instance" {
        token = ""
      }
    ```

- Terraform Settings

  - ```
      terraform {
        required_version = ">= 0.12"
        required_providers {
          aws = {
            source  = "hashicorp/aws"
            version = ">= 2.0"
          }
        }
      }
    ```

- Variables

  - ```
      variable "example" {
        token = ""
        default = ""
        description = ""
      }
    ```

- Outputs

  - ```
      output "instance_ip" {
        value = ip
      }
    ```
