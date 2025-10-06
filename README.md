<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Economía Mundial — Libro Interactivo</title>

  <!-- Estilos del libro -->
  <style>
    body {
      background: linear-gradient(135deg, #007bff, #00b4d8);
      margin: 0;
      font-family: 'Georgia', serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
    }

    .book {
      width: 800px;
      height: 500px;
      perspective: 2000px;
      position: relative;
    }

    .page {
      width: 400px;
      height: 100%;
      background: white;
      position: absolute;
      top: 0;
      left: 50%;
      transform-origin: left;
      transition: transform 1s ease;
      box-shadow: 0 0 15px rgba(0,0,0,0.3);
      border-radius: 5px;
    }

    .page-content {
      padding: 30px;
      overflow-y: auto;
      height: 100%;
    }

    .cover {
      background: linear-gradient(135deg, #004e92, #000428);
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2em;
      font-weight: bold;
      text-align: center;
    }

    .cover h1 {
      font-size: 2.3em;
      line-height: 1.2em;
      padding: 20px;
    }

    .controls {
      position: absolute;
      bottom: 20px;
      display: flex;
      width: 100%;
      justify-content: space-between;
      padding: 0 50px;
    }

    button {
      background: #007bff;
      border: none;
      color: white;
      font-size: 1em;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background: #0056b3;
    }
  </style>
</head>

<body>
  <div class="book">
    <!-- Portada -->
    <div class="page cover">
      <h1>Economía Mundial<br>Siglos XX y XXI</h1>
    </div>

    <!-- Página 1 -->
    <div class="page">
      <div class="page-content">
        <h2>Introducción</h2>
        <p>
          Este libro digital ofrece un análisis comparativo de la evolución económica mundial
          durante los siglos XX y XXI. Se abordan los principales modelos de desarrollo,
          transformaciones estructurales y los efectos de la globalización.
        </p>
        <p>
          La metodología combina análisis histórico, comparativo y estudios de caso por continente.
          El enfoque es didáctico y busca resaltar causas, consecuencias y lecciones aprendidas.
        </p>
      </div>
    </div>

    <!-- Página 2 -->
    <div class="page">
      <div class="page-content">
        <h2>América</h2>
        <p>
          En el siglo XX, América experimentó la Gran Depresión, la industrialización sustitutiva
          de importaciones y la influencia de la Guerra Fría. En el siglo XXI, la región enfrenta
          desafíos de desigualdad, deuda y dependencia de materias primas.
        </p>
      </div>
    </div>

    <!-- Página 3 -->
    <div class="page">
      <div class="page-content">
        <h2>Europa</h2>
        <p>
          Europa fue el epicentro de dos guerras mundiales y la posterior reconstrucción económica.
          Con la Unión Europea, surgió un modelo de integración regional único. Hoy enfrenta retos
          de envejecimiento poblacional y transición energética.
        </p>
      </div>
    </div>

    <!-- Página 4 -->
    <div class="page">
      <div class="page-content">
        <h2>Conclusiones</h2>
        <p>
          La economía mundial ha pasado por profundas transformaciones. El futuro dependerá
          de la cooperación internacional, la sostenibilidad y la innovación tecnológica.
        </p>
      </div>
    </div>

    <!-- Botones -->
    <div class="controls">
      <button id="prev">⬅ Atrás</button>
      <button id="next">Siguiente ➡</button>
    </div>
  </div>

  <!-- Script de animación -->
  <script>
    const pages = document.querySelectorAll('.page');
    const next = document.getElementById('next');
    const prev = document.getElementById('prev');
    let current = 0;

    next.addEventListener('click', () => {
      if (current < pages.length - 1) {
        pages[current].style.transform = 'rotateY(-180deg)';
        current++;
      }
    });

    prev.addEventListener('click', () => {
      if (current > 0) {
        current--;
        pages[current].style.transform = 'rotateY(0deg)';
      }
    });
  </script>
</body>
</html>
