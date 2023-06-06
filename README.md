# HTML5-CSS-Udemy
HTML5 e CSS Aprendendo criar sites do zero na pratica

## <strong>HTML - Tópicos importantes</strong>

- HTML: HyperText Markup Language (Linguagem de marcação de texto)
- Responsável pelos contéudos, imagens, textos, vídeos, etc

### <strong>Tag &lt;a&gt;</strong>
- target="_blank" -> redirecionar em uma nova guia
  - Ao usar isso, é interessante utilizar os atributos noopener e noreferrer para impedir que um link externo assuma o controle da janela do navegador de origem do usuário e para evitar que sites externos saibam que você incluiu links para o material deles em seu site, respectivamente.

### <strong>&lt;div&gt; x &lt;span&gt;</strong>
- &lt;div&gt; -> elemento de nível de bloco
- &lt;span&gt; -> elemento em linha, deve ser usado somente quando nenhum outro elemento semântico for apropriado.

### <strong>Lista Ordenada x Lista</strong>
- &lt;ul&gt; -> lista sem ordem
- &lt;ol&gt; -> lista ordenada

### <strong>Tabelas</strong>
- &lt;tr&gt; -> linhas (row)
- &lt;th&gt; -> cabeçalho
- &lt;td&gt; -> dados 
- &lt;caption&gt; -> titulo/legenda da tabela

### <strong>Formulários</strong>
- &lt;input&gt; 
  - type hidden -> input não visível para o usuário
  - type radio -> marcar caixinhas
- &lt;select&gt;

### <strong>Negrito, itálico e sublinhado</strong>
- &lt;b&gt;: especifica negrito, aplicando estilo à fonte, o que não permite ser modificado no CSS.
- &lt;strong&gt;: tag semântica - especifica que o texto deve ser destacado de alguma forma, geralmente em negrito e itálico, mas permite que o estilo real seja controlado via CSS. Portanto, estes são preferidos em páginas da web modernas.
- &lt;i&gt;: texto em itálico
- &lt;u&gt;: texto sublinhado

### <strong>Sobrescrito e subscrito - Ex: 25<sup>th</sup> and C<sub>8</sub>H<sub>10</sub></strong>
- &lt;sup&gt;: sobrescrito
- &lt;sub&gt;: subscrito

### <strong>Propriedades/atributos de áudio e vídeo</strong>
- poster -> definir uma capa para o vídeo
- controls -> mostrar barra de controles para o usuário
- loop -> ativar video em loop
- muted -> iniciar video mutado
- autoplay -> iniciar video automático ao carregar a página



## <strong>CSS - Tópicos importantes</strong>

- CSS: Cascading Style Sheets (Folhas de estilo)
- Responsável pelo design, tamanhos, posicionamento, cores

### <strong>3 formas de aplicar estilos CSS em uma página</strong>

- Inline CSS - Direto no html/tag (não é uma boa prática).    
  ```
  <h1 style="color: red; font-size: 14px;"&gt;Bem vindo!</h1>
  ```
- CSS Interno - Direto no head do html, dentro da tag style.
  ``` 
  <style>
    h1{
      color: green;
    }
  </style>
    
  ```     
   
- CSS Externo - Criar um arquivo separado .css com seu estilo.

### <strong>Usar classes ou id</strong>
- Classe: quando quiser aplicar estilo em mais de um elemento.
- Id: quando quiser aplicar estilo em apenas um elemento.

### <strong>Margin x Padding</strong>
- Margin: aplicada ao espaçamento externo;
  - Margin: auto -> útil para centralizar
- Padding: aplicado ao espaçamento interno;

### <strong>Box-sizing</strong>
- border-box -> não deixa o conteúdo sair para fora do box -> boa prática.
- content-box -> permite o contéudo extrapolar o box -> má prática.

### <strong>Position</strong>
- Static -> padrão
- Relative -> o elemento é posicionado em relação a sua posição normal. (top, bottom, left, right)
- Absolute -> o elemento é posicionado em relação ao seu elemento pai mais próximo que possui relative, se não tiver relative, é posicionado em relação ao body. 
- Fixed -> o elemento é posicionado em uma posição fixa, independente do tamanho do view port.
- Sticky -> o elemento é posicionado em uma posição fixa em relação ao scrool -> interessante para o header do site.

### <strong>"Reset" do CSS - IMPORTANTE!</strong>
- Sempre ao iniciar um projeto, uma boa prática é realizar o "reset" do css para remover estilos que já vem por padrão em algumas tags html, margin, etc. Exemplo de alguns estilos que geralmente são removidos:
  ```
  *{
    box-sizing: border-box; /* evitar que o contéudo ultrapasse seu box */
    margin: 0;
    padding: 0;
    outline: 0;
  }
  ```
 
### <strong>Flex Box</strong>
- flex-direction -> por padrão é row, onde os elementos filho se organizam em linha, mas pode ser modificado para column ou até row-reverse e column-reverse.
- flex-basis -> define um tamanho fixo para cada elemento filho.
- flex-shrink
- order -> definir a ordem dos elementos filhos
- justify-content -> alinhar horizontalmente -> aplicado ao elemento pai, juntamente do display flex
  - space-between -> aplicar espaçamento igual entre os elementos filhos
  - space-around -> aplicar espaçamento igual entre os elementos filhos, tanto para left quanto right.
- align items -> alinhar verticalmente -> aplicado ao elemento pai, juntamente do display flex
- align self -> alinhar verticalmente o elemento filho 

### <strong>Animação de zoom ao passar o mouse</strong>
1. Aplicar a propriedade transition ao button, definindo o tempo de transição desejável. Ex. -> transition: 0.9s;
2. Aplicar a propriedade transform: scale() ao hover do button, definindo o tamanho que desejar do zoom. Ex. -> transform: scale(1.5);

### <strong>Propriedade z-index</strong>
- Definir uma ordem de prioridade para elementos sobreporem outros. Ex -> z-index: 9;
- Por padrão, todo elemento tem z-index auto.
- Se uma navbar tiver z-index = 9, e um elemento p, um z-index = 8, significa que a navbar irá sobrepor o elemento p. 

### <strong>Responsividade - Media queries</strong
  - Definir um max-width para ser o break point, onde será definido as mudanças de css para telas menores ou maiores.
