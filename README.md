# Well-Architected


O Well-Architected Framework foi desenvolvido para ajudar os arquitetos de nuvem a criar uma infraestrutura com os mais altos níveis de segurança, performance, resiliência e eficiência possíveis para seus aplicativos. Baseado em cinco pilares, excelência operacional, segurança, confiabilidade, eficiência de performance e otimização de custos, o Framework fornece uma abordagem consistente para que clientes e parceiros avaliem arquiteturas e implementem designs que serão escalados ao longo do tempo.

- Cobre estratégias e melhores práticas para arqutetura em cloud computing.
- Ele provê uma maneira de mensurar sua arquitetura de acordo com as recomendações da AWS, corrigindo deficiênias e endereçando de melhoria.
- Decisões mais assertivas, pensamento cloud-native e potencial impacto ao negócio.
- Melhora da conscientização sobre as melhore práticas de arquitetura.
- Endereça áreas de base (fundamentos) que frequentemente são negligenciadas.
- Provê uma abordagem conistente para avaliação da arquitetura.

![Well-arc-pilares](./img/well-arc-pilares.png)

## General principles design

- Não é preciso estimar (adivinhar) a capacidade requerida.
- Testes podem ser realizados em escala de produção.
- Crie e experimento facilmente as soluções.
- Permite a criação e evolução da arquitetura.
- Soluções são criadas em base nas necessidades (data-driven).
- Melhore através de `game days` (eventos em produção).


## Fundamentado em pilares

Baseado em cico pilares, excelência operacional, segurança, confiabilidade, eficiência de performance e otimização de custos, o Framework fornece uma abordagem consistente para que clientes e parceiros avaliem arquiteturas e implementem designs que serão escalados ao longo do tempo.

![Pilares](./img/pilares.png)

- **Execelência operacional:** se concentra em `executar` e `monitorar` sistemas entregar valor empresarial e melhorar continuamente processos e procedimentos. Os principais incluem gerenciamento e automação de alterações, reação a eventos e definição de padrões para gerenciar com êxito as operações diárias.
- **Segurança:** se concentra em proteger informações e sistemas. Os principais tópicos incluem `confiabilidade` e `integridade de dados`,identificação e gerenciamento de quem pode fazer o quê como o gerenciamento de privilégios, proteção de sistemas e estabelicimento de controles para detectar eventos de segurança.
- **Confiabilidade:** se concentra na capacidade de eveitar e se recuperar rapidamente das falhas para atender a demanda comercial e de clientes. Os principais tópicos incluem elementos básicos sobre configuração, requisitos entre projetos, planejamento e recuperação e como lidamos com as mudanças.
- **Eficiência de performance:** se concentra no uso eficiente de recursos de TI e computação. Os principais tópicos incluem seleção dos tipos e dos tamanhos certos dos recursos, tomando como base os requisitos de carga de trabalho, a performance do monitoramento e a tomada de decisões fundamentadas para manter a eficiência à medida que as necessidades comerciais evoluem.
- **Otimização de custos:** visa a evitar gastos desnecessários. Os principais tópicos compreensão e controle de onde o dinheiro está sendo gasto, seleção do núero certo e mais adequado dos tipos de recurso, análise dos gastos ao longo do tempo e escalabilidade para atender às necessidades de negócios sem gastar excessivamente.

## Usos comuns do Well-architected

- Aprender como criar arquiteturas nativas de cloud.
- Construir um base de conhecimento para mitigar falhas técnicas e riscos.
- Utilização como um mecanismo de padronização e governança antes da produção.
- Comparar a maturidade enre diferentes times, sistemas e produtos.
- Apresentar ao mercado características de `due-dilligence`.

---

# Execelência operacional

>> Alguns pilares podem ser adequados a cada tipo de realidade nas organizações como (`Reliability`, `Performance efficiency` e `Cost optimization`), porém **`Operational Excellence` e `Security` são pré-requisitos**.


## Design principles

