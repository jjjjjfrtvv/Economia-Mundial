<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Economía Mundial – Libro Digital</title>
  <style>
    body {
      margin: 0;
      font-family: 'Georgia', serif;
      background: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .book {
      width: 800px;
      height: 500px;
      perspective: 2000px;
      position: relative;
    }
    .cover {
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, #0044cc, #0099ff);
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      font-size: 2em;
      border-radius: 10px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      position: absolute;
      transform-origin: left;
      transition: transform 1s;
      cursor: pointer;
    }
    .cover.open {
      transform: rotateY(-180deg);
    }
    .page {
      width: 100%;
      height: 100%;
      background: white;
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.2);
      position: absolute;
      transform-origin: left;
      transform-style: preserve-3d;
      transition: transform 1s;
      padding: 30px;
      box-sizing: border-box;
      overflow-y: auto;
    }
    .page:nth-child(even) {
      transform: rotateY(180deg);
      z-index: 0;
    }
    .page h2 {
      text-align: center;
      color: #0044cc;
    }
    .controls {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      gap: 10px;
    }
    button {
      background: #0044cc;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 6px;
      cursor: pointer;
      font-size: 1em;
      transition: background 0.3s;
    }
    button:hover {
      background: #002a80;
    }
  </style>
</head>
<body>
  <div class="book" id="book">
    <div class="cover" id="cover">
      <h1>Economía Mundial</h1>
      <p>Siglos XX y XXI</p>
      <p><small>Haz clic para abrir</small></p>
    </div>

    <div class="page">
      <h2>Introducción</h2>
      <p>Este libro digital ofrece un análisis comparativo de la evolución económica de los continentes durante los siglos XX y XXI. Se destacan los modelos de desarrollo, los cambios estructurales y los desafíos contemporáneos.</p>
    </div>

    <div class="page">
      <h2>América</h2>
      <p>Durante el siglo XX, América enfrentó la Gran Depresión, la Guerra Fría y procesos de industrialización. En el siglo XXI, las economías latinoamericanas se han diversificado, aunque persisten desigualdades estructurales.</p>
    </div>

    <div class="page">
      <h2>Asia</h2>
      <p>El auge de Japón, Corea del Sur y posteriormente China transformó el panorama económico mundial. Asia se consolidó como un motor de crecimiento e innovación tecnológica.</p>
    </div>

    <div class="page">
      <h2>Europa</h2>
      <p>La reconstrucción tras la Segunda Guerra Mundial y la creación de la Unión Europea redefinieron el modelo económico europeo. Los retos actuales giran en torno a la energía, la migración y la sostenibilidad.</p>
    </div>

    <div class="page">
      <h2>África</h2>
      <p>África ha transitado de economías coloniales a procesos de integración regional. En el siglo XXI, el continente enfrenta desafíos de infraestructura, educación y equidad.</p>
    </div>

    <div class="page">
      <h2>Conclusiones</h2>
      <p>El estudio comparado de los continentes revela patrones de desarrollo desiguales pero interconectados. La globalización redefine las dinámicas productivas, tecnológicas y sociales.</p>
    </div>
  </div>

  <script>
    const cover = document.getElementById('cover');
    const book = document.getElementById('book');
    const pages = document.querySelectorAll('.page');
    let current = 0;

    cover.addEventListener('click', () => {
      cover.classList.add('open');
      setTimeout(() => {
        pages[current].style.transform = 'rotateY(-180deg)';
      }, 800);
    });

    document.body.addEventListener('keydown', (e) => {
      if (e.key === 'ArrowRight' && current < pages.length - 1) {
        pages[current].style.transform = 'rotateY(-180deg)';
        current++;
      }
      if (e.key === 'ArrowLeft' && current > 0) {
        pages[current - 1].style.transform = 'rotateY(0deg)';
        current--;
      }
    });
  </script>
</body>
</html>
