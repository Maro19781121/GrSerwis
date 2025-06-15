<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GR SERWIS - Profesjonalny Warsztat Samochodowy</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Montserrat', sans-serif; background-color: #0d0d0d; color: #f0f0f0; line-height: 1.6; }
    header { background: none; position: relative; overflow: hidden; }
    header video { position: absolute; width: 100%; height: 100%; object-fit: cover; z-index: -1; }
    header .logo { max-height: 80px; margin-bottom: 1rem; }
    header h1 { font-size: 4rem; color: #FFD700; text-shadow: 2px 2px 4px #000; }
    header p { font-size: 1.5rem; margin-top: 1rem; }
    nav { background-color: #1a1a1a; padding: 1rem; text-align: center; position: sticky; top: 0; z-index: 1000; }
    nav a { margin: 0 1rem; text-decoration: none; color: #f0f0f0; font-weight: bold; }
    nav a:hover { color: #FFD700; }
    section { padding: 4rem 2rem; max-width: 1000px; margin: auto; }
    .highlight { color: #FFD700; }
    h2 { margin-bottom: 2rem; font-size: 2rem; border-bottom: 2px solid #FFD700; display: inline-block; padding-bottom: .5rem; }
    ul { list-style: none; padding: 0; }
    ul li { margin-bottom: 1rem; padding-left: 1rem; position: relative; }
    ul li::before { content: '✔'; color: #FFD700; position: absolute; left: 0; }
    form input, form textarea { width: 100%; padding: 1rem; margin-bottom: 1rem; border: none; border-radius: 5px; }
    form button { background-color: #FFD700; color: #000; padding: 1rem 2rem; border: none; border-radius: 5px; font-weight: bold; cursor: pointer; transition: all 0.3s ease; }
    form button:hover { background-color: #e6c200; transform: scale(1.05); }
    footer { background-color: #111; color: #aaa; text-align: center; padding: 2rem; margin-top: 4rem; }

    .hidden { opacity: 0; transform: translateY(30px); transition: all 0.8s ease-out; }
    .visible { opacity: 1; transform: translateY(0); }

    @media (max-width: 768px) {
      header h1 { font-size: 2.5rem; }
      header p { font-size: 1.2rem; }
      section { padding: 2rem 1rem; }
      h2 { font-size: 1.5rem; }
      nav a { margin: 0 0.5rem; font-size: 0.9rem; }
    }
  </style>

  <script>
    // Animacja pojawiania się sekcji
    document.addEventListener('DOMContentLoaded', () => {
      const sections = document.querySelectorAll('section');
      const options = { threshold: 0.1 };
      const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
            observer.unobserve(entry.target);
          }
        });
      }, options);
      sections.forEach(section => {
        section.classList.add('hidden');
        observer.observe(section);
      });

      // Licznik lat
      const counter = document.getElementById("counter");
      if (counter) {
        let count = 0;
        const interval = setInterval(() => {
          if (count < 15) {
            count++;
            counter.textContent = count;
          } else {
            clearInterval(interval);
          }
        }, 100);
      }
    });
  </script>
</head>

<body>
  <header>
    <video autoplay muted loop playsinline>
      <source src="https://cdn.coverr.co/videos/coverr-car-in-the-shop-4817/1080p.mp4" type="video/mp4">
    </video>
    <img src="images/logo.png" alt="GR SERWIS Logo" class="logo">
    <h1>GR SERWIS</h1>
    <p>Specjalistyczny warsztat samochodowy | Off-road i nie tylko</p>

    <div style="width: 100%; max-height: 500px; overflow: hidden;">
      <img src="images/konserwacja.jpg" alt="Konserwacja podwozia - przed i po" style="width: 100%; object-fit: cover;">
    </div>
  </header>

  <nav>
    <a href="#onas">O nas</a>
    <a href="#oferta">Oferta</a>
    <a href="#galeria">Galeria</a>
    <a href="#kontakt">Kontakt</a>
  </nav>

  <section id="onas">
    <h2>O nas</h2>
    <p>GR Serwis to <span class="highlight">profesjonalny warsztat samochodowy</span> z wieloletnim doświadczeniem. Specjalizujemy się w serwisie i modyfikacjach pojazdów terenowych (off-road), ale obsługujemy również samochody osobowe, dostawcze i ciężarowe.</p>
  </section>

  <section id="oferta">
    <h2>Oferta</h2>
    <ul>
      <li>Zabezpieczenie antykorozyjne podwozia suchym woskiem</li>
      <li>Profesjonalne wyważanie wałów napędowych</li>
      <li>Diagnostyka komputerowa</li>
      <li>Naprawy mechaniczne i serwis eksploatacyjny</li>
      <li>Modernizacje off-road (lift, wzmocnienia, snorkele, opony)</li>
    </ul>
  </section>

  <section id="galeria">
    <h2>Galeria</h2>
    <p>Wkrótce dodamy zdjęcia naszej pracy, warsztatu i realizacji.</p>
  </section>

  <section id="doswiadczenie" style="text-align: center;">
    <h2>Nasze doświadczenie</h2>
    <div style="font-size: 3rem; color: #FFD700;" id="counter">0</div>
    <p>Lat doświadczenia w branży motoryzacyjnej</p>
  </section>

  <section id="dlaczego-my">
    <h2>Dlaczego warto nas wybrać?</h2>
    <ul style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 2rem;">
      <li><img src="https://cdn-icons-png.flaticon.com/512/2936/2936777.png" width="48"><br>Profesjonalne wyważanie wałów napędowych</li>
      <li><img src="https://cdn-icons-png.flaticon.com/512/685/685655.png" width="48"><br>Konserwacja podwozi</li>
      <li><img src="https://cdn-icons-png.flaticon.com/512/3050/3050525.png" width="48"><br>Modernizacje off-road</li>
      <li><img src="https://cdn-icons-png.flaticon.com/512/5822/5822873.png" width="48"><br>Warsztat z pasją</li>
    </ul>
  </section>

  <section id="kontakt">
    <h2>Kontakt</h2>
    <form>
      <input type="text" name="name" placeholder="Imię i nazwisko" required>
      <input type="email" name="email" placeholder="Email" required>
      <textarea name="message" rows="5" placeholder="Wiadomość" required></textarea>
      <button type="submit">Wyślij</button>
    </form>
    <p>Telefon: <span class="highlight">(tu podasz numer)</span><br>
       Social media: <span class="highlight">(tu podasz linki)</span></p>
  </section>

  <footer>
    <p>&copy; 2025 GR SERWIS. Wszelkie prawa zastrzeżone.</p>
  </footer>
</body>
</html>
