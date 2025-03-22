# Resumo-do-lab AZ-900
## Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO


### AZ-900: Introdução aos conceitos básicos do Microsoft Azure ☁️
O que é computação em nuvem? => é o fornecimento de serviço de computação pela internet habilitando inovações mais rápidas, recursos flexíveis e economia de escalas.
Computação – Rede - Armazenamento

1. Nuvem privada = Quando se possui a própria arquitetura ambiente em nuvem no próprio Data Center, as organizações são responsáveis por 
     operar os serviços não fornece acesso aos usuários fora da organização.
2. Nuvem Publica = Quando a entrega de serviços e recursos a uma serie de clientes por meio de um único provide(no caso aqui 
     Microsoft)vantagem quando empresa multinacional.
3. Nuvem hibrida = Geralmente usado por empresa solida usando o melhor dos dois mundos nesse caso ambas se enxergam.
4. Nuvem Multi Cloud = Quando se trabalha em paralelo com mais de um ambiente (recurso no Azure e também na AWS) e ainda tem o Data center.

 ========== Comparando modelos: ========== 

=>	Nuvem publica = nenhuma despesa de capital para escalar verticalmente (CapEx) aplicativos podem ser provisionados e desprovisionados 
     rapidamente as organizações pagam apenas pelo que utiliza.
     
=>	Nuvem privada = As organizações que tem o controle sobre os recursos tais como: segurança, manutenção e atualizações do hardware.

=>	Nuvem Hibrida =  As organizações que determina onde executar os app, controla a segurança, a conformidade e os requisitos legais nesse 
     caso  fornece maior flexibilidade.

========== Comparando CapEx e OpEx: ==========

CapEx = despesa de capital => quando há gasto inicial de dinheiro em infraestrutura física essas despesas se reduzem com o tempo.

OpEx = despesa operacionais => gastar com produtos e serviços conforme necessários, pagamento conforme uso, cobrado imediatamente.
Modelo baseado em consumo.

Modulo 1: Conceitos de nuvem

 => Alta disponibilidade (SLA acordos de nível de serviço) isso garante que o serviço tenha disponibilidade máxima haja o que houver e como aplica-lo no dia a dia? 
=> Escalabilidade = capacidade de ajustar recursos para atender a demanda
Ex:. servidor arquivo adicionaríamos um disco, memoria RAM, CPU, ou seja, adaptando para uma nova necessidade.
=>Elasticidade = quando n sei o quanto o serviço irá crescer dai nesse caso e possível adicionar maquinas virtuais ou contêineres e caso haja queda os recursos implantados são automaticamente reduzidos(horizontalmente)
  	Ex: números de requisições, acessos

=> Confiabilidade = por ser um serviço descentralizado e permitir que você tenha recursos implantados em varias regiões do mundo naturalmente a nuvem da suporte u uma infraestrutura confiável e resiliente. (se recupera de falha e continua funcionando)

=>	Previsibilidade = Está muito relacionado a confiança, desempenho, custo conseguir permitir ao cliente utilizar recursos de ponta.
=>	Segurança = A nuvem oferece ferramentas de segurança, mas a implementação de muitas dela deve ser realizada pelo cliente.

========== Governança e Gerenciabilidade =========

Governança = como vão ser geridos os recursos, que a empresa precisa seguir (padrões corporativos)
Gerenciabilidade = podem ser feitos através do próprio portal, linha de comando, chamadas de APis, power shell etc... caso demanda grande há maneiras de implantar recursos usando modelo pre-configurado evitando a necessidade de fazer manual.

========== Tipos de Serviço de Nuvem na Azure ===========

IaaS – PaaS – SaaS => trata-se de serviços genéricos de nuvem cada provide possuem seus produtos.

	Infraestrutura como serviço = Servidores e armazenamento, Firewall e segurança de rede, Planta física e edifício de data center, serviço de nuvem mais flexível, você configura e gerencia o hardware para seu app. Maior gestão.

	Plataforma como serviço = Engloba IaaS, mas não foca no gerenciamento da infraestrutura <- ferramentas para desenvolvedores, analise de negócios de gerenciamento de data-base, Sistemas operacionais focado no desenvolvimento de app o gerenciamento é feito pelo provedor de nuvem. Gestão Intermediaria.

	Software como serviço = Aplicativos e Apps hospedados ,onde já se sabe o que entrega, o que determina (o que usuários veem) é o modelo de licenciamento adquirido, preço de pagamento conforme o uso pelo software utilizado. Menor gestão.

