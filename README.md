<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portafolio - Mis Habilidades</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f4f6f9;
      margin: 0;
      padding: 20px;
      color: #333;
    }
    h1 {
      text-align: center;
      margin-bottom: 30px;
    }
    h2 {
      margin-top: 40px;
      color: #222;
    }
    .skills-category {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 25px;
      margin-top: 20px;
    }
    .skill {
      text-align: center;
    }
    .circle {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 10px;
      font-weight: bold;
      font-size: 18px;
      position: relative;
      background: conic-gradient(#4CAF50 calc(var(--percent) * 1%), #ddd 0%);
    }
    .circle::after {
      content: "";
      width: 90px;
      height: 90px;
      background: #fff;
      border-radius: 50%;
      position: absolute;
    }
    .circle span {
      position: absolute;
    }
  </style>
</head>
<body>
  <h1>Mis Habilidades</h1>

  <!-- Business Analytics -->
  <h2>Business Analytics</h2>
  <div class="skills-category">
    <div class="skill">
      <div class="circle" style="--percent: 85;">
        <span>85%</span>
      </div>
      <p>Power BI</p>
    </div>
    <div class="skill">
      <div class="circle" style="--percent: 80;">
        <span>80%</span>
      </div>
      <p>SQL Server</p>
    </div>
    <div class="skill">
      <div class="circle" style="--percent: 70;">
        <span>70%</span>
      </div>
      <p>Tableau</p>
    </div>
  </div>

  <!-- Business Intelligence -->
  <h2>Business Intelligence</h2>
  <div class="skills-category">
    <div class="skill">
      <div class="circle" style="--percent: 75;">
        <span>75%</span>
      </div>
      <p>MS Project</p>
    </div>
  </div>

  <!-- Ofimática -->
  <h2>Ofimática</h2>
  <div class="skills-category">
    <div class="skill">
      <div class="circle" style="--percent: 95;">
        <span>95%</span>
      </div>
      <p>Word</p>
    </div>
    <div class="skill">
      <div class="circle" style="--percent: 90;">
        <span>90%</span>
      </div>
      <p>Excel</p>
    </div>
    <div class="skill">
      <div class="circle" style="--percent: 85;">
        <span>85%</span>
      </div>
      <p>PowerPoint</p>
    </div>
  </div>
</body>
</html>
