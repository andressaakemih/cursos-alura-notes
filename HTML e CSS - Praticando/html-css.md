# HTML e CSS: Praticando

*Assunto: HTML e CSS
*Criado: March 25, 2022 4:02 PM
*Finalizado: Yes
*Materiais: https://cursos.alura.com.br/course/html-css-praticando-html-css/task/103160
*Plataforma: Alura

### Anotações

100vh (vieweport height) a altura da tela

## Iniciando o projeto

### **Atividade → Variáveis CSS**

I - No vídeo anterior, declaramos variáveis que representam o hexadecimal das cores ao invés de usar esse valor diretamente nos atributos CSS. Qual afirmação abaixo representa melhor a motivação do uso de variáveis CSS?

→ Variáveis CSS facilitam o entendimento do uso das cores, a atribuição e manutenção.

→ Variáveis CSS auxiliam no entendimento do uso das cores por terem nomes que fazem sentido com o seu uso, consequentemente isso também facilita a atribuição nos elementos HTML. Além desses dois benefícios, facilita na manutenção do código: é possível alterar o valor de alguma cor reescrevendo um único lugar do código.

### **Atividade** → **A motivação da imagem**

II - Acabamos de inserir duas imagens de maneira distinta no nosso código. A imagem do Combo+ foi implementada no arquivo index.html dessa maneira:

```html
<img src=”img/Combo” alt=”O combo+ é a junção do alura+ e o alura lingua”>
```

Já a imagem de fundo, que apresenta vários instrutores da Alura, foi implementada no arquivo styles.css desse jeito:

```css
.principal {
background-image: url(“img/Background”);
}
```

Por que a imagem dos instrutores e instrutoras não foi colocada dentro da tag de imagem, a `<img>`?

→ Pois a imagem “Background.png” é decorativa e seu contexto não muda a leitura da página.

→ É  isso aí! Quando estamos inserindo uma imagem, é importante pensar: essa
 imagem faz parte do conteúdo da página? Se não, é possível colocá-la 
como `background-image()`
 de algum elemento.

### Nessa aula, você aprendeu como:

- Criar a pasta do projeto e os arquivos HTML e CSS no seu computador, assim como abrir a pasta no editor de código;
- Escrever o código base do arquivo HTML, através das tags que compõem a estrutura básica desse tipo de arquivo;
- Preencher os dados que são inseridos dentro da tag `<head>` que auxiliam o navegador a entender a codificação de caracteres, o tamanho do dispositivo e a conexão de arquivos externos;
- Estabelecer variáveis CSS e usar as mesmas, que ajudam a compreender melhor as
cores por possuírem agora um nome ao invés do código hexadecimal;
- Instalar a extensão Live Server para conseguir ver as alterações no código automaticamente ao salvar o arquivo;
- Alterar a cor de fundo da página com `background-color` e da escrita com `color`;
- Inserir imagem de fundo com `background-image` e com a tag `<img>` assim como compreender suas diferenças de utilização.

## A dupla HTML e CSS

### Atividade → **Botão ou âncora?**

Não seja levado pelas aparências: os elementos `<a>` e `<button>`  podem ser exatamente iguais aos nossos olhos, pois basta que sejam estilizados apropriadamente. Porém, por trás, não são iguais. 

Eles possuem significados diferentes, e cabe à pessoa desenvolvedora compreender o contexto para escolher qual utilizar.

Analise o botão do layout a seguir e escolha qual elemento é mais apropriado para usar e a sua motivação:

![](HTML e CSS - Praticando/img/Untitled 1.png)

→ O elemento que deverá ser usado é o `<button>` por executar uma função ao ser clicado: apagar os dados do formulário.

→ Quando queremos que um evento aconteça a partir do clique do mouse, utilizamos os botões.

### Atividade: **Dividindo nossa section**

Utilizando do conhecimento adquirido no vídeo anterior, qual código abaixo resulta na divisão da tela representada pela imagem a seguir?

