# Objetivo

Neste documento, irei destacar alguns pontos de atenção relacionados à qualidade do código, com foco em práticas que tornam o projeto mais manutenível.

# Pontos de Atenção

## 1. Nomenclaturas

* Embora não seja um problema crítico, é uma boa prática adotar padrões consistentes de nomenclatura no ambiente de desenvolvimento.
  Quando lidamos com arquivos ou funções com nomes compostos, é recomendado utilizar **snake_case** (funcao_que_faz_alguma_coisa) ou **camelCase** (funcaoFazAlgumaCoisa). Isso facilita a leitura e deixa mais claro o propósito de cada elemento.

* Também vale destacar que alguns nomes de arquivos estão genéricos demais, dificultando entender o que representam.
  Exemplos: *bandeirat3*, *canecaP*.
  Nomes pouco descritivos prejudicam a manutenção e a navegação pelo projeto.


## 2. Estrutura do Repositório

* Ao fazer o *git clone*, tive dificuldade inicial em distinguir quais arquivos eram páginas e quais eram apenas assets (imagens e fontes).

* Em projetos desse porte, é essencial pensar desde cedo na organização, já que isso impacta diretamente a manutenção futura. É recomendado seguir uma estrutura de pastas definida, por exemplo:

```
src/
├── assets/
│   ├── imgs/
│   ├── fonts/
├── index
├── carrinho
├── loginpage
```

* Com uma estrutura mais clara, o desenvolvimento se torna mais ágil, pois reduz o tempo gasto procurando arquivos específicos.


## 3. Layout das Páginas

Nesta seção, destaco alguns ajustes visuais e estruturais que podem melhorar a experiência do usuário.

### Header

* O header contém muitas informações (logo, links de navegação e botões), e apesar de lembrar outros sites do mesmo segmento, falta organização.
  Uma solução comum é separar o header em dois grandes grupos:
  (1) Logo + navegação
  (2) Ações (botões/ícones)
  Isso deixa o layout mais limpo e agradável.

* Sobre o agrupamento dos três ícones (lupa, carrinho e perfil):
  Recomendo reduzir para apenas um ícone principal (perfil), que abriria um menu contendo entrar/cadastrar e carrinho.
  A lupa, por exemplo, não faz sentido no contexto atual, já que o site possui apenas uma landing page e não há conteúdo a ser pesquisado.


### Banner

* Os dois banners estão visualmente bons, porém a altura reduzida transmite a sensação de que falta algo. Talvez aumentá-los para ocupar cerca de 90vh deixaria a experiência mais imersiva.

* No segundo banner, utilizar um layout diferente traria contraste e dinamismo ao carrossel.
  Alterar a posição da imagem e do texto já seria suficiente para quebrar a repetição.
  Também vale notar que essa é a única área onde aparece uma paleta de violeta/roxo bem clara, destoando do restante do site.


### Sobre

* A forma como os títulos estão estruturados a partir dessa seção não traz tanta visibilidade e pode gerar dúvidas. Em alguns casos, é preciso reler 2 ou 3 vezes para compreender o que está escrito.

* Os cards estão bem organizados, mas a quantidade reduzida de texto passa a sensação de que cada card é apenas uma continuação literal do anterior, como se o conteúdo estivesse fragmentado entre eles.


