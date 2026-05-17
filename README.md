<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>CARLOS CELL | Qualidade e Confiança</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins', sans-serif;
      scroll-behavior:smooth;
    }

    body{
      background:#000;
      color:white;
      overflow-x:hidden;
    }

    ::selection{
      background:#ff0000;
      color:white;
    }

    header{
      position:fixed;
      width:100%;
      top:0;
      left:0;
      z-index:1000;
      padding:20px 8%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      backdrop-filter:blur(12px);
      background:rgba(0,0,0,0.75);
      border-bottom:1px solid rgba(255,255,255,0.08);
    }

    .logo{
      font-size:34px;
      font-weight:900;
      letter-spacing:3px;
      color:#ff0000;
    }

    .logo span{
      color:#d4af37;
    }

    nav a{
      text-decoration:none;
      color:white;
      margin-left:30px;
      font-weight:600;
      transition:0.3s;
    }

    nav a:hover{
      color:#ff0000;
    }

    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      padding:150px 8% 80px;
      background:
      radial-gradient(circle at top, rgba(255,0,0,0.35), transparent 40%),
      #000;
    }

    .hero-content{
      max-width:750px;
    }

    .tag{
      display:inline-block;
      padding:12px 24px;
      border-radius:100px;
      border:1px solid #ff0000;
      background:rgba(255,0,0,0.15);
      color:#ff4d4d;
      margin-bottom:25px;
      animation:pulse 4s infinite;
    }

    @keyframes pulse{
      0%{transform:scale(1);}
      50%{transform:scale(1.03);}
      100%{transform:scale(1);}
    }

    .hero h1{
      font-size:75px;
      line-height:1.1;
      margin-bottom:25px;
      font-weight:900;
    }

    .hero h1 span{
      color:#ff0000;
    }

    .hero p{
      color:#ccc;
      font-size:19px;
      line-height:1.8;
      margin-bottom:40px;
    }

    .buttons{
      display:flex;
      gap:20px;
      flex-wrap:wrap;
    }

    .btn{
      padding:18px 35px;
      border-radius:18px;
      text-decoration:none;
      font-weight:700;
      transition:0.3s;
      display:inline-block;
    }

    .btn-red{
      background:#ff0000;
      color:white;
    }

    .btn-red:hover{
      background:#cc0000;
      transform:translateY(-4px);
    }

    .btn-gold{
      border:2px solid #d4af37;
      color:#d4af37;
    }

    .btn-gold:hover{
      background:#d4af37;
      color:black;
    }

    section{
      padding:100px 8%;
    }

    .section-title{
      text-align:center;
      margin-bottom:60px;
    }

    .section-title p{
      color:#d4af37;
      font-weight:700;
      margin-bottom:10px;
    }

    .section-title h2{
      font-size:55px;
      font-weight:900;
    }

    .diferenciais{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:25px;
    }

    .diferencial{
      background:rgba(255,255,255,0.05);
      border:1px solid rgba(255,255,255,0.08);
      padding:35px;
      border-radius:30px;
      text-align:center;
      transition:0.4s;
      backdrop-filter:blur(12px);
    }

    .diferencial:hover{
      transform:translateY(-10px);
      box-shadow:0 20px 40px rgba(255,0,0,0.2);
    }

    .diferencial h3{
      color:#ff0000;
      margin-bottom:15px;
      font-size:25px;
    }

    .service-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:20px;
    }

    .service{
      background:rgba(255,255,255,0.05);
      padding:25px;
      border-radius:25px;
      border:1px solid rgba(255,255,255,0.08);
      transition:0.3s;
      font-weight:600;
    }

    .service:hover{
      background:#ff0000;
      transform:scale(1.03);
    }

    .catalogo{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(270px,1fr));
      gap:30px;
    }

    .produto{
      background:rgba(255,255,255,0.05);
      border-radius:30px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,0.08);
      transition:0.4s;
    }

    .produto:hover{
      transform:translateY(-10px);
      box-shadow:0 20px 40px rgba(255,0,0,0.25);
    }

    .produto img{
      width:100%;
      height:260px;
      object-fit:cover;
    }

    .produto-info{
      padding:25px;
    }

    .produto-info h3{
      margin-bottom:15px;
      font-size:21px;
    }

    .price{
      color:#d4af37;
      font-size:30px;
      font-weight:900;
      margin-bottom:20px;
    }

    .sobre{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:50px;
      align-items:center;
    }

    .box{
      background:rgba(255,255,255,0.05);
      border-radius:30px;
      padding:40px;
      border:1px solid rgba(255,255,255,0.08);
    }

    .box h3{
      font-size:35px;
      color:#ff0000;
      margin-bottom:25px;
    }

    .box p{
      color:#ccc;
      line-height:1.9;
      margin-bottom:15px;
    }

    .promo{
      background:
      linear-gradient(135deg,#3a0000,#000);
      border-radius:40px;
      padding:70px;
      text-align:center;
      border:1px solid rgba(255,255,255,0.08);
      animation:pulse 4s infinite;
    }

    .promo h2{
      font-size:60px;
      margin-bottom:20px;
    }

    .promo p{
      color:#ccc;
      margin-bottom:35px;
      font-size:18px;
    }

    .contact{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(320px,1fr));
      gap:50px;
    }

    form input,
    form textarea{
      width:100%;
      background:#111;
      border:1px solid #333;
      padding:18px;
      border-radius:18px;
      color:white;
      margin-bottom:20px;
      outline:none;
    }

    form button{
      border:none;
      cursor:pointer;
    }

    footer{
      padding:50px;
      text-align:center;
      border-top:1px solid #111;
      color:#777;
    }

    .whatsapp{
      position:fixed;
      right:25px;
      bottom:25px;
      width:70px;
      height:70px;
      background:#25d366;
      border-radius:50%;
      display:flex;
      justify-content:center;
      align-items:center;
      font-size:34px;
      text-decoration:none;
      z-index:999;
      box-shadow:0 10px 30px rgba(0,0,0,0.4);
    }

    @media(max-width:900px){

      nav{
        display:none;
      }

      .hero h1{
        font-size:48px;
      }

      .section-title h2{
        font-size:40px;
      }

      .promo{
        padding:40px 25px;
      }

      .promo h2{
        font-size:40px;
      }

    }

  </style>
