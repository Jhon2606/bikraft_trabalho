# Bikraft
---
*03 de setembro de 2024*

## Estrutura da Página Inicial

A página inicial do site da **Bikraft** foi projetada com uma organização clara e funcional, dividida nas seguintes seções:

### 1. Head
- Contém o **título da página** e uma **breve descrição**.
- Links para a folha de estilos **CSS** e fontes externas para estilizar o conteúdo.

### 2. Header
- Apresenta o **logotipo da empresa**.
- Inclui um **menu de navegação** com links para as demais páginas do site.

### 3. Main
- Apresenta uma **introdução** com um título impactante e uma breve descrição dos produtos disponíveis.
- Inclui um botão de chamada para ação **"Escolha a sua"**, que redireciona para a página de bicicletas.
- Exibe uma **imagem de uma bicicleta elétrica**.

### 4. Lista de Bicicletas (Article)
- Exibe uma relação de produtos com **imagens, nomes e valores**.
- Cada item é clicável, levando a uma página com **mais detalhes** do produto.

### 5. Tecnologia (Article)
- Destaque para as **vantagens tecnológicas** das bicicletas.
- Contém **textos explicativos** e **imagens ilustrativas**.

### 6. Parceiros (Section)
- Apresenta uma **lista de logos** de empresas parceiras.

### 7. Depoimento (Section)
- Exibe o **testemunho** de uma cliente satisfeita com os produtos.

### 8. Seguros (Article)
- Apresenta os planos de seguros **"Prata"** e **"Ouro"**, com seus respectivos **preços e benefícios**.
- Inclui um botão para **solicitar inscrição**.

### 9. Footer
- Contém **dados de contato**, links para **redes sociais**, um menu extra de navegação e o aviso de **direitos autorais**.

---
*06 de setembro de 2024*
## Adição de Estilos Responsivos e Interativos

Nesta atualização, foram adicionados estilos responsivos e interativos para a exibição da lista de bicicletas, visando melhorar a usabilidade e a experiência do usuário em diferentes dispositivos.

### 1. `.bicicletas-lista`
- Define o espaçamento superior e inferior da seção que exibe a lista de bicicletas:
  - `padding-top: 60px`
  - `padding-bottom: 120px`
  
### 2. `.bicicletas-lista h2`
- Ajusta o espaçamento inferior do título (h2) da seção de bicicletas:
  - `margin-bottom: 40px`

### 3. `.bicicletas-lista ul`
- Estabelece a estrutura de layout em grade para os itens da lista com:
  - `display: flex`
  - `gap: 40px`
- Limita a largura máxima da lista em `max-width: 1400px`.
- Centraliza a lista horizontalmente com:
  - `margin-left: auto`
  - `margin-right: auto`
- Permite rolagem horizontal com:
  - `overflow-x: auto`
- Adiciona preenchimento interno:
  - `padding: 0 20px 20px 20px`

### 4. `.bicicletas-lista li`
- Define o comportamento flexível dos itens, garantindo uma largura mínima de:
  - `min-width: 280px`

### 5. `.bicicletas-lista a`
- Garante que o link que envolve cada bicicleta seja um bloco completo:
  - `display: block`

### 6. `.bicicletas-lista img`
- Adiciona espaçamento inferior para separar a imagem da descrição:
  - `margin-bottom: 16px`

### 7. `.bicicletas-lista h3`
- Define o espaçamento entre o título do modelo da bicicleta e o preço:
  - `margin-bottom: 8px`
- Alinha os itens internamente com:
  - `display: flex`
  - `align-items: center`

### 8. `.bicicletas-lista h3::before`
- Adiciona um ícone retangular antes do título da bicicleta com:
  - `height: 8px`
  - `width: 12px`
  - Cor primária: `var(--cor-p1)`
- Configura a transição da largura do ícone:
  - `transition: width 0.2s`

### 9. `.bicicletas-lista a:hover h3::before`
- Ao passar o mouse sobre o link da bicicleta, a largura do ícone aumenta de:
  - `width: 12px` para `24px`, criando um efeito visual interativo.

### 10. `.bicicletas-lista li span`
- Adiciona preenchimento à esquerda do preço da bicicleta:
  - `padding-left: 20px`

---

## Responsividade

### 11. `@media (max-width: 800px)`
Para melhorar a visualização em dispositivos menores:
- Reduz o espaçamento inferior da lista de bicicletas de `120px` para `60px`.
- Diminui o espaçamento entre os itens de `40px` para `20px`.

