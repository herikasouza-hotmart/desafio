Desafio Engenheiro de Networking
**Descrição enviada pelo Jonas

Etapa 1 - Ambiente Cloud (parte prática)

O desafio consiste em construir uma stack de infraestrutura que provisione um ambiente para rodar duas aplicacoes, sendo que cada uma delas deverá rodar em um cloud provider distinto (AWS, Azure ou GCP) conforme dados abaixo:

Aplicação 1 (servidor 1) - (Cloud Provider 1): Servidor linux com qualquer serviço http habilitado (apache, nginx, etc...)
Aplicação 2 (servidor 2) - (Cloud Provider 2): A aplicação 2, deverá rodar em um outro servidor e em um segundo cloud provider. A aplicação 2, deverá ser um script em qualquer linguagem, que ao ser executado, faz uma chamada http (GET) na aplicacao 1 do servidor 1, imprimindo na tela o tempo gasto para essa requisição (tempo de resposta), e se possível, também o status code dessa chamada (200, 404, etc..).
A comunicação entre a aplicação 1 (cloud provider 1) e a aplicação 2 (cloud provider 2), deverá ser feita de forma privada, exemplo VPN.
Observações importantes:

Ambos os servidores devem responder pelo mesmo domínio de DNS.
Para aumentar um pouco a segurança, o acesso ao serviço web do servidor 1, deverá ser restrito somente ao servidor 2.
A aplicação 2 devera chamar aplicação 1 através de DNS, e não por IP.
Tecnologias sugeridas:

Cloud Formation
Terraform
Ansible
Python
Shell Script
Instancias de maquinas virtuais OBS: outras ferramentas/soluções também são bem vindas, desde que funcione de forma simples e eficiente.
Etapa 2 - Topologia (Desenho arquitetural)

O cenário construído na Etapa 1 irá atender a necessidade de uma grande empresa do ramo de mobilidade. 

Esta empresa tem o desafio de migrar todo o seu workload, atualmente onpremises, para este novo ambiente de nuvem. 

Também são características importantes desta empresa:

O Workload atual está hospedado em dois datacenters distintos, com serviços operando em modo active-active nestes dois DCs.
A matriz da empresa possui aproximadamente 3000 funcionários, que também usam os sistemas hospedados nos DCs.
No prédio da matriz existe uma grande operação de call center, utilizando soluções 100% IP. Os servidores e demais equipamentos desta solução estão atualmente dentro dos DCs
A empresa possui aproximadamente 1500 filiais e franquias espalhadas em todo o Brasil e na américa latina.
Dentro das filiais, os funcionários utilizam várias aplicações que estão hospedadas nos DCs e também na internet.
O time de Cyber Security está muito empenhado em ter um alto nível de segurança na infraestrutura de redes destas filiais tanto na LAN/WLAN, quanto na WAN.
A comunicação de voz entre matriz e filiais é feita através de tecnologia IP.
As filiais possuem em média 5 computadores, 1 impressora, 2 telefones IP e 8 dispositivos conectados na rede wifi (tablets e smartphones)
O time de redes se preocupa muito em manter uma altíssima qualidade e disponibilidade do link destas filiais, com um desafio extra de pensar em otimizar custos
O time de redes se preocupa muitíssimo com o monitoramento de toda essa infraestrutura, para que possam agir pro ativamente junto ao NOC em caso de possíveis problemas.
O time de redes está redesenhando a atual arquitetura de DNS, DHCP e autenticação dos dispositivos de rede para atender a demanda atual e também para os próximos anos.
 

Desenhe uma arquitetura que você vê como estado da arte, de acordo com o cenário descrito acima e possíveis evoluções. 

Você tem um check em branco nas mãos. Capriche em sua topologia e soluções. 

Abuse da ousadia, protagonismo, inovação, e também, austeridade. Lembre-se que o negócio desta empresa depende desta infraestrutura, e que ela, a empresa, está iniciando uma jornada de migração de todo o seu workload para nuvem. 

Esta jornada está prevista para durar aproximadamente 18 meses.

 

Em nosso próximo bate papo, iremos falar sobre:

Organização
Percentual de entrega
Criatividade
Roadmap de futuras melhorias
Qualidade da documentação
Uso de ferramentas de automatização
Elegância na solução proposta
Simplicidade e eficiência
Técnicas e boas práticas de segurança
Entrega:

A documentação e código (caso exista) deverão ser entregues em um repositório git hospedado na nuvem (ex: GitHub).
