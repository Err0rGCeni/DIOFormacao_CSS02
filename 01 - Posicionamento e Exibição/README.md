# Posicionamentos e Exibição de Elementos com CSS

## Propriedades de Exibição

A propriedade `display` vai determinar como as caixas dos elementos devem se comportar no momento de serem exibidas na tela.

### display: block

Gera uma "caixa de bloco", gerando quebras de linha antes e depois do elemento quando no fluxo normal.

### display: inline

Gera uma ou mais caixas que não geram quebras de linha antes ou depois de si mesmas.

Propriedades `height` e `width` serão ignoradas.

### display: inline-block

Semelhante ao **inline**, mas aceitando valores de dimensões e espaçamentos.

Utiliza-se `vertical-align` para o alinhamento vertical de blocos inline ou células de tabelas.

### display: none

Desativa a exibição de um elemento para que não tenha efeito no layout (documento renderizado como se o elemento não existisse), diferente do `visibility: hidden;`, que mantém o espaço ocupado pelo elemento.

### display: flex

O Flexbox é uma forma de organizar os elementos em uma página dentro de containers e de forma dinâmica, organizando os elementos em uma dimensão: ou horizontalmente (linhas), ou verticalmente (colunas).

### display: grid

O Grid Layout vai organizar os elementos em duas dimensões: de forma horizontal e vertical, definindo linhas e colunas para que os conteúdos da página sejam posicionados.

## Posicionando os Elementos

A propriedade `position` ajuda a manipular a localização/posição do elemento na página.

### position: static

O elemento é posicionado de acordo com o fluxo normal do documento. As propriedades `top`, `right`, `bottom`, `left` e `z-index` não têm efeito. Este é o valor padrão.

### position: relative

O elemento é posicionado de acordo com o fluxo normal do documento e depois deslocado em relação a si mesmo.

### position: absolute

O elemento é removido do fluxo normal de documentos e nenhum espaço é criado para o elemento no layout da página. Ele é posicionado em relação ao seu ancestral posicionado mais próximo, se houver.

Para que o **absolute** tenha referência no seu elemento pai, utilizar `position: relative` no pai.

### position: fixed

O elemento é removido do fluxo normal e permanece na mesma posição na tela, independente do scroll.

### position: sticky

Similar ao `position: fixed`, mas é usado para posicionar um elemento de forma relativa até que ele atinja uma determinada posição na janela de visualização. Quando o elemento atinge essa posição, ele é fixado no lugar e permanece lá enquanto a página é rolada.

Diferente do `position: fixed`, não é removido do fluxo normal, fazendo com que permaneça ocupando espaço.

### Z-index

Controla como elementos sobrepostos estão organizados no eixo Z, ou seja, quem fica sobreposto a quem.