---
*09 de setembro de 2024*
## Atualização dos Estilos - Seção de Depoimento

### 1. `.depoimento`
- Configura o layout da seção de depoimentos com **grid** em duas colunas de tamanho igual:
  - `grid-template-columns: 1fr 1fr`
- Aplica a cor de fundo principal:
  - `background-color: var(--cor-p1)`
- Impede que conteúdo excedente seja exibido:
  - `overflow: hidden`

### 2. `.depoimento img`
- Ajusta as imagens para ocupar 100% da largura e altura do contêiner:
  - `object-fit: cover`
- Remove as bordas arredondadas:
  - `border-radius: 0px`

### 3. `.depoimento-conteudo`
- Define o espaçamento interno:
  - `padding: 0 40px 80px`
- Alinha o conteúdo ao final da área do grid:
  - `align-self: end`

### 4. `.depoimento-conteudo p`
- Limita a largura do parágrafo a 32 caracteres:
  - `max-width: 32ch`
- Aplica a fonte serifada, itálica e em negrito:
  - `font-family: "Merriweather", serif`
  - `font-style: italic`
  - `font-weight: 900`
- Adiciona espaçamento inferior de 32px e aspas decorativas com `position: relative`.

### 5. `.depoimento p::before, .depoimento p::after`
- Insere aspas estilizadas com:
  - `font-size: 5rem`
  - `color: var(--cor-p2)`
  - `position: absolute`

#### `.depoimento p::before`
- Insere aspas de abertura (“) antes do parágrafo, posicionadas à esquerda e acima:
  - `left: -50px`
  - `top: -20px`

#### `.depoimento p::after`
- Insere aspas de fechamento (”) ao final do parágrafo.

### 6. Responsividade - `@media (max-width: 800px)`
- O layout muda para uma única coluna:
  - `grid-template-columns: 1fr`
- O texto é centralizado:
  - `text-align: center`
- Limita a altura das imagens a 200px.
- O espaçamento interno da `.depoimento-conteudo` é ajustado para:
  - `padding: 0 40px 20px`
  - `margin: auto`

---

## Atualização dos Estilos - Seção de Introdução

### 1. `.introducao-bg`
- Define o fundo da introdução com a cor `var(--cor-12)` e uma sombra interna:
  - `box-shadow: inset 0 -120px var(--cor-0)`

### 2. `.introducao`
- Utiliza **grid** com duas colunas iguais:
  - `grid-template-columns: 1fr 1fr`
- Define um espaçamento entre colunas de 40px.

### 3. `.introducao-conteudo`
- Alinha o conteúdo ao final da coluna:
  - `align-self: end`
- Adiciona um espaçamento inferior de 200px.

### 4. `.introducao img`
- As imagens ocupam 100% da largura e altura do contêiner:
  - `object-fit: cover`
  - `border-radius: 4px`

### 5. `.introducao h1`
- Define a margem inferior do título:
  - `margin-bottom: 32px`

### 6. `.introducao p`
- Define a margem inferior dos parágrafos:
  - `margin-bottom: 20px`

### 7. Responsividade - `@media (max-width: 800px)`
- A cor de fundo muda para `var(--cor-11)` e o padding superior para 40px.
- A sombra interna é reduzida:
  - `box-shadow: inset 0 -60px #ffffff`
- O grid passa a uma coluna, e o espaçamento entre elementos é ajustado para 32px.
- A altura das imagens é limitada a 300px.
- O padding inferior da `.introducao-conteudo` é removido.

---

## Atualização dos Estilos - Seção de Parceiros

### 1. `.parceiros`
- Define o padding superior e inferior da seção para garantir um bom espaçamento.
- Ajusta o padding inferior em telas menores (máx. 800px).

### 2. `.parceiros ul`
- Aplica um layout de **grid** com 4 colunas para telas maiores e 2 colunas para telas menores.
- Estiliza bordas verticais e horizontais nos itens da lista.

### 3. Responsividade - `@media (max-width: 800px)`
- Ajustes no layout, margens e espaçamento para telas menores.

---

## Atualização dos Estilos - Seção de Tecnologia

### 1. `.tecnologia-bg`
- Define a cor de fundo e adiciona uma sombra interna para criar profundidade:
  - `box-shadow: inset`

### 2. `.tecnologia`
- Configura o layout com duas colunas e um espaçamento de 40px.

### 3. `.tecnologia-imagem`
- As imagens preenchem completamente o contêiner com:
  - `object-fit: cover`
  - `object-position: left`

