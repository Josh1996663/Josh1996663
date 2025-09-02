<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Portafolio Joshua</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f9;
      color: #333;
      text-align: center;
      padding: 30px;
    }
    h1 {
      margin-bottom: 40px;
    }
    h2 {
      margin: 30px 0 15px;
      color: #444;
      border-bottom: 2px solid #ccc;
      display: inline-block;
      padding-bottom: 5px;
    }
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 30px;
      margin-top: 20px;
    }
    .skill {
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    canvas {
      width: 150px !important;
      height: 150px !important;
    }
    .label {
      margin-top: 10px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>💼 Portafolio de Habilidades - Joshua</h1>

  <!-- Business Analytics -->
  <h2>📊 Business Analytics</h2>
  <div class="skills-grid">
    <div class="skill">
      <canvas id="sql"></canvas>
      <div class="label">SQL Server (95%)</div>
    </div>
    <div class="skill">
      <canvas id="python"></canvas>
      <div class="label">Python (85%)</div>
    </div>
    <div class="skill">
      <canvas id="msproject"></canvas>
      <div class="label">MS Project (90%)</div>
    </div>
  </div>

  <!-- Business Intelligence -->
  <h2>📈 Business Intelligence</h2>
  <div class="skills-grid">
    <div class="skill">
      <canvas id="powerbi"></canvas>
      <div class="label">Power BI (95%)</div>
    </div>
    <div class="skill">
      <canvas id="tableau"></canvas>
      <div class="label">Tableau (80%)</div>
    </div>
  </div>

  <!-- Ofimática -->
  <h2>🖥️ Ofimática</h2>
  <div class="skills-grid">
    <div class="skill">
      <canvas id="word"></canvas>
      <div class="label">Word (90%)</div>
    </div>
    <div class="skill">
      <canvas id="excel"></canvas>
      <div class="label">Excel (95%)</div>
    </div>
    <div class="skill">
      <canvas id="powerpoint"></canvas>
      <div class="label">PowerPoint (85%)</div>
    </div>
  </div>

  <script>
    function crearGrafico(id, porcentaje, color) {
      new Chart(document.getElementById(id), {
        type: 'doughnut',
        data: {
          datasets: [{
            data: [porcentaje, 100 - porcentaje],
            backgroundColor: [color, '#e6e6e6'],
            borderWidth: 0
          }]
        },
        options: {
          cutout: '75%',
          plugins: {
            tooltip: { enabled: false },
            legend: { display: false },
            beforeDraw: (chart) => {
              const {width} = chart;
              const ctx = chart.ctx;
              ctx.restore();
              ctx.font = "bold 18px Arial";
              ctx.textBaseline = "middle";
              const text = porcentaje + "%";
              const textX = Math.round((width - ctx.measureText(text).width) / 2);
              const textY = chart._metasets[0].data[0].y;
              ctx.fillText(text, textX, textY);
              ctx.save();
            }
          }
        }
      });
    }

    // Llamamos a la función para cada habilidad
    crearGrafico("sql", 95, "#00758F");
    crearGrafico("python", 85, "#3776AB");
    crearGrafico("msproject", 90, "#217346");

    crearGrafico("powerbi", 95, "#F2C811");
    crearGrafico("tableau", 80, "#1F77B4");

    crearGrafico("word", 90, "#2B579A");
    crearGrafico("excel", 95, "#217346");
    crearGrafico("powerpoint", 85, "#B7472A");
  </script>
</body>
</html>
