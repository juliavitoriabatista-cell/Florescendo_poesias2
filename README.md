 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Florescendo Poesias</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">

  <style>
    :root {
      --roxo-escuro: #4b286d;
      --roxo: #76529a;
      --roxo-claro: #a987c4;
      --lilas: #eee4f5;
      --creme: #fffaff;
      --texto: #44364d;
      --dourado: #c9a96e;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background:
        radial-gradient(circle at 10% 10%, #eadcf4 0, transparent 25%),
        radial-gradient(circle at 90% 80%, #e5d4f0 0, transparent 25%),
        var(--creme);

      color: var(--texto);
      font-family: "Montserrat", sans-serif;
      line-height: 1.8;
    }

    /* Flores decorativas */

    .flor {
      position: fixed;
      font-size: 2rem;
      opacity: 0.35;
      pointer-events: none;
      animation: flutuar 6s ease-in-out infinite;
      z-index: 0;
    }

    .flor-1 {
      top: 8%;
      left: 4%;
    }

    .flor-2 {
      top: 35%;
      right: 5%;
      animation-delay: 1s;
    }

    .flor-3 {
      bottom: 12%;
      left: 7%;
      animation-delay: 2s;
    }

    .flor-4 {
      bottom: 30%;
      right: 8%;
      animation-delay: 3s;
    }

    @keyframes flutuar {
      0%, 100% {
        transform: translateY(0) rotate(0deg);
      }

      50% {
        transform: translateY(-15px) rotate(8deg);
      }
    }

    /* Cabeçalho */

    header {
      min-height: 90vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 60px 20px;
      position: relative;
      overflow: hidden;

      background:
        linear-gradient(
          rgba(72, 38, 102, 0.82),
          rgba(111, 72, 145, 0.78)
        ),
        url("sua-imagem-de-flores.jpg");

      background-size: cover;
      background-position: center;
    }

    header::after {
      content: "✿";
      position: absolute;
      bottom: 30px;
      font-size: 2rem;
      color: #fff;
      animation: florescer 2s infinite alternate;
    }

    @keyframes florescer {
      from {
        transform: scale(0.8);
        opacity: 0.5;
      }

      to {
        transform: scale(1.2);
        opacity: 1;
      }
    }

    .hero {
      max-width: 800px;
      color: white;
      animation: aparecer 1.5s ease;
    }

    @keyframes aparecer {
      from {
        opacity: 0;
        transform: translateY(30px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .hero .florzinha {
      font-size: 2rem;
      margin-bottom: 15px;
    }

    h1 {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(4rem, 10vw, 7rem);
      font-weight: 500;
      letter-spacing: 2px;
    }

    .subtitulo {
      font-family: "Cormorant Garamond", serif;
      font-size: 1.6rem;
      font-style: italic;
      margin-top: 10px;
    }

    /* Introdução */

    .introducao {
      max-width: 850px;
      margin: 90px auto;
      padding: 0 25px;
      text-align: center;
    }

    .introducao h2 {
      font-family: "Cormorant Garamond", serif;
      color: var(--roxo-escuro);
      font-size: 2.8rem;
      margin-bottom: 25px;
    }

    .introducao p {
      font-size: 1.05rem;
      margin-bottom: 20px;
    }

    .ornamento {
      color: var(--dourado);
      font-size: 1.8rem;
      margin: 25px 0;
    }

    /* Área dos poemas */

    main {
      width: min(1000px, 92%);
      margin: auto;
      position: relative;
      z-index: 1;
    }

    .poema {
      background: rgba(255, 250, 255, 0.92);
      border: 1px solid #dfcde9;
      border-radius: 22px;
      padding: 45px;
      margin: 50px 0;

      box-shadow:
        0 15px 40px rgba(75, 40, 109, 0.10);

      position: relative;
      overflow: hidden;

      transition: 0.4s ease;
    }

    .poema:hover {
      transform: translateY(-6px);
      box-shadow:
        0 20px 50px rgba(75, 40, 109, 0.16);
    }

    .poema::before {
      content: "❀";
      position: absolute;
      top: 15px;
      right: 25px;
      color: var(--roxo-claro);
      font-size: 2rem;
      opacity: 0.5;
    }

    .poema h2 {
      font-family: "Cormorant Garamond", serif;
      color: var(--roxo-escuro);
      font-size: 2.6rem;
      font-weight: 600;
      margin-bottom: 25px;
    }

    .poema .autor {
      color: var(--roxo);
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 25px;
    }

    .poema p {
      font-family: "Cormorant Garamond", serif;
      font-size: 1.35rem;
      white-space: pre-line;
    }

    /* Citação */

    .citacao {
      max-width: 850px;
      margin: 80px auto;
      padding: 50px 35px;
      text-align: center;

      background: linear-gradient(
        135deg,
        #f0e5f7,
        #faf3fc
      );

      border-radius: 30px;
      border: 1px solid #dec9e9;
    }

    .citacao p {
      font-family: "Cormorant Garamond", serif;
      font-size: 1.8rem;
      font-style: italic;
      color: var(--roxo-escuro);
    }

    .citacao span {
      display: block;
      margin-top: 20px;
      font-size: 0.85rem;
      letter-spacing: 2px;
      color: var(--roxo);
    }

    /* Rodapé */

    footer {
      margin-top: 100px;
      padding: 60px 20px;
      text-align: center;
      background: var(--roxo-escuro);
      color: white;
    }

    footer h2 {
      font-family: "Cormorant Garamond", serif;
      font-size: 2.5rem;
      font-weight: 500;
    }

    footer p {
      margin-top: 10px;
      opacity: 0.8;
    }

    .flores {
      margin-top: 25px;
      font-size: 1.8rem;
      letter-spacing: 10px;
    }

    /* Responsividade */

    @media (max-width: 600px) {

      header {
        min-height: 75vh;
      }

      h1 {
        font-size: 4rem;
      }

      .subtitulo {
        font-size: 1.3rem;
      }

      .poema {
        padding: 30px 22px;
      }

      .poema h2 {
        font-size: 2.1rem;
      }

      .poema p {
        font-size: 1.2rem;
      }

      .citacao p {
        font-size: 1.5rem;
      }
    }
  </style>
</head>

<body>

  <!-- Flores decorativas -->
  <div class="flor flor-1">🌸</div>
  <div class="flor flor-2">✿</div>
  <div class="flor flor-3">🌷</div>
  <div class="flor flor-4">❀</div>

  <!-- Capa -->

  <header>
    <div class="hero">
      <div class="florzinha">❀</div>

      <h1>Jardim de Poesias</h1>

      <p class="subtitulo">
        "Olá, querido leitor. Sente-se e aprecie um bom poema."
      </p>
    </div>
  </header>


  <!-- Introdução -->

  <section class="introducao">

    <div class="ornamento">✿</div>

    <h2>Onde as palavras florescem</h2>

    <p>
      Poesias podem mudar a forma como você vê o mundo,
      a forma como você se vê.
    </p>

    <p>
      Ao contrário do que muita gente pensa, poesia não fala
      somente de amor. Ela fala de tudo aquilo que dói,
      floresce e permanece no âmago da alma humana.
    </p>

    <div class="ornamento">❀</div>

  </section>


  <main>

    <!-- Citação -->

    <section class="citacao">

      <p>
        "Não lemos nem escrevemos poesia por ser algo bonito
        ou fofo, mas porque fazemos parte da raça humana,
        que é repleta de paixão."
      </p>

      <span>— Professor John Keating</span>

    </section>


    <!-- Clarice -->

    <article class="poema">

      <h2>Palavras de Clarice</h2>

      <div class="autor">Clarice Lispector</div>

      <p>
        “Até cortar os próprios defeitos pode ser perigoso.
        Nunca se sabe qual é o defeito que sustenta
        nosso edifício inteiro.”

        “Enquanto eu tiver perguntas e não houver resposta,
        continuarei a escrever.”
      </p>

    </article>


    <!-- Vinicius -->

    <article class="poema">

      <h2>A Rosa de Hiroshima</h2>

      <div class="autor">Vinicius de Moraes</div>

      <p>
        hjhhgg
        hjhh
        jjj
      </p>

    </article>


    <article class="poema">

      <h2>A Felicidade</h2>

      <div class="autor">Vinicius de Moraes</div>

      <p>
        <!-- Cole aqui o texto completo do poema,
        se possuir autorização para publicá-lo. -->

        Tristeza não tem fim.
        Felicidade sim.
      </p>

    </article>


    <article class="poema">

      <h2>Soneto do Amor Total</h2>

      <div class="autor">Vinicius de Moraes</div>

      <p>
        <!-- Área reservada para o poema -->

        Amo-te tanto, meu amor...
      </p>

    </article>


    <article class="poema">

      <h2>Eu Sei Que Vou Te Amar</h2>

      <div class="autor">Vinicius de Moraes</div>

      <p>
        Eu sei que vou te amar 
        Eu sei que vou te amar 
        Por toda a minha vida eu vou te amar 
        Em cada despedida eu vou te amar 
        Desesperadamente 
        Eu sei que vou te amar 
        E cada verso meu será pra te dizer 
        Que eu sei que vou te amar 
        Por toda a minha vida 
        Eu sei que vou chorar 
        A cada ausência tua eu vou chorar, 
        Mas cada volta tua há de apagar 
        O que essa ausência tua me causou 
        Eu sei que vou sofrer 
        A eterna desventura de viver a espera 
        De viver ao lado teu Por toda a minha vida.
      </p>

    </article>


    <article class="poema">

      <h2>Soneto de Separação</h2>

      <div class="autor">Vinicius de Moraes</div>

      <p>
        <!-- Área reservada para o poema -->

        De repente, do riso fez-se o pranto,
        silencioso e branco como a bruma...
      </p>

    </article>


    <article class="poema">

      <h2>Tomara</h2>

      <div class="autor">Vinicius de Moraes</div>

      <p>
     Que a tristeza te convença 
     Que a saudade não compensa 
     E que a ausência não dá paz
     E o verdadeiro amor de quem se ama
     Tece a mesma antiga trama Que não se desfaz 
     E a coisa mais divina Que há no mundo 
     É viver cada segundo 
     Como nunca mais...
      </p>

    </article>

  </main>


  <footer>

    <h2>Continue florescendo.</h2>

    <p>
      Que nunca nos faltem palavras para sentir,
      escrever e transformar o mundo.
    </p>

    <div class="flores">
      ✿ ❀ 🌸 ❁
    </div>

  </footer>

</body>
</html>
```