Modelo de responsabilidade compartilhada 

As responsabilidades diferem de acordo com o tipo de serviço adquirido e ou contratado.

Modulo 2: Arquitetura e Serviços do Azure

	Componentes de Arquitetura do Azure

Regiões = zonas de disponibilidade que se comunicam através da rede Microsoft são compostas por um ou mais datacenters próximos, fornece flexibilidade e escala para reduzir a latência do cliente as residências dos dados são preservadas abrangendo a oferta de conformidade. 

Pares de regiões e grupos de recursos = os pares consistem no mínimo 300 milhas de separação entre pares de região (os serviços de desastre recovery vão ser direcionados).

Regiões Soberanas = instancias fisicamente separadas dos serviços de nuvem do azure operada pela 21Vianet. Os recursos são os mesmos.

	Os recursos do Azure = maquinas virtuais, contas de armazenamento, redes virtuais, serviços de aplicativos, banco de dados SQL, funções.

	Grupo de recursos = container usado para gerenciar e agregar recursos de forma a organizar as coisas em uma única unidade, podem existir em apenas um grupo de recursos, e podem existir em diferentes regiões, podem ser movidos para diferentes grupos de recursos, os aplicativos podem utilizar vários grupos de recursos.

	Assinatura da Azure e grupos de gerenciamento

Conta do azure = uma única assinatura que pode utilizar vários recursos.
1 conta pode ter diversas assinaturas, mas 1 assinatura esta associada a apenas	uma conta, as assinaturas herdam as condições aplicadas ao grupo de gerenciamento.

=========== Criando grupo de recursos visão pratica ============

Criando grupo de Recursos = onde será criado o grupo que compartilhará mesmo ciclo de vida, permissões e politica.

Em Região será definido o local onde esse grupo estará 

     **Logs de atividades = quando queremos saber algo **
     ** IAM = permissões definidas no grupo/usuário **
     ** Visualizador de recursos = conforme é criado os recursos ele vai moldando os desenhos de forma a criar arvore **
     ** Eventos = está relacionado a automatizações **
     
Criando também uma rede virtual = que sera utilizado para o endereçamento( ex:. ao criar maquinas virtuais)é possível através de modelo via código criar automações de forma que seja replicado, trocando somente nome do resouce group gerando mais praticidade e rapidez na entrega do servico.

     E assim ficou meu primeiro grupo de recurso, vazio por hora, porem criado 😅
     
