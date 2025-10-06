
 ![alt text](stack_cformation-1.png)
 
 ***Implementando uma Stack com AWS CloudFormation***

Este repositório faz parte do Bootcamp Santander Code Girls/Dio, e tem como proposta registar insights das aulas sobre: o uso de uma Stack no AWS CloudFormation.
Em **AWS CloudFormation**, uma **stack** é o resultado da execução de um “Template”. Podemos considerar uma stack como sendo um contêiner lógico que agrupa todos os recursos da AWS que foram criados a partir de um único template. Tenha em mente, enquanto o template é o plano da sua infraestrutura, a stack é a implementação desse plano.
**Como funciona**

![alt text](image.png)
1.	Primeiro, crie um template em formato Yaml ou Json:
Este arquivo de texto descreve todos os recursos da AWS que você deseja criar por exemplo, um servidor EC2, um banco de dados RDS, um bucket S3 ou um grupo de segurança e como eles se conectam.
![alt text](image-1.png)
2.	Em seguida, use o CloudFormation para criar uma stack a partir do template: 
O CloudFormation lê o template e provisiona todos os recursos específicos, garantindo que eles sejam criados na ordem correta, com as configurações corretas.
![alt text](image-2.png)
3.	O resultado final desse processo é a Stack. A Stack se torna assim a unidade de gerenciamento:
A Stack é o conjunto completo de todos os recursos que foram criados a partir do template
**O Papel da Stack no**:
1.*Gerenciamento do Ciclo de vida do seu projeto*
  Criação: A stack sabe que precisa criar o Grupo de Segurança antes da instância EC2.
  Atualização: por exemplo deseja alterar o tipo de instância.
  Exclusão: quando não for mais necessário, a stack pode ser removida.
Vantagens: Automação Total.
2.*Gerenciamento Unificado.
  Repetibilidade*.
  O template é o plano detalhado, e nele que especificamos: 
 	O tipo de servidor – InstanceType (Tipo de CPU e memória)
 	O sistema operacional – Linux, Windows ou Mac
 	As permissões e regras: SecurityGroup e IamRoles.
Nele colocamos todas as informações em um único arquivo de texto. Ao ter o plano completo e detalhado, entregamos ao cloudFormation. Este lê o plano e, com base nas especificações existentes, cria todos os recursos na ordem correta e com as configurações exatas.
O CloudFormation só precisa do template para te entregar a Stack.   O Stack é o resultado final, transformando todos os recursos separados em uma única unidade.
E a stack é a forma como o CloudFormation organiza e gerencia o resultado final do projeto, transformando os recursos separados em uma única unidade.
