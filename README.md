<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AquaMais × V4 Company — Estratégia 1.000 Cotas/Mês</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500;600&family=Bebas+Neue&display=swap" rel="stylesheet">
<style>
  :root {
    --ocean: #0a3d62;
    --wave: #1e88e5;
    --aqua: #00c9d4;
    --sand: #f5e6c8;
    --coral: #ff6b35;
    --gold: #f0a500;
    --dark: #050e1a;
    --card-bg: rgba(255,255,255,0.04);
    --border: rgba(0,201,212,0.2);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--dark);
    color: #e8f4f8;
    overflow-x: hidden;
  }

  /* ─── HERO ─── */
  .hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 60px 24px;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 50% 120%, #0a3d6280 0%, transparent 70%),
      radial-gradient(ellipse 60% 40% at 80% -10%, #00c9d420 0%, transparent 60%),
      radial-gradient(ellipse 50% 30% at 10% 20%, #1e88e515 0%, transparent 50%);
    pointer-events: none;
  }

  .wave-bg {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 200px;
    background: linear-gradient(180deg, transparent, #0a3d6240);
    mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 120'%3E%3Cpath d='M0,60 C300,120 600,0 900,60 C1050,90 1150,40 1200,60 L1200,120 L0,120 Z' fill='%23000'/%3E%3C/svg%3E");
    mask-size: cover;
    opacity: 0.4;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(0,201,212,0.12);
    border: 1px solid var(--aqua);
    border-radius: 100px;
    padding: 6px 16px;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--aqua);
    margin-bottom: 32px;
    animation: fadeUp 0.8s ease both;
  }

  .badge span { width: 6px; height: 6px; background: var(--aqua); border-radius: 50%; animation: pulse 1.5s infinite; }

  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.4;transform:scale(1.5)} }

  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(42px, 7vw, 90px);
    font-weight: 900;
    line-height: 1;
    margin-bottom: 12px;
    animation: fadeUp 0.8s 0.1s ease both;
  }

  h1 .blue { color: var(--aqua); }
  h1 .coral { color: var(--coral); }

  .hero-sub {
    font-size: clamp(14px, 2vw, 20px);
    font-weight: 300;
    color: #a0c4d8;
    max-width: 600px;
    margin-bottom: 48px;
    line-height: 1.6;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .hero-metrics {
    display: flex;
    gap: 32px;
    flex-wrap: wrap;
    justify-content: center;
    animation: fadeUp 0.8s 0.3s ease both;
  }

  .metric-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px 32px;
    text-align: center;
    backdrop-filter: blur(10px);
  }

  .metric-card .num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 52px;
    color: var(--aqua);
    line-height: 1;
  }

  .metric-card .label { font-size: 12px; color: #7fb3c8; text-transform: uppercase; letter-spacing: 1.5px; margin-top: 4px; }

  /* ─── SECTIONS ─── */
  section { padding: 80px 24px; max-width: 1100px; margin: 0 auto; }

  .section-tag {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--aqua);
    margin-bottom: 12px;
  }

  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(28px, 4vw, 48px);
    font-weight: 700;
    margin-bottom: 16px;
    line-height: 1.1;
  }

  h3 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 12px;
  }

  .lead { font-size: 17px; color: #a0c4d8; line-height: 1.7; margin-bottom: 48px; }

  /* ─── DIVIDER ─── */
  .divider {
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--aqua), transparent);
    margin: 0 auto 80px;
    opacity: 0.3;
  }

  /* ─── GRID ─── */
  .grid-2 { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; margin-bottom: 48px; }
  .grid-3 { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 20px; margin-bottom: 48px; }
  .grid-4 { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; margin-bottom: 48px; }

  /* ─── CARDS ─── */
  .card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 28px;
    transition: transform 0.3s, border-color 0.3s;
  }

  .card:hover { transform: translateY(-4px); border-color: var(--aqua); }

  .card-icon {
    font-size: 32px;
    margin-bottom: 16px;
  }

  .card h3 { font-size: 18px; margin-bottom: 8px; }
  .card p { font-size: 14px; color: #7fb3c8; line-height: 1.6; }

  .card.highlight { border-color: var(--coral); background: rgba(255,107,53,0.06); }
  .card.gold { border-color: var(--gold); background: rgba(240,165,0,0.06); }

  /* ─── SWOT ─── */
  .swot-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 2px; border-radius: 20px; overflow: hidden; margin-bottom: 48px; }

  .swot-cell {
    padding: 32px;
    position: relative;
  }

  .swot-cell.s { background: rgba(0,201,212,0.1); }
  .swot-cell.w { background: rgba(255,107,53,0.1); }
  .swot-cell.o { background: rgba(30,136,229,0.1); }
  .swot-cell.t { background: rgba(240,165,0,0.1); }

  .swot-label {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 48px;
    opacity: 0.15;
    position: absolute;
    top: 12px;
    right: 20px;
  }

  .swot-title {
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 16px;
  }

  .swot-cell.s .swot-title { color: var(--aqua); }
  .swot-cell.w .swot-title { color: var(--coral); }
  .swot-cell.o .swot-title { color: var(--wave); }
  .swot-cell.t .swot-title { color: var(--gold); }

  .swot-list { list-style: none; }
  .swot-list li { font-size: 13.5px; padding: 5px 0; color: #c8dde8; border-bottom: 1px solid rgba(255,255,255,0.05); }
  .swot-list li::before { content: '→ '; opacity: 0.5; }

  /* ─── FUNNEL ─── */
  .funnel { margin-bottom: 48px; }
  .funnel-step {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 12px;
    position: relative;
  }

  .funnel-step::after {
    content: '';
    position: absolute;
    left: 24px;
    top: 52px;
    width: 2px;
    height: 12px;
    background: var(--border);
  }

  .funnel-step:last-child::after { display: none; }

  .funnel-num {
    width: 48px;
    height: 48px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    flex-shrink: 0;
  }

  .funnel-body { flex: 1; background: var(--card-bg); border: 1px solid var(--border); border-radius: 14px; padding: 18px 22px; }
  .funnel-body .title { font-weight: 600; font-size: 15px; margin-bottom: 4px; }
  .funnel-body .desc { font-size: 13px; color: #7fb3c8; }
  .funnel-kpi { text-align: right; flex-shrink: 0; }
  .funnel-kpi .kpi-num { font-family: 'Bebas Neue', sans-serif; font-size: 28px; color: var(--aqua); }
  .funnel-kpi .kpi-label { font-size: 10px; color: #5a8a9f; text-transform: uppercase; letter-spacing: 1px; }

  /* ─── PLANS ─── */
  .plan-block {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    margin-bottom: 24px;
  }

  .plan-header {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 22px 28px;
    border-bottom: 1px solid var(--border);
  }

  .plan-emoji { font-size: 28px; }
  .plan-header h3 { font-size: 20px; margin: 0; }
  .plan-header .plan-tag {
    margin-left: auto;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    padding: 4px 12px;
    border-radius: 100px;
  }

  .tag-hot { background: rgba(255,107,53,0.2); color: var(--coral); border: 1px solid var(--coral); }
  .tag-viral { background: rgba(0,201,212,0.2); color: var(--aqua); border: 1px solid var(--aqua); }
  .tag-scale { background: rgba(240,165,0,0.2); color: var(--gold); border: 1px solid var(--gold); }

  .plan-body { padding: 28px; }
  .plan-body p { font-size: 14px; color: #a0c4d8; line-height: 1.7; margin-bottom: 16px; }

  .action-list { list-style: none; }
  .action-list li {
    display: flex;
    gap: 12px;
    padding: 10px 0;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    font-size: 14px;
    color: #c8dde8;
    line-height: 1.5;
  }

  .action-list li .check { color: var(--aqua); font-size: 16px; flex-shrink: 0; }

  /* ─── KPI TABLE ─── */
  .kpi-table { width: 100%; border-collapse: collapse; margin-bottom: 48px; font-size: 14px; }
  .kpi-table th { text-align: left; padding: 12px 16px; background: rgba(0,201,212,0.1); color: var(--aqua); font-weight: 600; font-size: 12px; letter-spacing: 1px; text-transform: uppercase; }
  .kpi-table td { padding: 14px 16px; border-bottom: 1px solid rgba(255,255,255,0.05); color: #c8dde8; }
  .kpi-table tr:hover td { background: rgba(255,255,255,0.03); }
  .kpi-table .num { font-family: 'Bebas Neue', sans-serif; font-size: 20px; color: var(--aqua); }
  .kpi-table .coral { color: var(--coral); }
  .kpi-table .gold { color: var(--gold); }

  /* ─── TIMELINE ─── */
  .timeline { position: relative; padding-left: 40px; }
  .timeline::before { content: ''; position: absolute; left: 12px; top: 0; bottom: 0; width: 2px; background: linear-gradient(180deg, var(--aqua), var(--coral)); }

  .timeline-item { position: relative; margin-bottom: 32px; }
  .timeline-dot {
    position: absolute;
    left: -34px;
    top: 4px;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    border: 2px solid var(--aqua);
    background: var(--dark);
  }

  .timeline-week { font-size: 11px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--aqua); margin-bottom: 6px; }
  .timeline-title { font-weight: 600; font-size: 16px; margin-bottom: 4px; }
  .timeline-desc { font-size: 13px; color: #7fb3c8; line-height: 1.6; }

  /* ─── PIX REFERRAL ─── */
  .referral-box {
    background: linear-gradient(135deg, rgba(0,201,212,0.08), rgba(30,136,229,0.08));
    border: 1px solid var(--aqua);
    border-radius: 20px;
    padding: 40px;
    margin-bottom: 48px;
    position: relative;
    overflow: hidden;
  }

  .referral-box::before {
    content: '💰';
    position: absolute;
    font-size: 120px;
    right: -10px;
    bottom: -20px;
    opacity: 0.08;
  }

  .referral-tiers { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 16px; margin-top: 24px; }

  .tier {
    background: rgba(255,255,255,0.05);
    border-radius: 14px;
    padding: 20px;
    text-align: center;
  }

  .tier .tier-val { font-family: 'Bebas Neue', sans-serif; font-size: 36px; color: var(--gold); }
  .tier .tier-name { font-size: 12px; color: #7fb3c8; text-transform: uppercase; letter-spacing: 1px; margin-top: 4px; }
  .tier .tier-cond { font-size: 11px; color: #5a8a9f; margin-top: 6px; }

  /* ─── SCRIPTS ─── */
  .script-box {
    background: rgba(255,255,255,0.03);
    border-left: 3px solid var(--aqua);
    border-radius: 0 12px 12px 0;
    padding: 20px 24px;
    margin-bottom: 20px;
    font-size: 14px;
    color: #c8dde8;
    line-height: 1.7;
    font-style: italic;
  }

  .script-label { font-style: normal; font-size: 11px; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--aqua); margin-bottom: 8px; }

  /* ─── FOOTER ─── */
  footer {
    background: rgba(255,255,255,0.02);
    border-top: 1px solid var(--border);
    text-align: center;
    padding: 40px 24px;
    font-size: 13px;
    color: #4a7a90;
  }

  footer strong { color: var(--aqua); }

  /* ─── ANIM ─── */
  @keyframes fadeUp { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }

  @media(max-width:600px) {
    .swot-grid { grid-template-columns: 1fr; }
    .hero-metrics { flex-direction: column; align-items: center; }
    .funnel-kpi { display: none; }
  }
</style>
</head>
<body>

<!-- ═══════════════════════════════════════ HERO -->
<div class="hero">
  <div class="wave-bg"></div>
  <div class="badge"><span></span> V4 Company × AquaMais — Confidencial</div>
  <h1>
    <span class="blue">1.000 Cotas</span><br>
    Por <span class="coral">Mês.</span>
  </h1>
  <p class="hero-sub">
    Análise profunda + máquina de vendas completa para o parque aquático mais ambicioso de Minas Gerais — com início de operação em 48 horas.
  </p>
  <div class="hero-metrics">
    <div class="metric-card">
      <div class="num">200k</div>
      <div class="label">m² de terreno</div>
    </div>
    <div class="metric-card">
      <div class="num">118k</div>
      <div class="label">Seguidores Instagram</div>
    </div>
    <div class="metric-card">
      <div class="num">2026</div>
      <div class="label">Inauguração prevista</div>
    </div>
    <div class="metric-card">
      <div class="num">30min</div>
      <div class="label">Distância de BH</div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════ ANÁLISE -->
<section>
  <div class="section-tag">01 — Inteligência de Mercado</div>
  <h2>Análise Profunda: AquaMais Parque</h2>
  <p class="lead">
    O AquaMais é um empreendimento em construção em Betim, MG, posicionado como o maior parque aquático de Minas Gerais. Seu diferencial é o conceito "Copacabana em Minas" — ondas artificiais, areia branca, coqueiros e cenário tropical na Região Metropolitana de BH. O produto comercializado hoje são <strong>cotas Platinum VIP</strong> de sócio-fundador, com benefícios exclusivos e preço de early adopter.
  </p>

  <div class="grid-2">
    <div class="card">
      <div class="card-icon">🏗️</div>
      <h3>O Empreendimento</h3>
      <p>200.000 m² perto da BR-262. Inauguração prevista: fim de 2026. Razão social: Premier Conceitos e Entretenimentos Ltda. Sócio-fundador e gestor comercial: <strong>Gilmar Nardy Braga Jr.</strong> CNPJ: 57.073.908/0001-42 (fundada ago/2024).</p>
    </div>
    <div class="card">
      <div class="card-icon">🎯</div>
      <h3>O Produto Atual</h3>
      <p>Cota Platinum VIP — título de sócio-fundador com acesso VIP, área exclusiva, vantagens especiais. A entrada promocional tem sido ofertada por <strong>R$ 10 na primeira parcela</strong>. Programa de indicação já existe: quem indica ganha vaga extra na cota.</p>
    </div>
    <div class="card">
      <div class="card-icon">📱</div>
      <h3>Presença Digital</h3>
      <p>@aquamaisoficial: <strong>118K seguidores</strong>. @aquamais.betim: <strong>47K seguidores</strong> (canal de vendas). @aquamaisvendasoficial também ativo. Campanha Google Ads rodando (fonte da URL fornecida). Total de 200+ profissionais já mobilizados antes da V4.</p>
    </div>
    <div class="card highlight">
      <div class="card-icon">⚡</div>
      <h3>Janela Estratégica</h3>
      <p>O parque ainda não inaugurou — isso é um <strong>superpoder comercial</strong>. Quem compra agora é fundador, paga menos e tem benefícios que nunca mais existirão. Essa escassez genuína é o motor de urgência mais poderoso do processo de vendas.</p>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ SWOT -->
<section>
  <div class="section-tag">02 — Diagnóstico</div>
  <h2>Análise SWOT para o CEO & Diretor Comercial</h2>
  <p class="lead">O que a V4 precisa saber antes de ligar a máquina.</p>

  <div class="swot-grid">
    <div class="swot-cell s">
      <div class="swot-label">S</div>
      <div class="swot-title">Forças</div>
      <ul class="swot-list">
        <li>Conceito único: "Copacabana em Minas" — apelo emocional fortíssimo</li>
        <li>200.000 m² — maior escala do estado (tamanho impressiona)</li>
        <li>Já tem audiência digital real (118K + 47K seguidores)</li>
        <li>Preço de entrada baixíssimo (R$10 primeira parcela — zero barreira)</li>
        <li>Google Ads já rodando (tráfego pago ativo)</li>
        <li>Programa de indicação já existente — base para escalar</li>
        <li>Localização estratégica: 30min de BH + BR-262</li>
      </ul>
    </div>
    <div class="swot-cell w">
      <div class="swot-label">W</div>
      <div class="swot-title">Fraquezas</div>
      <ul class="swot-list">
        <li>Parque ainda não inaugurado — compra baseada em promessa</li>
        <li>Sem processo de vendas estruturado (V4 começa do zero)</li>
        <li>Risco de percepção de "golpe" por parte do público cético</li>
        <li>Falta de prova social tangível (sem clientes usando o clube)</li>
        <li>Preço da cota sobe conforme mais cotas são vendidas (precisa virar argumento)</li>
        <li>Sem CRM estruturado (dados de leads provavelmente dispersos)</li>
      </ul>
    </div>
    <div class="swot-cell o">
      <div class="swot-label">O</div>
      <div class="swot-title">Oportunidades</div>
      <ul class="swot-list">
        <li>RMGBH: ~6 milhões de pessoas sem opção de praia acessível</li>
        <li>Classe C-B2 ávida por lazer familiar de qualidade</li>
        <li>Pagamento PIX por indicação = exército de vendedores sem CLT</li>
        <li>Acesso a clubes parceiros da região: benefício imediato concreto</li>
        <li>Lives no Instagram do cliente = alcance orgânico massivo gratuito</li>
        <li>Descontos progressivos criam gamificação de grupo na venda</li>
        <li>Mercado de cotas de lazer em expansão no Brasil pós-pandemia</li>
      </ul>
    </div>
    <div class="swot-cell t">
      <div class="swot-label">T</div>
      <div class="swot-title">Ameaças</div>
      <ul class="swot-list">
        <li>Concorrente direto: Aquabeat (São José da Lapa, já inaugurado)</li>
        <li>Desconfiança do consumidor com pré-vendas de lazer (casos históricos)</li>
        <li>Prazo de entrega 2026 — pode gerar churn se atrasar</li>
        <li>Custo de tráfego pago pode escalar demais sem otimização</li>
        <li>Regulação de programas de indicação com pagamento em dinheiro</li>
      </ul>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ FUNIL -->
<section>
  <div class="section-tag">03 — Arquitetura do Processo</div>
  <h2>O Funil de 1.000 Vendas/Mês</h2>
  <p class="lead">
    Para 1.000 vendas/mês, com taxa de conversão conservadora de 3% do fundo de funil, precisamos de <strong>~33.000 leads qualificados</strong> por mês. Os números abaixo são o blueprint da operação.
  </p>

  <div class="funnel">
    <div class="funnel-step">
      <div class="funnel-num" style="background:rgba(0,201,212,0.2);color:var(--aqua);border:2px solid var(--aqua)">1</div>
      <div class="funnel-body">
        <div class="title">🌊 ATRAÇÃO — Tráfego Pago + Orgânico + Indicação</div>
        <div class="desc">Meta Ads, Google Ads, Lives no Instagram, conteúdo viral, programa de afiliados. Meta: alcançar 150.000+ pessoas por mês.</div>
      </div>
      <div class="funnel-kpi">
        <div class="kpi-num">150k</div>
        <div class="kpi-label">Alcance/mês</div>
      </div>
    </div>

    <div class="funnel-step">
      <div class="funnel-num" style="background:rgba(30,136,229,0.2);color:var(--wave);border:2px solid var(--wave)">2</div>
      <div class="funnel-body">
        <div class="title">🎯 CAPTURA — Lead Qualificado</div>
        <div class="desc">Landing page otimizada, WhatsApp opt-in, formulário de interesse. CTAs: "Garanta sua cota por R$10" e "Quero ser fundador". Taxa de conversão: 22%.</div>
      </div>
      <div class="funnel-kpi">
        <div class="kpi-num">33k</div>
        <div class="kpi-label">Leads/mês</div>
      </div>
    </div>

    <div class="funnel-step">
      <div class="funnel-num" style="background:rgba(240,165,0,0.2);color:var(--gold);border:2px solid var(--gold)">3</div>
      <div class="funnel-body">
        <div class="title">🔥 AQUECIMENTO — Sequência de Nutrição</div>
        <div class="desc">WhatsApp automático (N8N), stories de bastidores da obra, depoimentos de sócios, lives exclusivas, contador de cotas disponíveis. 48h de nutrição antes de abordagem.</div>
      </div>
      <div class="funnel-kpi">
        <div class="kpi-num">16k</div>
        <div class="kpi-label">Leads quentes</div>
      </div>
    </div>

    <div class="funnel-step">
      <div class="funnel-num" style="background:rgba(255,107,53,0.2);color:var(--coral);border:2px solid var(--coral)">4</div>
      <div class="funnel-body">
        <div class="title">📞 ABORDAGEM — Time de Vendas</div>
        <div class="desc">SDRs fazem primeiro contato (WhatsApp + ligação). Closers fecham. Meta: 100 ligações/dia por vendedor, time de 20 SDRs + 10 closers. Script validado.</div>
      </div>
      <div class="funnel-kpi">
        <div class="kpi-num">5k</div>
        <div class="kpi-label">Oportunidades</div>
      </div>
    </div>

    <div class="funnel-step">
      <div class="funnel-num" style="background:rgba(0,201,212,0.3);color:var(--aqua);border:2px solid var(--aqua)">5</div>
      <div class="funnel-body">
        <div class="title">✅ FECHAMENTO — Cota Platinum</div>
        <div class="desc">20% de conversão na abordagem. Urgência real: preço sobe a cada lote vendido. Oferta final: R$10 na 1ª parcela + clube parceiro imediato + PIX de indicação.</div>
      </div>
      <div class="funnel-kpi">
        <div class="kpi-num">1.000</div>
        <div class="kpi-label">Cotas/mês</div>
      </div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ PLANOS -->
<section>
  <div class="section-tag">04 — Planos de Ação</div>
  <h2>7 Máquinas de Venda</h2>
  <p class="lead">Múltiplos vetores de geração de cotas, cada um com meta própria e execução imediata.</p>

  <!-- PLANO 1 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">🔴</div>
      <h3>PLANO 1 — Máquina de Indicação (PIX Viral)</h3>
      <div class="plan-tag tag-hot">🔥 Prioridade #1</div>
    </div>
    <div class="plan-body">
      <p>O maior canal de aquisição de custo zero. Cada sócio vira vendedor quando o incentivo é tangível, instantâneo e fácil. Com PIX na hora, você cria um exército de 1.000+ vendedores ativos sem pagar salário fixo.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>Estruture 3 tiers de recompensa por indicação:</strong> Pix imediato ao confirmar pagamento da 1ª parcela do indicado.</li>
        <li><span class="check">✦</span><strong>Crie landing page de afiliado simples:</strong> Link único por sócio. Quando alguém compra pelo link dele, ele recebe automaticamente.</li>
        <li><span class="check">✦</span><strong>WhatsApp broadcast semanal para a base de sócios:</strong> "Você tem R$X para receber — indique 1 amigo hoje."</li>
        <li><span class="check">✦</span><strong>Stories kit para os sócios postarem:</strong> Template pronto pra eles colarem o link deles e postar. Quanto menos fricção, mais indicações.</li>
        <li><span class="check">✦</span><strong>Ranking público de top indicadores:</strong> Gamificação — "Top 10 fundadores que mais trouxeram sócios" ganha upgrade de cota ou benefício extra.</li>
        <li><span class="check">✦</span><strong>Challenge de indicação mensal:</strong> Quem indicar 5 no mês ganha convite para dia VIP na obra + fotos exclusivas com o fundador.</li>
      </ul>
    </div>
  </div>

  <!-- PLANO 2 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">📱</div>
      <h3>PLANO 2 — Lives de Conversão no Instagram</h3>
      <div class="plan-tag tag-viral">💥 Alcance Orgânico</div>
    </div>
    <div class="plan-body">
      <p>Com acesso ao @aquamaisoficial (118K seguidores reais), cada live bem executada pode gerar 50–200 vendas num único dia. Trate cada live como um evento de vendas ao vivo, não como conteúdo.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>Live "Bastidores da Obra" — semanal:</strong> Mostre o parque sendo construído. Câmera na drone, no canteiro. Nada converte mais que ver o produto existindo.</li>
        <li><span class="check">✦</span><strong>Live "Sócio Fundador do Mês":</strong> Sócio conta ao vivo por que comprou. Depoimento em tempo real = prova social máxima.</li>
        <li><span class="check">✦</span><strong>Live com oferta de 24h:</strong> "Só hoje o preço atual. Amanhã sobe." Link no bio com contador regressivo. Time de SDRs acompanha live e responde comentários em tempo real.</li>
        <li><span class="check">✦</span><strong>Live "Família Fundadora":</strong> Famílias com crianças testando os clubes parceiros que os sócios já podem usar. Mostra o benefício imediato.</li>
        <li><span class="check">✦</span><strong>Lives com influenciadores locais de BH/Betim:</strong> Micro-influenciadores de família (50K–300K seguidores) com público local têm conversão altíssima para esse produto.</li>
      </ul>
    </div>
  </div>

  <!-- PLANO 3 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">🎯</div>
      <h3>PLANO 3 — Meta Ads: Funil de Performance</h3>
      <div class="plan-tag tag-hot">💰 Previsível</div>
    </div>
    <div class="plan-body">
      <p>Tráfego pago bem estruturado é o único canal 100% previsível e escalável. Com o criativo certo e segmentação precisa, cada real investido retorna em cotas vendidas.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>Topo de funil (Awareness):</strong> Vídeo emocional 15s "Você merece praia. Betim tem." Segmentação: RMGBH, 25–50 anos, C+ e B, interesses: família, viagens, lazer, praia. Objetivo: Alcance + Reconhecimento.</li>
        <li><span class="check">✦</span><strong>Meio de funil (Consideração):</strong> Carrossel mostrando benefícios: clube parceiro agora, preço de fundador, preço sobe a cada lote. CTA: "Quero saber mais". Lead WhatsApp.</li>
        <li><span class="check">✦</span><strong>Fundo de funil (Conversão):</strong> Vídeo de depoimento de sócio + oferta "R$10 na 1ª parcela". Retargeting de quem interagiu nos últimos 30 dias. CTA: "Garantir minha cota agora".</li>
        <li><span class="check">✦</span><strong>Criativo de urgência dinâmica:</strong> "Lote X: 87 cotas restantes ao preço atual." Contador real. A cada lote vendido, anúncio atualiza.</li>
        <li><span class="check">✦</span><strong>Google Ads — Intenção de compra:</strong> Keywords: "parque aquático BH", "clube aquático Betim", "clube aquático família BH", "sócio parque aquático MG". Captura quem já está procurando.</li>
      </ul>
    </div>
  </div>

  <!-- PLANO 4 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">🤝</div>
      <h3>PLANO 4 — Clube de Empresas e RH</h3>
      <div class="plan-tag tag-scale">📈 Alto Ticket Médio</div>
    </div>
    <div class="plan-body">
      <p>Uma única empresa de 500 funcionários pode ser responsável por 50–100 cotas de uma vez. Canal B2B com menor CPL e maior volume por venda. V4 tem estrutura para isso.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>Mapeie as 200 maiores empregadoras de Betim e contorno:</strong> Fiat, petroquímica, logística, varejo. Proposta de "Benefício Corporativo AquaMais" para o RH.</li>
        <li><span class="check">✦</span><strong>Proposta corporativa exclusiva:</strong> Desconto progressivo: empresa que garante 20+ cotas leva preço de lote anterior. Pagamento facilitado via CNPJ.</li>
        <li><span class="check">✦</span><strong>Evento presencial "AquaMais Business Day":</strong> Café da manhã de 45min para RHs e diretores. Apresentação do projeto, maquete, vídeo da obra. Meta: 15 empresas por evento.</li>
        <li><span class="check">✦</span><strong>Sindicatos e associações de classe:</strong> Parceria com sindicatos de trabalhadores da indústria. Eles comunicam para a base = custo zero de aquisição.</li>
        <li><span class="check">✦</span><strong>Clubes de bairro e associações de moradores:</strong> Apresentação em reunião de condomínio. Uma reunião com 100 moradores pode gerar 8–15 vendas diretas.</li>
      </ul>
    </div>
  </div>

  <!-- PLANO 5 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">🏅</div>
      <h3>PLANO 5 — Descontos Progressivos como Motor de Grupo</h3>
      <div class="plan-tag tag-viral">🌊 Efeito Manada</div>
    </div>
    <div class="plan-body">
      <p>Você já tem a inteligência de que o preço sobe com o volume — transforme isso em urgência coletiva. Quando as pessoas entendem que "quanto mais amigos eu trazer, mais barato fica pra todo mundo", você cria o efeito manada.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>Sistema de "Turma de Fundadores":</strong> Grupo de WhatsApp com 10–20 pessoas que se juntam para comprar juntas e garantir preço de lote coletivo. A turma mais rápida a completar 20 leva desconto extra.</li>
        <li><span class="check">✦</span><strong>Tabela de preços pública por lote:</strong> "Lote atual: R$297/mês. Próximo lote: R$347/mês." Transparência total. O próprio comprador corre pra indicar antes de sair do lote.</li>
        <li><span class="check">✦</span><strong>"Fundador traz Fundador" — desconto em mensalidade:</strong> A cada amigo indicado que compra, o sócio ganha 5% de desconto permanente na mensalidade futura. Até 30% de desconto acumulável.</li>
        <li><span class="check">✦</span><strong>Campanha "Família Fundadora":</strong> Família que compra 3+ cotas (pai, mãe, filho maior) recebe benefício extra: mesa reservada na área VIP no dia de inauguração.</li>
      </ul>
    </div>
  </div>

  <!-- PLANO 6 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">🎪</div>
      <h3>PLANO 6 — Eventos Presenciais de Conversão</h3>
      <div class="plan-tag tag-hot">🏟️ Alta Conversão</div>
    </div>
    <div class="plan-body">
      <p>Evento presencial tem a maior taxa de conversão de qualquer canal. Quando a pessoa está lá, com a maquete na frente, o fundador ao vivo, e a oferta expirando, a conversão explode. Meta: 2 eventos/semana.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>"Noite do Fundador" — evento semanal no escritório:</strong> Ambiente temático (praia/Copacabana), drinks, maquete iluminada, vídeo da obra em loop, equipe de vendas pronta. Convide 80 pessoas, converta 20+.</li>
        <li><span class="check">✦</span><strong>Pop-up em shoppings de Betim e BH:</strong> Stand com TV mostrando vídeo do parque. Equipe abordando ativamente. Oferta exclusiva para quem fechar no stand. Meta: 30 cotas/fim de semana por stand.</li>
        <li><span class="check">✦</span><strong>Visita guiada à obra:</strong> Sábados às 10h. Tour em ônibus fretado. Quem vai, vê o projeto com os próprios olhos. Taxa de conversão estimada: 40%. Acompanhe com closer no ônibus de volta.</li>
        <li><span class="check">✦</span><strong>Parceria com escolas e cursos de idiomas:</strong> "Seu filho terá um verão inesquecível" — apresentação para pais após reunião escolar. Datas quentes: agosto-setembro (pré-verão).</li>
      </ul>
    </div>
  </div>

  <!-- PLANO 7 -->
  <div class="plan-block">
    <div class="plan-header">
      <div class="plan-emoji">🤖</div>
      <h3>PLANO 7 — Automação de Nutrição (N8N + WhatsApp)</h3>
      <div class="plan-tag tag-scale">⚙️ Escalável</div>
    </div>
    <div class="plan-body">
      <p>Com N8N (que você já domina) + Evolution API, é possível criar uma sequência automática de nutrição que mantém o lead aquecido por 7–14 dias antes e depois da abordagem humana.</p>
      <ul class="action-list">
        <li><span class="check">✦</span><strong>Sequência Dia 0 (imediata):</strong> "Olá [nome]! Vi que você se interessou pelo AquaMais 🌊 Aqui está o vídeo exclusivo da nossa obra + uma surpresa pra você." → Vídeo + oferta R$10.</li>
        <li><span class="check">✦</span><strong>Dia 1 — Prova Social:</strong> "Só ontem mais 47 famílias garantiram a cota de fundador. Veja o que elas disseram 👇" → Print de depoimentos.</li>
        <li><span class="check">✦</span><strong>Dia 2 — Urgência de Preço:</strong> "⚠️ AVISO: O lote atual tem apenas 120 cotas restantes. Quando esgotar, o próximo começa em R$347/mês." + Tabela de lotes.</li>
        <li><span class="check">✦</span><strong>Dia 3 — Benefício Imediato:</strong> "Sabia que como Platinum você já pode usar clubes parceiros AGORA, mesmo antes de o AquaMais abrir? Aqui estão os 5 clubes disponíveis na sua região 🏊"</li>
        <li><span class="check">✦</span><strong>Dia 5 — SDR Humano Entra:</strong> Mensagem personalizada simulando texto manual. "Oi [nome], aqui é o [nome do SDR] do AquaMais. Você teve a chance de ver o projeto? Posso te ligar em 5 minutos?"</li>
        <li><span class="check">✦</span><strong>Dia 7 — Última chance:</strong> "Esse é o nosso último contato com preço atual. Veja o quanto você economiza entrando hoje vs. mês que vem:" + calculadora de economia.</li>
      </ul>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ PIX REFERRAL -->
<section>
  <div class="section-tag">05 — Programa de Indicação</div>
  <h2>Estrutura do PIX de Indicação</h2>
  <p class="lead">Transforme cada sócio em um vendedor ativo. A estrutura abaixo precisa ser simples, transparente e pagar na hora.</p>

  <div class="referral-box">
    <h3 style="margin-bottom:8px">💸 Tabela de Recompensas por Indicação</h3>
    <p style="font-size:14px;color:#7fb3c8;margin-bottom:8px">Pix enviado automaticamente em até 24h após confirmação do pagamento do indicado. Sem burocracia, sem demora.</p>
    <div class="referral-tiers">
      <div class="tier">
        <div class="tier-val">R$50</div>
        <div class="tier-name">Bronze</div>
        <div class="tier-cond">1ª indicação confirmada</div>
      </div>
      <div class="tier">
        <div class="tier-val">R$80</div>
        <div class="tier-name">Silver</div>
        <div class="tier-cond">2ª a 5ª indicação</div>
      </div>
      <div class="tier">
        <div class="tier-val">R$120</div>
        <div class="tier-name">Gold</div>
        <div class="tier-cond">6ª+ indicação</div>
      </div>
      <div class="tier">
        <div class="tier-val">R$500</div>
        <div class="tier-name">Platinum</div>
        <div class="tier-cond">Bônus ao indicar 10+ no mês</div>
      </div>
    </div>
  </div>

  <div class="grid-2">
    <div class="card gold">
      <div class="card-icon">🏊</div>
      <h3>Clube Parceiro: Benefício Imediato</h3>
      <p>Sócio que compra hoje já ganha acesso a clubes parceiros da região enquanto o AquaMais é construído. Esse é o argumento que vence o ceticismo: <strong>você já tem algo AGORA.</strong> Liste os clubes com foto, endereço e dias de uso no material de vendas.</p>
    </div>
    <div class="card gold">
      <div class="card-icon">📊</div>
      <h3>Desconto Progressivo na Mensalidade</h3>
      <p>Cada indicação confirmada = -5% na mensalidade futura do sócio, até 30%. Exemplo: quem indica 6 amigos nunca mais paga mensalidade cheia. Esse argumento faz o sócio "trabalhar" para o AquaMais espontaneamente.</p>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ SCRIPTS -->
<section>
  <div class="section-tag">06 — Scripts de Venda</div>
  <h2>3 Scripts Validados para o Time</h2>

  <div class="script-box">
    <div class="script-label">📱 Script WhatsApp — Primeiro Contato (SDR)</div>
    "Oi [nome]! Aqui é o [nome] do AquaMais 🌊 Vi que você se interessou em conhecer o projeto. Você sabia que o AquaMais será o maior parque aquático de MG — na sua região, a 30 min de BH?<br><br>
    Hoje a gente tem uma condição especial de fundador: você garante a cota pagando só R$10 na primeira parcela, e já pode usar clubes parceiros na sua cidade enquanto o parque fica pronto.<br><br>
    Posso te mandar o vídeo completo do projeto e os detalhes da oferta? É rápido 🙏"
  </div>

  <div class="script-box">
    <div class="script-label">📞 Script Ligação — Closer (Objeção "Ainda não inaugurou")</div>
    "Entendo sua pergunta — faz todo sentido. Mas deixa eu te mostrar uma perspectiva diferente: foi exatamente por não ter inaugurado ainda que você tem acesso ao menor preço que o AquaMais vai ter na história. Quem comprou apartamento na planta pagou menos. Quem comprou ações da Petrobras antes da abertura pagou menos.<br><br>
    Os sócios que garantiram hoje já estão usando os clubes parceiros — então o benefício é real agora. E quando o parque abrir em 2026, você vai estar lá como fundador, com área VIP, sem pagar preço de balcão.<br><br>
    Qual seria o melhor dia para a sua família aproveitar o clube parceiro mais próximo essa semana?"
  </div>

  <div class="script-box">
    <div class="script-label">💰 Script Indicação — Mensagem do Sócio para Amigos</div>
    "Ei [nome]! Acabei de garantir minha cota de fundador no AquaMais — aquele parque aquático que vai ser o Copacabana de Minas aqui em Betim! 🏝️<br><br>
    Entrei por R$10 na primeira parcela e já recebi acesso ao clube aqui perto. Quando o parque abrir, tenho área VIP garantida.<br><br>
    Se você usar meu link pra entrar hoje, eu recebo um PIX e você garante o mesmo preço que eu paguei (amanhã já sobe de lote). Aqui está: [LINK]<br><br>
    Qualquer dúvida, fala comigo! 🌊"
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ KPIs -->
<section>
  <div class="section-tag">07 — Dashboard de KPIs</div>
  <h2>Métricas que o CEO & Diretor Comercial acompanham toda semana</h2>

  <table class="kpi-table">
    <thead>
      <tr>
        <th>KPI</th>
        <th>Meta Semanal</th>
        <th>Meta Mensal</th>
        <th>Responsável</th>
        <th>Fonte</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Leads captados</td>
        <td><span class="num">8.250</span></td>
        <td><span class="num">33.000</span></td>
        <td>Tráfego</td>
        <td>Meta Ads / Google</td>
      </tr>
      <tr>
        <td>Leads qualificados (WA opt-in)</td>
        <td><span class="num">4.000</span></td>
        <td><span class="num">16.000</span></td>
        <td>SDR</td>
        <td>CRM / N8N</td>
      </tr>
      <tr>
        <td>Oportunidades abertas</td>
        <td><span class="num">1.250</span></td>
        <td><span class="num">5.000</span></td>
        <td>Time de Vendas</td>
        <td>CRM</td>
      </tr>
      <tr>
        <td>Cotas vendidas</td>
        <td><span class="num coral">250</span></td>
        <td><span class="num coral">1.000</span></td>
        <td>Closers</td>
        <td>CRM / Financeiro</td>
      </tr>
      <tr>
        <td>Cotas via indicação</td>
        <td><span class="num">75</span></td>
        <td><span class="num">300</span></td>
        <td>Programa de Afiliados</td>
        <td>Link rastreável</td>
      </tr>
      <tr>
        <td>Custo por Lead (CPL)</td>
        <td colspan="2"><span class="num gold">R$ 8–15</span></td>
        <td>Tráfego</td>
        <td>Meta / Google Ads</td>
      </tr>
      <tr>
        <td>Custo por Cota Vendida (CPA)</td>
        <td colspan="2"><span class="num gold">R$ 150–300</span></td>
        <td>Diretor Comercial</td>
        <td>Financeiro</td>
      </tr>
      <tr>
        <td>Taxa de conversão SDR → Closer</td>
        <td colspan="2"><span class="num">30%</span></td>
        <td>SDR Manager</td>
        <td>CRM</td>
      </tr>
      <tr>
        <td>Taxa de conversão Closer → Venda</td>
        <td colspan="2"><span class="num">20%</span></td>
        <td>Closer Manager</td>
        <td>CRM</td>
      </tr>
      <tr>
        <td>Views médias por live</td>
        <td colspan="2"><span class="num">5.000+</span></td>
        <td>Social Media</td>
        <td>Instagram Analytics</td>
      </tr>
      <tr>
        <td>PIX pagos por indicação</td>
        <td><span class="num">70</span></td>
        <td><span class="num">300</span></td>
        <td>CS / Financeiro</td>
        <td>Planilha de Afiliados</td>
      </tr>
    </tbody>
  </table>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ CRONOGRAMA -->
<section>
  <div class="section-tag">08 — Plano de 30 dias</div>
  <h2>Semana a semana: do zero a 1.000</h2>

  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-dot" style="border-color:var(--coral)"></div>
      <div class="timeline-week">Dias 1–2 (AGORA)</div>
      <div class="timeline-title">🚀 Ativação de Emergência</div>
      <div class="timeline-desc">Reunião com equipe AquaMais + levantamento do CRM atual. Auditoria das campanhas de Google Ads ativas. Mapear base de sócios existentes para programa de indicação. Definir preços por lote. Configurar link rastreável por sócio. Briefing completo para o time de vendas.</div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-week">Semana 1 — Dias 3–9</div>
      <div class="timeline-title">🔥 Lançamento da Máquina</div>
      <div class="timeline-desc">Landing page nova com oferta "R$10 + clube agora". Sequência N8N no ar. Meta Ads: 3 campanhas ativas (topo, meio, fundo). Live de lançamento com oferta 24h (@aquamaisoficial). Primeira "Noite do Fundador" no escritório. Broadcast para base de sócios: ative o PIX de indicação. Meta semana 1: 150 cotas.</div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-week">Semana 2 — Dias 10–16</div>
      <div class="timeline-title">📊 Otimização e B2B</div>
      <div class="timeline-desc">Análise de CPL e ajuste de criativos. Prospecção B2B: primeiros 20 contatos com RHs de grandes empresas de Betim. Pop-up em shopping (fim de semana). Segunda live — "Bastidores da Obra com Drone". Início das visitas guiadas à obra (sábado). Meta semana 2: 220 cotas.</div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-week">Semana 3 — Dias 17–23</div>
      <div class="timeline-title">📈 Aceleração de Indicações</div>
      <div class="timeline-desc">Top 10 indicadores da semana 1 publicados nas redes. Challenge "Indique 5 em 7 dias" ativado. Parceria com 2–3 micro-influenciadores locais. Live com depoimento ao vivo de sócio + oferta relâmpago 2h. Evento presencial #2. Meta semana 3: 280 cotas.</div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot" style="border-color:var(--aqua)"></div>
      <div class="timeline-week">Semana 4 — Dias 24–30</div>
      <div class="timeline-title">🎯 Fechamento Agressivo</div>
      <div class="timeline-desc">Todos os leads não convertidos recebem oferta de "última chance do lote". Live de encerramento de lote — "O preço muda na segunda-feira." Evento B2B: "AquaMais Business Day". Review geral do mês: CAC, churn, NPS dos sócios. Planejamento do mês 2. Meta semana 4: 350 cotas. Total mês 1: 1.000+</div>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ ESTRUTURA DO TIME -->
<section>
  <div class="section-tag">09 — Time Ideal</div>
  <h2>Estrutura da Equipe Comercial V4</h2>
  <p class="lead">Para 1.000 cotas/mês você precisa de uma máquina humana bem calibrada. Abaixo, o organograma mínimo viável.</p>

  <div class="grid-3">
    <div class="card">
      <div class="card-icon">👑</div>
      <h3>Diretor Comercial (V4)</h3>
      <p>Define estratégia semanal, acompanha KPIs diários, resolve gargalos em tempo real. Participa das lives e eventos presenciais como rosto da operação.</p>
    </div>
    <div class="card">
      <div class="card-icon">🎯</div>
      <h3>Gestor de Tráfego</h3>
      <p>Meta Ads + Google Ads. Responsável por CPL abaixo de R$15 e volume de leads. A/B test de criativos semanalmente. Integração com N8N para automação de follow-up.</p>
    </div>
    <div class="card">
      <div class="card-icon">📱</div>
      <h3>Social Media / Live</h3>
      <p>Gestão do @aquamaisoficial + produção das lives de conversão. Conteúdo de bastidores da obra. Template de indicação para sócios postarem. Identidade visual das campanhas.</p>
    </div>
    <div class="card">
      <div class="card-icon">⚡</div>
      <h3>SDRs (8–12 pessoas)</h3>
      <p>Primeiro contato WhatsApp e ligação. Meta: 80–100 abordagens/dia por SDR. Qualificar, aquecer e passar para o closer. Roteiro validado + CRM atualizado em tempo real.</p>
    </div>
    <div class="card">
      <div class="card-icon">🏆</div>
      <h3>Closers (4–6 pessoas)</h3>
      <p>Recebem leads quentes dos SDRs. Conversão-alvo: 20–25%. Domínio das objeções ("parque não inaugurou", "confio?"). Autorização para aplicar descontos de fechamento.</p>
    </div>
    <div class="card">
      <div class="card-icon">🤝</div>
      <h3>CS / Afiliados</h3>
      <p>Gerencia programa de indicação. Processa PIX aos indicadores. Onboarding dos novos sócios + acesso ao clube parceiro. Alimenta o NPS e depoimentos para as lives.</p>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ═══════════════════════════════════════ ALERTAS ESTRATÉGICOS -->
<section>
  <div class="section-tag">10 — Alertas para CEO e Diretor</div>
  <h2>O que não pode dar errado</h2>
  <p class="lead">Erros que derrubam operações como essa antes de chegarem a 500 cotas/mês.</p>

  <div class="grid-2">
    <div class="card highlight">
      <div class="card-icon">⚠️</div>
      <h3>Transparência Total sobre a Obra</h3>
      <p>Mostre a obra semanalmente. Video, foto, drone. Nunca deixe 2 semanas sem atualização visual. Sócio que não vê progresso cancela. Sócio que vê fica e indica.</p>
    </div>
    <div class="card highlight">
      <div class="card-icon">⚠️</div>
      <h3>Pix de Indicação: Pague SEMPRE na hora</h3>
      <p>Um atraso de 48h no pagamento do PIX de indicação mata o programa. O boca-a-boca negativo é instantâneo. Automatize o pagamento via N8N ou tenha alguém dedicado exclusivamente para isso.</p>
    </div>
    <div class="card highlight">
      <div class="card-icon">⚠️</div>
      <h3>Clube Parceiro: Funcione de Verdade</h3>
      <p>O benefício do clube parceiro é o que converte o cético. Se o sócio tentar usar e tiver problema no acesso, a reputação do AquaMais despenca. Teste antes de prometer.</p>
    </div>
    <div class="card highlight">
      <div class="card-icon">⚠️</div>
      <h3>CRM desde o Dia 1</h3>
      <p>Sem CRM, você não tem operação de vendas — tem caos. RD Station, HubSpot ou até uma planilha bem estruturada. Cada lead precisa ter status, última abordagem e próximo passo registrado.</p>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════ FOOTER -->
<footer>
  <p>Preparado pela <strong>UltraWork AI × V4 Company</strong> | Operação AquaMais Parque — Betim, MG</p>
  <p style="margin-top:8px">Este documento é confidencial e de uso exclusivo da equipe comercial. Abril 2026.</p>
</footer>

</body>
</html>