- Perform operations as code (Execute a operação como código)
- Annotate documentation (anotar documentação)
- Make frequent, small, reversible changes (Alterações frequentes, peguenas e reversíveis)
- Refine operations procedures frequently (Refine os procedimentos de operação frequentemente e melhorias)
- Anticipate failure (Antecipação as falhas)
- Learn from all operational failures (Aprenda com todas as falhas na operação)

### Melhores praticas

#### 1 - Preparar/Planejar

- Business (solicitações workload)
- Checklist (validação)
- Treinamento (capacitação do time)
- Experimentação (testar time)

#### 2 - Operar

- Saúde da operação (monitoramento, metricas operacionais, Runbook "descrição e padronização do ambiente" e playbook "respostas automatizadas tratadas no playbook")
- Insigts técnicos e de negócios (Metricas voltadas ao negócio)
- Resposta a eventos (Automatização de resposta a eventos)

#### 3 - Evoluir

- Ciclos de melhorias incrementais
- Revendo as prioridades definidas
- Provendo feedback as áreas da empresa
- Compartilhando lições aprendidas e as oportunidades de melhorias das análises efetuadas
- `DevOps` para codificação, testes e deploy contínuo de forma automatizada na empresa

### Serviços Chaves AWS

Alguns serviços da aws para lhe auxiliar na execelência operacional

- CloudFormation (IaC)
- CloudWatch (Monitoramento)
- VPC Flow logs (Monitoramento do trafego de um VPC)
- Cloud trail (Autoria de chamadas de API)
- Config (Automatização e padronização de recursos)
- Elasticsearch (Analise de tedências)
- X-Ray (Visibilidade do workload)
---

# Segurança

### Design principles

- Implement a strong identify foundation (Implemente uma gestão de identidades bem fundamentada)
  - Privilegio minimo  
  - Separation of duties
  - Centralização da gestão de identidades
  - ~~Long-term credentials~~ (Utilize roles com permissões temporárias)
- Enable tracebility (Permitir a rastreabilidade)
- Apply security at all layers (Apligue segurança em todas as camadas)
- Automate security best pratices (Automatize as melhores práticas de segurança `IaC`)
- Protect data in trasit and at rest (Proteja os dados em trânsito e descanso)
- Keep people away from data (Mantenha as pessoas longe dos dados)
- Prepare for security events (Prepare-se para eventos de segurança)


#### Identify and Access management

- Somente o pessoal autorizado e autenticado tenha acesso aos recursos da maneira prevista.
  - AWS Shared Responsibility Model
  ![Shared_Responsibility_Model](https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg)
- Estrutura bem definida de gerenciamento de privilégios, como políticas de acesso com granularidade.
- Política de senhas fortes, Multi-factor authentication (MFA), Federação de diretórios e Credenciais temporárias.

#### Detective controls

- Controles detectivos devem ser utilizados para identificar potenciais ameaças de segurança ou incidentes, EX:
  - Avaliação de inventário de ativos e auditoria interna
- Implementação de controles que possam identificar e reagir a qualquer atividade anormal. Através do processamento de logs, eventos e monitoramento. Análise automatizadas e alarmes em tempo real.
- Gerencimaneto de logs é essencial para responder a eventos de segurança, análise forense e compliance com requisitos legais.

#### Infrastructure protection

- Proteção da infraestrutura inclui defesa em profundidade (múltilas camadas de defesa).
- Podem ser implementadas estratégias de segmentação de redes (pública e privada), inspeção de pacotes, isolamento de recursos, topologia de redes (gateway, tabelas de roteamento, etc.)
- Enforcement de tráfego de entrada e saída, monitoramento dos acessos e alertas.
- Hardening de sitema operacional e escolha de serviços gerenciados pela aws.

#### Data protection

- Classificação de dados para a proteção das informações (controle criptográficos, níveis de acesso, etc.).
- O cliente mantêm o controle completo sobre os dados, podendo utilizar serviços da AWS para proteger a confidencialidade e integridade dos dados.
- Logs detalhados de acesso, mecanismos de recuperação e durabilidade dos dados devem ser planejados. Podendo ser adotadas estratégias de replicação e gerenciamento do ciclo de vida dos dados.

