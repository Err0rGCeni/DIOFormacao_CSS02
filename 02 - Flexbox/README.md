# Trabalhando com Flexbox no CSS

    display: flex;
    flex: <flex-grow> <flex-shrink> <flex-basis>;

## Conceitos

O _flexbox_ (_Flexible Box Module_) oferece uma maneira mais eficiente de organizar, alinhar e distribuir o espaço entre os itens do _container_, mesmo que o tamanho do elemento seja dinâmico.

Permite posicionar os elementos dentro de outro elemento (container). Os elementos dentro do container são conhecidos como itens.

## Eixos

O eixo principal (main axis) define qual a direção que o container vai organizar os itens. O eixo transversal (cross axis) é perpendicular ao eixo principal.

O eixo principal é definido pelo `flex-direction`.

## Flex-Wrap

Definem se os itens são forçados a ficarem na mesma linha ou se podem ser quebradas em varias linhas.

- **nowrap**: Os itens flexíveis são agrupados em uma unica linha, permitindo que o flex container "transborde".
- **wrap**: Os itens são quebrados em multiplas linhas.
- **wrap-reverse**: Se comporta como o wrap, mas com as linhas contrárias.

>> `flex-flow`: É uma _shorthand_ para valores de `flex-direction` e `flex-wrap`.

### Justify-Content

Propriedade responsável pelo alinhamento dos itens no eixo principal: **start**, **end**, **flex-start**, **flex-end**, **center**, **left**, **right**, **normal**, **space-between**, **space-around**, **space-evenly**, **stretch**, **safe**, **unsafe**.

### Align-Items

Propriedade responsável pelo alinhamento dos itens no eixo transversal: **normal**, **flex-start**, **flex-end**, **center**, **start**, **end**, **self-start**, **self-end**, **baseline**, **first baseline**, **last baseline**, **stretch**, **safe**, **unsafe**.

### Gap

É uma propriedade shorthand para `row-gap` (controlar o espaçamento entre as linhas) e `column-gap` (controlar o espaçamento entre as colunas). Se fosse utilizado `margin`, esse espaçamento seria aplicado para todos os itens, e não entre.

### Order

Aplicado aos itens, é responsável por organizar um ou mais itens no container. Prioridade de ordem do menor para o maior número.

### Flex-Grow

A propriedade fará com que espaços extras no container sejam usados pelos itens, dando capacidade do item crescer ao longo do eixo principal, caso necessário.

Esse crescimento é limitado por `max-width` e `max-height`.

### Flex-Shrink

Controla o quanto um item vai encolher, caso seja necessário.

### Flex-Basis

Define o tamanho base dos itens no container, antes do espaço de sobra ser redistribuído. `flex-grow` e `flex-shrink` são aplicados com base no `flex-basis`.

É limitado por propriedades min/max.

### Align-Self

Permite sobrescrever o alinhamento padrão aplicado pela propriedade `align-items`.
