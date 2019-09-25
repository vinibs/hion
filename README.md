# HiON
### Hypertext in Object Notation

## Uma maneira diferente de escrever páginas HTML estáticas

A ideia do projeto é criar uma ferramenta de conversão de código em notação de objetos (como JSON) em código HTML (aplicadas boas práticas).

Alguns requisitos são previamente definidos, antes do início do desenvolvimento. Esses requisitos são listados abaixo.


## Extensão customizada do arquivo

Espera-se a criação de uma extensão de arquivo customizada, **`.hion`**.

Esse formato de arquivo será baseado em arquivos JSON, com a construção de um - único - objeto raiz, equivalente ã tag `html` (e suas propriedades relacionadas, como `lang` e `doctype`).


## Importação da ferramenta

Todo o código deve estar contido em um único arquivo JavaScript para ser importado em qualquer página como um código JS qualquer, através da tag `script`.


## Utilização de mídias e conteúdos externos

No código estruturado (em formato de objeto) deve ser possível referenciar elementos externos como em uma página HTML comum, como imagens, CSS e arquivos JS.

É uma possibilidade que um objeto interno, na hierarquia, possua conteúdos embutidos de JavaScript e estilos (equivalente às tags `style` e `script` nativas do HTML), mas não é objeto de foco inicialmente.


## Renderização da tela

A renderização da tela deve dar-se por meio de uma função simples, que recebe o caminho/nome do arquivo **.hion** a ser convertido para HTML. Um modelo ilustrativo seria:

    hion.render('src/pages/home.hion');

Esse exemplo demonstra a implicação de um objeto instanciado no código JS da ferramenta, chamado `hion` e da presença de um método chamado `render()` em seu escopo.


## Compatibilidade

### Navegadores e tecnologias
A ferramenta deve utilizar recursos do ES5 para questões de compatibilidade. Alguns recursos do ES6 podem ser aplicados também, se já bem difundidos atualmente entre os navegadores mais recentes (e algumas das suas versões anteriores).

## Frameworks
É importante que a estrutura do projeto permita sua fácil aplicação em códigos comuns e em diferentes frameworks, assim como é o caso do Bootstrap e jQuery.

No entanto, é preciso haver compatibilidade confirmada com os frameworks [Luvi](https://github.com/vinibs/luvi) (PHP) e [Lira](https://github.com/vinibs/lira) (JavaScript/Single Page Application). Estes frameworks podem futuramente incorporar o HiON em seu código, baseando-se nas versões já liberadas no projeto atual.


## Referências

Ferramentas semelhantes que podem (e devem) ser observadas a fim de extrair pontos fortes a serem aplicados no projeto:

- [Pug](https://pugjs.org)
- [JSON2HTML](https://json2html.com)