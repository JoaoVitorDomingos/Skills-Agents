[JAVASCRIPT__BADGE]: https://img.shields.io/badge/Javascript-000?style=for-the-badge&logo=javascript
[HTML__BADGE]: https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white 
[CSS__BADGE]: https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white
[BOOTSTRAP__BADGE]: https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white 
[MIT__BADGE]: https://img.shields.io/github/license/Naereen/StrapDown.js.svg

<h1 align="center" style="font-weight: bold;">MoveX</h1>

![html][HTML__BADGE]
![css3][CSS__BADGE]
![javascript][JAVASCRIPT__BADGE]
![bootstrap][BOOTSTRAP__BADGE]
![mit][MIT__BADGE]

<p align="center">
  <a href="#sobre">Sobre</a> • 
  <a href="#acesso">Acesse Aqui</a> • 
  <a href="#detalhamento">Detalhamento</a> • 
  <a href="#contribuidores">Contribuidores</a> •
  <a href="#licenca">Licença</a>
</p>

<br>
<p align="center">
    <img src="imagens/readme/1.png" alt="Imagem do Projeto" width="800px">
</p>
<br>

<h2 id="sobre">📌 Sobre</h2>
Este é um projeto de um site de uma loja de roupas esportivas, chamada MoveX. Este site foi feito com <strong>HTML</strong>, <strong>CSS</strong>, <strong>Javascript</strong> e <strong>Bootstrap</strong>, utilizando a prática <strong>Mobile First</strong>, com o objetivo de colocar em prática o que estudei, principalmente em <ins>Bootstrap</ins>. Também foi utilizada uma Biblioteca chamada <strong><a href="https://swiperjs.com/">Swiper</a></strong>, para facilitar a implementação de um elemento e o <strong>Git</strong> para controle de versões.
<br>
<br>

<h2 id="acesso">🚀 Acesse o Projeto</h2>
Veja o projeto você mesmo: https://joaovitordomingos.github.io/moveX/
<br>
<br>

<h2 id="detalhamento">📋 Detalhamento</h2>
<p>Nesta seção detalharei sobre o projeto, citando os pontos mais importantes sobre ele e sua criação.</p>
<details>
  <summary><h3>Sumário</h3></summary>
  <ol>
    <li><a href="#mobile_first">Mobile First</a></li>
    <li><a href="#menu">Menu de Navegação</a></li>
    <li><a href="#swiper">Carrossel - Biblioteca Swiper</a></li>
  </ol>
</details>

<h3 id="mobile_first">Mobile First</h3>
<p>Foi utilizado a prática Mobile First para a criação do site, para garantir que nos dispositivos móveis o site não apresente nenhum problema visual e funcional.</p>
<p>Depois de finalizado a parte mobile, a criação se expandiu para telas maiores, como para tablet, notebook e no final computadores e telas maiores.</p>
<p>Deste modo há a garantia que o site estará funcional e visível para todos os tipos de telas e também não haverá nenhuma feature excluída para as telas menores, já que foi realizado em Mobile First.</p>
<p>Segue algumas imagens das partes do site em diferentes tamanhos de tela:</p>
<br>
<h4 align="center">Área do menu e do Banner</h4>
<div align="center">
  <img src="imagens/readme/menu_banner/cell.png" alt="Área do menu e do banner nas telas mobile" width="200px">
  <img src="imagens/readme/menu_banner/tablet.png" alt="Área do menu e do banner nas telas de tablet" width="300px">
  <img src="imagens/readme/menu_banner/maiores.png" alt="Área do menu e do banner nas telas de notebook pra cima" width="700px">
</div>
<br>
<br>
<h4 align="center">Área de Contato</h4>
<div align="center">
  <img src="imagens/readme/contato/cell.png" alt="Área de contato nas telas mobile" width="200px">
  <img src="imagens/readme/contato/tablet.png" alt="Área de contato nas telas de tablet" width="300px">
  <img src="imagens/readme/contato/maiores.png" alt="Área de contato nas telas de notebook pra cima" width="700px">
</div>

<br>
<br>

