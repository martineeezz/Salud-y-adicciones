<!DOCTYPE html>
<html>
<html lang="es">
<head>
<img>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Salud y Drogas</title>
    <link rel="stylesheet" href="stilo.css">
    <title>Política de privacidad</title>
    <style>
        body{
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            background-color: #ffffff;
            margin: 0;
            padding: 0;
            color: #000000;
            text-align: center;
        }

        header {
            background-color: #20b2aa;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            background-color: #1d9e98;
            overflow: hidden;
            text-align: center;
            padding: 1%;
        }
        section {
            padding: 20px;
            margin: 10px;
        }
        section h2 {
            color: #000000;
        }
        section p, section li {
            line-height: 1.6;
        }
        h1 {
            color: #ffffff;
        }
        ul {
            list-style-type: square;
        }
        form {
            background-color: #e0ffff;
            padding: 20px;
            border-radius: 5px;
            margin-top: 20px;
        }
        form label {
            display: block;
            margin-top: 10px;
        }
        form input, form textarea, form button {
            display: block;
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        form button {
            background-color: #20b2aa;
            color: white;
            border: none;
            cursor: pointer;
        }
        form button:hover {
            background-color: #008080;
        }
        .test-section {
            margin-bottom: 20px;
        }
        .test-section h2 {
            margin-top: 0;
        }
        footer {
            background-color: #008080;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        footer a {
            color: #e0ffff;
            text-decoration: none;
            text-align: center;
        }
        footer a:hover {
            text-decoration: underline;
        }
        .popup {
			position: fixed;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			width: 80%;
			max-width: 400px;
			background: white;
			padding: 20px;
			box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
			border-radius: 5px;
			z-index: 9999;
			display: none;
		}
		.overlay {
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
			height: 100%;
			background: rgba(0, 0, 0, 0.5);
			z-index: 9998;
			display: none;
		}
        #consejo-container {
    width: 80%;
    max-width: 600px;
    margin: 50px auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  #lista-actividades {
    width: 80%;
    max-width: 600px;
    margin: 50px auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  #frase-container {
    width: 80%;
    max-width: 600px;
    margin: 50px auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
    
    </style>
</head>
<body>
    <header>
        <h1>Salud y Drogas</h1>
    </header>
    <nav>
        <a href="#inicio">Introducción</a>
        <a href="#efectos">Efectos</a>
        <a href="#prevencion">Prevenciónes y preguntas</a>
    </nav>
    <body>
        <button
        onclick="cambiarColor ()">Cambiar Color de Fondo</button>
        <script>
        function cambiarColor() {
        document.body.style.backgroundColor ="turquoise";
        }
        </script> 
        </body>
    <button onclick="mostrarPopup()">Ver política de privacidad</button>

<div class="popup" id="popup">
	<h2>Política de privacidad</h2>
	<p>1. Recolección de Información
        Recopilamos información personal como nombre, correo electrónico y datos médicos a través de formularios y consultas en línea para brindar un servicio personalizado.</p>
        2. Uso de la Información
        Utilizamos la información para mejorar nuestros servicios, enviar información relevante, responder a consultas y proporcionar apoyo y seguimiento.</p>
        3. Protección de Datos
        Implementamos medidas de seguridad para proteger la información contra accesos no autorizados, alteraciones, divulgaciones o destrucción. Solo el personal autorizado tiene acceso a estos datos.</p>
        4. Compartición de Información
        No compartimos información personal con terceros sin el consentimiento del usuario, excepto cuando es requerido por ley o para proporcionar servicios solicitados por el usuario.</p>
        5. Derechos del Usuario
        Los usuarios tienen el derecho de acceder, corregir y eliminar su información personal en cualquier momento, así como de retirar su consentimiento para el uso de sus datos.</p>
	<button onclick="cerrarPopup()">Aceptar</button>
</div>
<div id="consejo-container">
    <h2>Consejo del día:</h2>
    <p id="consejo"></p>
  </div>
  
  <script>
    var consejos = [
      "Practica la meditación diaria para mantener la calma.",
      "Busca el apoyo de amigos y familiares en tu proceso de recuperación.",
      "Identifica tus desencadenantes y evita situaciones que te lleven a recaer.",
      "Busca ayuda profesional de un terapeuta especializado en adicciones.",
      "Encuentra actividades saludables que te apasionen para remplazar el comportamiento adictivo.",
      "Aprende técnicas de respiración profunda para controlar la ansiedad.",
      "Establece metas realistas y celebra tus logros, por pequeños que sean.",
      "Practica el autocuidado y dedica tiempo para ti mismo cada día.",
      "Participa en grupos de apoyo para compartir experiencias y aprender de otros.",
      "Recuerda que cada día es una nueva oportunidad para empezar de nuevo."
    ];
  
    
    function obtenerConsejoAleatorio() {
      var index = Math.floor(Math.random() * consejos.length);
      return consejos[index];
    }
  
    document.getElementById("consejo").textContent = obtenerConsejoAleatorio();
  </script>
  <div id="frase-container">
    <h2>Frases Motivadoras</h2>
    <p id="frase"></p>
    <button onclick="generarFrase()">Generar Frase</button>
  </div>
  
  <script>
    var frases = [
      "El éxito es la suma de pequeños esfuerzos repetidos día tras día.",
      "Cree en ti mismo y todo será posible.",
      "El único lugar donde el éxito viene antes que el trabajo es en el diccionario.",
      "Nunca es demasiado tarde para ser lo que podrías haber sido.",
      "El optimismo es la fe que conduce al logro. Nada puede hacerse sin esperanza y confianza.",
      "El camino hacia el éxito y el camino hacia el fracaso son casi exactamente iguales."
    ];
  
    function generarFrase() {
      var index = Math.floor(Math.random() * frases.length);
      document.getElementById("frase").textContent = frases[index];
    }
  
    
    generarFrase();
  </script>

<div class="overlay" id="overlay"></div>

<script>
	function mostrarPopup() {
		document.getElementById("popup").style.display = "block";
		document.getElementById("overlay").style.display = "block";
	}

	function cerrarPopup() {
		document.getElementById("popup").style.display = "none";
		document.getElementById("overlay").style.display = "none";
	}
</script>
    <section id="inicio">
        <h2>Introducción</h2>
        <p>En esta página web nos encargamos de atender la salud física y mental de cualquier paciente, ya sea con problemas psicológicos, de drogas, alcoholismo, estrés, etc. 
            Cualquier problema mencionado anteriormente afecta gradualmente la salud, dejando al paciente sin posibilidad de salvar lo que algún día podría haber llegado a ser.</p>
         
    <section id="efectos">
        <h2>Efectos de las Drogas</h2>
        <p>Las drogas actúan sobre los neurotransmisores alterando y perturbando el correcto funcionamiento, afectando a la conducta, estado de ánimo o percepción. Además, son susceptibles de crear dependencia física y/o psicológica.</p>

    </section>
    <section id="prevencion">
        <h2>Prevención</h2>
        <ul>
            <p>Fomentar la autoestima desde la infancia; los padres deben estar atentos a la forma en que se desarrolla la autoestima de sus hijos.</p>
            <p>Es importante acompañarlos, quererlos, entenderlos y en todo momento comunicarse con ellos.</p>
            <p>Hay que adoptar medidas que estimulen que el niño tenga un buen concepto de sí mismo, lo que es un factor que tiene un gran impacto</p> 
            <p>Mantener una buena comunicación con los padres es una forma de reducir el miedo y la incertidumbre de los hijos frente a todos los cambios que ocurren en su cuerpo y en su mente en la adolescencia.</p>
        </ul>
    </section>
    <section id="saludmental">
        <h2>Salud Mental</h2>
        
        <h3>Datos y números de la salud del adolescente en México</h3>
        <p>En México, se estima que el 15% de los adolescentes entre 12 y 17 años han experimentado algún trastorno mental. La depresión y la ansiedad son los problemas más comunes en este grupo de edad.</p>
        
        <h3>Factores que afectan la salud mental en los adolescentes</h3>
        <p>Los factores que pueden influir en la salud mental de los adolescentes incluyen el estrés escolar, problemas familiares, bullying, presiones sociales y cambios hormonales.</p>
        
        <h3>¿Qué es el trastorno emocional?</h3>
        <p>El trastorno emocional se refiere a condiciones como la depresión y la ansiedad, que afectan el estado emocional de una persona y pueden interferir con su capacidad para llevar una vida normal.</p>
        
        <h3>¿Qué es el trastorno de comportamiento?</h3>
        <p>Los trastornos de comportamiento incluyen conductas disruptivas y desafiantes, como el trastorno de déficit de atención con hiperactividad (TDAH) y el trastorno de conducta, que pueden afectar el desempeño académico y las relaciones personales.</p>
        
        <h3>¿Qué es el trastorno alimenticio?</h3>
        <p>Los trastornos alimenticios, como la anorexia, la bulimia y el trastorno por atracón, implican comportamientos alimenticios extremos y preocupaciones obsesivas con el peso y la figura corporal.</p>
        
        <h3>Promoción y Prevención para el control de emociones y Salud Mental</h3>
        <p>La promoción de la salud mental y la prevención de trastornos incluyen programas escolares de bienestar emocional, actividades extracurriculares y apoyo psicológico para manejar el estrés y las emociones.</p>
    <section id="prevencionadicciones">
        <h2>Prevención y Control de Adicciones</h2>
        
        <h2>Datos y cifras de adicciones: </h2>
        <p>Según la Encuesta Nacional de Consumo de Drogas, Alcohol y Tabaco (ENCODAT), el 17% de los adolescentes han probado alguna droga ilícita, con el alcohol y el tabaco siendo las sustancias más comunes.</p>
        
        <h2>Principales adicciones: </h2>
        <p>Las principales adicciones entre los adolescentes mexicanos incluyen el consumo de alcohol, tabaco, marihuana y, en menor medida, drogas sintéticas como el éxtasis.</p>
        
        <h2>Cómo influyen las adicciones: </h2>
        <p>Las adicciones pueden agravar o desencadenar problemas de salud mental como la depresión, la ansiedad y otros trastornos emocionales, creando un ciclo difícil de romper.</p>
        
        <h2>Recomendaciones: </h2>
        <p>Para prevenir las adicciones en adolescentes, se recomienda la educación temprana sobre los riesgos, el fomento de actividades recreativas saludables, y la vigilancia y apoyo de los padres y educadores.</p>
        
    </section>
    <div id="lista-actividades">
        <h2>Lista de Actividades para Prevenir Adicciones</h2>
        <ul id="actividades">
          <li><input type="checkbox" id="actividad1"><label for="actividad1">Practicar ejercicio físico regularmente.</label></li>
          <li><input type="checkbox" id="actividad2"><label for="actividad2">Mantener una dieta equilibrada y saludable.</label></li>
          <li><input type="checkbox" id="actividad3"><label for="actividad3">Participar en actividades sociales y recreativas.</label></li>
          <li><input type="checkbox" id="actividad4"><label for="actividad4">Buscar apoyo emocional en amigos y familiares.</label></li>
          <li><input type="checkbox" id="actividad5"><label for="actividad5">Desarrollar habilidades de afrontamiento para manejar el estrés.</label></li>
          <li><input type="checkbox" id="actividad6"><label for="actividad6">Buscar ayuda profesional si es necesario.</label></li>
        </ul>
      </div>
    <section>
            </section>
            <h1>Cuestionario de Autoevaluación: Prevención de Drogas y Salud Mental</h1>

<form action="#" method="post">
  
  <fieldset>
    <legend>Pregunta 1</legend>
    <label for="pregunta1">¿Estás informado sobre los riesgos asociados al consumo de drogas?</label><br>
    <input type="radio" id="pregunta1a" name="pregunta1" value="si">
    <label for="pregunta1a">Sí</label><br>
    <input type="radio" id="pregunta1b" name="pregunta1" value="no">
    <label for="pregunta1b">No</label><br>
  </fieldset>
  
  <fieldset>
    <legend>Pregunta 2</legend>
    <label for="pregunta2">¿Realizas actividades para cuidar tu salud mental, como ejercicio o meditación?</label><br>
    <input type="radio" id="pregunta2a" name="pregunta2" value="si">
    <label for="pregunta2a">Sí</label><br>
    <input type="radio" id="pregunta2b" name="pregunta2" value="no">
    <label for="pregunta2b">No</label><br>
  </fieldset>
  
  <fieldset>
    <legend>Pregunta 3</legend>
    <label for="pregunta3">¿Conoces a alguien que esté luchando contra la adicción a las drogas?</label><br>
    <input type="radio" id="pregunta3a" name="pregunta3" value="si">
    <label for="pregunta3a">Sí</label><br>
    <input type="radio" id="pregunta3b" name="pregunta3" value="no">
    <label for="pregunta3b">No</label><br>
  </fieldset>
  
  <fieldset>
    <legend>Pregunta 4</legend>
    <label for="pregunta4">¿Te sientes cómodo buscando ayuda profesional si la necesitas?</label><br>
    <input type="radio" id="pregunta4a" name="pregunta4" value="si">
    <label for="pregunta4a">Sí</label><br>
    <input type="radio" id="pregunta4b" name="pregunta4" value="no">
    <label for="pregunta4b">No</label><br>
  </fieldset>
  
 
    <form action="guardar_datos.php" method="POST">
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required>
        <label for="correo">Correo electrónico:</label>
        <input type="email" id="correo" name="correo" required>
        <label for="mensaje">Mensaje:</label>
        <textarea id="mensaje" name="mensaje" required></textarea>
        <input type="submit" value="Enviar">
 
    </form>

    <section>
        <head>
            <title>Validar Formulario</title>
              </head>
               <body>
                 <form onsubmit="returnvalidarFormulario()">
            Comentario: <input type="text"id="nombre"><br>
            
            <input type="submit"value="Enviar">
            </form>
            
            <form id="commentForm" onsubmit="submitComment(event)">
                <textarea id="comment" required></textarea><br><br>
                <button type="submit">Enviar Comentario</button>
            </form>
        
            <script>
                function submitComment(event) {
                    event.preventDefault(); // Evita el envío del formulario
                    const comment = document.getElementById('comment').value;
                    if (comment.trim() !== '') {
                        alert('Comentario enviado');
                        document.getElementById('commentForm').reset(); // Limpia el formulario
                    }
                }
            </script>
            </script>
            </body>
            </html>
<style>
                .hidden {
                  display: none;
                }
              </style>
              </head>
              <body>
              <h1>Mostrar u ocultar información</h1>
              <button onclick="toggleInfo('section1')">Mostrar/Ocultar </button>
              <button onclick="toggleInfo('section2')">Mostrar/Ocultar</button>
              
              <section id="section1" class="hidden">
                <h2>Acerca de nosotros:</h2>
                <p>Jair Andre Martinez jimenez<br>
                    Elias Izael Piña Delgado <br>
                    Angel Israel Delgado osorio <br>
                    Jose Carlo Gaytan Velazques<br>
                    Axel Gabriel Hernandez Pacheco<br>
                    Jorge Alejandro España Loyola<br>
              </section>
              
              <section id="section2" class="hidden">
                <h2>Con ayuda de:</h2>
                <p>Cecytem Coacalco<br>
                    Maestra Aurora Yolanda Garcia Ulloa</p>
              </section>
              
              <script>
                function toggleInfo(sectionId) {
                  const section = document.getElementById(sectionId);
                  if (section.classList.contains('hidden')) {
                    section.classList.remove('hidden');
                  } else {
                    section.classList.add('hidden');
                  }
                }
              </script>
              </body>
</section>
    <head>
        <title>Adicciones</title>
        </head>
        <body>
        
        <h1>Información sobre las adicciones</h1>
        
        <p>Las adicciones son un problema grave que afecta a muchas personas en el mundo. Es importante buscar ayuda para superar cualquier tipo de adicción.</p>
        
        <button onclick="mostrarAyuda()">¿Necesitas ayuda?</button>
        
        <p id="ayuda" style="display:none;">Si necesitas ayuda para superar una adicción, no dudes en contactar a un profesional de la salud o a un grupo de apoyo. Recuerda que no estás solo en esta lucha.</p>
        
        <script>
        function mostrarAyuda() {
          document.getElementById("ayuda").style.display = "block";
        }
        </script>
        
        </body>
    <p>En México, algunas instituciones reconocidas para el tratamiento de adicciones son:</p>
    <ul>
        <p><a href="https://www.conadic.salud.gob.mx">Consejo Nacional contra las Adicciones (CONADIC)</a></p>
        <p><a href="https://www.centromedicoabc.com">Centro Médico ABC</a></p>
        <p><a href="https://www.fundacionbest.org.mx">Fundación Best</a></p>
    </ul>
    <script>
        document.getElementById('testForm').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Gracias por completar el test. Sus respuestas han sido enviadas.');
        });
    </script>
</body>
</html>
