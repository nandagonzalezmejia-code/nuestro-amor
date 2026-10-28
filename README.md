# nuestro-amor
una sorpresa hecha con amor para ti
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para mi persona favorita 💗</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: Georgia, serif;
  background: linear-gradient(135deg, #ffd6e7, #f9a8d4, #e9c8ff);
  color: #84365e;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  overflow-x: hidden;
  padding: 25px 15px;
}

.card {
  background: rgba(255,255,255,0.82);
  max-width: 520px;
  width: 100%;
  padding: 35px 24px;
  border-radius: 30px;
  box-shadow: 0 15px 45px #a64c7b38;
  border: 2px solid white;
  position: relative;
  z-index: 2;
}

.heart {
  font-size: 65px;
  animation: latir 1.2s infinite;
}

h1 {
  font-size: 32px;
  color: #c0447c;
}

.subtitle {
  font-size: 18px;
  line-height: 1.8;
}

button {
  background: linear-gradient(45deg, #e75496, #b66be8);
  color: white;
  border: none;
  padding: 15px 24px;
  border-radius: 30px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 18px;
  box-shadow: 0 5px 15px #d88bb9;
}

button:hover {
  transform: scale(1.05);
}

#carta {
  display: none;
  line-height: 1.9;
  font-size: 17px;
  margin-top: 25px;
  animation: aparecer 1s ease;
}

.firma {
  font-style: italic;
  color: #c0447c;
  font-size: 19px;
}

.flotante {
  position: fixed;
  bottom: -40px;
  font-size: 24px;
  animation: subir 8s linear infinite;
  pointer-events: none;
  z-index: 1;
}

@keyframes latir {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.18); }
}

@keyframes subir {
  to {
    transform: translateY(-115vh) rotate(360deg);
    opacity: 0;
  }
}

@keyframes aparecer {
  from { opacity: 0; transform: translateY(15px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>
</head>

<body>

<div class="card">
  <div class="heart">💗</div>

  <h1>Para mi persona favorita</h1>

  <p class="subtitle">
    Si pudiera elegir mil veces,<br>
    mil veces encontraría mi camino hacia ti. ✨
  </p>

  <p>Preparé una pequeña sorpresa para ti...</p>

  <button onclick="abrirCarta()">
    💌 Abre tu cartita
  </button>

  <div id="carta">
    <h2>Mi lugar favorito eres tú 🥹❤️</h2>

    No sé cómo explicarte todo lo que siento,
    pero desde que llegaste a mi vida,
    hay momentos que se volvieron inolvidables
    simplemente porque estás tú.

    <br><br>

    Quiero seguir coleccionando recuerdos contigo,
    reírnos por tonterías, abrazarte cuando lo necesites
    y recordarte que eres alguien muy especial para mí.

    <br><br>

    No necesito que todo sea perfecto.
    Solo quiero que lo nuestro tenga amor,
    sinceridad, detalles y ganas de seguir eligiéndonos.

    <br><br>

    <span class="firma">
      Si volviera a comenzar mi historia,<br>
      ojalá volviera a encontrarte. 💗<br><br>
      Con todo mi cariño, para ti. ♾️
    </span>
  </div>
</div>

<script>
function abrirCarta() {
  const carta = document.getElementById("carta");
  carta.style.display = "block";
  document.querySelector("button").textContent =
    "💖 Mi corazón es tuyo";

  for (let i = 0; i < 18; i++) {
    setTimeout(() => {
      const corazon = document.createElement("div");
      corazon.className = "flotante";
      corazon.textContent =
        ["💗", "💕", "💖", "✨", "💘"][Math.floor(Math.random() * 5)];
      corazon.style.left = Math.random() * 100 + "vw";
      corazon.style.animationDuration = (4 + Math.random() * 4) + "s";
      document.body.appendChild(corazon);
      setTimeout(() => corazon.remove(), 8500);
    }, i * 120);
  }
}
</script>

</body>
</html>
