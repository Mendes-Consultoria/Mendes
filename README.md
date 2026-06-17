[index.html](https://github.com/user-attachments/files/29053737/index.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mendes Consultoria | Consultoria Fitness Online e Presencial</title>

  <style>
    :root {
      --bg: #050505;
      --bg-2: #0b0b0b;
      --card: rgba(15, 15, 15, 0.92);
      --card-2: rgba(22, 22, 22, 0.92);
      --gold: #d8b42c;
      --gold-2: #f1cf45;
      --red: #d90429;
      --text: #ffffff;
      --muted: #a7a7a7;
      --muted-2: #737373;
      --line: rgba(255,255,255,0.10);
      --shadow: 0 22px 80px rgba(0,0,0,0.45);
      --radius: 24px;
      --max: 1180px;
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
      font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at 80% 12%, rgba(216,180,44,0.18), transparent 28%),
        radial-gradient(circle at 8% 5%, rgba(217,4,41,0.10), transparent 25%),
        linear-gradient(180deg, #050505 0%, #090909 55%, #050505 100%);
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background-image:
        linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
      background-size: 56px 56px;
      mask-image: linear-gradient(to bottom, black, transparent 92%);
      z-index: 0;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(var(--max), calc(100% - 40px));
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }

    .topbar {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(18px);
      background: rgba(5,5,5,0.86);
      border-bottom: 1px solid var(--line);
    }

    .nav {
      height: 84px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 28px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 14px;
      min-width: 230px;
    }

    .brand-mark {
      width: 42px;
      height: 42px;
      border-radius: 12px;
      background: linear-gradient(135deg, var(--gold), #8a6a07);
      color: #050505;
      display: grid;
      place-items: center;
      font-weight: 900;
      letter-spacing: -1px;
      box-shadow: 0 0 26px rgba(216,180,44,0.26);
    }

    .brand-name {
      font-weight: 900;
      letter-spacing: -0.03em;
      line-height: 1;
      font-size: 16px;
    }

    .brand-sub {
      color: var(--gold-2);
      font-size: 10px;
      font-weight: 800;
      letter-spacing: 0.26em;
      margin-top: 4px;
    }

    .nav-links {
      display: flex;
      gap: 28px;
      align-items: center;
      color: #a8a8a8;
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .nav-links a:hover {
      color: var(--gold);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      min-height: 50px;
      padding: 0 28px;
      border-radius: 999px;
      font-weight: 900;
      font-size: 14px;
      border: 1px solid transparent;
      cursor: pointer;
      transition: 0.2s ease;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold-2), #c9a51f);
      color: #050505;
      box-shadow: 0 18px 40px rgba(216,180,44,0.18);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      filter: brightness(1.05);
    }

    .btn-outline {
      border-color: rgba(216,180,44,0.55);
      color: var(--gold-2);
      background: transparent;
    }

    .btn-outline:hover {
      background: rgba(216,180,44,0.10);
    }

    .hero {
      padding: 112px 0 76px;
      text-align: center;
      position: relative;
    }

    .eyebrow {
      color: var(--gold-2);
      font-size: 12px;
      font-weight: 900;
      letter-spacing: 0.36em;
      text-transform: uppercase;
      margin-bottom: 24px;
    }

    h1 {
      font-size: clamp(46px, 7vw, 86px);
      line-height: 0.95;
      letter-spacing: -0.07em;
      max-width: 980px;
      margin: 0 auto 28px;
    }

    .gold {
      color: var(--gold-2);
    }

    .hero p {
      color: #b8b8b8;
      font-size: clamp(16px, 2vw, 20px);
      max-width: 760px;
      margin: 0 auto 38px;
    }

    .hero-actions {
      display: flex;
      justify-content: center;
      gap: 16px;
      flex-wrap: wrap;
    }

    .stats {
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
      background: rgba(255,255,255,0.018);
      padding: 22px 0;
    }

    .stats-inner {
      display: flex;
      justify-content: center;
      gap: 42px;
      flex-wrap: wrap;
      color: #8d8d8d;
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 0.16em;
      text-transform: uppercase;
    }

    .stats-inner span strong {
      color: var(--gold);
    }

    section {
      padding: 92px 0;
      position: relative;
    }

    .section-head {
      margin-bottom: 44px;
    }

    .center {
      text-align: center;
    }

    .section-head h2 {
      font-size: clamp(34px, 5vw, 58px);
      line-height: 1.02;
      letter-spacing: -0.06em;
      margin-bottom: 18px;
    }

    .section-head p {
      color: #aaa;
      font-size: 17px;
      max-width: 730px;
    }

    .center p {
      margin-inline: auto;
    }

    .grid-4 {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 20px;
    }

    .feature-card,
    .plan,
    .mfit-panel,
    .testimonial,
    .ebook-box,
    .calc-card {
      background: linear-gradient(180deg, rgba(18,18,18,0.96), rgba(8,8,8,0.96));
      border: 1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .feature-card {
      padding: 34px;
      min-height: 240px;
    }

    .icon {
      width: 50px;
      height: 50px;
      border-radius: 14px;
      display: grid;
      place-items: center;
      background: rgba(216,180,44,0.12);
      border: 1px solid rgba(216,180,44,0.32);
      color: var(--gold-2);
      margin-bottom: 28px;
      font-weight: 900;
    }

    .feature-card h3 {
      font-size: 20px;
      margin-bottom: 12px;
      letter-spacing: -0.03em;
    }

    .feature-card p {
      color: #aaa;
      font-size: 15px;
    }

    .process {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 52px;
      align-items: center;
    }

    .steps {
      display: grid;
      gap: 28px;
    }

    .step {
      display: grid;
      grid-template-columns: 54px 1fr;
      gap: 18px;
    }

    .step-num {
      width: 54px;
      height: 54px;
      border-radius: 15px;
      background: rgba(255,255,255,0.04);
      border: 1px solid var(--line);
      color: var(--gold);
      display: grid;
      place-items: center;
      font-weight: 900;
    }

    .step small {
      color: var(--gold-2);
      font-weight: 900;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      font-size: 10px;
    }

    .step h3 {
      margin: 7px 0 8px;
      font-size: 19px;
    }

    .step p {
      color: #aaa;
      font-size: 15px;
    }

    .mfit-panel {
      padding: 34px;
      overflow: hidden;
      position: relative;
      min-height: 440px;
    }

    .mfit-screen {
      background: #f7f9fc;
      color: #182236;
      border-radius: 24px;
      overflow: hidden;
      border: 1px solid rgba(255,255,255,0.08);
      box-shadow: 0 30px 80px rgba(0,0,0,0.45);
    }

    .mfit-top {
      background: #263d58;
      color: #fff;
      padding: 22px;
      text-align: center;
      font-size: 24px;
      font-weight: 900;
      letter-spacing: -0.03em;
    }

    .mfit-body {
      padding: 24px;
      display: grid;
      gap: 14px;
    }

    .mfit-item {
      background: white;
      border-radius: 16px;
      padding: 18px;
      display: flex;
      align-items: center;
      gap: 16px;
      border: 1px solid #e8edf5;
    }

    .mfit-badge {
      width: 44px;
      height: 44px;
      border-radius: 14px;
      background: #dff1ff;
      color: #0d8de4;
      display: grid;
      place-items: center;
      font-weight: 900;
      flex: none;
    }

    .mfit-item b {
      display: block;
      font-size: 16px;
      color: #182236;
      margin-bottom: 2px;
    }

    .mfit-item span {
      color: #64748b;
      font-size: 13px;
    }

    .plans {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 28px;
    }

    .plan {
      padding: 34px;
      position: relative;
      overflow: hidden;
    }

    .plan.featured {
      border-color: rgba(216,180,44,0.62);
      background: linear-gradient(180deg, rgba(31,31,31,0.98), rgba(9,9,9,0.98));
      transform: translateY(-10px);
    }

    .tag {
      position: absolute;
      top: 0;
      right: 0;
      background: var(--gold);
      color: #050505;
      padding: 10px 22px;
      border-radius: 0 24px 0 16px;
      font-size: 11px;
      font-weight: 1000;
      letter-spacing: 0.16em;
      text-transform: uppercase;
    }

    .tag-red {
      background: var(--red);
      color: #fff;
    }

    .plan h3 {
      font-size: 24px;
      margin-bottom: 6px;
    }

    .plan .sub {
      color: var(--gold-2);
      font-size: 13px;
      font-weight: 900;
      margin-bottom: 26px;
    }

    .price {
      display: flex;
      align-items: baseline;
      gap: 7px;
      margin-bottom: 26px;
    }

    .price small {
      color: #999;
    }

    .price strong {
      font-size: 44px;
      line-height: 1;
    }

    .plan p {
      color: #aaa;
      margin-bottom: 26px;
      min-height: 76px;
    }

    .checks {
      display: grid;
      gap: 14px;
      margin-bottom: 34px;
    }

    .checks li {
      list-style: none;
      color: #bdbdbd;
      font-size: 15px;
      display: flex;
      gap: 12px;
      align-items: flex-start;
    }

    .checks li::before {
      content: "✓";
      width: 22px;
      height: 22px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      flex: none;
      color: var(--gold-2);
      border: 1px solid rgba(216,180,44,0.45);
      background: rgba(216,180,44,0.10);
      font-size: 12px;
      font-weight: 900;
    }

    .calculator {
      max-width: 900px;
      margin: 0 auto;
    }

    .calc-card {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      overflow: hidden;
    }

    .calc-form {
      padding: 34px;
      border-right: 1px solid var(--line);
    }

    .calc-results {
      padding: 34px;
      display: grid;
      place-items: center;
      text-align: center;
      min-height: 410px;
    }

    .field-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
      margin-bottom: 18px;
    }

    .field {
      display: grid;
      gap: 8px;
    }

    label {
      color: #aaa;
      font-size: 11px;
      text-transform: uppercase;
      font-weight: 900;
      letter-spacing: 0.14em;
    }

    input,
    select {
      width: 100%;
      height: 52px;
      border-radius: 14px;
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.04);
      color: #fff;
      padding: 0 16px;
      outline: none;
      font-size: 15px;
    }

    select option {
      color: #111;
    }

    input:focus,
    select:focus {
      border-color: rgba(216,180,44,0.7);
      box-shadow: 0 0 0 4px rgba(216,180,44,0.08);
    }

    .sex-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-bottom: 18px;
    }

    .sex-btn {
      height: 52px;
      border-radius: 14px;
      border: 1px solid var(--line);
      background: rgba(255,255,255,0.04);
      color: #858585;
      font-weight: 900;
      cursor: pointer;
    }

    .sex-btn.active {
      border-color: rgba(216,180,44,0.74);
      background: rgba(216,180,44,0.12);
      color: var(--gold-2);
    }

    .result-number {
      font-size: 54px;
      font-weight: 1000;
      letter-spacing: -0.06em;
      color: var(--gold-2);
      line-height: 1;
      margin-bottom: 10px;
    }

    .result-label {
      color: #aaa;
      font-weight: 800;
    }

    .mini-results {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      width: 100%;
      margin-top: 24px;
    }

    .mini {
      border: 1px solid var(--line);
      border-radius: 16px;
      padding: 18px;
      background: rgba(255,255,255,0.035);
    }

    .mini strong {
      color: #fff;
      font-size: 22px;
    }

    .mini span {
      display: block;
      color: #858585;
      font-size: 12px;
    }

    .ebook-box {
      max-width: 760px;
      margin: 0 auto;
      padding: 56px;
      text-align: center;
      border-color: rgba(216,180,44,0.25);
    }

    .ebook-box h3 {
      font-size: 30px;
      margin-bottom: 14px;
    }

    .ebook-box p {
      color: #aaa;
      max-width: 560px;
      margin: 0 auto 28px;
    }

    .testimonials {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
    }

    .testimonial {
      padding: 30px;
    }

    .stars {
      color: var(--gold-2);
      letter-spacing: 2px;
      margin-bottom: 18px;
    }

    .testimonial h3 {
      font-size: 18px;
      margin-bottom: 12px;
    }

    .testimonial p {
      color: #aaa;
      font-size: 15px;
      margin-bottom: 22px;
    }

    footer {
      padding: 70px 0 34px;
      border-top: 1px solid var(--line);
      background: rgba(0,0,0,0.35);
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1.4fr 0.8fr 0.8fr 0.8fr;
      gap: 40px;
      margin-bottom: 54px;
    }

    .footer-grid h4 {
      font-size: 13px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 18px;
    }

    .footer-grid a,
    .footer-grid p {
      display: block;
      color: #858585;
      margin-bottom: 12px;
      font-size: 14px;
    }

    .footer-grid a:hover {
      color: var(--gold);
    }

    .copyright {
      border-top: 1px solid var(--line);
      padding-top: 26px;
      display: flex;
      justify-content: space-between;
      gap: 20px;
      color: #656565;
      font-size: 13px;
      flex-wrap: wrap;
    }

    @media (max-width: 980px) {
      .nav-links {
        display: none;
      }

      .grid-4,
      .plans,
      .testimonials,
      .process,
      .calc-card,
      .footer-grid {
        grid-template-columns: 1fr;
      }

      .calc-form {
        border-right: none;
        border-bottom: 1px solid var(--line);
      }

      .plan.featured {
        transform: none;
      }
    }

    @media (max-width: 620px) {
      .container {
        width: min(100% - 26px, var(--max));
      }

      .nav {
        height: 76px;
      }

      .brand {
        min-width: unset;
      }

      .brand-name {
        font-size: 14px;
      }

      .brand-sub {
        font-size: 8px;
      }

      .topbar .btn {
        display: none;
      }

      .hero {
        padding: 78px 0 54px;
      }

      .hero-actions {
        display: grid;
      }

      .btn {
        width: 100%;
      }

      section {
        padding: 66px 0;
      }

      .field-grid,
      .mini-results,
      .sex-row {
        grid-template-columns: 1fr;
      }

      .feature-card,
      .plan,
      .calc-form,
      .calc-results,
      .ebook-box {
        padding: 26px;
      }

      h1 {
        font-size: 48px;
      }
    }
  </style>