![layout sessão se inscreva](https://github.com/andressaakemih/cursos-alura-notes/blob/main/HTML%20e%20CSS%20-%20Praticando/img/Untitled%201.png)

```css
display: grid;
grid-template-columns: 50% 25% 25%;
```

→ Dessa maneira, a primeira coluna ocupará metade da tela e em seguida serão construídas duas colunas menores, que ocupam a metade do tamanho da primeira cada uma.

### **Para saber mais: classes, unidades e grid!**

Ao continuar o projeto Alura Plus, foi necessário atribuir classes
 para os elementos, possibilitando a estilização de locais específicos. 
Quando você fez isso comigo, eu citei sobre um padrão de nomenclatura: o
 Block Element Modifier (BEM). Você pode ler mais sobre isso no artigo [“Nome de classes no CSS”](https://www.alura.com.br/artigos/nomes-de-classes-no-css), produzido pelo instrutor Yuri Padilha.

Para entender melhor sobre o uso de classes e conhecer outro atributo semelhante chamado id, convido você a ler o meu artigo [“Qual a diferença entre id e class”](https://www.alura.com.br/artigos/qual-diferenca-entre-id-e-class).

Apresentei a unidade de medida relativa “em” na criação do botão da 
página e há muitas além dessa com o mesmo intuito. Para conhecer ou 
compreender melhor o uso do “em”, você pode consultar o artigo [“Guia de unidades no CSS”](https://www.alura.com.br/artigos/guia-de-unidades-no-css) do instrutor Paulo Scalercio. Esse é um ponto de atenção importantíssimo!

Durante o desenvolvimento da primeira seção, também vimos o uso de 
Grid. Assim como os outros conteúdos, temos um artigo para você reforçar
 esse aprendizado e consultar quando for preciso. Apresento a você o [“Criando layouts com CSS Grid Layout”](https://www.alura.com.br/artigos/criando-layouts-com-css-grid-layout), produzido pelo Matheus Castiglioni.

Não deixe de consultar esses materiais sempre que precisar! :)

### **O que aprendemos?**

- Criar botões na página e como escolher qual elemento para isso;
- Como nomear classes com o padrão BEM (block element modifier);
- A diferença entre `<button>` e `<a>`;
- Unidade de medida responsiva em;
- Display inline e block;
- Usar as propriedades CSS grid e grid-template-columns para dividir a tela;
- Conferir através da ferramenta do desenvolvedor no navegador (F12) os grids na tela;
- Detectar diferentes tipos de fontes e tamanhos de letras no Figma;
- Escolher fontes no fonts.google.com;
- Importar fontes externas no arquivo HTML;
- Usar variáveis CSS para armazenar valores além de cores como o nome da fonte;
- Aplicar a fonte importada nos elementos através do CSS e outros atributos relacionados: font-family, font-size, font-weight;
- Remover a decoração do texto de links através do text-decoration.

 

### Posicionando elementos

### Atividade: **Separando elementos**

No vídeo anterior, foi demonstrado o uso de **margins** e as comparações dele com o **padding**. Das afirmações abaixo, quais são corretas?

I. Margins criam um espaçamento ao redor do elemento.

II. Paddings criam um espaçamento dentro do elemento.

III. Paddings afastam um elemento do outro.

IV. É possível configurar valores de margins diferentes para cada lado.

→ Somente I, II e IV.

→ Margins realmente criam espaço ao redor do elemento e paddings criam dentro dele, ou seja, o padding afasta o conteúdo da borda e não um elemento do outro. Por fim, também podemos configurar valores diferentes para cada lado do elemento e, no vídeo, vimos diversas maneiras de fazer isso.

### Atividade: **Centralizando elementos**

No último vídeo, conhecemos as propriedades de alinhamento `text-align` e `align-itens`.

Imagine que você está desenvolvendo outro projeto ao mesmo tempo no nosso time, o Alura Cats, que consiste em um container com um título, uma imagem, um parágrafo e uma âncora:

```html
<div class="container">
	<h2 class="container__titulo">Alura Cats!</h2>
	<img src="https://thecatapi.com/api/images/get?format=src&type=gif" alt=”imagem de gatos” class="container__imagem">
	  <p>Para mais informações:</p>
	<a href="www.alura.com.br" class="container__botao">Acesse a Alura<a>
</div>
```

Visualmente, após algumas estilizações feitas com CSS, o resultado desse código ficará assim:

![Untitled](HTML%20e%20CSS%20Praticando%206758b2cc0a7043b3bade98e5bf18bbe3/Untitled%202.png)

Você pode testar o código do Alura Cats no meu [repositório do codepen](https://codepen.io/mmhillman/pen/JjOwNMB).

Tendo isso pronto, qual propriedade CSS a seguir você usaria para alinhar ao centro todos os itens deste container e por quê?

→ `text-align`, porque ele consegue alinhar todos elementos inline dentro do bloco.

→ O código começa com um elemento de bloco (a div), ou seja, que tem display block, e há elementos dentro dele que são inline. Dessa maneira, usar a propriedade text-align na div permitirá alinhar para qualquer lado que você desejar os elementos filhos da div.

### **Para saber mais: Inline-block**

Nessa aula, você conheceu uma nova forma de display: o inline-block. Para te ajudar com isso, recomendo a leitura do artigo [“Pare de chutar e aprenda como funciona o display: inline-block”](https://medium.com/collabcode/pare-de-chutar-e-aprenda-como-funciona-o-display-inline-block-4e6cba2f19d4), que também tem um vídeo-explicativo.

### **Nessa aula, você aprendeu:**

- Afastar elementos dos cantos da tela e de outros elementos;
- A diferença entre margin e padding;
- Diversas maneiras de determinar os valores e as direções das margens dentro da propriedade margin;
- Construir uma nova section;
- Reutilizar estilos através das classes dentro da nova section;
- Atribuir mais de uma classe nos elementos para incluir novas estilizações além das existentes.

### **Para saber mais: CSS interativo?**

Uma **pseudo-classe CSS** é uma propriedade que é 
adicionada ao final dos seletores que especifica o estado que esse 
elemento está. Ele detecta, por exemplo, se o elemento está com um mouse
 em cima dele, construindo uma experiência interativa com o usuário. 
Aqui, você pode conferir uma lista de pseudo-classes para testar no seu 
projeto:

`:focus`: é aplicada quando um elemento está em foco, pode
 ser pelo clique do mouse ou seleção pelo teclado. Um exemplo é quando 
os campos de escrita em formulários estão selecionados para o usuário 
escrever.

`:hover`: detecta quando um usuário está com o mouse em cima do elemento, sem necessariamente estar clicando.

`:active`: detecta quando o elemento está ativo, quando há uma interação, por exemplo: o link `<a>` está sendo clicado.

`:visited`: detecta quando o link `<a>` já foi visitado, ou seja, se você já clicou anteriormente naquele link.

`:link`: detecta quando é um link `<a>` que nunca foi clicado antes.

A sintaxe correta de uso de pseudo-classes é essa:

```css
seletor:pseudo-classe {
  propriedade: valor;
}
```

Um exemplo de utilização na prática seria este de trocar a cor do botão para azul quando o mouse estiver em cima dele:

```css
.container__botao:hover {
  background-color: blue;
}
```

### **Curiosidade**

Lembra que na primeira aula colocamos o termo `:root` no `styles.css`? Percebe que a estrutura é bem semelhante ao que estamos vendo agora? Isso acontece porque o root também é uma pseudo-classe!

Porém, essa pseudo-classe não tem um intuito mais interativo, ou 
seja, não há como usar pra trocar alguma coisa quando o usuário 
interage. Sua especificidade é bem alta, representando o documento 
inteiro. É comumente usada para a declaração de variáveis CSS.

Você pode ler mais sobre pseudo-classes no [MDN Web Docs](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-classes),
 um projeto colaborativo de código aberto que documenta tecnologias de 
plataforma da Web, incluindo CSS, HTML, JavaScript e APIs da Web.

### **Nessa aula aprendemos:**

- Usar flexbox e seu significado;
- Flex-containers, flex-itens, flex-direction;
- A tag footer;
- Colocar o conhecimento em prática;
- Pseudo-classes no CSS: hover e active.

### Atividade: **O famoso Github!**

Acabamos de criar a nossa conta no Github, criar nosso repositório e inserir os 
arquivos. Analisando o que fizemos, qual das opções abaixo **NÃO** é uma função do Github?

→ Executar código.

→ Não conseguimos executar o código, apenas fazer o deploy da aplicação através do Github Pages ou outras aplicações semelhantes como a Vercel.

### **Para saber mais: Deploy**

Esse processo que nós acabamos de fazer se chama **deploy**. O verbo *deploy*,
 em inglês, quer dizer implantar. Em programação, seu sentido está 
diretamente relacionado à sua tradução literal: fazer um deploy 
significa **colocar no ar alguma aplicação que teve seu desenvolvimento concluído**.
 Quando um site é finalizado por um desenvolvedor e, após seus testes, é
 finalmente hospedado e colocado no ar, ele passa pelo processo de 
deploy.

Primeiramente, hospedamos o Alura Plus no [Github Pages](https://docs.github.com/pt/pages/getting-started-with-github-pages/about-github-pages),
 um serviço de hospedagem de site estático que usa arquivos HTML, CSS e 
JavaScript diretamente de um repositório no GitHub e, como opção, 
executa os arquivos por meio de um processo e publica um site. Em 
seguida, fizemos deploy do Alura Plus pela [Vercel](https://vercel.com/),
 uma plataforma voltada para a hospedagem gratuita de aplicações de uma 
forma bem simples e rápida. Ela é conhecida por ser a empresa criadora 
do framework Next JS, voltado para o React.

Caso você tenha interesse em conhecer mais sobre esse tipo de serviço ou conhecer outros sites, vou recomendar o artigo [“Heroku, Vercel e outras opções de cloud como plataforma”](https://www.alura.com.br/artigos/heroku-vercel-outras-opcoes-cloud-plataforma) do João Manoel.

### **Para saber mais: próximos passos**

Terminamos o projeto Alura Plus, hospedamos e compartilhamos. Mas e
 agora? Para onde você deve seguir nessa jornada de estudos front-end?

Primeiramente, já que você construiu o repositório desse projeto, que tal editar o arquivo README que foi criado junto com ele? **O README**
 é um arquivo com extensão .md, ou seja, ele é escrito em Markdown que é
 uma linguagem de marcação utilizada para converter o texto em um HTML 
válido. **A função desse arquivo é apresentar informações do projeto**, como:

- Descrição do seu projeto;
- Funcionalidades;
- Como os usuários podem utilizá-lo;
- Onde os usuários podem encontrar ajuda sobre seu projeto;
- Autores do projeto.

Você pode editá-lo com o VSCode Web, da mesma maneira que fizemos no 
vídeo passado. Também trago algumas dicas da instrutora Camila no seu 
artigo [“Como escrever um bom README”](https://www.alura.com.br/artigos/escrever-bom-readme) que tenho certeza que te ajudará a deixar o seu README bonitão :)

Também recomendo estudar mais sobre o Github. Esse tipo de site para 
compartilhamento de código é usado no dia a dia das empresas, pois os 
códigos são compartilhados entre vários membros dentro de uma equipe. 
Além disso, usa-se também a ferramenta de controle de versão chamada 
Git. Que tal desbravar esse conteúdo no curso [“Git e Github: Controle e compartilhe seu código”](https://cursos.alura.com.br/course/git-github-controle-de-versao) do instrutor Vinicius Dias?

Depois de tudo isso, partiu aprender uma linguagem de programação 
para evoluir nosso código estático? Geralmente usamos Javascript no 
front-end e a Alura tem diversos conteúdos para te auxiliar nisso! Que 
tal dar uma olhada nos cursos de JS da [formação front-end](https://cursos.alura.com.br/formacao-front-end) e quem sabe dar continuidade na Alura Plus no futuro.

E por fim, nessa jornada, você vai se deparar com a escolha de ter 
seu primeiro pokemon… OPS! seu primeiro framework! E adivinha? A Alura 
também pode te ajudar com isso. Você pode encontrar conteúdos iniciais e
 intermediários de alguns frameworks e bibliotecas como:

- [ReactJS](https://cursos.alura.com.br/formacao-react-js)
- [Angular](https://www.alura.com.br/formacao-angular)
- [VueJS](https://www.alura.com.br/formacao-vuejs)

### Nessa aula aprendemos:

- Criar uma conta no Github;
- Construir um repositório com o código do curso;
- Escrever commits;
- Fazer deploy no Github Pages e Vercel;
- Editar código no VSCode Web;
- Enviar alterações para o repositório já existente.
