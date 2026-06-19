# ebook-clt
ebook - investimento para clt
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Análise Fundamentalista para Quem Vive de CLT — E-book</title>
<style>
  :root {
    --navy: #0d3b66;
    --navy-deep: #07203a;
    --gold: #d4af37;
    --gold-deep: #a8841f;
    --cream: #f7f5ef;
    --cream-deep: #efebe0;
    --green: #2d6b2d;
    --ink: #1a2332;
    --slate: #4a5a6b;
    --line: #e3ddd0;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    background: var(--cream);
    color: var(--ink);
    line-height: 1.6;
    font-size: 16px;
  }
  h1, h2, h3, h4 {
    font-family: Georgia, 'Times New Roman', serif;
    font-weight: 700;
    color: var(--navy);
    line-height: 1.2;
  }
  .wrap { max-width: 1080px; margin: 0 auto; padding: 0 24px; }
  a { color: inherit; }
  img, svg { display: block; max-width: 100%; }

  /* ===== TOP BAR ===== */
  .topbar {
    background: var(--navy-deep);
    color: #cdd9e5;
    font-size: 13px;
    text-align: center;
    padding: 9px 16px;
    letter-spacing: 0.3px;
  }
  .topbar strong { color: var(--gold); }

  /* ===== NAV ===== */
  nav {
    background: var(--cream);
    border-bottom: 1px solid var(--line);
    position: sticky;
    top: 0;
    z-index: 50;
  }
  .nav-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 16px 24px;
    max-width: 1080px;
    margin: 0 auto;
  }
  .nav-logo {
    font-family: Georgia, serif;
    font-weight: 700;
    font-size: 18px;
    color: var(--navy);
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .nav-logo .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--gold); }
  .nav-cta {
    background: var(--navy);
    color: white;
    padding: 10px 22px;
    border-radius: 4px;
    font-weight: 600;
    font-size: 14px;
    text-decoration: none;
    white-space: nowrap;
  }

  /* ===== HERO ===== */
  .hero {
    background: linear-gradient(155deg, var(--navy) 0%, var(--navy-deep) 70%);
    color: white;
    position: relative;
    overflow: hidden;
    padding: 64px 0 80px;
  }
  .hero::before {
    content: "";
    position: absolute;
    top: -120px; right: -140px;
    width: 420px; height: 420px;
    border-radius: 50%;
    background: rgba(212,175,55,0.08);
  }
  .hero-grid {
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 56px;
    align-items: center;
    position: relative;
    z-index: 2;
  }
  .eyebrow {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: 12px;
    font-weight: 700;
    color: var(--gold);
    margin-bottom: 20px;
  }
  .eyebrow::before { content: "●"; font-size: 8px; }
  .hero h1 {
    font-size: 42px;
    color: white;
    margin-bottom: 20px;
  }
  .hero h1 em { color: var(--gold); font-style: normal; }
  .hero-sub {
    font-size: 17px;
    color: #c9d6e3;
    max-width: 480px;
    margin-bottom: 32px;
  }
  .hero-bullets { list-style: none; margin-bottom: 36px; }
  .hero-bullets li {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    margin-bottom: 12px;
    font-size: 15px;
    color: #dde6ef;
  }
  .hero-bullets li::before {
    content: "✓";
    color: var(--gold);
    font-weight: 800;
    flex-shrink: 0;
    margin-top: 1px;
  }
  .hero-cta-row { display: flex; align-items: center; gap: 18px; flex-wrap: wrap; }
  .btn-primary {
    display: inline-block;
    background: var(--gold);
    color: var(--navy-deep);
    font-weight: 800;
    font-size: 16px;
    padding: 17px 34px;
    border-radius: 5px;
    text-decoration: none;
    box-shadow: 0 10px 30px rgba(212,175,55,0.25);
    transition: transform 0.15s ease;
  }
  .btn-primary:hover { transform: translateY(-2px); }
  .price-hint { font-size: 13px; color: #9fb3c8; }
  .price-hint strong { color: white; font-size: 15px; }

  /* ===== COVER MOCKUP ===== */
  .cover-mock {
    width: 100%;
    max-width: 320px;
    margin: 0 auto;
    aspect-ratio: 210/297;
    background: linear-gradient(160deg, #0d3b66 0%, #0a2a4a 55%, #07203a 100%);
    border-radius: 4px;
    box-shadow: 0 30px 70px rgba(0,0,0,0.45), 0 0 0 1px rgba(255,255,255,0.06);
    position: relative;
    overflow: hidden;
    padding: 13% 11%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    transform: rotate(2deg);
  }
  .cover-mock::before {
    content: "";
    position: absolute;
    top: -40px; right: -40px;
    width: 160px; height: 160px;
    border-radius: 50%;
    background: rgba(212,175,55,0.12);
  }
  .cm-eyebrow {
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-size: 9px;
    color: var(--gold);
    font-weight: 700;
    margin-bottom: 10px;
  }
  .cm-divider { width: 30px; height: 2px; background: var(--gold); margin-bottom: 14px; }
  .cm-title {
    font-family: Georgia, serif;
    font-size: 19px;
    font-weight: 800;
    color: white;
    line-height: 1.2;
    margin-bottom: 10px;
  }
  .cm-title span { color: var(--gold); }
  .cm-sub {
    font-family: Georgia, serif;
    font-style: italic;
    font-size: 10px;
    color: #c9d6e3;
    line-height: 1.4;
  }
  .cm-footer {
    position: absolute;
    bottom: 16px; left: 11%; right: 11%;
    display: flex; justify-content: space-between;
    font-size: 7px; color: #8fa3b8; letter-spacing: 0.5px;
  }

  /* ===== SECTIONS ===== */
  section { padding: 76px 0; }
  .section-head { text-align: center; max-width: 640px; margin: 0 auto 48px; }
  .section-eyebrow {
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: 12px;
    font-weight: 700;
    color: var(--gold-deep);
    margin-bottom: 12px;
  }
  .section-head h2 { font-size: 30px; margin-bottom: 14px; }
  .section-head p { color: var(--slate); font-size: 16px; }

  /* ===== PAIN ===== */
  .pain { background: white; }
  .pain-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
  }
  .pain-card {
    background: var(--cream);
    border-radius: 8px;
    padding: 28px 24px;
    border: 1px solid var(--line);
  }
  .pain-card .icon { font-size: 26px; margin-bottom: 14px; }
  .pain-card h3 { font-size: 17px; margin-bottom: 8px; color: var(--navy); }
  .pain-card p { font-size: 14.5px; color: var(--slate); }

  /* ===== WHAT'S INSIDE ===== */
  .inside { background: var(--cream); }
  .inside-layout {
    display: grid;
    grid-template-columns: 0.85fr 1.15fr;
    gap: 56px;
    align-items: start;
  }
  .chapter-list { list-style: none; }
  .chapter-list li {
    display: flex;
    gap: 16px;
    padding: 16px 0;
    border-bottom: 1px solid var(--line);
  }
  .chapter-list li:first-child { padding-top: 0; }
  .chap-num {
    font-family: Georgia, serif;
    font-weight: 800;
    font-size: 20px;
    color: var(--gold-deep);
    min-width: 30px;
  }
  .chap-text h4 { font-size: 15.5px; color: var(--navy); margin-bottom: 3px; }
  .chap-text p { font-size: 13.5px; color: var(--slate); }

  .indicators-card {
    background: white;
    border-radius: 10px;
    padding: 32px;
    box-shadow: 0 8px 30px rgba(13,59,102,0.08);
    border: 1px solid var(--line);
  }
  .indicators-card h3 {
    font-size: 18px;
    margin-bottom: 18px;
    padding-bottom: 14px;
    border-bottom: 2px solid var(--gold);
  }
  .indicator-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 24px;
  }
  .tag {
    background: var(--cream);
    border: 1px solid var(--line);
    color: var(--navy);
    font-size: 12.5px;
    font-weight: 600;
    padding: 7px 12px;
    border-radius: 20px;
    font-family: 'Courier New', monospace;
  }
  .bonus-box {
    background: var(--navy);
    color: white;
    border-radius: 8px;
    padding: 20px;
    margin-top: 8px;
  }
  .bonus-box .bonus-label {
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-size: 11px;
    color: var(--gold);
    font-weight: 700;
    margin-bottom: 8px;
  }
  .bonus-box p { font-size: 14px; color: #dde6ef; }
  .bonus-box strong { color: white; }

  /* ===== FOR WHO ===== */
  .forwho { background: white; }
  .forwho-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
  }
  .forwho-card {
    border-radius: 10px;
    padding: 30px;
  }
  .forwho-card.yes { background: #f0f7f0; border: 1px solid #cfe4cf; }
  .forwho-card.no { background: #fdf3ee; border: 1px solid #f0d8cd; }
  .forwho-card h3 { font-size: 17px; margin-bottom: 16px; }
  .forwho-card.yes h3 { color: var(--green); }
  .forwho-card.no h3 { color: #a8472f; }
  .forwho-card ul { list-style: none; }
  .forwho-card li {
    display: flex;
    gap: 10px;
    margin-bottom: 12px;
    font-size: 14.5px;
    color: var(--ink);
  }
  .forwho-card.yes li::before { content: "✓"; color: var(--green); font-weight: 800; }
  .forwho-card.no li::before { content: "✕"; color: #a8472f; font-weight: 800; }

  /* ===== AUTHOR / TRUST ===== */
  .trust { background: var(--cream); }
  .trust-grid {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 28px;
    align-items: center;
    background: white;
    border-radius: 12px;
    padding: 36px;
    border: 1px solid var(--line);
  }
  .trust-avatar {
    width: 84px; height: 84px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--navy), var(--navy-deep));
    display: flex; align-items: center; justify-content: center;
    color: var(--gold);
    font-family: Georgia, serif;
    font-weight: 800;
    font-size: 30px;
  }
  .trust-text h3 { font-size: 17px; margin-bottom: 6px; }
  .trust-text p { font-size: 14.5px; color: var(--slate); }

  /* ===== OFFER ===== */
  .offer {
    background: linear-gradient(155deg, var(--navy) 0%, var(--navy-deep) 100%);
    color: white;
    text-align: center;
  }
  .offer-card {
    background: white;
    color: var(--ink);
    max-width: 460px;
    margin: 0 auto;
    border-radius: 14px;
    padding: 40px 36px;
    box-shadow: 0 30px 70px rgba(0,0,0,0.3);
  }
  .offer-tag {
    background: var(--gold);
    color: var(--navy-deep);
    display: inline-block;
    font-size: 12px;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 1px;
    padding: 6px 14px;
    border-radius: 20px;
    margin-bottom: 18px;
  }
  .offer-card h3 { font-size: 22px; margin-bottom: 6px; }
  .offer-card .offer-desc { font-size: 14px; color: var(--slate); margin-bottom: 24px; }
  .offer-items { list-style: none; text-align: left; margin-bottom: 28px; }
  .offer-items li {
    display: flex;
    gap: 10px;
    padding: 10px 0;
    border-bottom: 1px dashed var(--line);
    font-size: 14.5px;
  }
  .offer-items li::before { content: "✓"; color: var(--green); font-weight: 800; }
  .price-row {
    display: flex;
    align-items: baseline;
    justify-content: center;
    gap: 12px;
    margin-bottom: 4px;
  }
  .price-old { font-size: 16px; color: #aab5c0; text-decoration: line-through; }
  .price-new { font-size: 40px; font-weight: 800; color: var(--navy); font-family: Georgia, serif; }
  .price-cents { font-size: 18px; color: var(--navy); }
  .price-installment { font-size: 13px; color: var(--slate); margin-bottom: 22px; }
  .offer-card .btn-primary { width: 100%; text-align: center; font-size: 17px; padding: 18px; }
  .guarantee-line {
    margin-top: 18px;
    font-size: 12.5px;
    color: var(--slate);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 6px;
  }

  /* ===== FAQ ===== */
  .faq { background: white; }
  .faq-item {
    border-bottom: 1px solid var(--line);
    padding: 22px 0;
    max-width: 760px;
    margin: 0 auto;
  }
  .faq-item h4 { font-size: 16px; color: var(--navy); margin-bottom: 8px; }
  .faq-item p { font-size: 14.5px; color: var(--slate); }

  /* ===== FOOTER ===== */
  footer {
    background: var(--navy-deep);
    color: #8fa3b8;
    padding: 40px 0 28px;
    font-size: 13px;
  }
  .footer-grid { display: flex; justify-content: space-between; align-items: flex-start; gap: 24px; flex-wrap: wrap; }
  footer .nav-logo { color: white; margin-bottom: 10px; }
  .footer-disclaimer { max-width: 480px; line-height: 1.7; font-size: 12px; color: #6e8198; }

  /* ===== STICKY MOBILE CTA ===== */
  .sticky-cta {
    display: none;
  }

  /* ===== RESPONSIVE ===== */
  @media (max-width: 860px) {
    .hero-grid { grid-template-columns: 1fr; gap: 40px; }
    .hero h1 { font-size: 32px; }
    .cover-mock { max-width: 240px; }
    .pain-grid { grid-template-columns: 1fr; }
    .inside-layout { grid-template-columns: 1fr; }
    .forwho-grid { grid-template-columns: 1fr; }
    .trust-grid { grid-template-columns: 1fr; text-align: center; justify-items: center; }
    section { padding: 56px 0; }
    .nav-cta { padding: 9px 16px; font-size: 13px; }
    body { padding-bottom: 70px; }
    .sticky-cta {
      display: flex;
      position: fixed;
      bottom: 0; left: 0; right: 0;
      background: var(--navy-deep);
      padding: 12px 16px;
      z-index: 100;
      box-shadow: 0 -6px 20px rgba(0,0,0,0.2);
      align-items: center;
      justify-content: space-between;
      gap: 12px;
    }
    .sticky-cta .price-new { font-size: 18px; color: white; }
    .sticky-cta .btn-primary { padding: 12px 20px; font-size: 14px; }
  }
</style>
</head>
<body>

<div class="topbar">📘 Material 100% digital — acesso imediato após a compra · <strong>Pagamento seguro via Kiwify</strong></div>

<nav>
  <div class="nav-inner">
    <div class="nav-logo"><span class="dot"></span>Fundamentos CLT</div>
    <a href="#oferta" class="nav-cta">Quero o e-book</a>
  </div>
</nav>

<!-- ===== HERO ===== -->
<header class="hero">
  <div class="wrap hero-grid">
    <div>
      <div class="eyebrow">Guia prático · ações e FIIs</div>
      <h1>Pare de investir no <em>achismo</em>. Aprenda a ler os números antes de comprar.</h1>
      <p class="hero-sub">Um guia direto ao ponto para quem trabalha de carteira assinada, tem pouco tempo e quer aprender a analisar ações e Fundos Imobiliários com os mesmos critérios que profissionais usam — sem economês e sem enrolação.</p>
      <ul class="hero-bullets">
        <li>Os 7 indicadores essenciais para avaliar qualquer ação</li>
        <li>Os 5 indicadores que realmente importam em FIIs</li>
        <li>Roteiro de 10 minutos para ler um balanço trimestral</li>
        <li>Planilha de análise em Excel inclusa, pronta para usar</li>
      </ul>
      <div class="hero-cta-row">
        <a href="#oferta" class="btn-primary">Quero aprender a analisar →</a>
        <span class="price-hint">A partir de <strong>R$ 27,90</strong> · acesso vitalício</span>
      </div>
    </div>
    <div>
      <div class="cover-mock">
        <div class="cm-eyebrow">Guia prático para investidores CLT</div>
        <div class="cm-divider"></div>
        <div class="cm-title">Análise Fundamentalista<br>para Quem Vive de <span>CLT</span></div>
        <div class="cm-sub">Como avaliar ações e Fundos Imobiliários com os mesmos números que os profissionais usam.</div>
        <div class="cm-footer"><span>EDIÇÃO 2026</span><span>GUIA DO INVESTIDOR CLT</span></div>
      </div>
    </div>
  </div>
</header>

<!-- ===== PAIN ===== -->
<section class="pain">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">O problema</div>
      <h2>Se você se reconhece em algum desses pontos, este guia foi escrito para você</h2>
      <p>A maioria de quem começa a investir não tem falta de dinheiro. Tem falta de critério.</p>
    </div>
    <div class="pain-grid">
      <div class="pain-card">
        <div class="icon">🤷</div>
        <h3>Compra por indicação</h3>
        <p>Você já investiu em alguma ação ou FII só porque "ouviu falar" ou viu um print de carteira nas redes sociais — sem entender o motivo real.</p>
      </div>
      <div class="pain-card">
        <div class="icon">📊</div>
        <h3>Números que não fazem sentido</h3>
        <p>P/L, P/VP, ROE, DY... você já viu essas siglas em algum lugar, mas nunca soube exatamente o que elas significam ou como usar.</p>
      </div>
      <div class="pain-card">
        <div class="icon">⏰</div>
        <h3>Pouco tempo no dia a dia</h3>
        <p>Entre o trabalho CLT e a vida pessoal, sobra pouco tempo para estudar o mercado financeiro — e os materiais que você encontra são longos demais ou complicados demais.</p>
      </div>
    </div>
  </div>
</section>

<!-- ===== WHAT'S INSIDE ===== -->
<section class="inside">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">O que você vai aprender</div>
      <h2>Um guia enxuto, sem enrolação, do início ao fim</h2>
      <p>9 capítulos organizados em sequência lógica — da mentalidade certa até a montagem da sua carteira.</p>
    </div>
    <div class="inside-layout">
      <ul class="chapter-list">
        <li><span class="chap-num">01</span><div class="chap-text"><h4>Por que o CLT precisa entender de fundamentos</h4><p>A vantagem que você já tem e não sabia</p></div></li>
        <li><span class="chap-num">02</span><div class="chap-text"><h4>A mentalidade do investidor com salário fixo</h4><p>Aportes recorrentes e reserva de emergência</p></div></li>
        <li><span class="chap-num">03</span><div class="chap-text"><h4>O que é análise fundamentalista</h4><p>Conceito, fontes de dados e onde pesquisar de graça</p></div></li>
        <li><span class="chap-num">04</span><div class="chap-text"><h4>Indicadores essenciais de ações</h4><p>P/L, P/VP, ROE, dívida, DY, margem e crescimento</p></div></li>
        <li><span class="chap-num">05</span><div class="chap-text"><h4>Indicadores essenciais de FIIs</h4><p>P/VP, DY, vacância, liquidez e tipos de fundo</p></div></li>
        <li><span class="chap-num">06</span><div class="chap-text"><h4>Como ler um balanço em 10 minutos</h4><p>Roteiro prático, minuto a minuto</p></div></li>
        <li><span class="chap-num">07</span><div class="chap-text"><h4>Montando sua carteira com aportes mensais</h4><p>Rotina compatível com quem trabalha 8h por dia</p></div></li>
        <li><span class="chap-num">08</span><div class="chap-text"><h4>Erros comuns de quem está começando</h4><p>As 7 armadilhas mais caras para iniciantes</p></div></li>
        <li><span class="chap-num">09</span><div class="chap-text"><h4>Glossário rápido</h4><p>Todos os termos do guia, em uma página de consulta</p></div></li>
      </ul>

      <div class="indicators-card">
        <h3>Indicadores que você vai dominar</h3>
        <div class="indicator-tags">
          <span class="tag">P/L</span>
          <span class="tag">P/VP</span>
          <span class="tag">ROE</span>
          <span class="tag">Dív. Líq./EBITDA</span>
          <span class="tag">Dividend Yield</span>
          <span class="tag">Margem Líquida</span>
          <span class="tag">CAGR</span>
          <span class="tag">Vacância</span>
          <span class="tag">Liquidez diária</span>
        </div>
        <div class="bonus-box">
          <div class="bonus-label">🎁 Bônus incluso</div>
          <p><strong>Planilha de Análise Fundamentalista</strong> em Excel — digite os dados de uma ação ou FII e ela calcula automaticamente todos os indicadores do guia, sinalizando pontos de atenção.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== FOR WHO ===== -->
<section class="forwho">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">Para quem é</div>
      <h2>Esse guia é para você?</h2>
    </div>
    <div class="forwho-grid">
      <div class="forwho-card yes">
        <h3>✓ Este e-book é para você se...</h3>
        <ul>
          <li>Você trabalha de carteira assinada e quer começar a investir com mais critério</li>
          <li>Já investe, mas escolhe ativos sem saber explicar o motivo</li>
          <li>Tem pouco tempo e quer um material direto, sem enrolação</li>
          <li>Quer entender os números antes de confiar em indicação de terceiros</li>
          <li>Pensa em construir patrimônio no longo prazo, com aportes mensais</li>
        </ul>
      </div>
      <div class="forwho-card no">
        <h3>✕ Este e-book não é para você se...</h3>
        <ul>
          <li>Você busca fórmula de "ficar rico rápido" ou day trade</li>
          <li>Já é analista certificado e domina os indicadores fundamentalistas</li>
          <li>Procura recomendações específicas de compra ou venda</li>
          <li>Não está disposto a dedicar nem 1 hora por mês à própria carteira</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ===== TRUST ===== -->
<section class="trust">
  <div class="wrap">
    <div class="trust-grid">
      <div class="trust-avatar">D</div>
      <div class="trust-text">
        <h3>Escrito por quem também é CLT</h3>
        <p>Este guia foi criado para quem precisa equilibrar trabalho, rotina e o desejo de investir melhor — com linguagem direta, exemplos práticos e zero jargão desnecessário. O objetivo não é te transformar em analista profissional, mas te dar autonomia para tomar decisões mais conscientes com o seu próprio dinheiro.</p>
      </div>
    </div>
  </div>
</section>

<!-- ===== OFFER ===== -->
<section class="offer" id="oferta">
  <div class="wrap">
    <div class="section-head" style="margin-bottom: 36px;">
      <div class="section-eyebrow" style="color: var(--gold);">Oferta</div>
      <h2 style="color: white;">Comece a investir com critério ainda hoje</h2>
    </div>
    <div class="offer-card">
      <span class="offer-tag">Acesso imediato</span>
      <h3>E-book + Planilha Bônus</h3>
      <p class="offer-desc">Análise Fundamentalista para Quem Vive de CLT</p>
      <ul class="offer-items">
        <li>E-book completo em PDF (9 capítulos)</li>
        <li>Planilha de análise fundamentalista em Excel</li>
        <li>Glossário rápido de consulta</li>
        <li>Acesso vitalício e atualizações gratuitas</li>
        <li>Compatível com celular, tablet e computador</li>
      </ul>
      <div class="price-row">
        <span class="price-old">R$ 47,90</span>
        <span class="price-new">R$ 27<span class="price-cents">,90</span></span>
      </div>
      <p class="price-installment">ou em até 3x no cartão · pagamento via Kiwify</p>
      <a href="#" class="btn-primary">Comprar agora →</a>
      <div class="guarantee-line">🔒 Compra 100% segura · 🛡️ Garantia de 7 dias</div>
    </div>
  </div>
</section>

<!-- ===== FAQ ===== -->
<section class="faq">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">Dúvidas</div>
      <h2>Perguntas frequentes</h2>
    </div>
    <div class="faq-item">
      <h4>Preciso ter experiência prévia em investimentos?</h4>
      <p>Não. O guia foi escrito justamente para quem está começando ou já investe sem critério claro. A linguagem é direta e evita jargão desnecessário.</p>
    </div>
    <div class="faq-item">
      <h4>O e-book indica quais ações ou FIIs comprar?</h4>
      <p>Não. O material é educacional e ensina o método de análise — quais indicadores olhar e como interpretá-los. A decisão de quais ativos comprar é sempre sua, com base na sua própria análise e perfil de risco.</p>
    </div>
    <div class="faq-item">
      <h4>Como recebo o material após a compra?</h4>
      <p>O acesso é liberado imediatamente após a confirmação do pagamento, direto na plataforma da Kiwify. Você recebe o link para baixar o PDF e a planilha em Excel.</p>
    </div>
    <div class="faq-item">
      <h4>A planilha funciona em celular?</h4>
      <p>A planilha foi feita em Excel e funciona melhor em computador. Ela também é compatível com Google Sheets, caso você prefira usar pelo celular ou tablet.</p>
    </div>
    <div class="faq-item">
      <h4>E se eu não gostar do material?</h4>
      <p>Você tem 7 dias de garantia. Se sentir que o conteúdo não é para você, basta solicitar o reembolso dentro desse prazo, sem burocracia.</p>
    </div>
  </div>
</section>

<footer>
  <div class="wrap footer-grid">
    <div>
      <div class="nav-logo"><span class="dot"></span>Fundamentos CLT</div>
      <p>Material 100% digital e educacional.</p>
    </div>
    <p class="footer-disclaimer">Este produto tem finalidade exclusivamente educacional e não constitui recomendação de investimento, oferta ou solicitação de compra ou venda de qualquer ativo financeiro. Investimentos em renda variável envolvem riscos, incluindo a possibilidade de perda do capital investido. Consulte um profissional certificado antes de tomar decisões de investimento.</p>
  </div>
</footer>

<div class="sticky-cta">
  <span class="price-new">R$ 27,90</span>
  <a href="#oferta" class="btn-primary">Comprar agora</a>
</div>

</body>
</html>
