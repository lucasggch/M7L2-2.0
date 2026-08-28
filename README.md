Instala las librerías necesarias
Instala discord para crear el bot.
Usa PIL para abrir y modificar imágenes.
Usa numpy para manejar los datos de las imágenes.
Usa tf_keras para cargar el modelo de inteligencia artificial.
Carga el modelo de IA
El programa utiliza keras_model.h5, que contiene el modelo entrenado.
También utiliza labels.txt, donde están los nombres de las clases que puede reconocer.
Prepara la imagen
Cuando recibe una imagen, la convierte a RGB.
La ajusta a un tamaño de 224 × 224 píxeles.
Normaliza los valores de los píxeles para que puedan ser utilizados por la red neuronal.
La IA analiza la imagen
El modelo hace una predicción.
np.argmax() busca cuál es la clase con mayor probabilidad.
Después obtiene el nombre de esa clase y el porcentaje/probabilidad de confianza.
Crea el bot de Discord
El bot utiliza $ como prefijo para los comandos.
Tiene un comando $hello que responde saludando.
Comando $check
Si mandás una imagen junto con $check, el bot:
Guarda la imagen.
Confirma que fue guardada.
La pasa al modelo de IA.
Devuelve qué clase detectó y su probabilidad.
Si no mandás ninguna imagen, responde que no se envió una.
📌 En resumen

Discord → imagen → procesamiento → modelo de IA → predicción → respuesta del bot.

Por ejemplo:

$check + foto
⬇️
🤖 El bot guarda la foto
⬇️
🧠 La IA la analiza
⬇️
📊 Elige la clase más probable
⬇️
💬 El bot responde algo como: “Clase: X — Probabilidad: 99%”