#### Incident response

- Ainda que controles detectivos e de prevenção estejam implantados é necessário um processo de resposta a incidentes de segurança, mitigando os impactos que possam advir na operação e nos objetivos de negócios.
- A arquite do workload afeta diretamente a habilidade em responder a um incidente de segurança, isolando, contendo e restaurando a operação a um estado normal.
- Ferramentas e automatização devem ser configurados para responder a incidentes, logs poderão ser analizados e utilizados na resposta.

## Serviços chaves

- Identify and Access management (IAM)
- CloudWatch
- VPC - (Segmentação de redes (pública e privada), inspeção de pacotes, isolamento de recursos, topologia de redes (gateways, tabelas de roteamentos, etc.))
  - subnet
- Cloud Trail
- Config
- Organizations
- KMS
- WAF
- Shield
- CloudFront (CDN)

---

# Confiabilidade

> O pilar de confiabilidade se concentra na capacidade de evitar e se recuperar rapidamente das falhas para atender a demanda comercial e de clientes.

## Design principles

- Test recovery procedures (Testar procedimentos de recuperação)
- Automatically recover from failure (Recuperação automática de falhas)
- Scale horizontally to increase aggregate system availabilit (Escalar horizontalmente para aumentar a disponibilidade do sistema como um todo)
- **Stop guessing capacity** (Para de desperdiçar capacidade)
- Manage change in automation (Gerencie mudanças por automação)

## Foundation

- Antes de arquitetar qualquer sistema os recursos de base (fundamentos) que influenciam a confiabilidade do sistema devem estar reservados.
- A alocação de recursos deve olhar entre projetos, evitando a negligência de considerar uma única demanda dentro da empresa.
- No ambiente de computação em nuvem os recursos de base são de responsabilidade do provedor, cabendo ao cliente selecionar os recursos e capacidade apropriadas ao seu workload visando a confiabilidade.


## Change management

- Esteja ciente de como as mudanças afetam os sistemas para planejar proativamente. O monitoramento vai permitir que tendências sejam identificadas evitando problemas de capacidade ou quebra de SLAs.
- A arquitetura do sistema deve prever mudanças automatizadas no ambiente para aumentar ou reduzir capacidade de forma automatizada (`self-heal`).
- Controles no processo de gerenciamento de mudanças devem assegurar que o *enforcement* de regras sejam aplicados ao ambiente, garantido a confiabilidade do sistema somente de mudanças autorizadas.

## Failure management

- Falhas são esperadas em qualquer sistema com uma complexidade razoável. É importante ter ciência desssas falhas responder adequadamente e prevenir que ela volte a ocorrer.
- Você deve utilizar do monitoramento e automação para reagir aos eventos de falha.
- Backups e restore regulares deverão se efetuados para assegurar a recuperação seja no nível lógico ou físico. RTO (Recovery Time Objectives) e RPO (Recovery Point Objectives) devem estar definidos, sendo testado continuamente o processo de falhas e recuperação para garantir seu atendimento.
  - RTO (Recovery Time Objectives) - Representa quantas horas você leva para retornar a um estado de trabalho após um desastre..
  - RPO (Recovery Point Objectives) - Quanto tempo minha aplicação pode ficar offiline.

## Serviços chave

- **Amazon CloudWatch**
- IAM
- Trusted advisor
- CloudTrail
- Config
- Shield
- Cloud formation
- Auto scaling
- DR (disaster recovery)
  - S3
  - Glacier
- Network
  - VPC
- Security
  - KMS

---

# Eficiência de performance

Este pilar se concentra no uso eficiente de recursos de TI em computação.

## Design principles

- Democratize advanced tecnologies (Democratizar tecnologias avançadas)
- Go global in minute (Torne-se global em minutos)
- Use serveless architecture (utilize arquitetura de computação sem servidores)
- Experiment more often (Experimente com mais frequência)
- Mechanical sympathy (simpatia mecânica)

