# bikraft
Trabalho de Engenharia de Software

03 de setembro de 2024

A estrutura da página inicial foi montada

Head: Contém o título da página e uma breve descrição, juntamente com links para a folha de estilos CSS e fontes para estilizar o conteúdo.

Header: Inclui o logotipo da empresa e um menu de navegação com links para outras páginas.

Main: Apresenta uma introdução com um título impactante, uma breve descrição dos produtos disponíveis e um botão de chamada para ação "Escolha a sua", que direciona para a página de bicicletas, acompanhado de uma imagem de uma bicicleta elétrica.

Lista de Bicicletas (Article): Mostra uma relação de produtos com imagens, nomes e valores. Cada item é clicável, levando a uma página com mais detalhes.

Tecnologia (Article): Destaca as vantagens tecnológicas das bicicletas, com textos explicativos e imagens ilustrativas.

Parceiros (Section): Apresenta uma lista de logos de empresas parceiras.

Depoimento (Section): Exibe o testemunho de uma cliente satisfeita com os produtos.

Seguros (Article): Apresenta os planos de seguros "Prata" e "Ouro", com seus respectivos preços e benefícios, além de um botão para solicitar a inscrição.

Footer: Inclui dados de contato, conexões com redes sociais, menu extra de navegação e aviso de direitos autorais.

06 de setembro de 2024

Adicionei estilos responsivos e interativos para as bicicletas

.bicicletas-lista:

Define o espaçamento superior e inferior da seção que exibe a lista de bicicletas, garantindo um layout arejado e espaçado com padding-top: 60px e padding-bottom: 120px.

.bicicletas-lista h2:

Ajusta o espaçamento inferior do título (h2) da seção de bicicletas, adicionando margin-bottom: 40px para criar espaço entre o título e a lista.

.bicicletas-lista ul:

Estabelece a estrutura de layout em grade para os itens da lista com display: flex e define um espaçamento entre eles com gap: 40px.

Garante que a lista ocupe o máximo de espaço horizontal dentro de um limite de 1400px (max-width: 1400px).

Centraliza a lista horizontalmente usando margin-left: auto e margin-right: auto.

Permite que a lista seja rolada horizontalmente quando o conteúdo exceder a largura da tela com overflow-x: auto.

Adiciona preenchimento interno com padding: 0 20px 20px 20px.

.bicicletas-lista li:

Define o comportamento dos itens individuais da lista, tornando-os flexíveis e garantindo que cada item ocupe no mínimo 280px de largura (min-width: 280px).

.bicicletas-lista a:

Garante que o link que envolve cada bicicleta seja exibido como um bloco com display: block, permitindo que o clique seja válido em toda a área do item.

.bicicletas-lista img:

Adiciona um espaçamento inferior de 16px para separar a imagem da descrição com margin-bottom: 16px.

.bicicletas-lista h3:

Adiciona um espaçamento inferior de 8px entre o título do modelo da bicicleta e o preço, além de garantir o alinhamento dos itens internos com display: flex e align-items: center.

.bicicletas-lista h3::before:

Adiciona um pequeno ícone retangular antes do título (h3) da bicicleta usando ::before. O ícone tem height: 8px, width: 12px e usa a cor primária definida por var(--cor-p1).

A transição de largura do ícone é configurada com transition: width 0.2s.

.bicicletas-lista a:hover h3::before:

Quando o link que envolve a bicicleta é "hovered" (passa o mouse sobre), a largura do ícone antes do título aumenta de 12px para 24px, criando um efeito visual interessante.

.bicicletas-lista li span:

Adiciona um preenchimento à esquerda do preço da bicicleta, criando um espaçamento de 20px com padding-left: 20px.

Responsividade - @media (max-width: 800px):

Ajustes para dispositivos menores:

Reduz o espaçamento inferior da lista de bicicletas de 120px para 60px (padding-bottom: 60px) para melhorar o layout em telas pequenas.

Reduz o espaçamento entre os itens da lista de 40px para 20px (gap: 20px) para melhor adequação em telas menores.

09 de setembro de 2024

Foram atualizados os estilos para a seção de depoimento

.depoimento