</head>
<body>

<header>

  <div class="logo">
    CARLOS <span>CELL</span>
  </div>

  <nav>
    <a href="#inicio">Início</a>
    <a href="#servicos">Serviços</a>
    <a href="#catalogo">Catálogo</a>
    <a href="#sobre">Quem Somos</a>
    <a href="#contato">Contato</a>
  </nav>

</header>

<section class="hero" id="inicio">

  <div class="hero-content">

    <div class="tag">
      Assistência Técnica Especializada
    </div>

    <h1>
      QUALIDADE E <span>CONFIANÇA</span>
    </h1>

    <p>
      Atendimento rápido, garantia estendida e serviços especializados em um só lugar.
      Tudo com honestidade, profissionalismo e confiança.
    </p>

    <div class="buttons">

      <a href="http://wa.me/5574974007181" target="_blank" class="btn btn-red">
        Solicitar Orçamento
      </a>

      <a href="#catalogo" class="btn btn-gold">
        Ver Catálogo
      </a>

    </div>

  </div>

</section>

<section>

  <div class="section-title">
    <p>DIFERENCIAIS</p>
    <h2>POR QUE ESCOLHER A CARLOS CELL?</h2>
  </div>

  <div class="diferenciais">

    <div class="diferencial">
      <h3>Confiança</h3>
      <p>Atendimento honesto e transparente.</p>
    </div>

    <div class="diferencial">
      <h3>Garantia</h3>
      <p>Garantia estendida em serviços.</p>
    </div>

    <div class="diferencial">
      <h3>Rapidez</h3>
      <p>Atendimento rápido e eficiente.</p>
    </div>

    <div class="diferencial">
      <h3>Especializado</h3>
      <p>Serviços técnicos profissionais.</p>
    </div>

  </div>

</section>

<section id="servicos">

  <div class="section-title">
    <p>SERVIÇOS</p>
    <h2>ASSISTÊNCIA COMPLETA</h2>
  </div>

  <div class="service-grid">

    <div class="service">Troca de Tela</div>
    <div class="service">Troca de Bateria</div>
    <div class="service">Desoxidação</div>
    <div class="service">Câmera</div>
    <div class="service">Conector</div>
    <div class="service">Atualização</div>
    <div class="service">Desbloqueio Android</div>
    <div class="service">Desbloqueio iPhone</div>
    <div class="service">Xerox</div>
    <div class="service">Impressões</div>
    <div class="service">Foto 3/4</div>
    <div class="service">Emissão de Documentos</div>
    <div class="service">Serviços DETRAN</div>
    <div class="service">Revelação de Fotos</div>
    <div class="service">Venda de Acessórios</div>

  </div>

</section>

