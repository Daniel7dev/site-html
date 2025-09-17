# site-html
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Site Exemplo — 4 "páginas" em 1 arquivo</title>
  <style>
    /* Pequeno CSS apenas para esconder/mostrar as "páginas" (poderia ser sem CSS, mas facilita a navegação) */
    .page { display: none; padding: 1rem; }
    .page:target { display: block; }
    /* mostrar a home por padrão se não houver hash */
    .page#home { display: block; }
    header nav ul { list-style: none; padding: 0; margin: 0 0 1rem 0; display: flex; gap: 1rem; }
    header nav a { text-decoration: none; }
    figure { margin: 0 0 1rem 0; }
  </style>
</head>
<body>
  <!-- Menu de navegação comum (links para âncoras internas) -->
  <header>
    <nav>
      <ul>
        <li><a href="#home" target="_self" title="Ir para Home" rel="noopener">Home</a></li>
        <li><a href="#menu" target="_self" title="Ver o Menu do Site" rel="noopener">Menu</a></li>
        <li><a href="#gallery" target="_self" title="Ir para a Galeria" rel="noopener">Galeria</a></li>
        <li><a href="#contact" target="_self" title="Ir para Contato" rel="noopener">Contato</a></li>
      </ul>
    </nav>
  </header>

  <!-- HOME (página 1) -->
  <main id="home" class="page" role="main" aria-labelledby="home-title">
    <h1 id="home-title">Bem-vindo ao Site Exemplo</h1>
    <h2>Apresentação</h2>
    <h3>O que você encontrará aqui</h3>
    <h4>Demonstração prática</h4>
    <h5>Exemplos de títulos</h5>
    <h6>Finalizando com h6</h6>

    <p>Esta é a <strong>página Home</strong> criada dentro de um único arquivo HTML. Aqui mostramos os títulos de <em>h1</em> até <em>h6</em> para cumprir o exercício.</p>

    <hr>

    <section>
      <h2>Imagem de destaque</h2>
      <p>Imagem de exemplo (placeholder).<br>
      Os atributos <mark>src</mark>, <mark>alt</mark>, <mark>width</mark> e <mark>height</mark> estão presentes no elemento <strong>img</strong>.</p>
      <img src="https://picsum.photos/seed/home/640/360" alt="Paisagem demonstrativa Home" width="640" height="360">
      <p>Fonte: <a href="https://picsum.photos" target="_blank" title="Abrir Picsum em nova aba" rel="noopener noreferrer">picsum.photos</a></p>
    </section>

    <hr>

    <p>Ir para: <a href="#menu" target="_self" title="Ir para Menu" rel="noopener">Menu</a> · <a href="#gallery" target="_self" title="Ir para Galeria" rel="noopener">Galeria</a> · <a href="#contact" target="_self" title="Ir para Contato" rel="noopener">Contato</a></p>
  </main>

  <!-- MENU (página 2) -->
  <article id="menu" class="page" role="article" aria-labelledby="menu-title">
    <h1 id="menu-title">Menu do Site</h1>
    <p>Esta é a <strong>página Menu</strong>. Ela explica a navegação do site e lista as seções disponíveis.</p>

    <section>
      <h2>Itens do Menu</h2>
      <ul>
        <li><strong>Home</strong> — página principal com demonstrações de títulos</li>
        <li><strong>Menu</strong> — você está aqui</li>
        <li><strong>Galeria</strong> — coleção de imagens</li>
        <li><strong>Contato</strong> — formulário de contato (mailto)</li>
      </ul>
    </section>

    <hr>

    <section>
      <h2>Links e referências</h2>
      <p>Exemplo de link externo seguro: <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTML" target="_blank" title="Abrir MDN em nova aba" rel="noopener noreferrer">MDN - HTML</a></p>
      <p>Texto com <em>itálico</em>, <strong>negrito</strong>, <u>sublinhado</u> e <mark>marca</mark> para demonstrar as tags obrigatórias.</p>
    </section>

    <hr>

    <p>Voltar para <a href="#home" target="_self" title="Voltar para Home" rel="noopener">Home</a> · Ir para <a href="#gallery" target="_self" title="Ir para Galeria" rel="noopener">Galeria</a> · Ir para <a href="#contact" target="_self" title="Ir para Contato" rel="noopener">Contato</a></p>
  </article>

  <!-- GALERIA (página 3) -->
  <section id="gallery" class="page" role="region" aria-labelledby="gallery-title">
    <h1 id="gallery-title">Galeria de Fotos</h1>
    <p>Veja abaixo algumas imagens de exemplo. Todas as imagens incluem src, alt, width e height.</p>

    <ul>
      <li>
        <figure>
          <img src="https://picsum.photos/seed/gallery1/400/300" alt="Foto 1 - paisagem" width="400" height="300">
          <figcaption>Foto 1 — paisagem</figcaption>
        </figure>
      </li>

      <li>
        <figure>
          <img src="https://picsum.photos/seed/gallery2/400/300" alt="Foto 2 - natureza" width="400" height="300">
          <figcaption>Foto 2 — natureza</figcaption>
        </figure>
      </li>

      <li>
        <figure>
          <img src="https://picsum.photos/seed/gallery3/400/300" alt="Foto 3 - urbano" width="400" height="300">
          <figcaption>Foto 3 — urbano</figcaption>
        </figure>
      </li>
    </ul>

    <hr>

    <p>Voltar para <a href="#home" target="_self" title="Voltar para Home" rel="noopener">Home</a> · Ver o <a href="#menu" target="_self" title="Voltar para Menu" rel="noopener">Menu</a> · Ir para <a href="#contact" target="_self" title="Ir para Contato" rel="noopener">Contato</a></p>
  </section>

  <!-- CONTATO (página 4) -->
  <section id="contact" class="page" role="form" aria-labelledby="contact-title">
    <h1 id="contact-title">Contato</h1>

    <section>
      <h2>Informações</h2>
      <p>Telefone: <strong>(00) 1234-5678</strong><br>
         Email: <a href="mailto:exemplo@dominio.com" target="_self" title="Enviar email" rel="noopener">exemplo@dominio.com</a></p>
    </section>

    <hr>

    <section>
      <h2>Formulário de contato (mailto)</h2>
      <p>Preencha o formulário e clique em <strong>Enviar</strong>. O envio usa <em>mailto</em> (abre o cliente de e-mail do sistema).<br>
      Caso não abra, use o link direto de e-mail acima.</p>

      <form action="mailto:exemplo@dominio.com" method="post" enctype="text/plain">
        <label for="nome"><strong>Nome:</strong></label><br>
        <input type="text" id="nome" name="Nome" required><br><br>

        <label for="email"><strong>Email:</strong></label><br>
        <input type="email" id="email" name="Email" required><br><br>

        <label for="mensagem"><strong>Mensagem:</strong></label><br>
        <textarea id="mensagem" name="Mensagem" rows="6" required></textarea><br><br>

        <button type="submit" title="Enviar mensagem">Enviar</button>
        <button type="reset" title="Limpar campos">Limpar</button>
      </form>

      <p><mark>Observação:</mark> envio por <em>mailto</em> depende do cliente de e‑mail. Se preferir envio sem mailto, posso integrar Formspree ou código com backend/JS.</p>
    </section>

    <hr>

    <p>Retornar para: <a href="#home" target="_self" title="Ir para Home" rel="noopener">Home</a> · <a href="#menu" target="_self" title="Ir para Menu" rel="noopener">Menu</a> · <a href="#gallery" target="_self" title="Ir para Galeria" rel="noopener">Galeria</a></p>
  </section>

  <footer>
    <p><strong>Resumo:</strong> todas as quatro "páginas" (Home, Menu, Galeria, Contato) estão dentro deste único arquivo, cada uma em uma seção/elemento distinto com id próprio. Use o menu para acessar cada página — os links são âncoras internas.</p>
  </footer>
</body>
</html>