### 4. `.tecnologia-conteudo`
- Define espaçamento superior e inferior para equilibrar o layout.

### 5. `.tecnologia-vantagens`
- Layout flexível com ajustes no espaçamento e largura das imagens.

### 6. Responsividade - `@media (max-width: 800px)`
- Remove a sombra interna e altera o layout para uma coluna.
- A imagem da tecnologia é ocultada.

### 7. Responsividade - `@media (max-width: 600px)`
- Modifica a direção dos itens para coluna.

---
*13 de setembro de 2024*
## Termos de Uso

Criamos uma página separada para os **Termos de Uso** da Bikraft. Essa página contém todas as condições e políticas da empresa.

---

## Adição de Estilos Globais

Foram adicionados estilos específicos para diversas **tags** do site, garantindo uma padronização no layout e comportamento dos elementos em todo o projeto.

---

## Adição de Estilo no Cabeçalho

Estilizamos o **header** (cabeçalho) do site, assegurando sua compatibilidade com diferentes tamanhos de tela e dispositivos, aplicando técnicas de **responsividade**.

---

## Adição de Estilo no Rodapé

Da mesma forma, o **footer** (rodapé) foi estilizado para manter a consistência visual, garantindo também a **responsividade** para diferentes dispositivos.

---

## Adição de Estilo na Seção de Seguros

A seção de **Seguros** recebeu uma estilização própria, incluindo ajustes responsivos para se adaptar corretamente em dispositivos móveis e telas menores.

---

## Adição de Estilo para Componentes

Criamos estilos para componentes individuais através de **classes** presentes no index, facilitando a reutilização e personalização de elementos em todo o site. A responsividade também foi implementada.

---

## Adição de Estilos de Cores

Foi criada uma estilização completa para todas as cores utilizadas no site, utilizando **pseudo-seletores** e **classes**. Isso garante que a paleta de cores siga o padrão visual estabelecido.

---

## Adição de Estilos nas Tipografias

Estilizamos todas as **fontes** do site, especificando tamanho, peso e tipo de fonte. Ajustes de responsividade também foram aplicados para manter a legibilidade em diferentes tamanhos de tela.

---
*17 de setembro de 2024*
## Adição de Ícone SVG

Foi adicionado um ícone **SVG** personalizado com dimensões de 136x32 pixels. Este ícone, preenchido com a cor branca (`#fff`), representa uma forma com contornos distintos, criada através de um único elemento `<path>`, com coordenadas e comandos precisos. O ícone aprimora a interface do usuário ao adicionar um toque visual exclusivo.

---

## Adição de Imagem de Bicicleta

Foram incluídas imagens representando **bicicletas**, que serão usadas como base nos anúncios de venda dos produtos. Essas imagens desempenham um papel importante na apresentação visual das ofertas no site.

---
*21 de setembro de 2024*
## Estilos para a Página de Termos e Condições

Foram adicionados estilos específicos para a página de **Termos e Condições**, com foco em espaçamentos, formatação de títulos e parágrafos. Esses estilos ajustam as margens e definem uma largura máxima de linha, melhorando a **legibilidade**.

---

## Organização dos Arquivos de Estilos

As importações dos arquivos **CSS** foram adicionadas ao arquivo `style.css` para organizar melhor os estilos do projeto. As categorias incluem **global**, **utilidades**, **home**, **bicicletas** e **seguros**, o que facilita a manutenção e a organização dos estilos.

---

## Ícone de Carbono

Adicionado um ícone **SVG** representando o carbono, com dimensões de **32x32 pixels** e preenchimento em **gradiente linear** (de amarelo `#FFBF00` para laranja `#F2A50C`). O ícone é composto por múltiplos `<path>`, utilizando o elemento `<linearGradient>` para definir o gradiente. O ícone inclui três camadas sobrepostas, simbolizando as estruturas do carbono.

---

## Ícone de Elétrica

Adicionado ícone de **elétrica** com dimensões de **32x32 pixels**, preenchido com um gradiente de amarelo-dourado `#FFBF00` para laranja `#F2A50C`. Criado com múltiplos `<path>`, representando energia de forma vibrante e dinâmica.

---

## Ícone de E-mail

Ícone representando um envelope, com dimensões de **20x20 pixels** e preenchimento em gradiente de amarelo-dourado `#FFBF00` para laranja `#F2A50C`. Usado para representar comunicação eletrônica, o ícone utiliza um `<path>` único.

---

## Ícone de Entrega

