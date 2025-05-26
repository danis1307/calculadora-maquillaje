# Calculadora de presupuesto de maquillaje
<!DOCTYPE html>
<html>
<head>
  <title>Calculadora de presupuesto de maquillaje</title>
</head>
<body>
  <h3>Calculadora de maquillaje</h3>

  <label>Base de maquillaje ($15 c/u): </label>
  <input type="number" id="base" min="0" value="0"><br><br>

  <label>Labial ($10 c/u): </label>
  <input type="number" id="labial" min="0" value="0"><br><br>

  <label>Rubor ($12 c/u): </label>
  <input type="number" id="rubor" min="0" value="0"><br><br>

  <button onclick="calcular()">Calcular total</button>

  <h4>Total: $<span id="total">0</span></h4>

  <script>
    function calcular() {
      let base = parseInt(document.getElementById('base').value) || 0;
      let labial = parseInt(document.getElementById('labial').value) || 0;
      let rubor = parseInt(document.getElementById('rubor').value) || 0;

      let total = (base * 15) + (labial * 10) + (rubor * 12);
      document.getElementById('total').innerText = total;
    }
  </script>
</body>
</html>
