# devops-impacta

APACHE HTTP SERVER 
*Apache 2.2*


Principais Melhorias
O novo módulo mod_proxy_balancer fornece serviços de carregamento de balenceamento para mod_proxy. O novo módulo mod_proxy_ajp oferece suporte para o Protocolo Apache JServ versão 1.3, usado pelo Apache Tomcat.
Filtragem Inteligente (Smart Filtering)
O mod_filter introduz configuração dinâmica para o filtro de saída de dados. Permitindo que os filtros sejam condicionalmente inseridos, baseando-se nos cabeçalhos Request ou Response ou em variáveis do ambiente, ele acaba com os problemas de dependências e pedidos da arquitetura 2.0.
Melhorias nos Módulos
mod_authnz_ldap
Este módulo é uma migração do mod_auth_ldap, da versão 2.0 para a estrutura 2.2 de Authn/Authz. As novas funcionalidades incluem o uso de atributos LDAP e filtros de procura complexos na diretriz Require.
mod_info
Adicionado um novo argumento ?config que mostra a configuração das diretrizes analisadas pelo Apache, incluindo o nome do arquivo e o número da linha. Esse módulo também mostra a ordem de todos os ganchos de pedidos (request hooks) e informações adicionais sobre a compilação, similar ao comando httpd -V.
top
Mudanças ao Desenvolvedor de Módulos
API do APR 1.0
O Apache 2.2 utiliza a API do APR 1.0. Todas as funções e símbolos antigos foram removidos do APR e APR-Util. Para mais detalhes, visite o Website do APR.
Registros de Erros de Conexão (logs)
Uma nova função ap_log_cerror, foi adicionada para registrar erros que ocorrem na conexão do cliente. Quando documentado no diário de log, a mensagem inclui o endereço IP do cliente.
Adicionado Gancho de Teste de Configuração
Um novo gancho (hook), test_config foi adicionado para auxiliar módulos que querem executar códigos especiais apenas quando o usuário passa o parâmetro -t para o httpd.
Ajustar o Stacksize dos "Threaded MPM's"
Uma nova diretriz chamada ThreadStackSize, foi adicionada para ajustar o tamanho das stacks em todos os threadeds MPMs. Essa é uma prática necessário para alguns módulos de terceiros em plataformas com tamanhos de stacks pequenos por padrão.Negociação de Protocolo para filtros de saída    No passado, todo filtro era responsável por garantir a geração de cabeçalhos de resposta correto que os afetava. Os filtros agora podem delegar o gerenciamento de protocolos comuns para mod_filter, usando chamadas de ap_register_output_filter_protocol ou ap_filter_protocol.
* *
*


Apache 2.4*

MPMs de carga em tempo de execução
Múltiplos MPMs agora podem ser criados como módulos carregáveis em tempo de compilação. O MPM de escolha pode ser configurado em tempo de execução via LoadModulediretiva.
Evento MPM
O Event MPM não é mais experimental, mas agora é totalmente suportado.
Suporte assíncrono
Melhor suporte para leitura / gravação assíncrona para suporte de MPMs e plataformas.
Configuração LogLevel por módulo e por diretório
O LogLevelagora pode ser configurado por módulo e por diretório. Novos níveis trace1 de trace8foram adicionados acima do debugnível de log.
Seções de configuração por solicitação
<If>, <ElseIf>E as <Else> seções podem ser usadas para configurar a configuração com base em critérios por solicitação.
Analisador de expressão de propósito geral
Um novo analisador de expressão permite especificar condições complexas usando uma sintaxe comum em directivas como SetEnvIfExpr, RewriteCond, Header, <If>, e outros.
KeepAliveTimeout em milissegundos
Agora é possível especificar KeepAliveTimeoutem milissegundos.
Diretriz NameVirtualHost
Não é mais necessário e agora está obsoleto.
Substituir a Configuração
A nova AllowOverrideList diretiva permite um controle mais fino que as diretivas são permitidas nos .htaccessarquivos.
Variáveis do arquivo de configuração
Agora é possível as Define variáveis na configuração, permitindo uma representação mais clara se o mesmo valor for usado em muitos lugares na configuração.
Redução de uso de memória
Apesar de muitos novos recursos, 2.4.x tende a usar menos memória do que 2.2.x.
 *****
 
 
 
 
 
 NGINX
 
 Desde a versão 5.2, o sistema operacional OpenBSD utiliza o Nginx como parte do sistema base, provendo uma alternativa ao fork do Apache 1.3 que o sistema utilizava, o qual o Nginx tinha como finalidade substituir[3], mas que acabou sendo subtituido por uma implementação própria de httpd[4].
 





