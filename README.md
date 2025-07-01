# Caldera Lab (AWS CloudFormation)

Este repositorio contiene una plantilla de CloudFormation para desplegar un entorno completo con MITRE Caldera en AWS.

## ¿Qué incluye?

- VPC dedicada
- Subnet pública
- Internet Gateway y tabla de ruteo
- Grupo de Seguridad (SSH y puerto 8888)
- EC2 Ubuntu 22.04 con Caldera preinstalado

## Uso

```bash
aws cloudformation create-stack \
  --stack-name caldera-lab \
  --template-body file://caldera-lab.yaml \
  --parameters ParameterKey=KeyName,ParameterValue=caldera-key \
  --capabilities CAPABILITY_NAMED_IAM
