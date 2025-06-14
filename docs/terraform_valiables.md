## 테라폼 변수

Terraform은 현재 디렉토리에 있는 .으로 끝나는 모든 파일을 로드하므로 .tf, 원하는 대로 구성 파일의 이름을 지정할 수 있습니다

## 테라폼 apply 할때 변수 주입하기

```
terraform apply -var "instance_name=YetAnotherName"
```

요런식으로 사용하면 기존에 작성되어있는 내용에 오버라이딩이 가능하다.
