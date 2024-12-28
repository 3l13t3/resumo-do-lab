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











