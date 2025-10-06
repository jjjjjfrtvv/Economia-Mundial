<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Economía Mundial — Siglos XX y XXI</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", Arial, sans-serif;
      background: #f4f4f4;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      width: 100%;
      text-align: center;
      background: linear-gradient(90deg, #1f60b5, #3c8bff);
      color: white;
      padding: 2rem 1rem;
      box-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }

    h1 {
      margin: 0;
      font-size: 2rem;
    }

    .book {
      width: 90%;
      max-width: 800px;
      height: 500px;
      margin: 3rem auto;
      perspective: 2000px;
      position: relative;
    }

    .page {
      width: 100%;
      height: 100%;
      background: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
      position: absolute;
      top: 0;
      left: 0;
      transition: transform 1s;
      transform-origin: left;
      backface-visibility: hidden;
      padding: 2rem;
      box-sizing: border-box;
      overflow-y: auto;
    }

    .page img {
      max-width: 100%;
      border-radius: 8px;
      margin: 1rem 0;
    }

    .page:nth-child(even) {
      transform: rotateY(-180deg);
    }

    .book.open .page:nth-child(even) {
      transform: rotateY(0deg);
    }

    .page h2 {
      color: #1f60b5;
      border-bottom: 2px solid #3c8bff;
      padding-bottom: 0.5rem;
    }

    .controls {
      margin: 1rem;
    }

    button {
      background: #1f60b5;
      color: white;
      border: none;
      padding: 0.7rem 1.5rem;
      margin: 0 0.5rem;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background: #3c8bff;
    }

    /* Portada */
    .cover {
      background: linear-gradient(135deg, #004aad, #007bff);
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }

    .cover h1 {
      font-size: 2.2rem;
      margin-bottom: 1rem;
    }

    .cover p {
      font-size: 1.2rem;
      max-width: 600px;
    }
  </style>
</head>
<body>
  <header>
    <h1>📘 Economía Mundial — Siglos XX y XXI</h1>
  </header>

  <div class="book" id="book">
    <div class="page cover">
      <h1>Economía Mundial</h1>
      <p>Un recorrido histórico por la evolución económica global durante los siglos XX y XXI.</p>
      <img src="https://upload.wikimedia.org/wikipedia/commons/6/6a/World_map_blank_without_borders.svg" alt="Mapa del mundo">
    </div>

    <div class="page">
      <h2>Introducción</h2>
      <p>Durante los siglos XX y XXI, la economía mundial ha pasado por transformaciones profundas. Desde la Revolución Industrial tardía hasta la era digital, los países han experimentado globalización, crisis y avances tecnológicos sin precedentes.</p>
    </div>

    <div class="page">
      <h2>América</h2>
      <p>En América, la economía ha estado marcada por el desarrollo industrial de EE. UU., la dependencia de materias primas en América Latina, y los esfuerzos de integración regional como el MERCOSUR o el T-MEC.</p>
    </div>

    <div class="page">
      <h2>Europa</h2>
      <p>Europa fue el epicentro de las grandes guerras, pero también del resurgimiento económico con la Unión Europea. El euro y el mercado común transformaron la integración regional.</p>
    </div>

    <div class="page">
      <h2>Asia y África</h2>
      <p>Asia se consolidó como motor industrial y tecnológico, con China, Japón y Corea del Sur a la cabeza. África, por su parte, enfrenta desafíos estructurales, aunque con un potencial enorme gracias a sus re
