# Study for Exam

## Inteligencia Artifical:

La inteligencia artificial es la imitación de características humanas, desde `El Habla`, `La Escucha`, `La Vision` y `El Procesamiento`, el punto es brindarle información a la AI que esta lo procese para poder lograr predecir o tomar decisiones con base en una predicción.
_Todo esto se hace por medio del azure machine learning_

Por medio del **Azure Studio** podremos empezar a crear un workspace que es el espacio donde podremos entrenar y testear nuestra AI,Dentro de este espacio tendremos que porvisionarnos de:

* Computación
* Datasets

Con esto podremos entrenar a los diferentes servicios con los que contamos.
Tenemos a grandes rasgos dos maneras específicas de entrenarlos:

Cuando tenemos data supervisada osea ya procesada y preparada para que el servicio que estemos ejecutando pueda procesarla de manera clara:

* **Entrenamiento por regression:** Este devolverá un `valor númerico` con base en la información con la que es alimentada.
* **Entrenamiento por classification:** Este devolverá `un grupo` en el que pueda categorizar a algo por ejemplo una fruta circular y roja lo clasificará como manzana.
* **Entrenamiento por Time Series:** Este devolverá un `valor a futuro` por ejemplo del valor de un auto en unos años.

Cuando tenemos data no supervisada:

* **Entrenamiento por Category:** Este devolverá una asociación de datos segun su análisis.

Tras pasar toda la data por este proceso puedo empezar a lanzar el proyecto a deploy, esto obviamente para testing y finalmente llevarlo al usuario final, se puede hacer en contenedores de Azure o con el servicio de testing AKS / ACI

Al lanzarlo el cliente final tendrás que tener un endpoint, clave del endpoint, y el proyecto y modelo.
Necesitarás estos elementos para poder generar conexiones a los proyectos que tengas montados.

### Los 6 Principios de Uso

Existen 6 principios de Uso para poder brindar una AI de un correcto funcionamiento:

* **Fairness (Justicia):** Sin ningun tipo de imparcialidad o sesgo (bias)
* **Reliability and Safety (Fiabilidad y Seguridad):** Construir rigurosos sistemas de testing que puedan brindar confianza.
* **Privacy and Security (Privacidad y Seguridad):** No permitir que los datos salgan o goteen, que se mantengan en el entrenamiento y aprendizaje.
* **Inclusive (Inclusivo):** Debe estar disponible para todos los sectores sociales sin importar distinción.
* **Transparency (Transparencia):** Debe quedar muy claro sus limitaciones y funcionamiento para que las personas que lo usan tengan presente en que condiciones y hasta donde han de usarlo.
* **Accountability (Rendir cuentas):** Que toda AI tenga parámetros éticos por los cuales no haya inconvenientes legales, poder rendir cuentas sin culpas o en caso tal poder sobrellevar problemas legales.

## Serivicios

### Vision Services

* **Image Classification:** Esta toma una imagen y puede determinar que hay en la imagen o da una descripción de la misma mediante Tags de los elementos presentes.

dentro de este analisis hay unos dominios especiales:

* `Celebrities`
* `Landmarks`

* **Object detection:** Este pondra cuadros delimitadores alrededor de los objetos que identifique en la imagen devolviendo unas cordenadas con el tag de lo que predice que puede ser el objeto en cuestion y su cantidad de confianza o de probabilidad de que si sea.

* **Semantic Segmentation:** Coloreará pixel por pixel del objeto para distinguirlos y así saber cuál es cada uno con su color específico y su tag.

* **Facial detection:** Este puede hacer varias cosas, crear cuadros delimitadores, analizar atributos como felicidad o cualidades, hacer reconocimiento facial.

* **OCR:** Reconoce texto en diferentes elementos y para diferentes situaciones tiene dos alternativas,OCR API para cantidades pequeñas de texto como un formulario, y el Read API para cantidad grandes de texto.

### Natural Language Services

* **Speech**
    * **Speech to text:** Llevar de un audio a texto, primero ondas de sonido, luego fonemas y luego palabras.
    * **Text to Speech:** llevar un texto que se separa por palabras, luego a fonemas y por último a ondas de sonido.
    * **Speech translation:** Por medio de audios convertir a texto y luego traducir.

* **Text**
    * **Analysis**
    * **Key phrase:** Obtener las palabras claves de la oración para saber el punto clave del texto.
    * **Entities:** Obtener las entidades mencionadas en el texto.
    * **Sentiment:** Analizar los sentimientos que se vean reflejados en el texto (Positive .90 and negative .10)
    * **Detect Language:** Determinar que idioma es el texto si es ambiguo devolver un NaN pero si lo determina puede devolver el codigo del lenguaje y su nombre.
    
    * **Translate:**
        * **Text:** es capaz de traducir hasta 60 lenguajes.
        * **Speech:** es capaz de entender el habla de 60 lenguajes.
        * **Language Understanding:** LUIS es el lenguaje que entiende la AI el cual busca las intenciones de una instrucción por ejemplo "Turn of the lights" Turn seria la intención.

### Conversational AI services

* **QnA Maker:** Extrae las preguntas de FAQ, support website y demás para poder mantener un tipo de encuentas o preguntas algo asi como un bot de preguntas y respuestas.

* **Azure Bot Service:** Con conocimiento recolectado podra compartirlo por diferentes medios.

### Azure services for AI

* **Cognitive Services:** Poder utilizar muchos al tiempo con un solo endpoint y una Key.

* **Computer Vision Services:** Todo lo que tiene que ver con vision de computadora pero sin poderlo entrenar con mis propios datos. `Está incluido en el cognitive Services`

*  **Custom vision Services:** _Dos elementos de vison pero ahora puedo entrenarlo._ `Está incluido en el cognitive Services`

* **Face Services:** _Todo con facial vision._ `Está incluido en el Cognitive Services`

*  **Form Recognized:** _Analisis de formularios con imagenes (max 20mb)._ `No hace parte del Cognitive Services`

*  **Text Analysis:** `Está incluido en el Cognitive Services`

*  **Speech:** _Si las preguntas van hacia cualquier combinación de texto y speech o only speech es este servicio._ `Está inlcuido en el Cognitive Services`

*  **Tranlator text:** `Está incluido en el Cognitive Services`

*  **QnA Maker:** `No hace parte del Cognitive Services`

*  **Azure bot Services:** `No hace parte del cognitive Services`