![Grupo De Recurso](https://github.com/3l13t3/resumo-do-lab/blob/main/GrupoRecursos.png)


========== Sobre recursos,dimensionamento em maquinas virtuais ==========

A configuração de recursos e o dimensionamento de máquinas virtuais (VMs) são essenciais para garantir que a infraestrutura virtualizada atenda às necessidades de desempenho, custo e escalabilidade. O processo envolve a escolha da quantidade de recursos (como CPU, memória e armazenamento) e a seleção da família de VMs mais adequada, levando em conta os requisitos de carga de trabalho.
A configuração dos recursos de uma máquina virtual inclui principalmente a quantidade de CPU, memória (RAM) e armazenamento. É importante entender a carga de trabalho que será executada na VM para determinar o que cada componente precisa.

-> CPU (Processador) Esta relacionado a capacidade de Processamento a escolha do número de núcleos de CPU e da frequência de operação depende da intensidade computacional da carga de trabalho. Aplicações como bancos de dados, processamento de dados e servidores de aplicação podem exigir mais núcleos ou uma maior frequência de CPU.

-> Memória (RAM) esta relacionado ao tamanho da Memória, a quantidade de RAM necessária depende de como a aplicação gerencia dados em memória. Por exemplo, bancos de dados e caches de aplicações demandam mais memória, enquanto outras cargas podem ser mais leves.desempenho de Memória/velocidade da memória também pode impactar o desempenho, mas normalmente é mais difícil de ajustar do que o tamanho.

-> Armazenamento o tipo de Armazenamento pode ser SSD (Solid State Drive), HDD (Hard Disk Drive) ou até opções mais avançadas como discos NVMe. VMs que envolvem grandes volumes de leitura e escrita frequentemente se beneficiam de SSDs a capacidade de Armazenamento determina o quanto de dados pode ser armazenado na VM. Aplicações que gerenciam grandes quantidades de dados, como sistemas de arquivos, bancos de dados ou sistemas de big data, precisarão de mais capacidade.

========== Escolha da Família de Máquinas Virtuais ==========

O Azure oferece diferentes famílias de máquinas virtuais, cada uma otimizada para cenários específicos. A escolha correta depende do tipo de carga de trabalho e dos requisitos de recursos da aplicação.
Famílias Baseadas em "Uso Geral"são equilibradas em termos de CPU, memória e armazenamento e são ideais para a maioria das aplicações gerais.
- Azure Série D =>  Equilibradas entre CPU e memória, adequadas para aplicativos como servidores web, bases de dados de médio porte e ambientes de desenvolvimento.

Famílias Otimizadas para Processamento são focadas em desempenho computacional intenso e são indicadas para cálculos pesados, como simulações científicas, renderização 3D, etc.
- Azure Série => Focadas em alta capacidade de processamento.

Famílias Otimizadas para Memória têm mais memória RAM disponível em relação à CPU, sendo indicadas para cargas de trabalho que exigem grande capacidade de memória, como bancos de dados em memória ou caches distribuídos.
- Azure Série E => Focadas em cargas de trabalho que exigem grande quantidade de RAM.

Famílias Otimizadas para Armazenamento são projetadas para fornecer alto desempenho em operações de leitura e gravação em discos e são indicadas para bancos de dados de alto desempenho ou big data.
- Azure Série Ls => Focada em alto desempenho de armazenamento.

Famílias para GPUs sao máquinas virtuais com GPUs ideais para cargas de trabalho como aprendizado de máquina, renderização gráfica, processamento de vídeo, etc.
- Azure Série N => Oferece VMs com GPUs NVIDIA para cargas de trabalho com gráficos ou IA.

 O que considerar na Escolha da Família de VMs?
->Custo = Cada família de VM tem um custo diferente. As VMs de alto desempenho (com mais CPU ou memória) tendem a ser mais caras. É importante balancear o custo com o desempenho exigido pela aplicação.
->Escalabilidade = Algumas famílias oferecem melhores opções de escalabilidade, como a capacidade de aumentar ou reduzir dinamicamente a quantidade de recursos conforme a carga de trabalho muda.
->Desempenho = Certifique-se de que a máquina virtual escolhida tem os recursos adequados para suportar o desempenho necessário para a aplicação.
->Localização e Disponibilidade = Considere onde a VM será hospedada e se ela está disponível em várias regiões, o que pode afetar a latência e a disponibilidade.
A configuração de recursos e o dimensionamento de máquinas virtuais são decisões cruciais para garantir que a infraestrutura virtualizada atenda de forma eficiente às necessidades de cada aplicação. A escolha da família de VMs deve considerar o tipo de carga de trabalho, os requisitos de desempenho e a relação custo-benefício, bem como a flexibilidade de dimensionamento e a escalabilidade da plataforma.

========= Armazenamento do Azure ==========

Contas de armazenamento deve ser um nome globalemente exclusivo(Tipo CPF)
ex:. STO+nomeprojeto/resoucegroup+nome deve ter acesso a internet em todo o mundo, determinar os serviços de armazenamento e opçoes de redundancia.

-> Redundancia de armazenamento
	
 .LRS(armazenamento com redundancia local) sua implantaçao e em datacenter individual 	  na regiao primaria sua durabilidade e de 11 noves.
	
 .ZRS(armazenamento com redundancia de zona) sua implantacao e em tres zonas de 	  disponibilidade na regiao primaria sua durabilidade e de 12 noves.
	
 .GRS(armazenamento com redundancia geografica) sua implantacao e em datacenter unico 	  no primario e regiao secundaria sua durabilidade e de 16 noves.
	
 .GZRS(armazenamento com redundancia de zona geografica) sua implantaçao e em tres 	  zonas de disponibilidade na regiao primaria e um unico datacerter na regiao 	  secundaria sua durabilidade e de 16 noves. 

 -> Os serviços  
 
 =>Blob do Azure otimizado para armazenaamento massivo de dados nao estruturados ex: Texto, dados binarios. Existem 4 modelos de dados que ele vai receber.

=> Disco do Azure fornece discos  para maquinas virtuais


=> Fila do Azure armazenamento para recuperaçao

=> Arquivos do Azure configura compartilhamento


=> Tabelas do Azure fornece opcao chave/atributo
  os pontos de extremidade publico tem o seguinte padrao
https://<storage-account-name>.blob.core.windows.net

-> Camadas de acesso 

Frequente = otimizado para acesso frequentes

Esporadico = otimizado para acesso com pouca frequencia pelo menos 30 dias

Frio = otimizado para acesso com pouca frequencia pelo menos 90 dias

Arquivo morto = otimizado para acesso raros pelo menos 180 dias  com requisito de latencia  flexivel.

->Migraçao para Azure

=> Azure Data Box utilizado para serviço de migraçao fisica ate 80T,dados sao totalmente criptografado.ideal para locais remotos  com conectividade limitada ou sem conectividade.

 => Opçoes de gerenciamento de arquivos - AzCopy(utilitario de linha de comando) copia dados para o Blobs ou arquivos para conta de armazenamento do Azure.
 
 => Gerenciamendor de armazenamento do azure(app instalado na maquina) é mais amigavel pois possui interface grafica e compativel com windows,MacOs e Linux.
 
 => Sincronizaçao de arquivos do Azure = sincroniza os arquivos  do azure e locais de forma biderecional,a camada de nuvem mantem os arquivos acessados com frequencia no local enquanto libera espaço. 


========= Microsoft Entra ID ==========

A segurança e identidade no Microsotf Azure sao aspectos fundamentais para proteger dados e recursos na nuvem, alem de garantir que somente usuarios e sistemas autorizados tenham acesso aos recursos adequados.

Para que as informações sejam validadas de forma correta usa-se o serviço de gerenciamento de identidade **Microsoft Entra ID**(ou antigamente chamado de Azure AD) com ele é feito a autenticação, logon único, gerenciamento de aplicativos, negócios para negócios(B2B) e gerenciar dispositivos.

* Autenticaçao: permite que você autentique usuarios e dispositivos(em nuvem ou on premise).suporta autenticaçao multifator(MFA) uma camada a mais de segurança.

*  Autorização: define o nivel de acesso,definem quais dados podem ser acessados inclusive em aplicativos de terceiros utilizando  atraves de politicas de acesso baseadas em funçao(RBAC)


   Otimizando custos no Azure 

========= Fatores que afetam os custos =========

1ºTipo de recurso

os custos sao especificos do recurso

2ºConsumo

com modelo pago conforme o uso

3ºManutençao

monitorar o volume do Azure e manter o ambiente

4ºArea geografica

dependendo da area geografica o mesmo tipo de recursos tem valores diferentes

5ºTrafego de rede

o custo para dados de saida ou dados entre recurso do azure é afetado por zonas de cobrança.

6º Assinatura

o tipo e  a configuraçao da assinatura

-> Azure Marketplace => onde e possivel encontrar recursos, experimente ou provisione app.
quand adicionado recurso nao nativo(o suporte n e da microsoft e sim do fabricante)


========== Calculando o custo total do Azure =========

Ela tras uma estimatica baseado nos recursos apresentados.
regiao - camada - opc de cobranca - opc de suporte - programa e ofertas - preco de desenvolvimento/teste do Azure.
TCO => ferramnta para ajudar ter uma visao de recursos(que ja tem,indo para a nuvem) dentro do Azure.
gerenciamento => relatorios de cobrança - enriquecimento de dados
ex: definir orçamento de gastos, quando custo excede os limites, recomendaçoes de custo.

========== Marcas(tags) no Azure ==========

sao elementos(nao obrigatorios e nao sao herdaveis) elas ->fornecem metadados aos recursos ->sao organizadas em uma taxonomia de maneira logica, ->consistem em um par nome-valor sao ->uteis para reunir informaçoes de cobrança.dica(criar apolice exigindo q se n tiver tag n sera criado ou colocar caso reccurso n tenha tag herdar do resource group )

Modulo 3: Gerenciamento e Governança

========= Governança e Conformidade =========


.Politicas(Azure Policy) => serve para criar padroes de conformidade referente a recursos dentro	da organizaçao ela fornece governança e consistencia de recursos com conformidade regulatoria,segurança,custo e gerenciamento.os conjuntos de regras sao definidas e aplicadas para garantir que os recursos sejam configurados de acordo com os requisitos da organizaçao ajudando a manter a governança sobre os recursos,permitindo automatizar e auditar a conformidade com as diretrizes da empresa.E como funciona? DEFINIR = a politica e definida de acordo com os requisitos especificos da organizaçao,como permitir ou negar o uso de determinado recurso. APLICAR = uma vez definida,apolitica pode ser aplicada em diferentes niveis.ex:assinatura, grupo de recursos ou uma unica instancia de recurso. AUDITAR = a politica pode ser configurada para auditar e relatar a conformidade sem forçar correçao de açoes ajudando a identificar recursos que estao fora das normas.AÇAO = dependendo da politica,pode permitir,negar ou modoficar açoes ou a criaçao de novos recursos que estejam em conformidade.E quais sao os tipo? POLITICA DE DEFINIÇAO onde e definido comportamento de um recurso,como tipo de maquina virtual permitida ou a utilizaçao de determinados TAG nos recursos. AUDITORIA permite auditar  se os recursos estao ou nao conformes com os requisitos da politica sem necessariamente bloquear açoes. FORÇAR aplicada para impedir que um recurso seja criado ou modificado se nao atender a determinada condiçoes.

.Bloqueio de recursos => Evitar que recursos sejam modificados, gerencia bloqueio 		na assinatura, grupo de recursos ou niveis de recursos individuais dentro 		do Azure.(bloqueios sao herdados)
	tipos de bloqueio  LER    Atualizar  Excluir 
	Excluir            sim    sim	     nao
	ReadOnly           sim    nao        nao


. Portal de confiança do serviço => Onde e identificado todas as regras que a 	microsoft segue(protocolo para atender as espectativas das empresas, 	governo).
.Microsoft Purview => Serve para gerenciamento de governança,risco e conformidade.
	tanto dados locais, multinuvem e de software como serviço.
	descoberta de dados automatizada	
	Classificaçao de dados confidenciais
	Linhagem de dados de ponta a ponta

 ========== Ferramentas de Gerenciamento e Implantação ==========
 
 -> ferramentas para interagir com o Azure
 
	.Portal do Azure     .Azure PowerShell
	.Azure Cloud Shell  .Interface de linha de comando(CLI)
 
->Azure Arc = ferramenta de multicloud ou seja é possível fazer a gestão num único portal(administra as maquinas que esta fora)

->Azure Resource Manager(ARM) fornece uma camada de gerenciamento que permite criar ,atualizar e excluir  recursos de assinatura do azure.

->Infraestrutura como código garante consistência na implantação em todo ecossistema de nuvem, gerencia a configuração em escala, provisionando ambientes adicionais  com base em uma configuração e um build padrão.


=========== Monitoramento Inteligente com o Azure ===========

As ferramentas de monitoramento são ideias para ajudar a garantir a saúde, o desempenho e a segurança dos recursos na nuvem, elas fornecem uma ampla gama de monitoramento e gerenciamento, desde infraestrutura ate segurança e aplicativos, permitindo um ambiente eficiente e protegido.

->	Azure Monitor 

É a plataforma centralizada de monitoramento para todos os serviços do Azure. Ele coleta dados de telemetria de várias fontes, como métricas, logs e diagnósticos.

-	Principais funcionalidades: 

o	Métricas e Logs: Coleta dados de métricas e logs dos recursos do Azure.

o	Alertas: Permite configurar alertas com base em métricas ou logs para notificar os administradores sobre qualquer anomalia.

o	Dashboards: Visualização personalizada dos dados coletados.

o	Application Insights: Uma extensão do Azure Monitor para monitorar e diagnosticar aplicações em tempo real.

-> Azure Log Analytics
-	Descrição: O Log Analytics é uma ferramenta do Azure Monitor que ajuda a consultar e analisar dados de logs.

o	Consultas em Log: Usa o Kusto Query Language (KQL) para consultas avançadas nos dados de log.

o	Armazenamento de Dados: Armazena logs e métricas de aplicativos, sistemas operacionais e serviços Azure.

o	Integração com outros serviços: Integra-se facilmente com o Azure Security Center, Azure Sentinel e outros.

->	Azure Application Insights 

-	Descrição: O Application Insights é uma ferramenta específica para monitoramento de desempenho de aplicativos. Ela ajuda a detectar problemas de desempenho e analisar o uso de aplicativos.
	
•	Principais funcionalidades:

o	Monitoramento de Aplicações: Coleta métricas e logs sobre a performance de aplicativos (front-end, back-end).

o	Análise de Falhas: Identifica e diagnostica falhas em tempo real.

o	Insights de Usuário: Fornece dados sobre como os usuários estão interagindo com a aplicação.

->	Azure Network Watcher

-	Descrição: O Network Watcher é uma ferramenta específica para monitoramento de rede no Azure.
	
•	Principais funcionalidades:

o	Monitoramento de Tráfego: Monitora e diagnostica o tráfego de rede entre recursos do Azure.

o	Visualização de Topologia de Rede: Permite visualizar a topologia de rede e suas interações.

o	Diagnóstico de Conectividade: Oferece ferramentas como a verificação de conectividade, capturas de pacotes e análise de fluxo de rede.

->	Azure Security Center 

-	Descrição: O Azure Security Center monitora a segurança dos recursos do Azure, oferecendo proteção contra ameaças e sugestões para melhorar a postura de segurança.
	
•	Principais funcionalidades: 

o	Avaliação de Segurança: Fornece recomendações baseadas nas melhores práticas de segurança.

o	Detecção de Ameaças: Detecta atividades suspeitas e gera alertas.

o	Compliance: Ajuda a garantir a conformidade com padrões de segurança, como ISO, GDPR, etc.


->	Azure Sentinel 

-	Descrição: O Azure Sentinel é uma solução de SIEM (Security Information and Event Management) baseada na nuvem para monitoramento e resposta a incidentes de segurança.
	
•	Principais funcionalidades: 

o	Análise de Dados de Segurança: Reúne dados de várias fontes e aplica análises para detectar ameaças.

o	Automação de Respostas: Permite automatizar respostas a incidentes de segurança.

o	Integração com Azure Security Center: Complementa o Azure Security Center com análises e visibilidade em tempo real.

->	Azure Automation 

-	Descrição: O Azure Automation ajuda a automatizar tarefas repetitivas e operações de TI.
  
•	Principais funcionalidades: 

o	Runbooks: Automatiza tarefas de gerenciamento de recursos no Azure.

o	Gestão de Atualizações: Automatiza o processo de atualização e patching de recursos.

o	Monitoramento e Alertas: Permite configurar alertas de execução de scripts e automações.


->	Azure Service Health

-	Descrição: O Azure Service Health fornece informações sobre a integridade dos serviços e recursos do Azure, alertando quando há problemas que possam afetar os serviços.
	
•	Principais funcionalidades: 

o	Alertas de Incidentes: Notifica sobre interrupções e degradações de serviço em tempo real.

o	Plano de Recuperação: Ajuda a criar planos de recuperação para garantir a continuidade dos negócios.

->	Azure Cost Management and Billing

-	Descrição: O Azure Cost Management ajuda a monitorar e gerenciar os custos de uso de recursos no Azure.
	
•	Principais funcionalidades: 

o	Monitoramento de Custos: Exibe o uso de recursos e os custos associados a eles.

o	Orçamento e Alertas de Custo: Permite definir orçamentos e configurar alertas para quando os custos atingem um limite.

->	Azure Advisor

-	Descrição: O Azure Advisor é uma ferramenta de recomendação personalizada que sugere boas práticas para otimizar a performance, segurança, custo e confiabilidade dos recursos no Azure.
  
•	Principais funcionalidades: 

o	Recomendações Personalizadas: Sugestões para melhorar a performance, segurança e reduzir custos.

o	Integração com outros serviços: Funciona em conjunto com outras ferramentas de monitoramento como Azure Monitor e Azure Security Center.