Adicionado um ícone SVG de um **veículo de entrega**, com dimensões de **16x16 pixels** e preenchido em cinza `#9C9C9C`. O ícone é composto por dois `<path>`, um representando o corpo do veículo e outro as rodas.

---

## Ícone de Estoque

Ícone de **estoque** com dimensões de **16x16 pixels** e preenchimento cinza `#9C9C9C`. O caminho principal (`<path>`) descreve um contêiner com múltiplas caixas organizadas.

---

## Ícone de Horário

Adicionado ícone de **relógio analógico** com dimensões de **20x20 pixels** e preenchido com um gradiente de amarelo-dourado `#FFBF00` para laranja `#F2A50C`, representando o conceito de tempo e agendamento.

---

## Ícone de Lista de Verificação

Ícone representando um **checklist**, com dimensões de **13x9 pixels** e preenchido em amarelo-dourado `#FB0`, ideal para sinalizar tarefas concluídas.

---

## Ícone de Localização

Adicionado ícone SVG de **localização** com dimensões de **20x20 pixels** e preenchimento com um gradiente de amarelo-dourado `#FFBF00` para laranja `#F2A50C`, representando mapas ou geolocalização.

---

## Ícone de Rastreador

Ícone de **rastreamento**, com dimensões de **32x32 pixels** e preenchido em gradiente de amarelo-dourado `#FFBF00` para laranja `#F2A50C`, simbolizando monitoramento.

---

## Ícone de Seguro

Ícone de **seguro** com dimensões de **32x32 pixels**, preenchido com gradiente de amarelo-dourado `#FFBF00` para laranja `#F2A50C`, representando proteção e segurança.

---

## Ícone de Seta

Ícone de **seta** com dimensões de **18x10 pixels** e preenchido em preto `#320`, projetado para navegação.

---

## Ícone de Seta para Abrir

Ícone de **seta para abrir**, com dimensões de **14x6 pixels** e preenchido em cinza `#B2B2B2`, usado para indicar ação de expandir conteúdo.

---

## Ícone de Símbolo Sustentável

Ícone representando um **símbolo de sustentabilidade**, com dimensões de **32x32 pixels** e preenchido com um gradiente de amarelo `#FFBF00` para dourado `#F2A50C`.

---

## Ícone de Telefone

Ícone de **telefone**, com dimensões de **20x20 pixels** e preenchido em gradiente de amarelo `#FFBF00` para dourado `#F2A50C`, simbolizando comunicação.

---

## Ícone de Velocidade

Ícone de **velocidade**, com dimensões de **32x32 pixels** e preenchido com gradiente de amarelo `#FFBF00` para dourado `#F2A50C`. Ideal para sinalizar rapidez e eficiência.

---

## Ícones de Logomarcas

Vários ícones de logomarcas foram adicionados, representando parcerias comerciais, como:

- **Caravan** (140x38 px, preenchido com cinza `#9C9C9C`)
- **Ranek** (149x36 px, preenchido com cinza `#9C9C9C`)
- **Dogs** (152x39 px, preenchido com cinza `#9C9C9C`)
- **Flexblog** (165x38 px, preenchido com cinza `#9C9C9C`)
- **Handel** (139x50 px, preenchido com cinza `#9C9C9C`)
- **Lescone** (208x41 px, preenchido com cinza `#9C9C9C`)
- **Wildbeast** (196x34 px, preenchido com cinza `#9C9C9C`)
- **Surfbot** (200x49 px, preenchido com cinza `#9C9C9C`)

---

## Ícones de Redes Sociais

Foram adicionados ícones para diversas redes sociais:

- **Facebook** (32x32 px, preenchido em branco ou com gradiente)
- **Instagram** (32x32 px, preenchido em branco ou com gradiente)
- **YouTube** (32x32 px, preenchido em branco ou com gradiente)

---

## Imagens de Demonstração dos Produtos

Imagens foram adicionadas para mostrar os modelos dos produtos vendidos no site, destacando suas características e detalhes visuais.

---

## Localização das Lojas

Imagens de **localização** foram incluídas para demonstrar onde estão as lojas físicas da empresa, facilitando a visualização para os usuários.

---

## Imagens para Página Inicial

Imagens usadas para ilustrar as mensagens de introdução, depoimentos e serviços como **seguros** e **tecnologia**.

---
*23 de setembro de 2024*
## SVG Canto Inferior Esquerdo