</head>

<body>
  <header class="topbar">
    <div class="container nav">
      <a href="#inicio" class="brand">
        <div class="brand-mark">MC</div>
        <div>
          <div class="brand-name">MENDES CONSULTORIA</div>
          <div class="brand-sub">PERFORMANCE</div>
        </div>
      </a>

      <nav class="nav-links">
        <a href="#inicio">Início</a>
        <a href="#autoridade">Autoridade</a>
        <a href="#mfit">MFIT</a>
        <a href="#planos">Planos</a>
        <a href="#calculadora">Calculadora</a>
        <a href="#ebooks">E-books</a>
      </nav>

      <a class="btn btn-primary" href="https://wa.me/5500000000000" target="_blank">Agendar Avaliação</a>
    </div>
  </header>

  <main>
    <section class="hero" id="inicio">
      <div class="container">
        <div class="eyebrow">Consultoria Fitness Premium</div>
        <h1>Mendes Consultoria para quem quer <span class="gold">resultado real</span>.</h1>
        <p>Treino, estratégia e acompanhamento profissional para transformar seu físico com método, consistência e execução correta.</p>

        <div class="hero-actions">
          <a class="btn btn-primary" href="https://wa.me/5500000000000" target="_blank">Agendar Avaliação</a>
          <a class="btn btn-outline" href="#planos">Conhecer Planos</a>
        </div>
      </div>
    </section>

    <div class="stats">
      <div class="container stats-inner">
        <span><strong>7+</strong> anos de experiência</span>
        <span><strong>MFIT</strong> entrega dos treinos</span>
        <span><strong>Online</strong> para todo Brasil</span>
        <span><strong>Presencial</strong> em Janaúba/MG</span>
      </div>
    </div>

    <section id="autoridade">
      <div class="container">
        <div class="section-head">
          <div class="eyebrow">Autoridade</div>
          <h2>Método validado por <span class="gold">execução, acompanhamento e consistência</span>.</h2>
          <p>Não é protocolo genérico. A consultoria une avaliação, planejamento de treino, orientação estratégica e ajustes conforme sua evolução real.</p>
        </div>

        <div class="grid-4">
          <div class="feature-card">
            <div class="icon">01</div>
            <h3>Avaliação estratégica</h3>
            <p>Análise inicial feita por informações, rotina, fotos e vídeos enviados pelo aluno de forma profissional.</p>
          </div>

          <div class="feature-card">
            <div class="icon">02</div>
            <h3>Treino individualizado</h3>
            <p>Programa ajustado ao seu objetivo, nível atual, disponibilidade, equipamentos e capacidade de recuperação.</p>
          </div>

          <div class="feature-card">
            <div class="icon">03</div>
            <h3>Entrega pelo MFIT</h3>
            <p>O aluno recebe a ficha no aplicativo com organização, histórico, feedbacks e vídeos demonstrativos.</p>
          </div>

          <div class="feature-card">
            <div class="icon">04</div>
            <h3>Evolução mensurável</h3>
            <p>Fotos, dados, frequência e execução ajudam a acompanhar o progresso com mais precisão.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="como-funciona">
      <div class="container">
        <div class="section-head center">
          <div class="eyebrow">Processo simples</div>
          <h2>Como funciona a <span class="gold">consultoria</span></h2>
          <p>Em poucos passos você recebe um planejamento completo e começa a executar com clareza.</p>
        </div>

        <div class="process">
          <div class="steps">
            <div class="step">
              <div class="step-num">1</div>
              <div>
                <small>Passo 01</small>
                <h3>Escolha seu plano</h3>
                <p>Selecione o nível de acompanhamento ideal para seu objetivo, rotina e necessidade de suporte.</p>
              </div>
            </div>

            <div class="step">
              <div class="step-num">2</div>
              <div>
                <small>Passo 02</small>
                <h3>Faça a avaliação inicial</h3>
                <p>Envie informações, fotos e vídeos para análise técnica. Na consultoria presencial, o atendimento ocorre em Janaúba/MG.</p>
              </div>
            </div>

            <div class="step">
              <div class="step-num">3</div>
              <div>
                <small>Passo 03</small>
                <h3>Receba sua ficha pelo MFIT</h3>
                <p>Seu treino fica disponível no app com exercícios, séries, repetições, intervalos e vídeos explicativos.</p>
              </div>
            </div>

            <div class="step">
              <div class="step-num">4</div>
              <div>
                <small>Passo 04</small>
                <h3>Acompanhe sua evolução</h3>
                <p>O progresso é monitorado por feedbacks, registros e atualizações conforme seu corpo responde.</p>
              </div>
            </div>
          </div>

          <div class="mfit-panel">
            <div class="mfit-screen">
              <div class="mfit-top">MFIT PERSONAL</div>
              <div class="mfit-body">
                <div class="mfit-item">
                  <div class="mfit-badge">▶</div>
                  <div>
                    <b>Vídeos explicativos</b>
                    <span>Visualize a execução dos exercícios dentro do aplicativo.</span>
                  </div>
                </div>

                <div class="mfit-item">
                  <div class="mfit-badge">📈</div>
                  <div>
                    <b>Evolução do aluno</b>
                    <span>Acompanhe registros, feedbacks e progresso do planejamento.</span>
                  </div>
                </div>

                <div class="mfit-item">
                  <div class="mfit-badge">📷</div>
                  <div>
                    <b>Fotos e comparativos</b>
                    <span>Armazene imagens de evolução para comparação durante a consultoria.</span>
                  </div>
                </div>

                <div class="mfit-item">
                  <div class="mfit-badge">✓</div>
                  <div>
                    <b>Ficha organizada</b>
                    <span>Treinos entregues com clareza, estrutura e acompanhamento profissional.</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="mfit">
      <div class="container">
        <div class="section-head center">
          <div class="eyebrow">Treine pelo MFIT</div>
          <h2>Sua consultoria dentro do <span class="gold">aplicativo</span></h2>
          <p>O MFIT concentra os treinos, vídeos demonstrativos, feedbacks e acompanhamento da evolução em um só lugar.</p>
        </div>

        <div class="grid-4">
          <div class="feature-card">
            <div class="icon">▶</div>
            <h3>Exercícios em vídeo</h3>
            <p>O aluno consegue visualizar como executar os movimentos com mais segurança.</p>
          </div>

          <div class="feature-card">
            <div class="icon">📋</div>
            <h3>Ficha de treino</h3>
            <p>Treinos com séries, repetições, cargas, intervalos e observações importantes.</p>
          </div>

          <div class="feature-card">
            <div class="icon">📷</div>
            <h3>Fotos de evolução</h3>
            <p>Registro visual para comparar progresso e ajustar a estratégia com mais precisão.</p>
          </div>

          <div class="feature-card">
            <div class="icon">💬</div>
            <h3>Feedbacks</h3>
            <p>Acompanhamento para corrigir rota, melhorar execução e manter constância.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="planos">
      <div class="container">
        <div class="section-head center">
          <div class="eyebrow">Consultoria</div>
          <h2>Escolha seu <span class="gold">plano</span></h2>
          <p>Do acompanhamento básico ao suporte completo. Os valores abaixo são editáveis no código.</p>
        </div>

        <div class="plans">
          <div class="plan">
            <h3>Essencial</h3>
            <div class="sub">Comece com direção</div>
            <div class="price"><small>R$</small><strong>100</strong><small>/mês</small></div>
            <p>Ideal para quem precisa de treino personalizado e acompanhamento inicial.</p>
            <ul class="checks">
              <li>Treino personalizado pelo MFIT</li>
              <li>Vídeos demonstrativos</li>
              <li>Ajuste mensal do programa</li>
              <li>Suporte por WhatsApp</li>
            </ul>
            <a class="btn btn-outline" href="https://wa.me/5500000000000" target="_blank">Quero esse plano</a>
          </div>

          <div class="plan featured">
            <div class="tag">Mais popular</div>
            <h3>Evolução</h3>
            <div class="sub">Acelere seus resultados</div>
            <div class="price"><small>R$</small><strong>150</strong><small>/mês</small></div>
            <p>Treino, estratégia e ajustes com melhor equilíbrio entre preço e acompanhamento.</p>
            <ul class="checks">
              <li>Treino personalizado pelo MFIT</li>
              <li>Avaliação inicial por fotos e vídeos</li>
              <li>Ajustes quinzenais</li>
              <li>Feedbacks e acompanhamento</li>
              <li>Comparativo de evolução</li>
            </ul>
            <a class="btn btn-primary" href="https://wa.me/5500000000000" target="_blank">Quero esse plano</a>
          </div>

          <div class="plan">
            <div class="tag tag-red">Vagas limitadas</div>
            <h3>Premium</h3>
            <div class="sub">Performance máxima</div>
            <div class="price"><small>R$</small><strong>250</strong><small>/mês</small></div>
            <p>Para quem quer suporte mais próximo, ajustes frequentes e máxima prioridade.</p>
            <ul class="checks">
              <li>Treino personalizado pelo MFIT</li>
              <li>Acompanhamento completo</li>
              <li>Ajustes semanais</li>
              <li>Suporte prioritário</li>
              <li>Análise de evolução detalhada</li>
              <li>Consultoria presencial em Janaúba/MG</li>
            </ul>
            <a class="btn btn-outline" href="https://wa.me/5500000000000" target="_blank">Quero esse plano</a>
          </div>
        </div>
      </div>
    </section>

    <section id="calculadora">
      <div class="container calculator">
        <div class="section-head center">
          <div class="eyebrow">Ferramenta gratuita</div>
          <h2>Calculadora de <span class="gold">Calorias</span></h2>
          <p>Calcule uma estimativa de TMB e gasto energético diário. Para precisão real, use isso como ponto de partida, não como plano alimentar final.</p>
        </div>

        <div class="calc-card">
          <div class="calc-form">
            <label>Sexo</label>
            <div class="sex-row">
              <button class="sex-btn active" type="button" id="sex-m">Masculino</button>
              <button class="sex-btn" type="button" id="sex-f">Feminino</button>
            </div>

            <div class="field-grid">
              <div class="field">
                <label>Idade</label>
                <input id="idade" type="number" placeholder="25">
              </div>
              <div class="field">
                <label>Peso kg</label>
                <input id="peso" type="number" placeholder="75">
              </div>
              <div class="field">
                <label>Altura cm</label>
                <input id="altura" type="number" placeholder="175">
              </div>
            </div>

            <div class="field" style="margin-bottom:18px;">
              <label>Nível de atividade</label>
              <select id="atividade">
                <option value="1.2">Sedentário — pouco ou nenhum exercício</option>
                <option value="1.375">Levemente ativo — 1 a 3x por semana</option>
                <option value="1.55" selected>Moderadamente ativo — 3 a 5x por semana</option>
                <option value="1.725">Muito ativo — 6 a 7x por semana</option>
                <option value="1.9">Extremamente ativo — treino intenso 2x ao dia</option>
              </select>
            </div>

            <button class="btn btn-primary" style="width:100%;" type="button" onclick="calcularCalorias()">Calcular Gasto Calórico</button>
          </div>

          <div class="calc-results">
            <div>
              <div class="result-number" id="get">—</div>
              <div class="result-label">GET estimado / kcal por dia</div>

              <div class="mini-results">
                <div class="mini">
                  <strong id="tmb">—</strong>
                  <span>TMB kcal/dia</span>
                </div>
                <div class="mini">
                  <strong id="deficit">—</strong>
                  <span>Déficit leve</span>
                </div>
              </div>

              <p style="color:#777; font-size:12px; margin-top:22px;">Estimativa baseada em Mifflin-St Jeor. Ajustes individuais dependem de rotina, adesão, treino e resposta corporal.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="ebooks">
      <div class="container">
        <div class="section-head center">
          <div class="eyebrow">E-books digitais</div>
          <h2>Conhecimento que <span class="gold">transforma</span></h2>
          <p>Protocolos, materiais e produtos digitais para quem quer evoluir com mais clareza.</p>
        </div>

        <div class="ebook-box">
          <div class="icon" style="margin-inline:auto;">🛍</div>
          <h3>Visite nossa loja online</h3>
          <p>Todos os e-books e materiais exclusivos estarão disponíveis na loja digital com pagamento seguro e entrega imediata.</p>
          <a class="btn btn-primary" href="#" target="_blank">Acessar Loja</a>
          <p style="font-size:12px; color:#666; margin-top:16px;">Substitua o “#” pelo link da loja quando estiver pronto.</p>
        </div>
      </div>
    </section>

    <section id="depoimentos">
      <div class="container">
        <div class="section-head center">
          <div class="eyebrow">Resultados</div>
          <h2>Histórias de <span class="gold">transformação</span></h2>
          <p>Use esta seção apenas com depoimentos reais. Os textos abaixo são exemplos editáveis.</p>
        </div>

        <div class="testimonials">
          <div class="testimonial">
            <div class="stars">★★★★★</div>
            <h3>Mais constância nos treinos</h3>
            <p>“Finalmente consegui seguir uma rotina organizada e adaptada para minha vida real.”</p>
            <strong>Aluno Mendes Consultoria</strong>
          </div>

          <div class="testimonial">
            <div class="stars">★★★★★</div>
            <h3>Treino mais claro</h3>
            <p>“Os vídeos e a ficha no aplicativo facilitaram muito a execução dos exercícios.”</p>
            <strong>Aluno Mendes Consultoria</strong>
          </div>

          <div class="testimonial">
            <div class="stars">★★★★★</div>
            <h3>Evolução visível</h3>
            <p>“Com acompanhamento e ajustes, consegui visualizar melhor meu progresso.”</p>
            <strong>Aluno Mendes Consultoria</strong>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-grid">
        <div>
          <a href="#inicio" class="brand" style="margin-bottom:22px;">
            <div class="brand-mark">MC</div>
            <div>
              <div class="brand-name">MENDES CONSULTORIA</div>
              <div class="brand-sub">PERFORMANCE</div>
            </div>
          </a>
          <p>Consultoria fitness online e presencial em Janaúba/MG para quem quer resultado com método, execução e acompanhamento.</p>
        </div>

        <div>
          <h4>Serviços</h4>
          <a href="#planos">Plano Essencial</a>
          <a href="#planos">Plano Evolução</a>
          <a href="#planos">Plano Premium</a>
          <a href="#mfit">Treinos pelo MFIT</a>
        </div>

        <div>
          <h4>Conteúdos</h4>
          <a href="#calculadora">Calculadora</a>
          <a href="#ebooks">E-books</a>
          <a href="#autoridade">Autoridade</a>
        </div>

        <div>
          <h4>Links rápidos</h4>
          <a href="#como-funciona">Como funciona</a>
          <a href="#planos">Planos</a>
          <a href="#depoimentos">Depoimentos</a>
          <a href="https://wa.me/5500000000000" target="_blank">WhatsApp</a>
        </div>
      </div>

      <div class="copyright">
        <span>© 2026 Mendes Consultoria. Todos os direitos reservados.</span>
        <span>Política de Privacidade · Termos de Uso</span>
      </div>
    </div>
  </footer>

  <script>
    let sexo = "M";

    const sexM = document.getElementById("sex-m");
    const sexF = document.getElementById("sex-f");

    sexM.addEventListener("click", function () {
      sexo = "M";
      sexM.classList.add("active");
      sexF.classList.remove("active");
      calcularCalorias();
    });

    sexF.addEventListener("click", function () {
      sexo = "F";
      sexF.classList.add("active");
      sexM.classList.remove("active");
      calcularCalorias();
    });

    function calcularCalorias() {
      const idade = parseFloat(document.getElementById("idade").value);
      const peso = parseFloat(document.getElementById("peso").value);
      const altura = parseFloat(document.getElementById("altura").value);
      const atividade = parseFloat(document.getElementById("atividade").value);

      if (!idade || !peso || !altura || idade <= 0 || peso <= 0 || altura <= 0) {
        document.getElementById("get").textContent = "—";
        document.getElementById("tmb").textContent = "—";
        document.getElementById("deficit").textContent = "—";
        return;
      }

      let tmb;

      if (sexo === "M") {
        tmb = (10 * peso) + (6.25 * altura) - (5 * idade) + 5;
      } else {
        tmb = (10 * peso) + (6.25 * altura) - (5 * idade) - 161;
      }

      const get = tmb * atividade;
      const deficit = get - 400;

      document.getElementById("get").textContent = Math.round(get).toLocaleString("pt-BR");
      document.getElementById("tmb").textContent = Math.round(tmb).toLocaleString("pt-BR");
      document.getElementById("deficit").textContent = Math.round(deficit).toLocaleString("pt-BR");
    }

    ["idade", "peso", "altura", "atividade"].forEach(function(id) {
      document.getElementById(id).addEventListener("input", calcularCalorias);
      document.getElementById(id).addEventListener("change", calcularCalorias);
    });
  </script>
</body>
</html>