Configura o layout da seção de depoimentos usando o grid com duas colunas de tamanho igual (1fr 1fr). Aplica a cor de fundo principal (var(--cor-p1)). O uso de overflow: hidden impede que qualquer conteúdo que ultrapasse os limites da caixa seja exibido, mantendo o visual mais organizado.

.depoimento img

As imagens dentro da seção são ajustadas para ocupar 100% da largura e altura do elemento pai. A propriedade object-fit: cover garante que as imagens sejam ajustadas proporcionalmente dentro do espaço, sem distorções. Além disso, as bordas arredondadas são removidas com border-radius: 0px, deixando as imagens com bordas retas.

.depoimento-conteudo

O espaçamento interno (padding) é definido com 40px nas laterais e 80px na parte inferior, permitindo mais espaço para o conteúdo textual. A propriedade align-self: end alinha o conteúdo ao final da área definida pelo grid, posicionando o texto mais próximo da parte inferior da seção.

.depoimento-conteudo p

O parágrafo tem sua largura limitada a 32 caracteres (max-width: 32ch), mantendo o texto mais conciso e legível. A fonte utilizada é "Merriweather", com estilo serifado, itálico e peso de 900, para dar destaque ao depoimento. Um espaçamento inferior de 32px é adicionado para separar o parágrafo de outros elementos. A posição relativa é usada para inserir aspas decorativas.

.depoimento p::before, .depoimento p::after

Esses elementos inserem aspas estilizadas antes e depois do parágrafo. As aspas são grandes (font-size: 5rem) e usam a cor secundária definida (var(--cor-p2)). A propriedade position: absolute permite que as aspas sejam posicionadas de maneira independente do fluxo natural do texto.

.depoimento p::before

Adiciona a aspas de abertura (“) antes do início do parágrafo, posicionando-a um pouco à esquerda e acima do texto (left: -50px; top: -20px).

.depoimento p::after

Adiciona a aspas de fechamento (”) no final do parágrafo.

@media (max-width: 800px)

Ajustes para telas com largura de até 800px.
O layout é reorganizado para uma única coluna (grid-template-columns: 1fr),ajudando na visualização em dispositivos menores.

O texto é centralizado (text-align: center). A altura máxima das imagens é limitada a 200px, para não ocupar muito espaço na tela.

O espaçamento interno da classe .depoimento-conteudo é ajustado para 40px nas laterais e 20px na parte inferior, deixando um layout mais compacto e centralizado (margin: auto).
Foi feito a estilização da sessão de introdução.

.introducao-bg

Define o fundo da seção de introdução com a cor var(--cor-12), de acordo com as cores estabelecidas no tema do site. Além disso, cria uma sombra interna (box-shadow: inset 0 -120px var(--cor-0)) que gera um efeito de profundidade no fundo, especialmente na parte inferior da seção.

.introducao

Usa o layout de grid com duas colunas iguais (grid-template-columns: 1fr 1fr), permitindo que o conteúdo e a imagem fiquem lado a lado. O espaçamento entre as colunas é de 40px, garantindo que os elementos não fiquem muito colados.

.introducao-conteudo

Essa classe faz com que o conteúdo textual fique alinhado no final da coluna com align-self: end, criando um visual mais equilibrado, com o texto próximo do rodapé da seção. Também adiciona um espaçamento inferior (padding) de 200px para garantir que o conteúdo tenha um respiro adequado.

.introducao img

As imagens são configuradas para ocupar 100% da largura e altura do contêiner, garantindo que se ajustem perfeitamente ao espaço disponível. O object-fit: cover faz com que a imagem seja cortada proporcionalmente para evitar distorção. Os cantos das imagens são levemente arredondados com border-radius: 4px, suavizando o visual.

.introducao h1

A margem inferior do título é definida em 32px, para que haja uma boa separação entre o título e os elementos seguintes, o que melhora a hierarquia visual.

.introducao p

Os parágrafos também têm uma margem inferior de 20px, criando espaço suficiente entre os blocos de texto, o que facilita a leitura e evita que o conteúdo fique amontoado.

@media (max-width: 800px)

Quando a tela é menor que 800px (como em smartphones), algumas alterações são feitas para garantir que o design continue funcional e agradável:

A cor de fundo muda para var(--cor-11), que é mais adequada para telas pequenas, e também é adicionado um padding-top de 40px para ajustar o espaço no topo da seção.