Implementado um gráfico **SVG** com uma matriz de **16 círculos** organizados em uma grade **4x4**, utilizando um canvas de **52x52 pixels**. Cada linha contém um círculo posicionado de forma alternada nos eixos **x** e **y**. A estrutura é otimizada com o uso de um único caminho (`<path>`), garantindo uniformidade visual e melhor desempenho. A disposição dos círculos parte do **canto inferior esquerdo**.

---

## SVG Canto Inferior Direito

Foi incorporado um ícone **SVG** com dimensões de **52x52 pixels**, preenchido com uma cor **cinza translúcida**. O ícone implementa uma matriz de **20 círculos**, organizados em uma grade, partindo do **canto inferior direito** da tela. O design foi otimizado utilizando um único caminho (`<path>`), visando eficiência e consistência visual.

---

## SVG Canto Inferior Direito-P

Adicionado um ícone **SVG** com dimensões de **52x52 pixels** e preenchido com uma cor **amarelo-dourada** (`#E4A30B`). O design segue o padrão de **círculos equidistantes** organizados nos eixos **x** e **y**, com um único caminho (`<path>`) que otimiza a estrutura do SVG e garante uma renderização eficiente. O ícone é ancorado no **canto inferior direito** da tela.

---

## SVG Canto Superior Esquerdo-P

O ícone **SVG** possui dimensões de **52x52 pixels** e é preenchido com uma cor **amarelo-dourada** (`#E4A30B`). O design inclui **20 círculos** organizados em linhas que começam no **canto superior esquerdo** e preenchem a área de forma progressiva. A estrutura foi otimizada com um único caminho (`<path>`), garantindo consistência visual e eficiência no código.

---

## SVG Canto Superior Direito

Ícone **SVG** com dimensões de **52x52 pixels** e preenchido com uma cor **cinza translúcida**. Os círculos estão distribuídos em uma grade que se estende a partir do **canto superior direito** do canvas. O uso de um único caminho (`<path>`) otimiza o código, garantindo uma renderização eficiente e uniforme.

---
*24 de setembro de 2024*
## Comentei o arquivo index.html para mais fácil compreensão do código

Todo o arquivo foi comentado

## Comentei o arquivo de estilo dos termos

Adicionei uma explicação por escrito do que cada parte do código faz

## Nomeei cada tipo de importação referente a estilos do site

Ficou muito mais fácil de identificar a importação de cada arquivo do projeto

---
*24 de setembro de 2024*
## Comentei o arquivo de estilo dos termos

Adicionei uma explicação por escrito do que cada parte do código faz

## Comentei o arquivo index.html para mais fácil compreensão do código

Todo o arquivo foi comentado

## Nomeei cada tipo de importação referente a estilos do site

Ficou muito mais fácil de identificar a importação de cada arquivo do projeto

---
*25 de setembro de 2024*
## Update footer.css

Alterei a cor do footer para a cor 10

## Update footer.css

Voltei para a cor original (cor 12).

## Update global.css

Mudei a cor do texto do body para azul

## Update global.css

Voltei para a cor original (preto).

## Update header.css

Voltei para a cor original (preto), fica mais bonito e menos chamativo.

## Update seguros.css

Alterei a cor do background da seção seguros para cinza (cor-7).

## Update seguros.css

Alterei a cor de fundo do item da seção seguros para um cinza mais escuro(cor-10)

## Update seguros.css

Alterei para a cor original (cor-11).

## Update seguros.css

Alterei a cor de fundo do item da seção seguros para a cor -12

## Update componentes.css

Modifiquei o padding-right para 30px.

## Update componentes.css

Alterei o tamanho do padding-right da classe container para 20px novamente.

## Update cores.css

Adicionei uma nova cor a cartela de cores utilizadas que seria a p6

## Update tipografia.css

Modifiquei o peso (da fonte) da classe .font-1-xs para  700

## Update tipografia.css

Alterei o peso (da fonte) da classe .font-1-xs  para 400 novamente

## código bicicletas-listas comentado

Códigos do arquivo bicicletas-listas.css foi comentado.

## Comentei o arquivo bicicletas-lista.css

Comentei o arquivo para entendimento das funções no código.

## Comentei o arquivo depoimento.css

Comentei o arquivo para entendimento das funções no código.

## Comentei o arquivo introducao.css 

Comentei o arquivo para entendimento das funções no código.

## Comentei o arquivo parceiros.css

Comentei o arquivo para entendimento das funções no código.

## Comentei o arquivo tecnologia.css

Comentei o arquivo para entendimento das funções no código.
