# Tinder

Tinder é um aplicativo de relacionamentos multiplataforma. Inicialmente disponível em versão mobile e para pessoas cadastradas no Facebook, a aplicação ganhou um grande número de usuários e se tornou um dos principais aplicativos do mundo. De acordo com o próprio site do Tinder, a aplicação recebe 1,6 bilhões de swipes por dia, os usuários têm mais de 1 milhão de dates, e a aplicação tem um total de mais de 20 bilhões de matches, se estendendo por mais de 190 países.

O Tinder cruza as informações dos perfis dos usuários com um sistema de geolocalização para sugerir os melhores candidatos, levando em conta a proximidade e os interesses em comum. Para a coleta desses dados, o aplicativo se integra com Facebook, Spotify e Instagram.

Todas essas funcionalidades transformaram o Tinder em uma opção interessante para ser aplicada na matéria de Requisitos de Software. Suas funções, como match, feed de notícias e perfil, indicaram requisitos diferentes das demais aplicações. Isso gerou interesse na equipe e garantiu que o Tinder fosse escolhido.

O Tinder cruza as informações dos perfis dos usuários com um sistema de geolocalização para sugerir os melhores candidatos, levando em conta a proximidade e os interesses em comum. Para a coleta desses dados, o aplicativo se integra com Facebook, Spotify e Instagram, permitindo que o algoritmo de recomendação analise diversos fatores como localização, idade, preferências de gênero, interesses e comportamento no aplicativo.

Banco de Dados Fragmentado e Transferência de Dados

O banco de dados do Tinder é fragmentado e distribuído globalmente para garantir eficiência e rapidez nas respostas. Utilizando a infraestrutura da AWS, os dados são armazenados em diferentes servidores baseados em diversas regiões geográficas. Essa fragmentação, conhecida como sharding, permite que os dados sejam acessados de forma distribuída, reduzindo a carga em servidores individuais e melhorando a velocidade de acesso.

Para transferir dados de maneira eficiente, o Tinder utiliza interfaces HTTP e WebSocket, que enviam e recebem dados estruturados no formato XML ou JSON. HTTP é usado para operações que não exigem atualizações em tempo real, enquanto WebSockets são utilizados para comunicação bidirecional em tempo real, como no envio e recebimento de mensagens de chat.



O número de usuários ativos mensais do Tinder é de cerca de 75 milhões de pessoas. Se os usuários do Tinder fossem uma nação, ela seria a 19ª mais populosa do mundo!

## Banco de Dados de Fragmentos

O banco de dados do mecanismo de recomendação do Tinder não é armazenado centralmente, mas compartilhado globalmente em diferentes servidores AWS para respostas mais rápidas e armazenamento contínuo.

## Transferência de Dados

Uma interface HTTP ou soquete da web transfere dados para o aplicativo, utilizando XML/JSON para criar um formato de dados estruturados.

### Geosharding

Geosharding é uma técnica de fragmentação geográfica usada para dividir os dados de usuários com base em suas localizações geográficas. Isso otimiza o desempenho e a velocidade das buscas, pois cada servidor é responsável por uma área específica. Quando um usuário faz uma consulta, o sistema identifica a célula correspondente à localização do usuário e direciona a consulta para o servidor responsável, reduzindo a latência e melhorando a eficiência do sistema.

### Busca e Armazenamento

O Tinder utiliza Elasticsearch para armazenar e buscar perfis de maneira rápida e eficiente, suportando pesquisas de texto completas. O MongoDB é usado para armazenamento persistente de dados de perfil, permitindo uma fácil escalabilidade e flexibilidade no armazenamento de documentos JSON. O Redis é utilizado para cache e operações rápidas na memória, ajudando a reduzir a carga no banco de dados principal e melhorando a velocidade de resposta do aplicativo.

### Moderação de Conteúdo

Para manter a qualidade e a segurança do ambiente do aplicativo, o Tinder usa sistemas de monitoramento de eventos como Kafka e Spark. Esses sistemas coletam e analisam eventos gerados pelos usuários, detectando comportamentos inadequados ou conteúdo impróprio. Algoritmos de aprendizado de máquina são aplicados para identificar e moderar automaticamente esses conteúdos.

### Monitoramento e Performance

Ferramentas como Prometheus são utilizadas para monitorar a performance do sistema, coletando dados de séries temporais e gravação de consultas em tempo real. Kafka processa logs de atividade e eventos do sistema, facilitando a identificação e resolução de problemas em tempo real e fornecendo dados históricos para análise contínua.

## Conclusão

O Tinder se destacou no mercado de aplicativos de relacionamento ao implementar uma arquitetura robusta e escalável, capaz de suportar milhões de usuários ativos diários. Com a fragmentação de dados geograficamente distribuída, tecnologias avançadas para busca e recomendação, e um sistema de monitoramento eficiente, o Tinder garante uma experiência de usuário rápida, segura e agradável."



# Referências:
https://requisitos-tinder.github.io/Tinder-2018-1/

https://pt.quora.com/Qual-linguagem-de-programação-o-Tinder-está-usando

https://roast.dating/pt/blog/estatisticas-tinder#

https://tecnoblog.net/responde/como-funciona-o-powering-tinder-o-algoritmo-por-tras-dos-matches/

https://www.techaheadcorp.com/blog/understanding-system-design-architecture-of-tinder/

https://medium.com/system-design-concepts/dating-application-system-design-aae411412267

https://www.tecmundo.com.br/redes-sociais/94783-descubra-melhor-horario-usar-o-tinder.htm#:~:text=O%20maior%20pico%20de%20acessos,com%20menor%20tempo%20de%20uso.

https://www.help.tinder.com/hc/pt-br/articles/115004647686-Vis%C3%A3o-geral-do-Tinder#:~:text=No%20momento%2C%20o%20Tinder%20%C3%A9,Safari%2C%20Edge%20etc.
