<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Malla Curricular Ingeniería Eléctrica</title>
  <style>
    body {
      font-family: sans-serif;
      padding: 20px;
      background: #f4f4f4;
    }

    h1 {
      text-align: center;
      margin-bottom: 40px;
    }

    .cuatrimestre {
      padding: 20px;
      margin-bottom: 30px;
      border-radius: 12px;
      color: #fff;
    }

    .cuatrimestre h2 {
      margin-top: 0;
    }

    .curso {
      background: #fff;
      color: #000;
      padding: 10px;
      margin: 8px;
      border-radius: 8px;
      border: 1px solid #ccc;
      cursor: pointer;
      transition: 0.3s;
    }

    .curso:hover {
      background-color: #e0f7fa;
    }

    #info {
      background: #fff;
      margin-top: 30px;
      padding: 15px;
      border-radius: 10px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <h1>Malla Curricular - Ingeniería Eléctrica</h1>

  <div class="cuatrimestre" style="background:#2196f3">
    <h2>Cuatrimestre 1</h2>
    <div class="curso" onclick="mostrar('ELEC-01', 'Historia del Arte', 86)">ELEC-01 - Historia del Arte (Nota: 86)</div>
    <div class="curso" onclick="mostrar('AN-304', 'Met. Investigación', 82)">AN-304 - Met. Investigación (Nota: 82)</div>
    <div class="curso" onclick="mostrar('CEM-101', 'Dibujo Técnico', 97)">CEM-101 - Dibujo Técnico (Nota: 97)</div>
    <div class="curso" onclick="mostrar('MA-1101', 'Intro. Cálculo', 71)">MA-1101 - Intro. Cálculo (Nota: 71)</div>
    <div class="curso" onclick="mostrar('CEM-102', 'Intro. Ingeniería', 81)">CEM-102 - Intro. Ingeniería (Nota: 81)</div>
  </div>

  <div class="cuatrimestre" style="background:#4caf50">
    <h2>Cuatrimestre 2</h2>
    <div class="curso" onclick="mostrar('MA-102', 'Cálculo I', 88)">MA-102 - Cálculo I (Nota: 88)</div>
    <div class="curso" onclick="mostrar('FI-201', 'Física I', 72)">FI-201 - Física I (Nota: 72)</div>
    <div class="curso" onclick="mostrar('FI-201L', 'Lab Física I', 78)">FI-201L - Lab Física I (Nota: 78)</div>
    <div class="curso" onclick="mostrar('II-240', 'Probabilidad', 70)">II-240 - Probabilidad (Nota: 70)</div>
    <div class="curso" onclick="mostrar('MA-104', 'Álgebra Lineal', 84)">MA-104 - Álgebra Lineal (Nota: 84)</div>
  </div>

  <!-- Puedes agregar más cuatrimestres aquí -->

  <div id="info">
    <em>Haz clic en un curso para ver más detalles.</em>
  </div>

  <script>
    function mostrar(codigo, nombre, nota) {
      const requisitos = {
        'ELEC-01': 'Sin requisitos',
        'AN-304': 'Sin requisitos',
        'CEM-101': 'Sin requisitos',
        'MA-1101': 'Sin requisitos',
        'CEM-102': 'Sin requisitos',
        'MA-102': 'Requiere MA-1101',
        'FI-201': 'Requiere MA-1101',
        'FI-201L': 'Requiere FI-201',
        'II-240': 'Requiere MA-102',
        'MA-104': 'Requiere MA-102',
      };

      const texto = `
        <h3>${codigo} - ${nombre}</h3>
        <p><strong>Nota:</strong> ${nota}</p>
        <p><strong>Requisitos:</strong> ${requisitos[codigo] || 'No especificado'}</p>
      `;
      document.getElementById("info").innerHTML = texto;
    }
  </script>
</body>
</html>
