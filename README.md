<div id="topo"></div>

# AWS Cloud Practitioner Foundational 2023

<p align="justify">Este repositório foi criado com o intuito de realizar minhas anotações durante meus estudos para a certificação <a href="https://aws.amazon.com/pt/certification/certified-cloud-practitioner/">AWS Certified Cloud Practitioner</a> e compartilhá-las com quem precise.</p>

<div id="topicos"></div>

* [Tópicos](#topicos)
    - [Pesos](#Pesos)
    - [Conceitos de nuvem](#nuvem)
    - [Segurança e conformidade](#seguranca)
    - [Tecnologia](#tecnologia)
    - [Faturamento e preços](#faturamento)
<hr>

<div id="Pesos"></div>

## Pesos
Domínio | % do exame
---------|----------|
Domínio 1: Conceitos de nuvem | 26%  
Domínio 2: Segurança e conformidade | 25%  
Domínio 3: Tecnologia | 33%  
Domínio 4: Faturamento e preços  | 16%  
TOTAL | 100%

**[REFERÊNCIA](https://d1.awsstatic.com/pt_BR/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf)** 
<hr>

<div id="nuvem"></div>

## Conceitos de nuvem

### 1. O que é Cloud Computing?
Define-se na utilização de recurso de TI sob demanda por meio da internet, permitindo escabilidade, e sua cobrança é realizada de acordo com o uso.

**[REFERÊNCIA](https://aws.amazon.com/pt/what-is-cloud-computing/)**

### 2. Vantagens em se utilizar Cloud Computing
* **Agilidade:** maior agilidade no processo de desenvolvimento e implatanção de soluções.
* **Elasticidade:** permite provisionar mais recurso às soluções de acordo com a demanda, aumentando e diminuindo seus recursos de forma automática, sem interrupção do serviço.
* **Economia de custo:** o custo é mais baixo devido a cobrança ser realizada de acordo com a utilização dos recursos, além de possibilitar a contratação de planos de economia, diminuindo ainda mais seu preço.
* **Implantação global em questão de minutos:** a nuvem possibilita ampliar seus atividades em várias regiões geográficas e implantação em minutos.

**[REFERÊNCIA](https://docs.aws.amazon.com/pt_br/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)**

### 3. Tipos de Cloud Computing
* **IaaS (Infrastructure as a Service):** oferece o mais alto nível de flexibilidade e controle de gerenciamento sobre recursos, contendo os componente básicos de TI em nuvem. Exemplo AWS EC2.
* **PaaS (Plataform as a Service):** não é necessário o gerenciamento de infraestutura (hardware e sistemas operacionais), focando na implantação e gerenciamento das aplicações. Exemplo AWS Lambda.
* **SaaS (Software as a Service):** oferece um produto completo, executado e gerenciado pelo provedor de serviços. Refere-se às aplicações de usuário final. Exemplo Amazon RDS.

<p align="center">
  <a><img src="./imgs/types.jpg"></a>
</p>

**[REFERÊNCIA](https://aws.amazon.com/pt/types-of-cloud-computing/)**

### 4. Modelos de Cloud Computing
* **Public:** modelo mais comum e utilizado, nesse tipo de contrato, o provedor tem servidores próprios onde aloca dados, softwares e sistemas de seus clientes de forma independente e isolada.
* **Private:** bem parecida com o modelo público, com a diferença que a infraestrutura contratada não é compartilhada com outros clientes.
* **Hybrid:** permite a mesclagem da praticidade da nuvem pública com a personalização e contenção da nuvem privada.
<hr>

<div id="seguranca"></div>

## Segurança e conformidade

### 1. Modelo de responsabilidade
Constitue em uma responsabilidade compartilhada entre a AWS e o cliente. A AWS opera, gerencia e controla os componentes do sistema operacional do host e a camada de virtualização, até a segurança física das instalações em que o serviço opera. O cliente assume a gestão e a responsabilidade pelo sistema operacional convidado (inclusive atualizações e patches de segurança), por outros softwares de aplicativos associados e pela configuração do firewall do grupo de segurança fornecido pela AWS.
* **Responsabilidade da AWS:** segurança da nuvem: a AWS é responsável por proteger a infraestrutura que executa todos os serviços oferecidos na sua nuvem.
* **Responsabilidade do cliente:** segurança na nuvem: a responsabilidade do cliente será determinada pelos Serviços de nuvem AWS selecionados por ele.

<p align="center">
  <a><img src="./imgs/responsibility.jpg"></a>
</p>

**[REFERÊNCIA](https://aws.amazon.com/pt/compliance/shared-responsibility-model/)**
<hr>

<div id="tecnologia"></div>

## Tecnologia

### 1. AWS CLI e CloudShell
* **AWS CLI:** ferramenta unificada para o gerenciamento de seus produtos da AWS, instalada localmente nas estações de trabalho.
* **CloudShell:** shell pré-autenticado baseado em navegador onde é possível iniciar diretamente do AWS Management Console.

**[REFERÊNCIA](https://docs.aws.amazon.com/pt_br/cloud9/latest/user-guide/sample-aws-cli.html)**

### 2. Infraestrutura global da AWS
A Nuvem AWS abrange 99 zonas de disponibilidade em 31 regiões geográficas por todo o mundo, com planos já divulgados para mais 15 zonas de disponibilidade e outras 5 regiões da AWS no Canadá, Israel, Malásia, Nova Zelândia e Tailândia. 

<p align="center">
  <a><img src="./imgs/global.png"></a>
</p>

### 3. Regiões da AWS
Local físico em todo o mundo onde datacenters são agrupados. Cada grupo de datacenters lógicos é chamado de zona de disponibilidade. Cada região da AWS consiste no mínimo em três AZs isoladas e separadas fisicamente em uma área geográfica.

### 4. Zonas de disponibilidade (AZ)
Consistem em um ou mais datacenters distintos com energia, rede e conectividade redundantes em uma região da AWS. As AZs proporcionam aos clientes a capacidade de operar suas aplicações com alta disponibilidade, tolerância a falhas e escalabilidade em níveis superiores aos que um único datacenter pode oferecer. As AZs são fisicamente separadas por uma distância significativa (vários quilômetros) das outras AZs, embora todas estejam em um raio de até 100 km entre si.

### 5. Zonas locais
Aproximam a computação, o armazenamento, o banco de dados e outros produtos da AWS selecionados dos usuários finais. Com isso é possível executar facilmente aplicativos altamente exigentes que exigem latências em milissegundos para seus usuários finais, como criação de conteúdo de mídia e entretenimento, jogos em tempo real, simulações de reservatórios, automação de projetos eletrônicos e machine learning.

### 6. AWS Wavelength
Implantações de infraestrutura da AWS que incorporam serviços de computação e armazenamento da AWS aos datacenters dos provedores de telecomunicações na borda das redes 5G e acessam facilmente a variedade de serviços da AWS na região.

**[REFERÊNCIA](https://aws.amazon.com/pt/about-aws/global-infrastructure/)**

### 7. AWS Outspots
Solução totalmente gerenciadas que fornece infraestrutura e serviços da AWS para praticamente qualquer local da borda ou on-premises para uma experiência híbrida verdadeiramente consistente. As soluções do Outposts permitem que os clientes estendam e executem serviços da AWS nativos on-premises.

**[REFERÊNCIA](https://aws.amazon.com/pt/outposts/)**

<hr>

<div id="faturamento"></div>

## Faturamento e preços 