# Dominando Grid Layouts no CSS

    display: grid;    
    display: inline-grid;

CSS Grid é um recurso que permite construir layouts baseados em grades bidimensionais, dividindo a página em regiões e definindo onde cada elemento deve ficar.

## Linhas e Colunas

Utiliza-se `grid-template-columns` e `grid-template-rows` para definir as colunas e as linhas do grid.

Além das unidades padrões, pode-se utilizar a unidade _fr_, que representa uma fração do espaço disponível no container do grid.

A função `repeate(<n>, <value>)` permite repetir um valor de forma menos prolixa. Usar **auto-fill** e **auto-fit** para repetir as faixas quantas vezes forem necessárias para preencher o container de grade. O **auto-fill** deixa faixas vazias se houver espaço extra. O **auto-fit** recolhe faixas vazias se houver espaço extra.

**Grid explícito** é quando define-se as colunas e linhas através das propriedades _template_. Se os itens não couberem, o grid colocará um item fora do mesmo, criando um **grid implícito**. Aos grid implícitos, utiliza-se propriedades _auto_.

A propriedade `grid-auto-flow` controla como o algoritmo de reposicionamento automático irá se comportar.

- **row**: Coloca os itens preenchendo cada linha de uma vez, adicionando novas linhas se necessário.
- **column**: Colocas os itens preenchendo colunas.
- **dense**: Tenta posicionar no grid o máximo de elementos, podendo desorganizar os elementos.

A função `minmax(n, m)` permite especificar um intervalo de tamanho ao item.

## Posicionamento

Cada linha possui um número para que possamos usar de referência (exceto grids implícitos). NÃO começa em 0.

Utiliza-se `grid-column-start`, `grid-column-end` (`grid-column`), `grid-row-start`, `grid-row-end` (`grid-row`) para definir o posicionamento e ocupação de itens em específico. Ao se utilizar **span**, o valor que o acompanha será considerado o tanto de linhas/colunas a se ocupar, e não o valor posicional final.

    grid-area: <grid-row-start>/<grid-column-start>/<grid-row-end>/<grid-column-end>;

É possível nomear as áreas do grid (`grid-template-areas`) e posicionar os itens dentro das mesmas, referenciando pelo nome.

    .container {
        grid-template-columns: repeat(4,1fr);
        grid-template-rows: repeat(3,50px);
        grid-template-areas:
        "header header header header"
        "main main . sidebar"
        "footer footer footer footer"
        ;
    }

    ...
    
    header {
        grid-area: header;
    }

O `grid-template` é o shorthand para rows, columns e areas.

    grid-template:
    "header header header header" 200px
    "main main . sidebar" 200px
    "footer footer footer footer" 200px
    / 1fr 3fr 1fr 1fr;
    ;

## Espaçamento

    gap: <row-gap> <column-gap>;

## Shorthand Grid

    grid: <grid-template> / <grid-auto-flow> <grid-auto-columns>?;
    grid: <grid-template-rows> / <grid-template-columns>;
    grid: auto-flow / <grid-template-columns>;
    grid: auto-flow dense auto-rows / <grid-template-columns>;

## Alinhamento

Para alinhamento horizontal, utilizar `justify-items`; e verticalmente utiliza-se `align-items`. Ou utilizar a shorthand `place-items`.

A propriedade `justify-content` e `align-content` são utilizadas para o alinhamento da área do grid dentro do container. E analogamente, há a shorthand `place-content`.

Para um item específico, utilizar `*-self`.

## Bonus

- Grid Garden;