## Melhores praticas

### Selection

- A melhor solução para um sistema em particular irá variar baseado no tipo de workload, frequentemente com múltiplas soluções combinadas.
- Um sistema bem arquitetado pode utilizar múltiplas soluções para habilitar diferentes features e aumentar a performance.
- Através das opções de serviços da nuvem podem ser escolhidos aqueles que melhor atendem o workload, diferente das restrições on-premises onde fazemos a seleção muitas vezes baseado em investimentos anteriores.

### Compute

- A escolha de uma solução de compute pode variar de acordo com o design da aplicação, padrão de uso e configuração requeridas. A arquitetura pode utilizar diferentes soluções de computação para vários componentes habilitando features para aumentar a performance.
- A solução de computação errada de irá levar a aplicação a uma baixa eficiência de performance.
  - EC2
  - ECS
  - Lambda

### Storage

- A solução mais otimizada de storage irá variar conforme o sistema em particular e método de acesso requerido (bloco, arquivo,objeto), padrões de acesso (randomico ou seguencial), throughput, freguência de acesso (online, offine, archival), freguência de update (WORM, dunamic) e características de disponibilidade e durabilidade dos dados.
- Na AWS você irá encontrar soluções de storage virtualizada para atender uma grande gama de workloads. Utilizando o S3 (object storage), EBS (HDD ou SSD), EFS (Elastic file system), entre outros, os quais podem ser facilmente criados, expandidos, clonados e desprovisionados conforme a demanda.

### Database

- A solução mais otimizaa de banco de dados irá variar conforme o requerimento de disponibilidade, consistência, tolerância de partição, latência, durabilidade, escalabilidade e tipo de consulta (query).
- Muitos sistemas usam diferentes tipos de banco de dados para atender variados cenários de performance.
- Na AWS você irá encontrar soluções de banco de dados para atender todos os tipos de workload.
  - Amazon RDS como um banco de dados gerenciado para SQL.
  - DynamoDB para NoSQL com alta performance, escalabilidade e baixa latência.
  - Amazon Redshift para data warehouse na ordem de petabytes.
  - Amazon Neptune para Graph.
  - Amazon Timestream para séries temporais.
  - Elasticache como BD em memória, entre outros.

