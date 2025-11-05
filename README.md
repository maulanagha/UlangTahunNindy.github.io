# UlangTahunNindy.github.io
Selamat Ulang Tahun
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>🎉 Selamat Ulang Tahun!</title>
  <style>
    :root{
      --bg1: #0f172a;
      --bg2: #0f3a52;
      --accent: #ffd166;
      --muted: #cbd6ea;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    body{
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(180deg,var(--bg1),var(--bg2));
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      text-align: center;
      padding: 24px;
    }
    .card{
      background: rgba(255,255,255,0.05);
      border-radius: 16px;
      padding: 32px 20px;
      max-width: 500px;
      box-shadow: 0 12px 30px rgba(0,0,0,0.4);
      animation: fadeIn 1.2s ease;
      position: relative;
      overflow: hidden;
    }
    h1{color: var(--accent);font-size: 28px;margin-bottom: 12px;}
    h2{margin-top:10px;color:#fff;font-size:22px}
    p{color:var(--muted);line-height:1.6;margin-top:10px;font-size:15px}
    @keyframes fadeIn{from{opacity:0;transform:scale(.9)}to{opacity:1;transform:scale(1)}}
    footer{margin-top:20px;font-size:13px;color:var(--muted)}
    .confetti span{
      position:absolute;width:8px;height:14px;
      border-radius:3px;
      animation:fall 3s linear infinite;
      opacity:0.9;
    }
    @keyframes fall{
      0%{transform:translateY(-10vh) rotate(0deg);}
      100%{transform:translateY(110vh) rotate(720deg);}
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="confetti" id="confetti"></div>
    <h1>🎂 Selamat Ulang Tahun!</h1>
    <h2 id="nama">Nindy</h2>
    <p id="pesan">Untuk orang yang paling berharga dihidupku, terimakasih telah dating mengisi hari-hari ku selama 2 tahun ini, terimakasih telah menjadi orang yang paling special dihidupku, terimakasih telah menjadi teman berbagi cerita random dan hal-hal aneh berbagi tawa dan sedih Bersama, terimakasih untuk semuanya yang sudah kamu berikan.
Selamat Ulang Tahun Nindy 💕 🎉</p>
    <footer>— Dikirim dengan cinta 💕</footer>
  </div>

  <script>
    // Ambil parameter dari URL
    const params = new URLSearchParams(window.location.search);
    const nama = params.get('nama') || 'Nindy;
    const pesan = params.get('pesan') || 'Semoga hari ini dipenuhi tawa, cinta, dan kue sebanyak-banyaknya! 🎉';

    // Tampilkan di halaman
    document.getElementById('Nindy').textContent = nama;
    document.getElementById('Selamat Ulang tahun').textContent = decodeURIComponent(pesan);

    // Efek konfeti
    const colors = ['#ffd166','#ef476f','#06d6a0','#118ab2','#f78c6b'];
    const confetti = document.getElementById('confetti');
    for(let i=0;i<40;i++){
      const s = document.createElement('span');
      s.style.left = (Math.random()*100) + '%';
      s.style.top = (-Math.random()*20) + 'vh';
      s.style.background = colors[Math.floor(Math.random()*colors.length)];
      s.style.width = (6 + Math.random()*6)+'px';
      s.style.height = (10 + Math.random()*10)+'px';
      s.style.animationDelay = (Math.random()*2)+'s';
      confetti.appendChild(s);
    }
  </script>
</body>
</html>
