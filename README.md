# desafio
# Desafio Localiza
**Etapa 1 - Ambiente Cloud (parte prática)**

O desafio consiste em construir uma stack de infraestrutura que provisione um ambiente para rodar duas aplicacoes, sendo que cada uma delas deverá rodar em um cloud provider distinto (AWS, Azure ou GCP) conforme dados abaixo:
>>
# **Aplicação 1 (servidor 1) - (Cloud Provider 1): Servidor linux com qualquer serviço http habilitado (apache, nginx, etc...)

>> Foi criado um servidor com SO CentOS na GCP com apache apenas com index.html para ser consumida pela aplicaçao 2
>> IP:10.182.0.3
>> Nome:webapp.herikamachado.com
>>
# **Aplicação 2 (servidor 2) - (Cloud Provider 2): A aplicação 2, deverá rodar em um outro servidor e em um segundo cloud provider. A aplicação 2, deverá ser um script em qualquer linguagem, que ao ser executado, faz uma chamada http (GET) na aplicacao 1 do servidor 1, imprimindo na tela o tempo gasto para essa requisição (tempo de resposta), e se possível, também o status code dessa chamada (200, 404, etc..).

>> Foi criado um servidor com SO CentOS na GCP criei um script para buscar o status da chamada (response) + o tempo gasto para requisiçao
>> IP:10.0.1.4
>> Nome:webmonitor.herikamachado.com
>>
# **A comunicação entre a aplicação 1 (cloud provider 1) e a aplicação 2 (cloud provider 2), deverá ser feita de forma privada, exemplo VPN.
Observações importantes:

>>Criado VPN AWS e GCP
>>Config VPN UP AWS
>>[![Screen-Shot-2021-07-28-at-22-38-56.png](https://i.postimg.cc/LsVLCWKy/Screen-Shot-2021-07-28-at-22-38-56.png)](https://postimg.cc/rdKDzQpW)
>>Config VPN UP GCP
>>[![Screen-Shot-2021-07-28-at-22-40-00.png](https://i.postimg.cc/QCF7MxBP/Screen-Shot-2021-07-28-at-22-40-00.png)](https://postimg.cc/FkQzWvVg)
>>
# **Ambos os servidores devem responder pelo mesmo domínio de DNS.

>>Dominio privado herikamachado.com
>>[![Screen-Shot-2021-07-28-at-22-42-30.png](https://i.postimg.cc/L8t15WXH/Screen-Shot-2021-07-28-at-22-42-30.png)](https://postimg.cc/9DfMNJZS)
>>
>>Para aumentar um pouco a segurança, o acesso ao serviço web do servidor 1, deverá ser restrito somente ao servidor 2.
[![Screen-Shot-2021-07-28-at-22-29-09.png](https://i.postimg.cc/L5gSXrmv/Screen-Shot-2021-07-28-at-22-29-09.png)](https://postimg.cc/8fG9XXJr)

>>A aplicação 2 devera chamar aplicação 1 através de DNS, e não por IP.

[![Screen-Shot-2021-07-28-at-22-33-28.png](https://i.postimg.cc/hPFvm0Nh/Screen-Shot-2021-07-28-at-22-33-28.png)](https://postimg.cc/grDGF3zP)



Tecnologias sugeridas:

Cloud Formation
Terraform
Ansible
Python
Shell Script
Instancias de maquinas virtuais OBS: outras ferramentas/soluções também são bem vindas, desde que funcione de forma simples e eficiente.