<h3 id="menu">Menu de Navegação</h3>
<p>O menu de navegação em telas médias e grandes, notebook para cima, é completo, com logo, links e ícones, como mostra a imagem:</p>
<div align="center"><img src="imagens/readme/navegacao/1.png" alt="Menu de navegação nas telas de notebook e maiores" width="800px"></div>
<p>Porém, em telas menores como tablet e celulares, este menu é minimizado, é utilizado um menu hambúrguer.</p>
<div align="center">
  <img src="imagens/readme/navegacao/2.png" alt="Menu de navegação nas telas de celulares" width="400px">
  <img src="imagens/readme/navegacao/3.png" alt="Menu de navegação nas telas de tablets" width="600px">
</div>
<p>Como é possível perceber, a posição do menu hambúrguer no celular é diferente do tablet, isso porque, no celular, ao expandir o menu hambúguer, ele cobre a tela toda, enquanto no tablet não e, também no tablet, é posicionado a direita.</p>
<h4 align="center">Celular</h4>
<div align="center">
  <img src="imagens/readme/menu_banner/cell.png" alt="Menu Hambúrguer nas telas de celulares" width="200px">
  <img src="imagens/readme/navegacao/4.png" alt="Menu Hambúrguer expandido nas telas de tablets" width="200px">
</div>
<h4 align="center">Tablet</h4>
<div align="center">
  <img src="imagens/readme/menu_banner/tablet.png" alt="Menu Hambúrguer nas telas de Tablet" width="300px">
  <img src="imagens/readme/navegacao/5.png" alt="Menu Hambúrguer expandido nas telas de tablets" width="300px">
</div>
<p>Para isto, foi utilizado Javascript. É pego a largura da tela do usuário e feito uma comparação simples, caso seja menor que 768px (celular) o elemento referente ao menu hambúrguer recebe a classe do Bootstrap <strong>"offcanvas-top"</strong>, caso seja maior, recebe a classe <strong>"offcanvas-end"</strong></p>
<p><strong>OBS: o menu hambúrguer foi feito com o Bootstrap.</strong></p>
<div align="center">
  <img src="imagens/readme/navegacao/6.png" alt="Código JS do menu hambúrguer" width="600px">
</div>
<p>Também foi adicionado um evento de <strong>"resize"</strong> ao <i>window</i> para que sempre que o usuário mudar o tamanho da tela, durante o uso do site, não ocorra um erro, isso não sendo algo totalmente necessário.</p>
<div align="center">
  <img src="imagens/readme/navegacao/7.png" alt="Código do Evento de Resize" width="400px">
</div>

<br>
<br>

<h3 id="swiper">Carrossel - Biblioteca Swiper</h3>
<p>Para o carrossel de produtos, não foi utilizado o do Bootstrap, mas sim da <a href="https://swiperjs.com/">Biblioteca Swiper</a>.</p>
<p>Isto porque, o Bootstrap não possui um carrossel com múltiplas imagens, então iria ser necessário adição de código personalizado. Para facilitar, foi utilizado o Swiper, que é focado em carrosseis.</p>
<h4 align="center">Código do Swiper</h4>
<div align="center">
  <img src="imagens/readme/codigo_swiper.png" alt="Código JS do Swiper" width="400px">
</div>
<p>Para telas de celulares, é apresentado apenas uma imagem de cada vez. Para tablets, 2. Notebook, 3. E telas de 1500px pra cima, 5.</p>
<div align="center">
  <img src="imagens/readme/carrossel/1.png" alt="Menu Hambúrguer nas telas de celulares" width="200px">
  <img src="imagens/readme/carrossel/2.png" alt="Menu Hambúrguer expandido nas telas de tablets" width="300px">
  <img src="imagens/readme/carrossel/3.png" alt="Menu Hambúrguer nas telas de celulares" width="500px">
  <img src="imagens/readme/carrossel/4.png" alt="Menu Hambúrguer expandido nas telas de tablets" width="900px">
</div>

<br>
<br>

<h2 id="contribuidores">🤝 Contribuidores</h2>
<p>Um agradecimento especial ao Luis Otávio, que criou todo o design do site, imagens, cores e fontes.</p>

<table>
  <tr>
    <td align="center">
      <a href="https://www.instagram.com/luiss_domingos/">
        <img src="imagens/readme/luis.jpeg" width="100px;" alt="Luis Otávio C. Domingos"/><br>
        <sub>
          <b>Luis Otávio C. Domingos</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

<br>
<br>

<h2 id="licenca">📃 Licença</h2>
Veja a licença do projeto: <a href="https://github.com/JoaoVitorDomingos/moveX?tab=MIT-1-ov-file">MIT License</a>
<br>
<br>