WORDPRESS 4.8.1
 
 Pequena melhoria no TinyMCE, o editor de textos usado no WordPress
O comunicado menciona que o editor visual terá uma experiência aprimorada na nova versão, com a possibilidade de navegar mais intuitivamente dentro e fora de elementos inline como links. É uma descrição um pouco misteriosa e genérica, ainda, embora a aparência de links no editor tenha mudado (apenas) um pouco:
Editor visual no widget de texto
Essa era uma das melhorias mais esperadas! Finalmente você não vai precisar mais brigar com HTML no widget de texto para adicionar formatação. Agora há um editor simplificado (e suficiente) disponível:
Você ainda pode usar o editor simples na aba “Texto”, tal como no editor normal de posts.
 Widget de imagem!
Você já se deparou com isso antes: a simples tarefa de exibir uma imagem na barra lateral exigia que você fizesse upload em “Mídia” e depois escrevesse um código em HTML para inserir a imagem em um widget de post. Não mais! Finalmente surgiu o widget de imagem oficial, que facilita essa tarefa:
O widget usa o uploader de mídia do WordPress e permite inserir a imagem facilmente, inclusive com a pré-visualização dela.
 Widget de vídeo!
Outra novidade! Agora há um widget de vídeo novo em folha que permite inserir vídeos facilmente não apenas via upload, mas também via YouTube ou Vimeo:
Novidade no widget de novidades do WordPress: WordCamps e MeetUps na sua região!
Uma novidade muito interessante pra quem gosta de participar da comunidade: o widget de novidades do WordPress (aquele que você nunca dá atenção, que eu sei!) agora inclui WordCamps e MeetUps filtrados por cidade! Você vai poder configurar sua cidade e saber quais são os próximos eventos:
melhorias no core
Como de costume, há também melhorias que não são tão visíveis ou relevantes para o usuário mas são importantes em termos de funcionamento da plataforma. Algumas delas são:
O painel de customização vai ter um tamanho proporcional em telas maiores
O nome do usuário agora vai ser mostrado de forma mais proeminente na tela de edição do usuário
Nova função get_term_parents_list() vai ser introduzida como uma versão taxonômico-agnóstica de get_category_parents()
 
 
 


WORDPRESS 4.8
 
 Os novos widgets no WordPress 4.8
O WordPress 4.8 trouxe consigo novos widgets para tornar a experiência de gestão de conteúdo ainda mais prática, dinâmica e rica.
São três novos widgets para imagem, vídeo e áudio. Um novo marco para a estrutura de widgets na plataforma, que agora faz uso e interage com a REST API. Uma base sólida para suportar novas adições de componentes no futuro e abrir as portas para integrações mais dinâmicas.
O widget “Texto” ganhou a adição do TinyMCE e, assim, passou a ter um editor para formatação dos textos. As opções de formatações são limitadas: negrito, itálico, lista ordenada ou não ordenada e links.
O widget “Novidades e eventos do WordPress” além das tradicionais “Novidades” agora exibe eventos da comunidade do WordPress próximos a localização do usuário logado no painel.

Acessibilidade melhorada no WordPress 4.8
O WordPress sempre se preocupou com acessibilidade. A cada nova versão, uma melhoria é considerada. Assim torna a experiência de uso mais fácil e respeitosa para com os usuários de leitores de tela e com necessidades especiais.

Cabeçalhos das páginas no painel

Desde a versão 4.3, os cabeçalhos das páginas do painel do WordPress tem sido revistos. O título principal de cada uma, por exemplo “Editar post” passou a utilizar a tag H1, ao contrário de H2.

Em seguida, a versão 4.4, passou a conter somente o texto referente ao título e não mais a marcação dos botões “Adicionar novo”.
Na versão 4.8 a atenção foi voltada para os plugins e temas que adicionam conteúdos extras ao cabeçalho principal da página, que faz uso da tag H1 e, assim, evita o prejuízo da hierarquia e semântica da informação.
Widget de Nuvem de tag
O widget de Nuvem de tag exibe o total de posts atrelados a uma tag através do atributo “title”. Esse atributo não é muito acessível, além disso, dependendo das configurações dos leitores de tela dos usuários, a informação contida nele é totalmente ignorada.
O WordPress 4.8 removeu esse atributo e passou a considerar a informação através do atributo “aria-label”. Opcionalmente é possível exibir o total de posts atrelados a uma tag junto ao texto.
 