<section id="catalogo">

  <div class="section-title">
    <p>CATÁLOGO</p>
    <h2>PRODUTOS EM DESTAQUE</h2>
  </div>

  <div class="catalogo">

    <div class="produto">
      <img src="https://images.pexels.com/photos/5208307/pexels-photo-5208307.jpeg">
      <div class="produto-info">
        <h3>Carregador 20W USB-C to lightning</h3>
        <div class="price">R$ 45,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="cabokaidi.png">
      <div class="produto-info">
        <h3>Cabo Kaidi Carga Rápida</h3>
        <div class="price">R$ 15,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="https://images.unsplash.com/photo-1601593346740-925612772716?q=80&w=1200&auto=format&fit=crop">
      <div class="produto-info">
        <h3>Capinhas Silicone Android</h3>
        <div class="price">R$ 20,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="https://images.unsplash.com/photo-1512499617640-c74ae3a79d37?q=80&w=1200&auto=format&fit=crop">
      <div class="produto-info">
        <h3>Capinhas Silicone iPhone</h3>
        <div class="price">R$ 20,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=1200&auto=format&fit=crop">
      <div class="produto-info">
        <h3>Fone O'Gold Mini</h3>
        <div class="price">R$ 55,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="https://images.unsplash.com/photo-1606220588913-b3aacb4d2f46?q=80&w=1200&auto=format&fit=crop">
      <div class="produto-info">
        <h3>Airdots Caixa Vermelha</h3>
        <div class="price">R$ 35,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="https://images.unsplash.com/photo-1512054502232-10a0a035d672?q=80&w=1200&auto=format&fit=crop">
      <div class="produto-info">
        <h3>Película 3D</h3>
        <div class="price">R$ 15,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

    <div class="produto">
      <img src="https://images.unsplash.com/photo-1512941937669-90a1b58e7e9c?q=80&w=1200&auto=format&fit=crop">
      <div class="produto-info">
        <h3>Película Privacidade iPhone</h3>
        <div class="price">R$ 20,00</div>
        <a href="http://wa.me/5574974007181" class="btn btn-red">Comprar</a>
      </div>
    </div>

  </div>

</section>

<section id="sobre">

  <div class="section-title">
    <p>QUEM SOMOS</p>
    <h2>CARLOS CELL</h2>
  </div>

  <div class="sobre">

    <div>

      <p style="color:#ccc; line-height:2; font-size:18px;">

        Somos um pequeno espaço criado pela vontade de Deus para trabalhar com honestidade e ajudar cada cliente enviado por Deus.

        Nosso compromisso é entregar atendimento rápido, serviço especializado, garantia e confiança em cada serviço realizado.

      </p>

    </div>

    <div class="box">

      <h3>Informações</h3>

      <p>
        <strong>Cidade:</strong><br>
        Projeto Curaçá NH3 - Curaçá/BA
      </p>

      <p>
        <strong>Endereço:</strong><br>
        Rua 1 da Vila Nova, Loja Carlos Cell,
        em frente a Edson que conserta TV.
      </p>

      <p>
        <strong>Horário:</strong><br>
        08:00 às 12:00 • 14:00 às 18:00
      </p>

      <p>
        <strong>Email:</strong><br>
        carlosgomeseee00@gmail.com
      </p>

    </div>

  </div>

</section>

<section>

  <div class="promo">

    <h2>PROMOÇÕES IMPERDÍVEIS</h2>

    <p>
      Capinhas, películas, carregadores e acessórios com preços especiais.
    </p>

    <a href="http://wa.me/5574974007181" target="_blank" class="btn btn-red">
      Chamar no WhatsApp
    </a>

  </div>

</section>

<section id="contato">

  <div class="section-title">
    <p>CONTATO</p>
    <h2>PEÇA SEU ORÇAMENTO</h2>
  </div>

  <div class="contact">

    <form>

      <input type="text" placeholder="Seu nome">

      <input type="text" placeholder="Seu WhatsApp">

      <textarea rows="6" placeholder="Digite seu problema ou orçamento"></textarea>

      <button class="btn btn-red">
        Enviar Solicitação
      </button>

    </form>

    <div class="box">

      <h3>Redes Sociais</h3>

      <p>

        📸 Instagram:<br><br>

        <a href="https://www.instagram.com/carloscell_nh3?igsh=bW11dWVoam8wYTJs"
        target="_blank"
        style="color:#d4af37; text-decoration:none;">

          @carloscell_nh3

        </a>

      </p>

      <br>

      <p>

        💬 WhatsApp:<br><br>

        <a href="http://wa.me/5574974007181"
        target="_blank"
        style="color:#d4af37; text-decoration:none;">

          Clique para conversar

        </a>

      </p>

    </div>

  </div>

</section>

<footer>

  <h2 style="font-size:40px; color:#ff0000; margin-bottom:10px;">
    CARLOS <span style="color:#d4af37;">CELL</span>
  </h2>

  <p>Qualidade e confiança.</p>

  <p style="margin-top:15px;">
    © 2026 - Todos os direitos reservados.
  </p>

</footer>

<a href="http://wa.me/5574974007181"
target="_blank"
class="whatsapp">

  💬

</a>

</body>
</html>