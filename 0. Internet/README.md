## Rede
	Grupo de computadores ou outros dispositivos conectados entre si. A internet é uma rede de redes

- Foi desenvolvida no final da década de 1960 pelo departamento de defesa dos Estados Unidos como um meio de criar uma rede de comunicação descentralizada que pudesse resistir a um ataque nuclear. 

## Visão Geral

- A internet funciona conectando dispositivos e sistemas de computador usando um conjunto de protocolos padronizados. Esses protocolos definem como as informações são trocadas entre dispositivos e garantem que os dados sejam transmitidos de forma confiável e segura
- O núcleo é uma rede global de roteadores interconectados que são responsáveis por direcionar o tráfego entre diferentes dispositivos e sistema.
- Quando você envia dados pela internet eles são divididos em pequenos pacotes enviados do seu dispositivo para um roteador. O roteador examina o pacote e o encaminha para o próximo roteador no caminho para o seu destino. 

- Protocolo de internet (IP)
- Protocolo de Controle de Transmissão (TCP)
- Domain Name System (DNS)
- Hypertext Transfer Protocol (HTTP)
- Secure Sockets Layers/Transport Layer Security (SSL/TLS)

# Conceitos básicos e terminologia

- Pacote: Pequena unidade que é transmitida pela internet
- Roteador: Um dispositivo que direciona pacotes de dados entre diferentes redes.
- Endereço IP: Identificador exclusivo atribuído a cada dispositivo em uma rede. 
- Nome de domínio: Nome legível por humanos que é usado para identificar um site (Google.com)
- DNS: Sistema de Nomes de domínio é responsável por traduzir nomes de domínio em endereço IP
- HTTP: Protocolo de transferência de hipertexto é usado para transferir dados entre um cliente (Como um navegador Web) e um servidor (Como um site)
- HTTPS: Versão criptografada do HTTP (Comunicação segura cliente x servidor)
- SSL/TLS: Usados para fornecer comunicação segura pela internet.

## Protocolos

- Conjunto de regras e padrões que definem como as informações são trocadas entre dispositivos e sistemas.
<br>
- IP: É responsável por rotear pacotes de dados para o seu destino correto.
- TCP e UDP: Garantem que os pacotes são transmitidos de forma confiável e eficiente. 
- DNS: Traduz nomes de domínio em endereços IP
- HTTP: Transfere dados entre clientes e servidor

## Endereços IP e Nomes de domínio

- Endereços IP são normalmente representados como uma série de quatro números separados por períodos como "192.168.1.1"
<br>
Ao criar aplicativos com TCP/IP existem alguns conceitos-chave para entender:

- Portas: São usadas para identificar o aplicativo ou serviço em execução em um dispositivo. Cada aplicativo ou serviço recebe um número de porta exclusivo, permitindo que os dados sejam enviados para o destino correto.
- Sockets: Combinação de endereço IP e número de porta, representando um ponto de extremidade específico para a comunicação. São usados para estabelecer conexões entre dispositivos e transferir dados entre aplicativos.
- Conexões: Dois soquetes quando dois dispositivos querem se comunicar uns com os outros. 
- Transferência de dados: Os dados são normalmente transmitidos em segmentos, com cada segmento contendo um número de sequência e outros metadados para garantir uma entrega confiável.

## Comunicação na internet com SSL/TLS

- Certificados: São usados para estabelecer a confiança entre o cliente e o servidor. Eles contêm informações sobre a identidade do servidor são assinados por um terceiro confiável para verificar sua autenticidade. 
- Handshake: O cliente e o servidor trocam informações para negociar o algoritmo de criptografia e outros parâmetros para a conexão segura.

O Protocolo de Transferência de Hipertexto (HTTP) é a base da internet e é usado para carregar páginas web usando links de hipertexto. O HTTP é um protocolo da [camada de aplicação](https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/) desenvolvido para transferir informações entre dispositivos em rede e é executado no topo de outras camadas da pilha de [protocolos](https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/) de rede. Um fluxo típico de HTTP envolve uma máquina cliente que faz uma solicitação a um servidor, o qual por sua vez, envia uma mensagem de resposta.

## O que há em uma solicitação HTTP?

Uma solicitação HTTP é a forma como as plataformas de comunicação da internet, como os navegadores web, pedem as informações de que necessitam para carregar um site.

Cada solicitação HTTP feita pela internet traz consigo uma série de dados codificados que trazem diferentes tipos de informações. Uma solicitação HTTP típica contém:

1. Tipo de versão do HTTP
2. uma URL
3. um método HTTP
4. Cabeçalhos de solicitação HTTP
5. Corpo opcional do HTTP.

