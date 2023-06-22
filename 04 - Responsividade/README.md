# Responsividade no CSS

> Design responsivo é uma técnica de estruturação do layout para que o site se adapte de acordo com a resolução em que ele está sendo visualizado. O objetivo é manter a coesão e uma boa experiência ao usuário independente do dispositivo.

Técnicas para responsividade por Ethan Marcotte:

- Ideia de grids fluídos;
- Técnica de imagens fluídas;
- Media Queries;

## Layouts Flexíveis

Uma das maneiras de se construit layouts flexíveis é usando o Grid Layout; Flexbox e Múltiplas Colunas, combinando com unidades de medidas relativas, incluindo as relacionadas à _viewport_.

### Multicolunas

Especifica-se em quantas colunas o conteúda será dividido e o navegador irá calcular o tamanho.

### Flexbox

Através do _flexbox_, os elementos da página serão capazes de encolher ou crescer, distribuindo o espaço entre os itens de acordo com o tamanho do _container_.

### Grids flexíveis

Utilização de Grid Layout com unidades _fr_, atribuindo o espaço disponível do container entre as colunas e linhas do grid.

### Meta Tag Viewport

A meta tag viewport irá informar para os navegadores que eles devem utilizar a largura da janela do dispositivo para exibir a página web, fazendo com que os navegadores as redimensionem melhor, ajudando na responsividade.

    <meta name="viewport" content="width=device-width, initial-scale=1">

- **width=device-width**: Sobrescreve a configuração padrão dos navegadores para a largura da janela.
- **initial-scale**: Define zoom inicial da página.
- **height**: Define altura específica para a viewport
- **minimum-scale**: Define o nível mínimo de zoom.
- **maximum-scale**: Define o nível máximo de zoom.
- **user-scalable**: Impede que o usuário aplique zoom na página caso tenha o valor definido como __no_.

## Media Queries

Recurso que permite aplicar propriedades do CSS somente para algumas regras de tipos de mídia específicos.

    @media screen(min-width: 320px) and (max-width: 768px) {
        ...
    }

Composto de:

- `at-rule`: Regra usada para identificar o tipo de mídia que uma página está sendo visualizada, informando os recursos que esse tipo de mídia suporta e os operadores que podem ser combinados para misturar algumas condições.
- `media type`: Define o tipo de mídia que os estilos CSS devem ser aplicados.
  - **all**: Corresponde a todos os dispositivos;
  - **print**: Corresponde a documentos que são uma pré-visualização de impressão, ou em qualquer mídia que será voltada para imprimir;
  - **screen**: Corresponde a dispositivos com telas integradas;
  - **speech**: Corresponde a dispositivos que leem o conteúdo de uma forma audível, como um leitor de tela.
- `media feature`:
  - **min-width/min-height/max-width/max-height/width/height**: Detecta a lrgura e altura da viewport;
  - **orientation**: Detecta se o dispositivo está em modo retrato ou paisagem;
  - **hover**: Indica que a página está sendo acessada através de um mecanismo de ponteiro, como um mouse;
  - **pointer**: Detecta quão preciso é o ponteiro;
    - **fine**: Algo como um mouse ou trackpad;
    - **coarse**: Dispositivos touchscreen;
    - **none**: Não possui "apontamento", provavelmente utilização de teclado e/ou sistema de comando de voz;
- `operator`: Permite combinar as media features com **AND**, **OR** e/ou **NOT**;

### Utilizações

- \<link rel="stylesheet" href="style.css" media="...">
- \<style media="..."> ... </style>
- ou JS

### Breakpoints

Os _breakpoints_ são os pontos de interrupção que colocamos nas media queries para tratar a quebra de layout ou ajustar algum conteúdo para determinado dispositivo para deixar as páginas responsivas.

- 576px: para dispositivos extra pequenos (telefones em retrato);
- 768px: para dispositivos pequenos (telefones em paisagem e tablets);
- 992px: para dispositivos médios (desktops pequenos);
- 1200px: para dispositivos grandes (desktops médios e grandes).

## Imagens Responsivas

Para imagens responsivas, pode-se definir uma largura máxima com CSS e/ou renderizar diferentes imagens para tamanhos de tela distintos.

    <picture>
      <source srcset="..." media=(...)>
      <source srcset="..." media=(...)>
      <source srcset="...">
      ...
    </picture>
  
## Tipografia Responsiva

Para textos responsivos, utiliza-se unidades de medidas relativas e media queries.

## Mobile First

> Desenvolver uma página a partir da menor viewport e ir realizando a adaptação do layout de acordo com que o tamanho da janela de visualização aumenta.
