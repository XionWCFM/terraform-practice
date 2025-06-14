
```
outputs.tf

output "instance_id" {
  description = "ID of the EC2 instance"
  value       = aws_instance.app_server.id
}

output "instance_public_ip" {
  description = "Public IP address of the EC2 instance"
  value       = aws_instance.app_server.public_ip
}
```

output 플래그를 정의해두고 terraform apply를 수행한 뒤엔 terraform output을 통해 아웃풋을 확인할 수 있습니다.

```
terraform output
instance_id = "i-0f747a85672da55ce"
instance_public_ip = "35.89.183.153"
```