Vamos explorar com mais profundidade de que forma essas solicitações funcionam e como o conteúdo de uma solicitação pode ser usado para compartilhar informações.

## O que é um método HTTP?

Um método HTTP, às vezes denominado verbo HTTP, indica a ação que a solicitação HTTP espera do servidor consultado. Por exemplo, dois dos métodos HTTP mais comuns são "GET" e "POST"; uma solicitação "GET espera receber informações de volta (geralmente na forma de um site), enquanto uma solicitação "POST" normalmente indica que o cliente está enviando informações ao servidor web (como informações de formulário, por exemplo, um nome de usuário e senha enviados).

## O que são cabeçalhos de solicitação HTTP?

Os cabeçalhos HTTP contêm informações de texto armazenadas em pares chave-valor e são incluídos em todas as solicitações HTTP (e respostas, falaremos mais sobre isso adiante). Esses cabeçalhos comunicam informações essenciais, como qual navegador o cliente está usando e quais dados estão sendo solicitados.

Exemplo de cabeçalhos de solicitação HTTP da guia de rede do Google Chrome:

![[Pasted image 20231217191144.png]]

## O que há no corpo de uma solicitação HTTP?

Corpo de uma solicitação é a parte que contém o "corpo" de informações que a solicitação está transferindo. O corpo de uma solicitação HTTP contém qualquer informação que está sendo enviada ao servidor web, como um nome de usuário e senha, ou quaisquer outros dados inseridos em um formulário.

## O que há em uma resposta HTTP?

Uma resposta HTTP é o que os clientes web (frequentemente navegadores) recebem de um servidor de internet em resposta a uma solicitação HTTP. Essas respostas comunicam informações valiosas com base no que foi pedido na solicitação HTTP.

Uma resposta HTTP típica contém:

1. um código de status HTTP
2. Cabeçalhos de resposta HTTP
3. corpo de HTTP opcional

## O que é um código de status HTTP?

Os códigos de status HTTP são códigos de três dígitos usados mais frequentemente para indicar se uma solicitação HTTP foi concluída com sucesso. Os códigos de status são divididos nos cinco blocos a seguir:

1. 1xx Informativo
2. 2xx Sucesso
3. 3xx Redirecionamento
4. 4xx Erro no cliente
5. 5xx Erro no servidor

O "xx" se refere a números diferentes entre 00 e 99.

## Os ataques DDoS podem ser lançados via HTTP?