![Databases](https://d1.awsstatic.com/AWS%20Databases/Use%20Cases/isa.aaf804f08b600074fbe7a9dc7b3800fecf1df57e.png)

### Network

- A solução mais otimizada de rede irá variar conforme o sistema em particular baseado em requisitos de latência e throughput. Restrições físicas de rede são removidas se comparadas ao mundo on-premises.
- Técnicas de distribuição de conteúdo próximo ao usuário (edge techniques) ou placement group o qual especifica como as máquinas virtuais serão dispostas em hardware adjacente ou não.
- A AWS oferece features como Enhanced networking, Amazon EBS-otimized instances, Amazon S3 tranfer acceleration, Amazon CloudFront, Amazon route 53 latency routing, Amazon VPC endpoints e AWS directs connect para entrega de rede otimizada seja internamente na AWS, na conexão como o  Datacenter on-premises ou serviços pela internet aos usuários.

### Review

- Quando realizamos a arquitetura de soluções temos algumas opções a escolher, entretanto, ao longo do tempo novas tecnologias são lançadas e outras formas de atender o workload podem estar disponíveis as quais podem melhorar a eficiência de performance da sua arqutetura.
- Entede onde a arquitetura tem restrições de performance também pode ajudar a focar a análise e dimensionar novas soluções que podem melhor atender o workload.

### Monitoring

- Depois de implementar sua arquitetura você deve monitorar sua performance constantemente para remediar problemas antes de impactar seus clientes.
- O monitoramento através de métricas irá indicar por alarmes quanto o threshould foi atingido, devendo automaticamente iniciar uma ação de contorno para resolver o problema de performance dos componentes.
- Garanta que seu monitoramento não gere muitos falso-positivos ou que sobrecarregue o sistema monitorado com geração de dados. Ações automatizadas com base em triggers ou threshoulds evitam erros humanos e podem resolver problemas mais rapidamente. Eventos de testes podem validar a efetividade do monitoramento.

### Tradeoffs

- Quando arquitetamos uma solução precisamos pensar sobre o tradeoff da mesma, ou seja, uma decisão que afeta dois ou mais pontos distintos como a consistência em leitura/escrita de dados, durabilidade, localidade, tempo de resposta e latência para entrega com a melhor performance.
- Utilizando computação em nuvem você pode torna-se global em minutos, dispondo seus serviços aos usuários com alta performance e disponibilidade. Sejam nos níveis de web, app ou banco de dados.
- Realizar um tradeoff consistent em uma arquitetura complexa pode requerer testes para garantir que os benefícios pretendidos sejam realmente obtidos.

## Serviços chaves

- CloudWatch
---
# Cost optimization

O pilar de otimização de custos inclui a habilidade de executar sistemas para **entregar valor ao negócio através do menor preço dispónivel**.

## Design principles

- Adopt a consumption model (adote um modelo de consumo)
- Measure overall efficiency (avalie a eficiência global)
- Stop spending money on data center operations (Para de gastar dinehiro com operações de data center)
- Analyze and attribute expenditure (Analize e atribua as dispesas)
- Use managed and application level services to reduce cost of ownership (User serviços gerenciados e de nível de aplicação para reduzir o custo total de propriedade)

# Melhores praticas

## Expenditure awsreness (gastar com conciência)

- Em cloud computing as restrições de hardware são removidas, podendo ser provisionado um número virtualmente ilimitado de recursos.
- Todo o time deve ser treinado sobre o uso de recursos de forma consciente visando evitar gastos desnecessários.
- Custos devem ser associados a departamentos, projetos, sistemas e áreas de negócio.
- O usuo de TAGs é essencial para controle dos gastos, sendo acompanhado através do *Cost Explorer*.
- A AWS bugdets pode ser utilizado para controlar os custos dos serviços atuais e previsão futura.

## Cost-Effective resources

- Utilização dos recursos apropriados (instâncias, bando de dados, armazenamento, etc) é um ponto chave para economia.
- Serviços gerenciados podem reduzir os custos da conta, por exemplo, para e-mails e SMS.
- Instâncias (`on-demand` / `reserved` / `spot`).
- `CloudFront` para minimizar os custos de conteúdo web.
- Amazon aurora para reduzir os custos de licenciamento.

## Matching supply and demand

- A otimização de custos inclui a execução do workload gastando o mínimo possível, mas, capacidade extra para entender demandas sazonais ou de queda de componentes individuais devem ser consideradas.
- Na AWS você pode provisionar automaticamente recursos (auto-scaling, IOPs, buffer, etc). Quando melhor sua antecipação a essas demandas, menos você irá gastar para assegurar os recursos e atender a demanda do workload.
- Quando realizar o planejamento para atender demandas sazonais pense do padrão de uso, tempo de execução e tipo de recurso que será provisionado.

## Optimizing over time

- A AWS lança continuamente novas features e serviços, você deve rever sua arquitetura para assegurar que continua com o melhor custo-benefícios.
- Conforme seu requisito de negócio se altera seja efetivo também no desprovisinamento de recursos, serviços e sistemas não mais requeridos.


## Serviços chaves

- A ferramenta de `Cost Explorer` irá ajudar a ganhar visibilidade e insights sobre a utilização através de todos os workloads da organização.





***
# Referência

- [Well-Architected](https://aws.amazon.com/pt/architecture/well-architected/)
- [AWS Artifact](https://aws.amazon.com/artifact/?nc1=h_ls)
- [AWS Shared Responsibility Model](https://wa.aws.amazon.com/wat.concept.sharedrspmodel.en.html)
- [Overview Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/?ref=wellarchitected)
- [Disaster recovery](https://aws.amazon.com/pt/disaster-recovery/)
- [Databases](https://aws.amazon.com/pt/products/databases/)
