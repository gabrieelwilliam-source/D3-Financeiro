[index.html](https://github.com/user-attachments/files/23320403/index.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>D3 Financeiro - Facilidade para crescer</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: radial-gradient(circle at top right, #00ffb3 0%, #0b0e10 60%);
      color: #ffffff;
      position: relative;
      overflow-x: hidden;
    }

    .bubble {
      position: absolute;
      border-radius: 50%;
      background: rgba(0, 255, 179, 0.1);
      filter: blur(40px);
      animation: float 10s infinite ease-in-out;
      z-index: 0;
    }
    .bubble:nth-child(1) {
      width: 200px; height: 200px;
      top: 10%; left: 10%;
      animation-delay: 0s;
    }
    .bubble:nth-child(2) {
      width: 150px; height: 150px;
      top: 50%; right: 15%;
      animation-delay: 2s;
    }
    .bubble:nth-child(3) {
      width: 250px; height: 250px;
      bottom: 5%; left: 30%;
      animation-delay: 4s;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

    header {
      text-align: center;
      padding: 80px 20px;
      position: relative;
      z-index: 1;
    }

    header img {
      width: 180px;
      margin-bottom: 20px;
    }

    header h1 {
      font-size: 48px;
      color: #17fcb4;
      margin-bottom: 10px;
    }

    header h2 {
      font-size: 22px;
      font-weight: 400;
      color: #e0e0e0;
    }

    .cta {
      margin-top: 30px;
    }

    .cta button {
      background-color: #17fcb4;
      color: #0d0f10;
      border: none;
      padding: 15px 30px;
      border-radius: 8px;
      font-size: 18px;
      cursor: pointer;
      transition: 0.3s;
    }

    .cta button:hover {
      background-color: #00d796;
    }

    .about {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      padding: 60px 20px;
      text-align: center;
      background-color: #111418;
      z-index: 1;
      position: relative;
    }

    .about-text {
      max-width: 600px;
      margin: 20px;
    }

    .about-text h3 {
      color: #17fcb4;
      font-size: 28px;
      margin-bottom: 10px;
    }

    .benefits {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 60px 20px;
      gap: 30px;
      text-align: center;
      background-color: #0d0f10;
      z-index: 1;
      position: relative;
    }

    .benefit {
      max-width: 250px;
      background-color: #111418;
      padding: 25px;
      border-radius: 10px;
      transition: 0.3s;
    }

    .benefit:hover {
      background-color: #00ffb31a;
    }

    .benefit h4 {
      color: #17fcb4;
      margin-bottom: 10px;
    }

    .contact {
      text-align: center;
      padding: 80px 20px;
      background-color: #111418;
      position: relative;
      z-index: 1;
    }

    .contact h3 {
      color: #17fcb4;
      font-size: 28px;
      margin-bottom: 20px;
    }

    .whatsapp-button {
      background-color: #25D366;
      color: #fff;
      border: none;
      padding: 16px 30px;
      border-radius: 8px;
      font-size: 18px;
      font-weight: 600;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      transition: 0.3s;
    }

    .whatsapp-button:hover {
      background-color: #1eb85a;
    }

    footer {
      background-color: #0b0e10;
      padding: 60px 20px;
      position: relative;
      color: #fff;
      font-size: 15px;
      z-index: 1;
    }

    footer::before {
      content: "";
      background-image: url('WhatsApp Image 2025-11-02 at 09.53.40-Photoroom.png');
      background-repeat: no-repeat;
      background-position: center;
      background-size: 200px;
      opacity: 0.05;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }

    .footer-content {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      gap: 40px;
      max-width: 900px;
      margin: 0 auto;
      position: relative;
      z-index: 2;
    }

    .footer-left {
      text-align: left;
      color: #17fcb4;
    }

    .footer-left h4 {
      margin-bottom: 10px;
      text-transform: uppercase;
      font-weight: 600;
      font-size: 16px;
    }

    .footer-left p {
      margin: 4px 0;
      color: #a8a8a8;
      font-size: 14px;
    }

    .footer-left a {
      color: #17fcb4;
      text-decoration: none;
    }

    .footer-right {
      text-align: center;
    }

    .footer-right img {
      width: 130px;
      margin-bottom: 8px;
    }

    .footer-right p {
      color: #17fcb4;
      font-size: 13px;
    }

    .footer-bottom {
      text-align: center;
      margin-top: 40px;
      font-size: 13px;
      color: #777;
    }
  </style>
</head>
<body>

  <div class="bubble"></div>
  <div class="bubble"></div>
  <div class="bubble"></div>

  <header>
    <img src="WhatsApp Image 2025-11-02 at 09.53.40-Photoroom.png" alt="Logo D3 Financeiro">
    <h1>D3 Financeiro</h1>
    <h2>Está sem tempo para suas finanças? Nós cuidamos disso para você!</h2>
    <div class="cta">
      <button onclick="document.getElementById('contato').scrollIntoView({behavior: 'smooth'})">Quero saber mais</button>
    </div>
  </header>

  <section class="about">
    <div class="about-text">
      <h3>Facilidade para crescer</h3>
      <p>Deixe suas rotinas financeiras conosco e tenha tempo para focar na visão do seu negócio. A D3 Financeiro é especialista em BPO Financeiro — nós otimizamos processos, garantimos organização e facilitamos o seu crescimento.</p>
    </div>
  </section>

  <section class="benefits">
    <div class="benefit">
      <h4>Mais tempo</h4>
      <p>Deixe a parte financeira conosco e dedique-se ao que realmente importa: o crescimento da sua empresa.</p>
    </div>
    <div class="benefit">
      <h4>Redução de custos</h4>
      <p>Evite erros e gastos desnecessários com um controle profissional e estratégico das suas finanças.</p>
    </div>
    <div class="benefit">
      <h4>Gestão eficiente</h4>
      <p>Com relatórios claros e organização total, você tem a visão completa do seu negócio em um só lugar.</p>
    </div>
  </section>

  <section class="contact" id="contato">
    <a href="https://wa.me/554797768710" target="_blank" class="whatsapp-button">Entrar em contato</a>
  </section>

  <footer>
    <div class="footer-content">
      <div class="footer-left">
        <h3>Gostaria de saber mais ?</h3>
        <h4>Entre em contato</h4>
        <p><strong>BPO Financeiro</strong></p>
        <p><em>Facilidade para crescer</em></p>
        <p>📧 <a href="mailto:adm@d3financeiro.com.br">adm@d3financeiro.com.br</a></p>
        <p>📞 +55 47 9776-8710</p>
      </div>
      <div class="footer-right">
      </div>
    </div>
    <div class="footer-bottom">
      © 2025 D3 Financeiro — Todos os direitos reservados.
    </div>
  </footer>

</body>
</html>