Lembre-se que o HTTP é um protocolo "stateless", o que significa que cada comando é executado independentemente de qualquer outro comando. Na especificação original, o HTTP solicita que cada um crie e feche uma conexão [TCP](https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/) . Em versões mais recentes do protocolo HTTP (HTTP 1.1 e superior), a conexão persistente permite que várias solicitações HTTP passem por uma conexão TCP persistente, melhorando o consumo de recursos. No contexto dos ataques [DoS](https://www.cloudflare.com/learning/ddos/glossary/denial-of-service/) ou [DDoS](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/), solicitações HTTP em grandes quantidades podem ser usadas para montar um ataque em um dispositivo visado, e são consideradas parte dos ataques da camada de aplicação ou ataques de [camada 7](https://www.cloudflare.com/learning/ddos/what-is-layer-7/).

Um nome de domínio é um endereço exclusivo e fácil de lembrar usado para acessar sites, como ‘google.com’ e ‘facebook.com’. Os usuários podem se conectar a sites usando nomes de domínio graças ao Sistema de Nomes de Domínio (DNS).

Qualquer computador conectado na Internet pode ser alcançado através de um endereço IP público, consistido de 32 bits para IPv4 (eles são, normalmente, escritos com quatro grupos de três números entre 0 e 255, separados por pontos (p.e., `173.194.121.32`) ou consistidos de 128 bits para IPv6 (eles são normalmente escritos com oito grupos de 4 números hexadecimais, separados por dois pontos (p.e., `2027:0da8:8b73:0000:0000:8a2e:0370:1337`). Computadores podem manipular esses endereços facilmente, mas as pessoas tem dificuldade em descobrir quem está executando o servidor ou que serviço o site oferece. Endereços de IP são difíceis de lembrar e podem mudar com o tempo. Para resolver todos esses problemas nós usamos endereços legíveis chamados domain names (nomes de domínio).

O TLD fornece as informações mais genéricas. TLDs informa aos usuários o propósito geral do serviço por trás do nome de domínio. Os TLDs mais genéricos (.com, .org, .net) não requer web services para atender a critérios rigorosos, mas alguns TLDs impõem políticas mais rigorosas. Por exemplo, TLDs locais tais como .us, .fr, or .sh podem exigir que o serviço seja fornecido em um determinado idioma ou hospedado em um determinado país.

[Label (ou componente)](https://developer.mozilla.org/pt-BR/docs/Learn/Common_questions/Web_mechanics/What_is_a_domain_name#label_ou_componente)

Os labels são os que seguem o TLD. Um label pode ser qualquer coisa, de uma letra a uma frase completa. O label localizado a direita antes do TLD pode também ser referido como um _Domínio de Nível Secundário_ (SLD). Um _nome de domínio_ pode ter muitos labels, não é obrigatório nem necessário ter 3 labels para formar um nome de domínio. Por exemplo, [www.inf.ed.ac.uk](http://www.inf.ed.ac.uk/) é um nome de domínio correto. Ao controlar a parte "superior" de um nome de domínio (p.e. [mozilla.org](https://mozilla.org/)), pode-se criar outros nomes de domínios (às vezes chamados de "subdomínios") (p.e. [developer.mozilla.org](https://developer.mozilla.org/)).

### [Comprando um nome de domínio](https://developer.mozilla.org/pt-BR/docs/Learn/Common_questions/Web_mechanics/What_is_a_domain_name#comprando_um_nome_de_dom%C3%ADnio)

#### Quem possui um nome de domínio?

Você não pode "comprar um nome de domínio". Você paga pelo direito de usar um nome de domínio por um ano ou mais. Você pode renovar seu direito, e sua renovação tem prioridade sobre as aplicações de outras pessoas. Mas você nunca possui o nome de domínio.

As empresas chamadas registradoras usam registros de nome de domínio para acompanhar as informações técnicas e administrativas que conectam você a seu nome de domínio.

#### Encontrando um nome de domínio disponível

Para descobrir se um determinado domain name está disponível,

- Ir até um site registrador de nome de domínio. A maioria deles fornece um serviço "whois" que diz se seu nome de domínio está disponível.
- Alternativamente, se você usa um sistema com shell embutido nele, digite um comnaod `whois` nele, como mostrado aqui para `mozilla.org`:

$ whois mozilla.org
Domain Name:MOZILLA.ORG
Domain ID: D1409563-LROR
Creation Date: 1998-01-24T05:00:00Z
Updated Date: 2013-12-08T01:16:57Z
Registry Expiry Date: 2015-01-23T05:00:00Z
Sponsoring Registrar:MarkMonitor Inc. (R37-LROR)
Sponsoring Registrar IANA ID: 292
WHOIS Server:
Referral URL:
Domain Status: clientDeleteProhibited
Domain Status: clientTransferProhibited
Domain Status: clientUpdateProhibited
Registrant ID:mmr-33684
Registrant Name:DNS Admin
Registrant Organization:Mozilla Foundation
Registrant Street: 650 Castro St Ste 300
Registrant City:Mountain View
Registrant State/Province:CA
Registrant Postal Code:94041
Registrant Country:US
Registrant Phone:+1.6509030800

Como você pode ver, eu não posso registrar `mozilla.org` porque a Mozilla Foundation já registrou.

Por outro lado, vamos ver se eu poderia registrar `afunkydomainname.org`:

$ whois afunkydomainname.org
NOT FOUND

Como você pode ver, o domínio não existe no banco de dados `whois` (neste momento em que escrevo), então poderíamos pedir para registrá-lo.

#### Obtendo um nome de domínio

O processo é bastante simples:

1. Ir para o site de um registrador.
2. Geralmente há um apelo chamativo "Obeter um domain name" call to action. Clique nele.
3. Preencher o formulário com todos os detalhes requeridos. Certifique-se especialmente de que você não digitou incorretamente o domain name desejado. Uma vez pago, é tarde demais!
4. O registrador informará quando o domain name estiver registrado corretamente. Dentro de algumas horas, todos os servidores de DNS receberão suas informações de DNS.

### [Como funciona uma solicitação de DNS?](https://developer.mozilla.org/pt-BR/docs/Learn/Common_questions/Web_mechanics/What_is_a_domain_name#como_funciona_uma_solicita%C3%A7%C3%A3o_de_dns)

Como já vimos, quando você deseja exibir uma página da Web em seu navegador, é mais fácil digitar um nome de domínio do que um endereço IP. Vamos dar uma olhada no processo:

1. Digite mozilla.org na barra de localização do seu navegador.
2. Seu navegador pergunta ao seu computador se ele já reconhece o endereço IP identificado por esse nome de domínio (usando um cache DNS local). Em caso afirmativo, o nome é traduzido para o endereço IP e o navegador negocia o conteúdo com o servidor da Web. Fim da história.
3. Se o seu computador não sabe qual IP está por trás do nome mozilla.org, ele vai perguntar a um servidor DNS, cujo trabalho é precisamente informar ao seu computador qual endereço IP corresponde a cada nome de domínio registrado.
4. Agora que o computador conhece o endereço IP solicitado, seu navegador pode negociar o conteúdo com o servidor da web.

# Hosting

## O que é e como funciona um Servidor de Hospedagem de Sites?

### Quais são os tipos de Hospedagem de Site?

- **[Hospedagem compartilhada](https://www.locaweb.com.br/hospedagem-de-sites-com-dominio-gratis/)::** 
    
    é a mais comum e mais utilizada entre os tipos de Hospedagem. Por ser um tipo de Hospedagem barata e que oferece diversas funcionalidades que atendem empresas de pequeno e médio portes, oferece um excelente custo-benefício. Consiste em um servidor compartilhado entre vários sites diferentes.
    
- Em muitos casos, a Hospedagem compartilhada oferece sites, bancos de dados, transferência e espaço em disco ilimitados, com certificado SSL incluso, criador de sites e suporte 24/7. Este caso apresenta o melhor custo-benefício pois apesar do valor ser um pouco maior, é uma Hospedagem completa com recursos e inclusos que fazem a diferença no dia a dia.
    
- **[Servidor Virtual Privado (VPS)](https://www.locaweb.com.br/hospedagem-dedicada/):** 
    
    Neste tipo de hospedagem, por meio virtualização, um servidor físico robusto é dividido em vários servidores virtuais isolados uns dos outros virtualmente. Apesar de compartilhem recursos físicos, processamento, tráfego, espaço em disco e memória RAM são totalmente dedicados a cada servidor virtual privado.
    
- **[Hospedagem Cloud](https://www.locaweb.com.br/cloud/):** 
    
    oferece recursos dedicados e exclusivos, com o mesmo painel da Hospedagem de Sites.
    
- **[Servidor dedicado](https://www.locaweb.com.br/servidores-dedicados/):** 
    
    é mais cara, privada e indicada para grandes empresas que necessitam de alto desempenho, disponibilidade e customização.

### Como funciona um Servidor para Hospedagem de Sites?

A Hospedagem de Sites compartilhada funciona dentro de um servidor de Hospedagem de Sites compartilhado, que é dividido entre diversos sites que utilizam este mesmo espaço. Um servidor é um computador físico que nunca é desligado com a finalidade de garantir que o site esteja sempre online.

O provedor de Hospedagem de Sites é responsável, portanto, por manter o site no ar funcionando normalmente, além de proteger de ataques maliciosos e transferir de forma eficaz e rápida o seu conteúdo de textos, imagens e arquivos até o navegador do visitante.

Um provedor de Hospedagem de Sites eficaz oferece outros serviços relacionados, como:

- Certificado SSL;
- E-mail incluso;
- Construtores de páginas (no caso da Locaweb o Criador de Sites);
- Suporte 24x7;
- Backup e restore;
- Instaladores automáticos (Wordpress, Joomla, Drupal);
- Entre outros.

De acordo com o [ranking do Tudo sobre Hospedagem de Sites](https://tudosobrehospedagemdesites.com.br/locaweb/), a Locaweb é uma das maiores provedoras brasileiras de Hospedagem de Sites e possui data center próprio no país. Os planos garantem espaço, tráfego e sites ilimitados, e contas de e-mail dedicadas. O ambiente é multiplataforma e permite optar por Linux ou Windows para cada site ativado.

# O que é DNS? | Como o DNS funciona

DNS é o que permite aos usuários se conectarem a sites usando nomes de domínio em vez de endereços de IP. Saiba como o DNS funciona.
## O que é DNS?

O Domain Name System (DNS) é a lista telefônica da internet. Os seres humanos acessam informações on-line por meio de [nomes de domínio](https://www.cloudflare.com/learning/dns/glossary/what-is-a-domain-name/), como nytimes.com ou espn.com. Os navegadores da web interagem por meio de endereços de [Protocolo de internet (IP)](https://www.cloudflare.com/learning/network-layer/internet-protocol/). O DNS converte os nomes de domínio em [endereços de IP](https://www.cloudflare.com/learning/dns/glossary/what-is-my-ip-address/) para que os navegadores possam carregar os recursos da internet.

Cada dispositivo conectado à internet tem um endereço IP único que outras máquinas utilizam para localizar o dispositivo. Os servidores de DNS eliminam a necessidade de que humanos memorizem endereços IP como 192.168.1.1 (no IPv4) ou endereços IP alfanuméricos mais complexos mais recentes, como 2400:cb00:2048:1::c629:d7a2 (no IPv6).

## Como funciona o DNS?

O processo de resolução do DNS envolve a conversão de um hostname (como www.example.com) em um endereço IP fácil de ser entendido por um computador (como 192.168.1.1). Um endereço IP é fornecido para cada dispositivo na internet, e esse endereço é necessário para que o dispositivo de internet apropriado seja encontrado — como um endereço postal é usado para encontrar uma determinada casa. Quando um usuário deseja carregar uma página da internet, precisa haver uma tradução daquilo que o usuário digita no navegador web (example.com) para o endereço de máquina necessário para localizar a página do site example.com.

Para entender o processo por trás da resolução do DNS, é importante aprender sobre os diferentes componentes de hardware pelos quais uma consulta de DNS deve passar. Para o navegador da web, a busca pelo DNS ocorre "nos bastidores" e não exige nenhuma interação do computados do usuário além da solicitação inicial.

## Existem 4 servidores de DNS envolvidos no carregamento de uma página da internet:

- **[Recursor de DNS](https://www.cloudflare.com/learning/dns/dns-server-types/)** — o recursor pode ser imaginado como um bibliotecário solicitado a procurar um livro específico em algum lugar de uma biblioteca. O recursor de DNS é um servidor projetado para receber consultas de máquinas clientes por meio de aplicações como navegadores web. De modo geral, o recursor é responsável por fazer solicitações adicionais para atender à consulta de DNS do cliente.
- **Servidor raiz** — o [servidor raiz](https://www.cloudflare.com/learning/dns/glossary/dns-root-server/) é a primeira etapa da tradução (resolução) de host names legíveis por humanos em endereços IP. Pode ser imaginado como um índice em uma biblioteca que aponta para diferentes estantes de livros — geralmente serve como referência para outros locais mais específicos.
- **[Nameserver TLD](https://www.cloudflare.com/learning/dns/dns-server-types/)** - Pense no servidor de domínio de nível superior ([TLD](https://www.cloudflare.com/learning/dns/top-level-domain/)) como uma estante de livros específica em uma biblioteca. Esse nameserver é o próximo passo na busca de um endereço de IP específico e hospeda a última parte de um hostname (em example.com, o servidor de TLD é "com").
- **[Servidor de DNS autoritativo](https://www.cloudflare.com/learning/dns/dns-server-types/)** — esse servidor de DNS final pode ser imaginado como um dicionário em uma estante de livros, no qual um nome específico pode ser traduzido em sua definição. O nameserver autoritativo é a última parada na consulta de um servidor de DNS. Se tiver acesso ao registro solicitado, o nameserver autoritativo retornará o endereço IP do hostname solicitado de volta ao recursor de DNS (o bibliotecário) que fez a solicitação inicial.

## Qual é a diferença entre um servidor DNS autoritativo e um resolvedor recursivo de DNS?

Ambos os conceitos se referem a servidores (grupos de servidores) que são parte integrante da infraestrutura do DNS, mas cada um desempenha uma função diferente e fica em locais diferentes dentro do pipeline de uma consulta de DNS. Uma forma de se pensar sobre a diferença é que o resolvedor [recursivo](https://www.cloudflare.com/learning/dns/what-is-recursive-dns/) está no início da consulta de DNS e o nameserver autoritativo está no final.

#### Resolvedor recursivo de DNS

O resolvedor recursivo é o computador que responde a uma solicitação recursiva de um cliente e dedica algum tempo a rastrear o [registro de DNS](https://www.cloudflare.com/learning/dns/dns-records/). Isso é feito por meio de uma série de solicitações até chegar ao nameserver autoritativo de DNS do registro solicitado (ou atingir o limite de tempo ou retornar um erro se nenhum registro for encontrado). Felizmente, nem sempre os resolvedores recursivos de DNS precisam fazer diversas solicitações para rastrear os registros necessários para responder a um cliente; o [armazenamento em cache](https://www.cloudflare.com/learning/cdn/what-is-caching/) é um processo de persistência de dados que ajuda a encurtar o caminho das solicitações necessárias fornecendo o registro do recurso solicitado mais no início da pesquisa de DNS.

![image](https://cf-assets.www.cloudflare.com/slt3lc6tev37/3NOmAzkfPG8FTA8zLc7Li8/8efda230b212c0de2d3bbcb408507b1e/dns_record_request_sequence_recursive_resolver.png)

#### Servidor de DNS autoritativo

Em termos simples, um servidor DNS autoritativo é o servidor que realmente mantém e é responsável pelos registros de recursos de DNS. Trata-se do servidor na parte inferior da cadeia de pesquisa de DNS, que responderá com o registro do recurso consultado, em última instância permitindo que o navegador de internet faça a solicitação para alcançar o endereço IP necessário para acessar um site ou outros recursos da internet. Um nameserver autoritativo pode atender a consultas com seus próprios dados, sem precisar consultar outra fonte, já que se trata da fonte final da verdade para determinados registros de DNS.

![image](https://cf-assets.www.cloudflare.com/slt3lc6tev37/6Cxvsc4NOvmU4pPkKbkDmP/a7588a4c8a3c187e9175a40fa1b3d548/dns_record_request_sequence_authoritative_nameserver.png)

Vale mencionar que, nos casos em que a consulta é para um subdomínio, como foo.example.com ou [blog.cloudflare.com](http://blog.cloudflare.com/), um nameserver adicional será adicionado à sequência após o nameserver autoritativo, que é responsável por armazenar o [registro CNAME](https://www.cloudflare.com/learning/dns/dns-records/dns-cname-record/) do subdomínio.

![image](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1O1o3jhs0ztWsD00k8RLIJ/f33c1793a7e21cb92678c1f35ef1b245/dns_record_request_sequence_cname_subdomain.png)

Há uma diferença fundamental entre os diversos serviços de DNS e o fornecido pela Cloudflare. Diferentes resolvedores recursivos de DNS, como o Google DNS, o OpenDNS e provedores como a Comcast, mantêm instalações de data center com resolvedores recursivos de DNS. Esses resolvedores permitem consultas rápidas e fáceis por meio de grupos otimizados de sistemas de computador otimizados para DNS, mas são fundamentalmente diferentes dos nameservers hospedados pela Cloudflare.

A Cloudflare mantém nameservers em nível de infraestrutura que são essenciais para o funcionamento da internet. Um exemplo importante é a [rede de servidores raiz F](https://blog.cloudflare.com/f-root/), por cuja hospedagem a Cloudflare é parcialmente responsável. O raiz F é um dos componentes da infraestrutura de nameservers de DNS no nível raiz, responsável por bilhões de solicitações de internet por dia. Nossa [rede Anycast](https://www.cloudflare.com/learning/cdn/glossary/anycast-network/) nos coloca em uma posição única para lidar com grandes volumes de tráfego de DNS sem interrupção do serviço.

## Quais são as etapas de uma pesquisa de DNS?

Na maioria das situações, o DNS se preocupa com a tradução de um nome de domínio para o endereço IP apropriado. Para aprender como esse processo funciona, é útil seguir o caminho de uma pesquisa de DNS à medida que ela viaja, partindo de um navegador web, ao longo do processo de pesquisa de DNS e de volta à origem. Vamos examinar essas etapas.

Observação: muitas vezes, as informações da pesquisa de DNS são armazenadas em cache localmente dentro do computador de consulta ou remotamente na infraestrutura de DNS. De modo geral, uma pesquisa de DNS tem 8 etapas. Quando as informações de DNS são armazenadas em cache, algumas etapas do processo de pesquisa de DNS são ignoradas, o que o torna mais rápido. O exemplo abaixo descreve todas as 8 etapas, quando não há nada armazenado em cache.

#### As 8 etapas de uma pesquisa de DNS:

1. Um usuário digita "example.com" em um navegador web; a consulta viaja para a internet e é recebida por um resolvedor recursivo de DNS.
2. O resolvedor então consulta um nameserver raiz de DNS(.).
3. O servidor raiz responde ao resolvedor com o endereço de um servidor DNS de Domínio de Nível Superior (TLD) (como .com ou .net) que armazena as informações de seus domínios. Quando buscamos example.com, nossa solicitação é direcionada para o TLD .com.
4. A seguir, o resolvedor faz uma solicitação ao TLD .com.
5. A seguir, o servidor de TLD responde com o endereço IP do nameserver do domínio, example.com.
6. Para finalizar, o resolvedor recursivo envia uma consulta ao nameserver do domínio.
7. O endereço IP de example.com é a seguir retornado ao resolvedor partindo do nameserver.
8. Em seguida, o resolvedor de DNS responde ao navegador web com o endereço IP do domínio solicitado inicialmente.

Assim que as 8 etapas da pesquisa de DNS tiverem retornado o endereço IP para example.com, o navegador consegue fazer a solicitação da página da internet:

10. O navegador faz uma solicitação de [HTTP](https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) para o endereço IP.
11. O servidor nesse IP retorna a página da internet que deverá ser renderizada no navegador (etapa 10).

![image](https://cf-assets.www.cloudflare.com/slt3lc6tev37/1NzaAqpEFGjqTZPAS02oNv/bf7b3f305d9c35bde5c5b93a519ba6d5/what_is_a_dns_server_dns_lookup.png)

## O que é um resolvedor de DNS?

O resolvedor de DNS é a primeira parada da pesquisa de DNS e é responsável por lidar com o cliente que fez a solicitação inicial. O resolvedor inicia a sequência de consultas que, em última instância, leva à tradução de uma URL para o endereço IP necessário.

Observação: uma pesquisa típica de DNS não armazenada em cache envolverá consultas recursivas e iterativas.

É importante estabelecer a diferença entre uma consulta [recursiva de DNS](https://www.cloudflare.com/learning/dns/what-is-recursive-dns/) e um resolvedor recursivo de DNS. A consulta refere-se à solicitação feita a um resolvedor de DNS requerendo a resolução da consulta. Um resolvedor recursivo de DNS é o computador que aceita uma consulta recursiva e processa a resposta fazendo as solicitações necessárias.

![image](https://cf-assets.www.cloudflare.com/slt3lc6tev37/rOXBgctX2gaXNDqP5ktek/7086a97e00525159c6bd9318819c2287/dns_recursive_query.png)

## Quais são os tipos de consultas de DNS?

Em uma pesquisa típica de DNS, ocorrem três tipos de consultas. Por meio do uso de uma combinação dessas consultas, um processo otimizado para a resolução do DNS pode resultar em uma redução da distância percorrida. Em uma situação ideal, os dados do registro armazenado em cache estarão disponíveis, permitindo que um nameserver de DNS retorne uma consulta não recursiva.

#### Três tipos de consultas de DNS:

1. **Consulta recursiva** — em uma consulta recursiva, um cliente de DNS solicita que um servidor de DNS (geralmente um resolvedor recursivo de DNS) responda ao cliente com o registro do recurso solicitado ou uma mensagem de erro se o resolvedor não conseguir encontrar o registro.
2. **Consulta iterativa** — nessa situação, o cliente de DNS permitirá que um servidor de DNS retorne a melhor resposta possível. Se não encontrar uma correspondência para o nome na consulta, o servidor de DNS consultado retornará uma recomendação para um servidor de DNS autoritativo para um nível inferior do namespace do domínio. O cliente de DNS, então, fará uma consulta ao endereço recomendado. Esse processo continua com servidores de DNS adicionais na cadeia de consulta até que ocorra um erro ou o limite de tempo seja atingido.
3. **Consulta não recursiva** — de modo geral, isso ocorre quando um resolvedor de DNS cliente consulta um servidor de DNS em busca de um registro ao qual ele tenha acesso porque é autoritativo para o registro ou o registro existe dentro de seu cache. De modo geral, o servidor de DNS irá armazenar os registros de DNS em cache para evitar um consumo adicional de largura de banda e carregar nos servidores mais acima na cadeia de consulta.

## O que é o armazenamento de DNS em cache? Onde o armazenamento de DNS em cache ocorre?

O objetivo do armazenamento em cache é armazenar dados temporariamente em um local que resulte em um aumento de desempenho e de confiabilidade para as solicitações de dados. O armazenamento de DNS em cache envolve o armazenamento de dados mais perto do cliente que os solicita, para que a consulta de DNS possa ser resolvida mais cedo e consultas adicionais mais à frente na cadeia de pesquisa de DNS possam ser evitadas, reduzindo os tempos de carregamento e o consumo de largura de banda/CPU. Os dados de DNS podem ser armazenados em cache em diversos locais, cada um dos quais irá armazenar registros de DNS por um período de tempo definido, determinado por uma [vida útil (TTL)](https://www.cloudflare.com/learning/cdn/glossary/time-to-live-ttl/).

#### Armazenamento em cache do DNS do navegador

Os navegadores web modernos são projetados por padrão para armazenar os registros de DNS em cache por um período de tempo definido. O objetivo aqui é óbvio: quanto mais próximo do navegador web o armazenamento do DNS em cache ocorrer, menos etapas de processamento precisarão ser realizadas para verificar o cache e fazer as solicitações corretas para um endereço de IP. Quando uma solicitação de um registro de DNS é feita, o cache do navegador é o primeiro local verificado na busca do registro solicitado.

No Chrome, você pode ver o status do seu cache de DNS acessando chrome://net-internals/#dns.

#### Armazenamento de DNS no cache ao nível do sistema operacional (OS)

O resolvedor de DNS no nível do sistema operacional é a segunda e última parada local antes que uma consulta DNS saia da sua máquina. O processo dentro do seu sistema operacional projetado para lidar com essa consulta geralmente é chamado de "resolvedor de stub" ou cliente de DNS. Quando recebe uma solicitação de uma aplicação, um resolvedor de stub primeiro verifica seu próprio cache para ver se tem o registro. Caso contrário, envia uma consulta de DNS (com um sinalizador recursivo definido) para fora da rede local, para um resolvedor recursivo de DNS dentro do provedor de serviços de internet (ISP).

Como ocorre em todas as etapas anteriores, quando recebe uma consulta de DNS o resolvedor recursivo dentro do ISP também verifica se a tradução do host em endereço IP solicitada já está armazenada dentro de sua camada de persistência local.

O resolvedor recursivo também apresenta uma funcionalidade adicional, dependendo dos tipos de registros que estão em seu cache:

1. Se não tiver os [registros A](https://www.cloudflare.com/learning/dns/dns-records/dns-a-record/), mas tiver os [registros de NS](https://www.cloudflare.com/learning/dns/dns-records/dns-ns-record/) dos nameservers autoritativos, o resolvedor consultará esses nameservers diretamente, ignorando as várias etapas de uma consulta de DNS. Esse atalho evita as pesquisas dos servidores raiz e dos nameservers .com (em nossa pesquisa do example.com) e ajuda a resolução da consulta de DNS a ocorrer mais rapidamente.
2. Se não tiver os registros NS, o resolvedor enviará uma consulta aos servidores de TLD (.com, no nosso caso), ignorando o servidor raiz.
3. Na improvável hipótese de não encontrar nenhum registro apontando para os servidores de TLD, o resolvedor irá consultar os servidores raiz. Esse evento geralmente ocorre após uma limpeza de um cache de DNS.

## Como funciona o DNS em quadrinhos:

https://howdns.works/pt-br/

## Como os navegadores funcionam

1. **Requisição de URL:**
    
    - O processo começa quando você digita uma URL na barra de endereços do navegador.
    - A URL é convertida em um endereço IP usando o DNS (Domain Name System).
2. **Solicitação ao Servidor:**
    
    - O navegador envia uma solicitação ao servidor web associado ao IP obtido.
    - A solicitação é composta por um cabeçalho que contém informações sobre o navegador, o tipo de conteúdo desejado, etc.
3. **Resposta do Servidor:**
    
    - O servidor processa a solicitação e envia de volta uma resposta.
    - A resposta inclui um cabeçalho com informações sobre o status da solicitação e o conteúdo real (página web, imagem, etc.).
4. **Renderização HTML:**
    
    - Se a resposta for uma página HTML, o navegador começa a analisar o código HTML.
    - Ele constrói uma árvore de elementos (DOM - Document Object Model) representando a estrutura da página.
5. **Processamento de Estilo e Layout:**
    
    - O navegador aplica estilos CSS à árvore DOM para determinar a aparência visual da página.
    - Ele realiza cálculos para determinar a posição e o tamanho dos elementos na página (layout).
6. **Renderização na Tela:**
    
    - O navegador converte a árvore DOM e as informações de layout em pixels na tela.
    - Isso é conhecido como renderização e resulta na exibição da página conforme projetada.
7. **Execução de Scripts:**
    
    - Se houver scripts (JavaScript) na página, o navegador os executa.
    - Os scripts podem interagir dinamicamente com a página, modificar o DOM e fazer solicitações adicionais ao servidor.
8. **Gerenciamento de Recursos:**
    
    - O navegador faz o download de recursos adicionais, como imagens, estilos, scripts, conforme necessário.
    - Esses recursos são armazenados em cache para melhorar o desempenho ao visitar páginas semelhantes.
9. **Interatividade do Usuário:**
    
    - O usuário interage com a página, clicando em links, preenchendo formulários, etc.
    - O navegador responde a essas interações, atualizando dinamicamente o DOM e, se necessário, fazendo novas solicitações ao servidor.
10. **Persistência de Dados:**
    
    - O navegador pode armazenar dados localmente, como cookies e cache, para melhorar o desempenho e manter o estado entre as sessões.

Essas são as etapas gerais de como os navegadores funcionam ao carregar e exibir páginas da web. O processo envolve a interação de várias tecnologias, como HTML, CSS, JavaScript, DNS, HTTP, e outros, para fornecer uma experiência de navegação na web.