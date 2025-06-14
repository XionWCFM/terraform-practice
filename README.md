# scripts

```
terrafrom state list
```

output : `aws_instance.app_server`

terraformstate에서 관리되고 있는 리소스가 aws_instance.app_server라는 뜻

# aws

```tf
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.16"
    }
  }

  required_version = ">= 1.2.0"
}

provider "aws" {
  region  = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}
```

## provider

provider는 terraform이 리소스를 생성하고 관리하는 데 사용하는 플러그인입니다.

테라폼 구성에서 여러 공급자 블록을 이용해서 다양한 공급자의 리소스를 관리할 수 있어요

여러 공급자를 함께 사용할 수도 있습니다.

## resource

resuorce 에서는 인프라의 components를 정의합니다. 예를들어 EC2 인스턴스가 될수도 있고 heroku 애플리케이션일수도있습니다.

## 디렉토리 초기화

새로운 구성을 생성하거나 버전 제어에서 기존 구성을 체크아웃하는 경우 디렉토리를 init해주는 작업을 수행해주어야합니다.