A sombra no fundo fica menos intensa, com um box-shadow reduzido (inset 0 -60px #ffffff), para ajustar o efeito ao novo layout.

O grid passa a ter apenas uma coluna (grid-template-columns: 1fr), com o conteúdo e a imagem ficando um embaixo do outro, o que é mais adequado para dispositivos móveis.

O espaçamento entre os elementos na grid aumenta para 32px para garantir que o conteúdo não fique muito apertado.

O padding inferior do .introducao-conteudo é removido para ajustar o alinhamento do texto nas telas pequenas.

A margem inferior do título (h1) é diminuída para 16px, fazendo com que o título fique mais compacto.

A altura da imagem é limitada a 300px, evitando que ela ocupe muito espaço em telas menores, enquanto sua largura continua ocupando todo o espaço disponível.

Foi adicionada a estilização para os parceiros
- Define o padding superior e inferior da seção ".parceiros" para garantir um bom espaçamento em diferentes tamanhos de tela.
- Ajusta o padding inferior para dispositivos com largura máxima de 800px, tornando o layout mais compacto em telas menores.
- Configura a lista de parceiros (.parceiros ul) com um layout de grid de 4 colunas para telas maiores e 2 colunas para telas menores, assegurando uma distribuição equilibrada dos itens.
- Aplica estilos de bordas verticais e horizontais nos itens da lista, removendo a borda à esquerda no primeiro e no quinto item e adicionando bordas superiores a partir do quinto item em telas grandes e do terceiro item em telas menores.
- Implementa ajustes de responsividade, modificando margens, espaçamento e layout dos itens para telas menores (máximo de 800px), incluindo a remoção das bordas à esquerda em itens ímpares.

Foi feito a estilização para sessão de tecnologia
- Define a cor de fundo e uma sombra interna para a .tecnologia-bg, criando um efeito visual interessante com as sombras internas.
- Ajusta a seção .tecnologia para ter um layout de grid com duas colunas e um espaçamento de 40px entre os itens.
- Faz com que a imagem dentro de .tecnologia-imagem preencha completamente o contêiner, usando object-fit: cover e object-position: left para um ajuste perfeito.
- Configura padding superior e inferior para a .tecnologia-conteúdo, garantindo que o espaçamento ao redor do conteúdo esteja bem equilibrado.
- Adiciona margens para vários elementos dentro de .tecnologia-conteúdo, como span, h2, p e links, para garantir um espaçamento consistente e visualmente agradável.
- Estiliza a .tecnologia-vantagens com um layout flexível, ajustando o espaçamento entre os itens e a largura das imagens para melhor apresentação.
- Faz ajustes de responsividade para telas menores: remove a sombra interna em telas com largura máxima de 800px, muda o layout de grid para uma coluna e oculta a imagem da tecnologia.
- Adiciona estilos específicos para dispositivos com largura máxima de 600px, modificando a direção dos itens em .tecnologia-vantagens para coluna.

13 de setembro de 2024

Termos de Uso

Este é um arquivo de uma página a parte do site que contém os termos de uso da empresa Bikcraft.
Adição de estilo global

Neste arquivo foi colocado estilos específicos para algumas tags.

Adição de estilo do cabeçalho

Neste arquivo estilizamos o header e fizemos a responsividade.

Adição de estilo do rodapé

Neste arquivo estilizamos o footer e fizemos a responsividade.

Adição de estilo na seção de seguros

Neste arquivo estilizamos a seção seguros e fizemos a responsividade.

Adição de estilo do componente

Neste arquivo foram criados estilos através das classes do index para facilitar o trabalho na hora de estilizar os elementos, como também foi realizado a responsividade.

Adição de estilo das cores

Neste arquivo temos a estilização de todas as cores utilizadas no site através de pseudo seletores e classes.

Adição de estilo nas tipografias

Neste arquivo estilizamos todas as fontes que foram utilizadas no site, definindo então seu tamanho, peso e tipo de fonte, como também realizamos a responsividade.

17 de setembro de 2024

Adiciona ícone SVG

bikcraft: Incluímos um ícone SVG personalizado com dimensões de 136 x 32 pixels. O ícone representa uma forma com contornos distintos e é preenchido com a cor branca (#fff).

Utilizamos um único elemento `<path>` para definir o design do ícone, com coordenadas e comandos específicos para criar a forma desejada, e será utilizado  para aprimorar a interface do usuário.

Adicional imagem de bicicleta

Incluímos imagens representando bicicletas, que serão utilizadas como base para a criação das imagens do anúncio das vendas dos produtos.

21 de setembro de 2024

Foi adicionado e editado estilos na página de Termos e Condições

Estilos específicos para a página de Termos e Condições, incluindo espaçamentos e formatação de títulos e parágrafos. O arquivo ajusta margens e define uma largura máxima de linha para melhorar a legibilidade.

Organizando as que são de estilo

Adicionei as importações dos arquivos CSS no arquivo style.css para organizar os estilos do projeto. Os arquivos são importados em categorias como global, utilidades, home, bicicletas e seguros, facilitando a manutenção e a organização dos estilos.

ícone de carbono


Adicionado ícone de carbono em formato SVG com preenchimento de gradiente linear que varia de amarelo (#FFBF00) para laranja (#F2A50C)  com dimensões de 32x32 pixels. As formas são desenhadas com o uso de múltiplos caminhos (`<path>`) definidos por coordenadas específicas. O gradiente é gerado usando o elemento `<linearGradient>` com os atributos `x1`, `y1`, `x2` e `y2`. O ícone inclui três camadas sobrepostas, com diferentes níveis de detalhes em seus caminhos e tamanhos, representando as diferentes estruturas do carbono. Possui definição do namespace `xmlns` para garantir compatibilidade e interpretação correta do SVG nos navegadores.

ícone de elétrica

O arquivo contém um ícone vetorial com dimensões de 32x32 pixels e preenchido com uma gradiente de cores amarelo-dourado (#FFBF00) e laranja (#F2A50C) representando um conceito de elétrica, aplicado via `<linearGradient>`, para representar a energia fluindo de uma forma vibrante e dinâmica. Criado com múltiplos caminhos (`<path>`), cada um com coordenadas cuidadosamente posicionadas para formar as partes da ilustração.

ícone de e-mail

O arquivo contém um ícone dimensões de 20x20 pixels e preenchido com uma gradiente de cores amarelo-dourado (#FFBF00) e laranja (#F2A50C). Adicionado ao projeto para uso relacionado a e-mails ou comunicação eletrônica. O ícone usa um `<path>` único para delinear o formato de um envelope. A estrutura visual inclui o desenho da borda superior do envelope e o detalhe central, representando a aba aberta e a entrega de mensagens.

ícone de entrega

Adicionado ícone SVG que representa um veículo de entrega, simbolizando transporte e logística. O ícone possui um `<path>` principal que descreve o veículo com linhas simples.O arquivo contém um ícone com dimensões de 16x16 pixels e preenchido com uma cor cinza (#9C9C9C).

O ícone utiliza duas partes principais:

  1. A primeira define o corpo do veículo de entrega com detalhes geométricos simples, como a área da cabine, caixa de carga e chassi.
  2. A segunda desenha as rodas traseiras e dianteiras do veículo, com preenchimento de cor sólida #9C9C9C.

ícone de estoque

ícone possui dimensões compactas (16x16 pixels), adequadas para interfaces minimalistas ou dashboards que gerenciam inventários e sistemas de estoque, e preenchido com uma cor cinza (#9C9C9C).O caminho principal (`<path>`) cria uma visualização de um contêiner de armazenamento com múltiplas caixas organizadas, simbolizando itens armazenados ou logística interna.

ícone de horário

O ícone com dimensões de 20x20 pixels e preenchido com uma gradiente de cores amarelo-dourado (#FFBF00) e laranja (#F2A50C),  que representa o conceito de "horário" com um design de relógio analógico, ideal para sinalizar tempo, agendamento ou cronograma.

ícone de lista de verificação

O ícone com dimensões de 13x9 pixels e preenchido com uma cor amarelo-dourado (#FB0). Representando uma marcação de checklist, para sinalizar tarefas concluídas, listas verificadas ou itens confirmados na interface de usuário.

ícone de localização

O  ícone SVG com dimensões de 20x20 pixels e preenchido com uma gradiente de cores amarelo-dourado (#FFBF00) e laranja (#F2A50C). Representando a localização, mapas ou geolocalização.
ícone de rastreador

O íconel com dimensões de 32x32 pixels e preenchido com uma gradiente de cores amarelo-dourado (#FFBF00) e laranja (#F2A50C). simbolizando localização, monitoramento e rastreamento.
ícone de seguro

O  ícone com dimensões de 32x32 pixels e preenchido com uma gradiente de cores amarelo-dourado (#FFBF00) e laranja (#F2A50C). Representando proteção, segurança, proteção ou confiabilidade.

ícone de seta

O  ícone SVG com dimensões de18x10 pixels e preenchido com uma gradiente de cor preta (#320).  Projetado para facilitar a navegação e indicar ações em interfaces de usuário. O SVG é escalável, garantindo qualidade em diferentes tamanhos e resoluções.

A estrutura de paths permite fácil modificação e personalização, caso necessário.

ícone de seta para abrir

O ícone SVG representando uma seta apontando para a direita, indicando ação de "abrir", projetada para indicar uma ação de "abrir" ou expandir conteúdo. Com dimensões de 14x6 pixels sendo preenchido na cor cinza  (#B2B2B2), é composto por um único path com regras de preenchimento e recorte, otimizando a renderização e a manipulação do ícone.
ícone de símbolo sustentável

O ícone SVG representa um símbolo de sustentabilidade. Com dimensões de 32x32 pixels, o ícone é preenchido com um gradiente que varia do amarelo (#FFBF00) ao dourado (#F2A50C), conferindo uma aparência vibrante. É composto por um único path, o que otimiza a renderização e a manipulação do ícone.

Ícone de telefone

O ícone SVG representa um telefone, simbolizando comunicação e conectividade. Com dimensões de 20x20 pixels, o ícone é preenchido com um gradiente que transita do amarelo (#FFBF00) ao dourado (#F2A50C). Ele é composto por um único path, otimizando sua renderização e manipulação.

Ícone de velocidade

O ícone SVG representa um símbolo de velocidade, ideal para indicar rapidez e eficiência. Com dimensões de 32x32 pixels, o ícone apresenta dois paths preenchidos com gradientes que variam do amarelo (#FFBF00) ao dourado (#F2A50C). O primeiro path simboliza movimento e desempenho, enquanto o segundo path, em forma de seta, reforça a ideia de ação e velocidade. Para aplicações relacionadas a transporte, desempenho de produtos ou qualquer interface que valorize agilidade.

Ícone da logomarca “caravana”

O ícone SVG representa "caravan", parceiro comercial e colaboração. Com dimensões de 140x38 pixels, é preenchido em um tom de cinza (#9C9C9C). A estrutura é composta por um único path que, através de formas e contornos bem definidos, transmite uma sensação de movimento e interconexão, para representar parcerias e redes de negócios.

Ícone da logomarca "ranek"

Ícone SVG representando a logo da marca "ranek". Com dimensões de 149x36 pixels, este ícone é preenchido na cor cinza (#9C9C9C) e consiste em um único path que captura a identidade visual da marca. Este design otimizado é ideal para aplicações que requerem a representação da marca em contextos digitais

Ícone da logomarca "dogs"

Ícone SVG representando a logomarca "dogs". Com dimensões de 152x39 pixels, este ícone é preenchido na cor cinza (#9C9C9C). O design é composto por múltiplos paths que capturam a essência da marca, refletindo um estilo moderno e amigável. Este icone esta representando a empresa colaboradora de forma clara e visualmente atrativa.

Ícone da logomarca "flexblog"

Ícone SVG representando a logomarca "flexblog". Com dimensões de 165x38 pixels, este ícone é preenchido na cor cinza (#9C9C9C). O design incorpora múltiplos paths que transmitem uma sensação moderna e dinâmica, alinhando-se à identidade visual da marca.

Ícone da logomarca "handel"

Ícone SVG representando a logomarca "handel". Com dimensões de 139x50 pixels, o design é preenchido na cor cinza (#9C9C9C) e apresenta uma tipografia estilizada que reflete a identidade da marca.

Ícone da logomarca "lescone"

Ícone SVG da logomarca "lescone" com dimensões de 208x41 pixels. O design utiliza um preenchimento cinza (#9C9C9C).

Ícone da logomarca "wildbeast"

Ícone SVG da logomarca "wildbeast" com dimensões de 196x34 pixels. O design apresenta um preenchimento cinza (#9C9C9C).

Ícone da logomarca "surfbot"

Ícone SVG da logomarca "surfbot" com dimensões de 200x49 pixels. O design utiliza um preenchimento cinza (#9C9C9C).

ícone da rede social Facebook

Ícone da rede social Facebook com dimensões de 32x32 pixels. O design utiliza um preenchimento branco e reflete o estilo característico da marca.

ícone da rede social Facebook com gradiente

Ícone SVG da rede social Facebook com dimensões de 32x32 pixels. O design utiliza um gradiente que vai do amarelo (#FFBF00) ao laranja (#F2A50C).

ícone SVG da rede social Instagram

Ícone SVG da rede social Instagram com dimensões de 32x32 pixels. O design utiliza uma paleta de cores vibrantes e modernas, predominando o branco (#FFFFFF) para o fundo. Este ícone representa a presença da empresa na plataforma Instagram.

ícone da rede social Instagram com gradiente

Ícone SVG da rede social Instagram com dimensões de 32x32 pixels. O design utiliza um gradiente que vai do amarelo (#FFBF00) ao laranja (#F2A50C), representando a presença da empresa nas redes sociais.

ícone da rede social YouTube

Ícone SVG da rede social YouTube com dimensões de 32x32 pixels. O design apresenta um retângulo em branco com um triângulo representando o botão "play", ideal para destacar a presença da empresa no YouTube.

ícone da rede social YouTube com gradiente

Ícone SVG da rede social YouTube com dimensões de 32x32 pixels. O design utiliza um gradiente que vai do amarelo (#FFBF00) ao laranja (#F2A50C). Este ícone representando a presença da empresa no YouTube.

imagens de demonstração dos produtos

Imagens dos modelos dos produtos, utilizadas para mostrar aos usuários os produtos a serem vendidos.

localização das lojas

Imagens utilizadas pra demonstrar a localização e endereço das lojas, para possibilitar que os usuário saibam e vejam onde estão localizadas as lojas da empresa.

imagens para pagina inicial

Imagens utilizadas para ilustrar as mensagens de introdução e depoimento, e serviços como serviços de seguro e tecnologia.

23 de setembro de 2024

SVG canto inferior esquerdo

Implementa um gráfico SVG com uma matriz de 16 círculos distribuídos em uma grade 4x4, o layout utiliza um canvas de 52x52 pixels. Cada linha contém um círculo posicionado de forma alternada entre os eixos x e y. A estrutura é definida com um atributo path para otimizar o código e manter a uniformidade dos elementos visuais A estrutura utiliza um caminho (path) para otimizar o código e garantir consistência visual, a disposição parte do canto inferior esquerdo.
SVG canto inferior direito

Incorporamos um ícone SVG ao nosso repositório. O ícone foi projetado com dimensões de 52x52 pixels e preenchido com uma cor cinza translúcida que implementa uma matriz de 20 círculos organizados em uma grade, partindo da parte inferior direita. A estrutura foi otimizada com o uso de um caminho (path) único, sendo ancorado no canto inferior direito da tela.
SVG canto inferior direito-p

Incorporamos o ícone SVG com dimensões de 52x52 pixels e preenchido com uma cor amarelo-dourada (#E4A30B). O uso de um único caminho (path) otimiza a estrutura do SVG, garantindo uma renderização eficiente e consistente. O padrão dos círculos segue uma disposição equidistante ao longo dos eixos x e y, sendo ancorado no canto inferior direito da tela.
SVG canto superior esquerdo-p

O ícone é um SVG com dimensões de 52x52 pixels e preenchido com uma cor amarelo-dourada (#E4A30B). A composição inclui 20 círculos. O uso de um caminho único (path) otimiza a estrutura do SVG, com os círculos organizados em linhas que começam do canto superior esquerdo e preenchem a área de forma progressiva.

SVG canto superior direito

O ícone é um SVG com dimensões de 52x52 pixels e preenchido com uma cor cinza translúcida. Define uma grade de círculos distribuídos a partir do canto superior direito com os círculos se estendendo verticalmente e horizontalmente ao longo do canvas. O uso de um caminho único (path) otimiza o código para garantir eficiência e consistência na renderização.
