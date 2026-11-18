# Bitácora del proyecto AntonyMath

Registro de avances, decisiones y pendientes del sitio web para los alumnos de bachillerato.

---

## 2026-09-18

- Arranque del proyecto. Objetivo: página web para alumnos de bachillerato de matemáticas, publicada con GitHub Pages.
- Definido con la maestra:
  - El sitio tendrá una subcarpeta por materia: 5 cursos de matemáticas + 1 optativa + 1 sección de "problemas para interprepas".
  - Dentro de cada subcarpeta, un archivo HTML por tema.
  - Los temarios de cada curso se subirán después.
- Verificado en GitHub: el nombre de usuario `AntonyMath` ya está ocupado por otra cuenta. Alternativas disponibles: `AntonyMathMX`, `ProfeAntonyMath`, `AntonyMathClass`. Pendiente que la maestra elija.
- Nombre de usuario de GitHub elegido: **AntonyMathClass**.
- Nombres de secciones confirmados: Matemáticas 1, Matemáticas 2, Matemáticas 3, Matemáticas 4,
  Matemáticas 5, Optativa, Problemas Interprepas. Se crearon las carpetas correspondientes
  (`matematicas-1` … `matematicas-5`, `optativa`, `interprepas`) con un `index.html` de portada
  cada una (aún sin temario, solo aviso de "próximamente").
- Se creó `index.html` (portada del sitio) y `style.css` (estilos compartidos) en la raíz.
- Intento de instalar Xcode Command Line Tools (`xcode-select --install`) falló con el error
  "No se puede instalar el software porque no está disponible en el servidor de actualizaciones
  de software" — problema del catálogo de Apple, no de la Mac de la maestra (fecha, versión de
  macOS 26.1 y conexión a internet están correctos).
- Se descartó la opción de un instalador independiente de Git (git-scm.com ya no lo ofrece desde 2021).
- Decisión: instalar **Xcode completo desde la Mac App Store** (incluye git) para que Claude pueda
  seguir haciendo los commits y push por la maestra desde la terminal, sin que ella tenga que
  aprender comandos. Es una descarga pesada (~15 GB); la maestra la inició y está en curso.
- Pendiente: que termine la instalación de Xcode; después, `git init` + conectar con GitHub.
- Se descargó GitHub Desktop (git interno no ejecutable por seguridad del sistema, ver más abajo).
- Cuenta de GitHub y repositorio `AntonyMathClass/AntonyMathClass.github.io` ya creados por la
  maestra (público, sin README/gitignore/license). Falta conectar la carpeta local desde
  GitHub Desktop (Add local repository → create a repository → Repository Settings → Remote →
  pegar la URL del repo → Push). Sigue pendiente que la maestra dé esos pasos, o que termine
  Xcode para que Claude lo haga por terminal.
- Se intentó usar el git interno de GitHub Desktop directamente desde la terminal (sin instalar
  Xcode): el sistema de seguridad de macOS borra automáticamente la app en cuanto se ejecuta
  algo dentro de ella desde un proceso no interactivo. Se descartó ese atajo.
- Nombre del sitio confirmado como "AntonyMathClass" (antes decía "AntonyMath" en encabezados);
  ya corregido en las 8 páginas existentes.
- Se armó un mockup de 6 paletas de color (3 pastel, 3 vibrantes, todas en tonos morado/rosa)
  en un Artifact de diseño para que la maestra elija. Pendiente su decisión final.
- Primer tema real creado: **Matemáticas 1 → Tema 1. Raíces por factorización**
  (`matematicas-1/tema-1-raices-por-factorizacion.html`), con teoría breve, un ejemplo paso a
  paso, 4 ejercicios resueltos (solución oculta con "Ver solución") y 8 ejercicios extra sin
  respuesta. Enlazado desde `matematicas-1/index.html`.
- Pendiente: temarios reales de las demás materias (los subirá la maestra) y su revisión del
  tema ya creado.
- Tema creado y reubicado: **Matemáticas 3 → Tema 1. Funciones y relaciones: la prueba de la
  recta vertical** (`matematicas-3/tema-1-funciones-y-relaciones.html`). Se creó primero por
  error dentro de Matemáticas 1 (Tema 2); la maestra indicó que va en Matemáticas 3, se movió
  y se corrigieron encabezados/migas/título. Gráficas dibujadas en SVG directo en el HTML (sin
  librerías externas): teoría breve, ejemplo con recta vertical marcada sobre una parábola
  (función) y un círculo (no función), 4 ejercicios resueltos con distintas curvas (recta,
  parábola acostada, V de valor absoluto, elipse inclinada) y 2 ejercicios extra sin respuesta
  (incluye el caso especial de la recta vertical x=k, que no es función). Enlazado desde
  `matematicas-3/index.html`.
- **Paleta de color elegida: Opción D — Púrpura Eléctrico y Fucsia.** Aplicada a `style.css`:
  fondo `#faf5ff`, texto `#2d1b4e`, acento `#7b2ff7`, acento secundario `#f72585`, encabezado
  con degradado de ambos, pie de página con fondo `#7b2ff7` y texto blanco. Tipografías Poppins
  (títulos) y Quicksand (texto), vía Google Fonts, agregadas a las 10 páginas existentes.
- Portada (`index.html`): las tarjetas de materias con contenido (Matemáticas 1 y 3) ahora se
  ven "activas" (fondo con degradado de la paleta, más contraste); las que aún no tienen
  material (Matemáticas 2, 4, 5, Optativa, Interprepas) se ven más discretas (opacas, borde
  punteado) y llevan una etiqueta "Próximamente".
- Pie de página: color cambiado de acento (morado) a acento-2 (fucsia), a pedido de la maestra.

## 2026-09-19

- La maestra pidió eliminar el Tema 1 (Raíces por factorización) de Matemáticas 1. Se borró
  `matematicas-1/tema-1-raices-por-factorizacion.html` y su enlace en `matematicas-1/index.html`
  (vuelve a mostrar el aviso de "temario no cargado"). Como Matemáticas 1 se quedó sin temas,
  su tarjeta en la portada volvió al estilo "Próximamente" (antes estaba "activa").
  Matemáticas 3 (funciones y relaciones) sigue como la única materia con contenido y tarjeta
  activa.
- La maestra compartió una foto de su cuaderno con 4 operaciones con decimales resueltas a mano
  (suma, resta, multiplicación, división) y pidió recrear ese estilo (acarreos/préstamos
  marcados en color) como nuevo Tema 1 de Matemáticas 1. Se creó
  `matematicas-1/tema-1-operaciones-con-decimales.html` con teoría breve, la resta como ejemplo
  y suma/multiplicación/división como ejercicios resueltos (con tablas HTML que recrean los
  acarreos en color y la división larga con verificación), más 6 ejercicios extra sin respuesta.
  Enlazado desde `matematicas-1/index.html`; su tarjeta en la portada volvió a "activa".
- La suma de la foto (39.4 + 4.0318 + 21.68) tenía un resultado incorrecto anotado (70.8118);
  con esos números el resultado correcto es 65.1118. La maestra confirmó corregirlo, así que se
  publicó con el resultado correcto.
- La maestra pidió simplificar la página: dijo que era mucha información y los alumnos no leen.
  Se rehízo como `matematicas-1/tema-1-operaciones-basicas.html` (se eliminó el archivo
  anterior): sin teoría en párrafos ni "ver solución" oculta — el ejemplo y todos los ejercicios
  resueltos quedan visibles directamente, solo con la operación (tabla con acarreos/préstamos en
  color) y una frase corta de regla debajo, para que sirvan de guía visual rápida. Se combinaron
  operaciones con **decimales**, **enteros** (signos) y **naturales** (a pedido de la maestra),
  organizadas en tres subsecciones dentro de "Ejercicios resueltos". Enlace actualizado en
  `matematicas-1/index.html`.
- Nueva vuelta de ajustes a la misma página, a pedido de la maestra:
  - Se quitó la sección de enteros.
  - El "Ejemplo" ahora es una sola caja con las 4 operaciones (suma, resta, multiplicación,
    división) alineadas una junto a otra.
  - Los ejercicios para resolver se organizan en 4 cajas tituladas "Producto 1" a "Producto 4"
    (así les llama la maestra a sus hojas de ejercicios; no tiene relación con la operación de
    multiplicar), cada una con el mismo número de ejercicios (7) numerados con círculos de color.
    "Producto 3" usa los números exactos de una foto que mandó la maestra; "Producto 1, 2 y 4"
    son ejercicios nuevos del mismo estilo (mezcla de naturales y decimales) creados por Claude.
  - Estilo de las cajas: título grande en mayúsculas con fondo resaltado y números en círculos
    de color, imitando el estilo de sus hojas hechas a mano.
- Ajustes adicionales: se regresaron los ejemplos con números naturales (además de los
  decimales) en la sección "Ejemplo", para que los alumnos comparen ambos. Las 4 cajas de
  Producto se hicieron compactas (menos relleno, texto más chico) pensando en impresión; se
  probó una cuadrícula de 2 columnas pero la maestra pidió quitarla, así que quedan apiladas
  verticalmente pero compactas.
- La maestra mostró como referencia un sitio externo ("2E Math") con cajas "Bloque" en
  cuadrícula de 3 columnas y una sección desplegable de "Respuestas". Se adoptó solo la barra
  de color sólido como título de cada caja de Producto (sin cambiar a cuadrícula, siguen
  apiladas) y se agregó una sección `<details>` "Respuestas" al final con las soluciones de los
  4 Productos (calculadas y verificadas por Claude; Producto 3 corresponde a los números que la
  maestra dio en su foto).
- Tras varias idas y vueltas (apiladas → sin cuadrícula → 2 columnas internas de texto), la
  maestra confirmó con una segunda captura de la misma referencia que sí quería la cuadrícula:
  las 4 cajas de Producto quedaron en cuadrícula de 2 columnas (1 columna en pantallas angostas),
  cada una con su lista de ejercicios en una sola columna interna.
- Se quitó el look de "tarjeta" de cada ejercicio (fondo blanco y borde por renglón) dentro de
  las cajas de Producto; ahora solo queda el número en círculo con el texto, sin separación en
  bloques, para ocupar menos espacio vertical.
- Ejemplo de división con decimales cambiado a 32.5 ÷ 0.16 (antes 325 ÷ 0.16), y se agregó una
  visualización lado a lado: a la izquierda el problema original con los puntos decimales
  marcados y flechitas indicando que se recorren 2 lugares, a la derecha el problema ya
  convertido a enteros (3250 ÷ 16), seguido de la división larga resuelta (= 203.125).
- Corregido: la línea divisora (`border-top`) en las tablas de suma, resta y multiplicación
  aparecía en la fila equivocada (arriba del último número, es decir entre los números a
  operar) en vez de debajo de todos ellos. Se movió la clase `linea` a la fila correcta en las
  6 tablas (decimales y naturales).

## 2026-09-19 (2)

- Se creó `Guia-trabajar-con-el-asistente.pdf` en la raíz del proyecto: una infografía de una
  página con 6 pasos para trabajar con Claude (pedir cambios simples, compartir fotos, revisar
  en el navegador, dar opinión, etc.), con la paleta del sitio. Generado con Chrome en modo
  headless (`--print-to-pdf`), ya que Python sigue sin funcionar por la instalación pendiente
  de Xcode.

## 2026-09-23

- Se creó `matematicas-1/tema-2-lectura-y-matematicas.html` (Tema 2. Lectura y matemáticas),
  enlazado desde `matematicas-1/index.html`. Misma estructura que el Tema 1: Ejemplo (los 3
  problemas de la foto de la maestra, con datos marcados con "marcatexto" y respuesta en oración),
  4 cajas de Producto (3 problemas cada una, creados por Claude: uno sin datos suficientes, uno
  de suma + resta, uno de división) y "Respuestas" desplegable.
- Corrección: en la foto, 675 + 1380 daba 2065 (en realidad es 2055). A petición de la maestra
  se cambió la segunda entrega a 1390, para que 675 + 1390 = 2065 y 2486 − 2065 = 421 queden
  exactos, como en su hoja. En el problema del azúcar se agregó
  que sobran 10 kg.
- Estilos nuevos al final de `style.css` (marcatexto, número de problema, caja de respuesta).

## 2026-09-23 (2)

- Se creó `matematicas-1/tema-3-divisibilidad-y-primos.html` (Tema 3. Divisibilidad y números
  primos), enlazado desde `matematicas-1/index.html`. Contiene los criterios del 2, 3 y 5 del
  apunte de la maestra (con sus ejemplos), una definición breve de número primo y un ejercicio
  interactivo de Criba de Eratóstenes del 1 al 100 (clic = tachar, 2.º clic = primo, 3.º =
  normal; botón "Borrar todo"). Se incluyó el paso de tachar múltiplos de 7 (necesario para
  llegar a 100). Respuestas desplegables: los 25 primos y la cuadrícula resuelta.

- Tema 3: a petición de la maestra se agregó el criterio del 7 (ejemplos 91 y 364) como
  criterio 4, y el paso 5 de la criba lo menciona. La maestra decidió NO agregar el criterio del 11.

- Tema 3: se agregó "Ejercicio 2: Descomposición en factores primos" (método de divisiones
  sucesivas en tabla; ejemplos 360 y 1470; 4 Productos de 5 números creados por Claude, todos
  con primos 2, 3, 5 y 7; Respuestas en forma de potencias). La criba pasó a "Ejercicio 1".

## 2026-09-23 (3)

- Se creó `matematicas-1/tema-4-mcd-y-mcm.html` (Tema 4. MCD y mcm), enlazado desde el índice.
  Definiciones, pasos del método de tabla simultánea (primos que dividen a todos van en círculo:
  MCD = producto de esos; mcm = producto de todos). Ejemplo 1 numérico (24 y 36; 12, 18 y 30).
  Ejemplo 2 con problemas: paquetes de lápices y borradores (MCD = 12) y autobuses cada 12 y 18
  min (mcm = 36, 7:36). Aún sin Productos/ejercicios: preguntar a la maestra.

- Tema 4 rehecho a petición de la maestra, "sin tanta explicación", al estilo de su apunte: se
  quitaron definiciones, pasos, pista y notas por renglón. MCD y mcm en tablas separadas (MCD
  solo divide entre primos comunes y el resultado va debajo de la columna; mcm divide hasta 1).
  Ejemplos de su apunte: MCD 72, 40, 36 = 4; mcm 25, 30, 100 = 300. Se conservaron los 2
  problemas (paquetes = MCD 12; autobuses = mcm 36). Nuevo: link al final "¿Tienes dudas?
  Repasa el tema anterior" (clase `link-repaso`) hacia el Tema 3.

- Tema 4: se quitó "Utiliza números primos" y la lista de primos; MCD y mcm quedaron lado a
  lado en una sola caja para ocupar menos espacio.

- Se agregó el link "¿Tienes dudas? Repasa el tema anterior" al final de los Temas 2 (→ Tema 1)
  y 3 (→ Tema 2). Hacerlo también en cada tema nuevo.

- Tema 4: se agregaron 4 cajas de Producto (6 ejercicios cada una: 2 MCD, 2 mcm con números y
  2 problemas, uno de MCD y otro de mcm; creados por Claude) y Respuestas desplegables
  (verificadas por computadora).

## 2026-09-23 (4)

- Se creó `matematicas-1/tema-5-operaciones-con-enteros.html` (Tema 5. Operaciones con
  enteros), enlazado desde el índice, con el apunte "Regla de signos" de la maestra en dos
  columnas (Suma | Multiplicación y división) y link al Tema 4. Corrección: en su apunte decía
  (−)(−) = −; se puso (−)(−) = +, que coincide con su ejemplo (−6)(−5) = +30.
- Tema 5: con el ejemplo "Regla con signos" de la maestra (7 tipos de ejercicio) se agregó la
  sección de ejemplo (completando el 7: 3(−2)² = 3(+4) = +12) y 4 Productos de 7 ejercicios del
  mismo tipo cada uno, creados por Claude y verificados, con Respuestas que muestran el paso
  intermedio.

- Tema 5: la "Regla de signos" se cambió de dos columnas a una tabla (Operación / Signos /
  ¿Qué se hace? / Signo del resultado / Ejemplos). La maestra reporta error en los ejemplos 4-7
  de "Regla con signos"; las cuentas son correctas, falta aclarar qué error ve.

- La maestra no quedó conforme con el Tema 5 y pidió borrarlo para empezar de nuevo mañana.
  Se movió `tema-5-operaciones-con-enteros.html` a la Papelera, se quitó su link del índice y se
  quitaron sus estilos de `style.css`. Material de la maestra para rehacerlo: apunte "Regla de
  signos" (ojo: decía (−)(−) = −, es +) y ejemplo "Regla con signos" de 7 tipos de ejercicio.

## 2026-09-26

- Se retomó el Tema 5 (Operaciones con enteros) que se había borrado el 23 de septiembre.
  Se recreó `matematicas-1/tema-5-operaciones-con-enteros.html` y se enlazó de nuevo desde el
  índice. La maestra volvió a mandar la foto de "Regla de signos" (suma; multiplicación y
  división) — coincide con la corregida antes ((−)(−) = +, no −, confirmado por su propio
  ejemplo (−6)(−5) = +30). Se puso en formato de tabla (Operación / Signos / ¿Qué se hace? /
  Signo del resultado / Ejemplos), como se había pedido la vez pasada.
- Pendiente antes de seguir con el Ejemplo y los Productos: la maestra no tenía a mano el
  ejemplo "Regla con signos" de 7 tipos de ejercicio (uno era 3(−2)² = 3(+4) = +12) ni la
  aclaración de qué vio mal en los ejercicios 4–7 de esa regla. Se le pidió reenviarlos antes de
  reconstruir esa parte, para no repetir el resultado con el que no quedó conforme.
- Título corregido: "Tema 5. Operaciones básicas con enteros" (la maestra dijo que se le había
  escapado "básicas").
- La maestra volvió a mandar la foto de "Regla con signos - Ejemplo" con los 7 tipos: 1) suma y
  resta en cadena (agrupando + y −), 2) signo de un signo −(−a)=+a, 3) multiplicación de 3
  factores, 4) multiplicación con suma/resta dentro del paréntesis, 5) potencia de un entero
  negativo (expandida), 6) división simple con signos, 7) número por una potencia (se resuelve
  la potencia primero) — este último lo dejó sin resolver y se completó: 3(−2)² = 3(+4) = +12.
  Se transcribió tal cual como la sección "Regla con signos — Ejemplo", y se rehicieron las 4
  cajas de Producto (7 ejercicios cada una, mismo patrón, números nuevos de Claude) y las
  Respuestas, ahora mostrando el paso intermedio como se pidió la vez anterior. Se agregó también
  el link "¿Tienes dudas? Repasa el tema anterior" hacia el Tema 4, siguiendo la convención de
  los demás temas.
- La maestra no quedó conforme con la tabla de "Regla de signos" y pidió regresar al diseño de
  su foto original: título grande arriba, dos columnas (Suma | Multiplicación y división)
  separadas por una línea, con títulos en globo de color, "Ejemplo:" en cursiva, y los ejemplos
  numerados en círculos. Se rehizo así, quitando la tabla.
- "Regla con signos — Ejemplo": se quitaron las explicaciones inventadas por Claude (p.ej.
  "Agrupa los negativos y los positivos...") y se dejó cada ejercicio apilado hacia abajo, tal
  cual la foto: círculo con el número, el planteamiento con el resultado en la misma línea, y el
  paso intermedio debajo (sin texto explicativo), uno tras otro en una sola columna en vez de
  una cuadrícula.
- La maestra seguía sin quedar conforme con "Regla de signos": pidió el orden de columnas
  invertido (izquierda: Multiplicación y división; derecha: Suma y resta) y que ocupara menos
  espacio pensando en imprimir. Se redujo bastante el tamaño de letra y los espacios, y se
  combinaron los ejemplos de multiplicación/división en 4 líneas (mismo signo y signo diferente
  lado a lado) en vez de 8 líneas en dos sub-columnas.
- Era el mismo problema de caché del navegador de antes (Cmd+Shift+R lo resolvió). El título
  "Regla de signos" se puso en color acento (antes usaba el color de texto normal) para que
  resalte más, como pidió la maestra.
- El subtítulo "Regla con signos — Ejemplo" tenía un error: debía decir "Operaciones con
  enteros", y la maestra pidió que fuera un título centrado y en su propia caja aparte (separado
  de la caja de "Regla de signos"). Se corrigió el texto y se separó en una segunda
  `caja-ejemplo` con el mismo estilo de título centrado en color.
- Se quitó la pregunta "¿Tienes dudas?" del link para regresar al tema anterior en los 4 temas
  que lo tienen (2, 3, 4 y 5); ahora dice solo "Tema anterior:" seguido del enlace.
- Tema 5: se quitó el encabezado "Ejemplo" de arriba de "Regla de signos" y se puso como
  subtítulo centrado debajo de "Operaciones con enteros" (donde sí corresponde). Se corrigió el
  ejercicio 3 del ejemplo: el primer número era 4, debía ser −4 → −4(−2)(+3) = +24 (antes decía
  4(−2)(+3) = −24).
- El ejercicio 1 de cada Producto (cadena de sumas/restas) siempre empezaba con número
  negativo; la maestra pidió variar. Producto 1 y 3 ahora empiezan positivo (6+3−2−5+8−1=9 y
  7+5−4−3+6−8=3); Producto 2 y 4 se quedaron empezando en negativo. Respuestas actualizadas.
- Se diversificaron los signos también en los ejercicios 2 al 7 de cada Producto (antes casi
  todos empezaban en positivo o seguían el mismo patrón): se mezclaron números iniciales
  negativos/positivos en las multiplicaciones de 3 factores y las de paréntesis, se varió
  −(−a) con −(+a), se cambiaron algunas divisiones a distintas combinaciones de signos
  (pos÷neg, neg÷neg), se agregó una base positiva en las potencias cúbicas (antes las 4 eran
  negativas), y una multiplicación por potencia con signo negativo. Respuestas de los 4
  Productos actualizadas y verificadas.
- Ejercicio 5 (potencias): antes las 4 eran base negativa elevada al cubo. Se diversificó base
  (positiva y negativa) y exponente (cuadrado, cubo, cuarta potencia), cuidando que los
  resultados no crecieran mucho: Producto 1 (−2)⁴=16, Producto 2 (−3)³=−27, Producto 3 (4)²=16,
  Producto 4 (5)³=125 (a petición de la maestra, cambiado de (2)³). Respuestas actualizadas con
  su paso intermedio.
- Ejercicio 7: se diversificó el número inicial (positivo/negativo) y la base de la potencia
  (usando 2, 6, 7, 8, 10 o 1, con signo) y el exponente (2, 3 o 4): Producto 1 3(−2)⁴=48,
  Producto 2 2(−1)³=−2 (ajustado a petición de la maestra, antes −2(1)³), Producto 3
  2(−6)²=72, Producto 4 −4(−10)³=+4000 (a petición de la maestra, antes −4(−2)³=32; aquí sí
  sale un número grande, fue explícito). Respuestas actualizadas.

## 2026-09-26 (2)

- Se creó **Tema 6. Jerarquía con enteros** (`matematicas-1/tema-6-jerarquia-con-enteros.html`),
  enlazado desde el índice, con link "Tema anterior" hacia el Tema 5. Con la foto de la maestra
  ("Jerarquía"): caja de reglas (paréntesis → potencias/raíces → multiplicación/división →
  suma/resta) y caja de Ejemplo con sus 3 problemas transcritos y verificados paso a paso
  (5−7(−2)²÷2−12÷4=−12; 8+2(−7+4)−(−4)(−2)(5)+2(−6)²=+34; −6+[5−3(−2(−6+4))]=−13).
- 4 Productos de 3 ejercicios cada uno (mismo tipo que los 3 ejemplos: combinada con potencia y
  dos divisiones exactas, combinada con paréntesis y producto de 3 factores, y con corchetes
  anidados), números nuevos de Claude, verificados, cuidando que todas las divisiones den enteros
  exactos (pedido explícito de la maestra). Respuestas con los pasos intermedios.
- Ejercicio 2 de cada Producto: se reordenaron los términos del planteamiento (antes: número
  solo, multiplicación+suma, producto de 3 factores, potencia+multiplicación). Ahora: producto
  de 3 factores primero, luego multiplicación+suma, luego potencia+multiplicación, y el número
  solo al final. El resultado de cada uno no cambia (es la misma suma, solo en otro orden); las
  Respuestas no necesitaron actualizarse.
- Ejercicio 1 de cada Producto: se reordenó (antes: número solo, potencia+mult/div, división) a
  (potencia+mult/div, número solo, división o multiplicación al final). Se diversificó el último
  término: Producto 1 y 3 se quedaron con división; Producto 2 y 4 cambiaron a multiplicación
  (−2(−4)²÷8+9−3(5)=−10 y −3(−6)²÷9+4−5(2)=−18, resultados nuevos por el cambio de operación).
  Respuestas actualizadas.
- Ejercicio 3, Producto 1: el "4" dentro del corchete cambió a "−4" → −5 + [−4 − 2(−3(−4+2))] =
  −21 (antes daba −13). Respuesta actualizada.
- Ejercicio 3, Producto 2: cambiado a 4 − [−6 + 3(−2(−5+3))] = −2 (antes −4 + [6 − 3(−2(−5+3))]
  = −10). Respuesta actualizada.
- Ejercicio 3, Producto 3: cambiado a −7 + [5 − 4(−2(−3 − 2))] = −42 (antes con −3+1 daba −18).
  Respuesta actualizada.
- Ejercicio 3, Producto 4: cambiado a −2[2 − 8(−3(−2 − 1))] = +140 (antes −3 + [8 − 2(−4(−2+5))]
  = +29). Nota: este usa multiplicación implícita antes del corchete (−2[...]) en vez de suma,
  para diversificar la estructura. Respuesta actualizada.
- Ejercicio 3, Producto 2: cambiado otra vez a −4[−6 + 3(−2(−5+3))] = −24 (también multiplicación
  por el corchete, igual que Producto 4; antes era 4 − [...] = −2). Respuesta actualizada.
- A petición de la maestra, se agregó resaltado tipo marcador (fondo de color) en los 3 ejemplos
  de la caja "Ejemplo": en cada línea de paso, la parte que se acaba de resolver queda marcada
  en color, para que se note claramente qué cambió de un paso a otro (imitando el estilo de sus
  apuntes a mano). No se tocaron los Productos ni las Respuestas.
- Ejemplo 1, último paso: decía "5 + (−17)"; el paréntesis se prestaba a confusión, se quitó y
  quedó "5 − 17".

## 2026-09-26 (3)

- Se creó **Tema 7. Potencias** (`matematicas-1/tema-7-potencias.html`), enlazado desde el
  índice, con link "Tema anterior" hacia el Tema 6. Con la foto de la maestra ("Potencias -
  Ejemplo", 11 ejercicios): se separaron los ejercicios 1-6 como caja de "Reglas de potencias"
  (aº=1, a⁻ⁿ=1/aⁿ, aᵐ·aⁿ=aᵐ⁺ⁿ, aᵐ÷aⁿ=aᵐ⁻ⁿ, (aᵐ)ⁿ=aᵐⁿ, (a/b)ⁿ=aⁿ/bⁿ, cada una con su ejemplo) y
  los ejercicios 7-11 como caja de "Ejemplo" (aplicaciones combinadas, con pasos resaltados
  igual que en el Tema 6). Nota: en el ejercicio 11 la maestra escribió 7³ en el denominador
  original pero el desarrollo solo cuadra si es 7⁻³ (se resolvió así, verificado que da 2²/7).
- 4 Productos de 6 ejercicios cada uno (uno por cada regla 1-6), números nuevos de Claude,
  verificados, dejando las respuestas en forma de potencia (no expandidas a números grandes,
  igual que el estilo de la maestra). Respuestas incluidas.
- A petición de la maestra, se rehicieron los Productos: ahora son **3 Productos con los 11
  ejercicios completos cada uno** (los 6 básicos + los 5 combinados, mismo tipo que su ejemplo:
  producto de potencias con exponentes negativos, tres factores con base común oculta, potencia
  entre potencia con base común oculta, y dos fracciones con exponentes negativos). Números
  nuevos de Claude, todos verificados numéricamente, respuestas en forma de potencia.
- Se agregó un componente de fracción en dos renglones (numerador, línea, denominador) en
  `style.css` (clase `.fraccion`) y se aplicó a todas las fracciones del Tema 7: reglas,
  ejemplo, los 3 Productos y las Respuestas (25 fracciones en total). Antes se escribían en
  línea con "/".

## 2026-09-26 (4)

- **¡Sitio conectado a GitHub y publicado!** Después de varios intentos fallidos con Xcode
  Command Line Tools (error del servidor de Apple, persistente desde el 18 de septiembre), se
  optó por GitHub Desktop. Problemas resueltos en el camino:
  - GitHub Desktop no podía crear el repositorio local por falta de permiso de macOS para
    escribir en la carpeta Escritorio (protección de privacidad de archivos/carpetas). Se movió
    todo el proyecto de `~/Desktop/AntonyMath` a `~/AntonyMath` (fuera de esa protección) y se
    dejó un acceso directo (symlink) en el Escritorio con el mismo nombre para que la maestra
    siga entrando igual.
  - Esta versión de GitHub Desktop no tiene campo para pegar la URL del remoto manualmente, solo
    un botón "Publish". Como ya existía un repositorio vacío creado a mano en GitHub.com con el
    nombre correcto, se borró ese repositorio vacío (Settings → Danger Zone) y se usó el botón
    "Publish Repository" de GitHub Desktop poniendo el nombre exacto `AntonyMathClass.github.io`
    para crear el repositorio ya conectado y con el primer commit subido.
  - Confirmado: los archivos ya están en
    https://github.com/AntonyMathClass/AntonyMathClass.github.io y GitHub Pages ya generó un
    despliegue automático (el repo tiene el nombre especial `usuario.github.io`, así que se
    publica solo). El sitio debería estar visible en **https://antonymathclass.github.io**.
  - Nota: en la vista de GitHub.com con el traductor de Chrome activado, las carpetas `.claude`
    e `interprepas` se veían mal traducidas como "Claude" e "intérpretes" — es solo un efecto
    del traductor, no carpetas reales de más.

## 2026-09-27

- Se creó `Guia-publicar-en-GitHub.pdf` en la raíz del proyecto: guía paso a paso (3 páginas,
  paleta del sitio) de la configuración de GitHub / GitHub Desktop / GitHub Pages del 26 de
  septiembre, cómo subir cambios en adelante (Commit to main → Push origin) y tabla de problemas
  resueltos. Generada con Chrome headless (`--print-to-pdf`).
- A petición de la maestra, ambos PDF (`Guia-trabajar-con-el-asistente.pdf` y
  `Guia-publicar-en-GitHub.pdf`) se movieron a la carpeta `~/Desktop/IEMS`, fuera del proyecto,
  para que no queden públicos en GitHub.
- Se creó **Tema 8. Radicales** (`matematicas-1/tema-8-radicales.html`), enlazado desde el
  índice, con link "Tema anterior" hacia el Tema 7. Con la foto de la maestra: caja "Regla de
  radicales" (ⁿ√aᵐ = a^(m/n), notas de índice par/impar) y caja "Ejemplo" con sus 7 ejercicios,
  pasos resaltados y tablas de factores a un lado (como en sus apuntes). Ejercicio 3 redactado
  como "No existen raíces pares de números negativos"; ejercicio 5 con resultado 2² · 3¹ · 5¹.
- 3 Productos de 7 ejercicios (uno de cada tipo del ejemplo), números nuevos de Claude,
  verificados; respuestas en forma de potencia.
- Nuevo componente en `style.css`: clase `.radical` (índice, signo √ y línea sobre el radicando;
  variante `.radical.alto` para fracciones) y `.factores-lado`.
- A petición de la maestra, el índice del radical se hizo más pequeño (etiqueta `<sup>`, 0.55em),
  así se ve chiquito aunque el navegador no cargue los estilos.
- Ejemplo 7, a petición de la maestra: el proceso ahora es ³√5 · ³√5² → ³√(5 · 5²) → ³√5³ → 5
  (antes pasaba por ³√125); la tabla de factores ahora es la de 25 = 5².
- Se agregó un **Producto 4** (7 ejercicios, mismos tipos, números nuevos verificados).
- Ejercicio 6 (suma de radicales semejantes), en el ejemplo y en los 4 Productos: ahora son 3
  términos combinando positivos y negativos (ejemplo: 4√2 − 9√2 + 3√2 = −2√2).
- Producto 3, ejercicio 6, a petición de la maestra: 4√7 − 9√7 − 4√10 = −5√7 − 4√10 (incluye un
  radical distinto que no se puede sumar con los otros).
- Producto 4, ejercicio 6, a petición de la maestra: −6√6 + 4√11 + 10√6 + 5√11 = 4√6 + 9√11
  (dos grupos de radicales semejantes; se usó √6 en vez de √8 para que no se pueda simplificar).
- Ejercicio 7 de los Productos (multiplicación de radicales), a petición de la maestra: ahora cada
  Producto usa un índice distinto: P1 √3 · √27 = 3² (índice 2), P2 ³√3 · ³√9 = 3 (índice 3),
  P3 ⁴√8 · ⁴√32 = 2² (índice 4), P4 ⁵√9 · ⁵√27 = 3 (índice 5).
- Tema 8 subido por la maestra y verificado en línea.
- Se creó **Tema 9. Operaciones con polinomios** (`matematicas-1/tema-9-operaciones-con-polinomios.html`;
  título elegido por la maestra en vez de "Polinomios"), enlazado desde el índice. Caja "Ejemplo" con
  sus 6 ejercicios (suma de términos semejantes, resta con paréntesis, multiplicación, división,
  potencia y raíz de monomios) y pasos resaltados. Ejercicio 2 corregido con su permiso: el − antes
  del paréntesis cambia también el +7 a −7, resultado −1a² + 2a − 2 (en la foto decía +12).
- 4 Productos de 6 ejercicios (uno por tipo), diversificados: distintas letras, signos mezclados,
  términos que se cancelan, potencias de coeficiente negativo, índices 3, 4 y 5. Verificados.
- Nuevo en `style.css`: clases `.sub-1`, `.sub-2`, `.sub-3` (subrayado de colores para términos
  semejantes, como en los apuntes; se usaron morado, fucsia y doble línea oscura para no salir de
  la paleta).
- Al final del Tema 9 se agregó un enlace "¿Dudas con los signos? Repasa la Regla de signos (Tema 5)"
  que lleva directo a esa caja (se le puso `id="regla-de-signos"` en el Tema 5).
- A petición de la maestra, se quitaron las explicaciones escritas del ejemplo del Tema 9 (solo quedan
  los pasos matemáticos resaltados y las reglas (+)(−) = − y (−)(−) = + de sus apuntes), para que el
  estudiante deduzca qué se hizo en cada paso.
- Ejemplo 1 del Tema 9: el subrayado de términos semejantes se pasó al enunciado mismo (como en el
  apunte) y se quitó el renglón repetido. Los subrayados ahora usan la etiqueta `<u>`, así se ven
  subrayados aunque el navegador no cargue los estilos (con estilos, salen en colores).
- Ejemplo 3 del Tema 9 cambiado por la maestra: (2x³y²z⁴)(−3xy³) = −6x⁴y⁵z⁴ (sin el + del 2 y con x sin
  exponente en el segundo factor, para que el alumno deduzca que x = x¹).
- Todo el Tema 9 se pasó al estilo de los libros (a petición de la maestra): sin + al inicio de un
  término y sin exponente ni coeficiente 1 (x en vez de x¹, z en vez de 1z, −a² en vez de −1a²),
  en ejemplo, Productos y Respuestas. En los pasos se dejan las operaciones como b^(1·2) o x^(3+1).
  Los Temas 7 y 8 se dejan con exponente 1 (5¹, 3¹, etc.), como en los apuntes (decisión de la maestra).
- Ejemplo 6 del Tema 9: la respuesta vuelve a ser x¹y³z⁶ (a petición de la maestra).
- Respuestas de los Productos del Tema 9 (ejercicios 3 a 6, monomios): se agrega el exponente 1
  (c¹, b¹, y¹, z¹). Los enunciados siguen al estilo de libro, sin ¹.
- Ejercicio 3 de los Productos 3 y 4 del Tema 9: ahora es producto de tres monomios con coeficientes
  pequeños: (−2m²n⁴p³)(−3m⁵n)(−4mp) = −24m⁸n⁵p⁴ y (−5a⁴b²c³)(3ab⁶c²)(2a²bc) = −30a⁷b⁹c⁶.
- Tema 9 subido por la maestra y verificado en línea (incluido el enlace a la Regla de signos).
- Siguiente: **Tema 10. Ecuaciones**. La maestra aún no está conforme con su apunte; lo trabajamos
  en la próxima sesión.

## 2026-10-03

- Nuevo **Tema 10. Plano cartesiano, área y perímetro** (Matemáticas 1), creado a partir de la foto
  del apunte de la maestra: `matematicas-1/tema-10-plano-cartesiano-area-y-perimetro.html`, enlazado
  en el índice. Por ahora tiene solo un ejemplo: rectángulo A(2,−1), B(7,−1), C(2,−8), D(7,−8), con
  la gráfica dibujada en la página.
- El apunte decía lado 8, área 40 y perímetro 26. Se corrigió (decisión de la maestra) porque de −1 a
  −8 hay 7: área 5 × 7 = 35 y perímetro 7 + 7 + 5 + 5 = 24.
- "Área = B × A" del apunte se escribió como "Área = base × altura", para no confundirlo con los
  vértices A y B.
- **El número 10 es provisional:** la maestra aún no decide qué número de tema le toca (antes se
  había apuntado "Tema 10. Ecuaciones"). **Todavía no se sube a GitHub.**
- Ejemplo 2 agregado: triángulo A(4,−2), B(−2,−2), C(1,5), con altura punteada. Área = (6 × 7)/2 = 21.
  Correcciones aceptadas por la maestra: el perímetro del apunte sumaba la altura 7 (6 + 7 + n + m =
  28.23); se dejó solo la suma de los lados, 6 + n + m ≈ 21.23. Además, √58 ≈ 7.616 (redondeado; el
  apunte decía 7.615).
- Ejemplo 3 agregado: circunferencia con centro C(6,4) y punto P(10,4), r = 4. Área = 3.1416 × 16
  ≈ 50.27 (redondeado; el apunte decía 50.26) y perímetro = 3.1416(8) ≈ 25.13. Se añadió el renglón
  "r = 10 − 6 = 4", que no venía en el apunte.
- **Decisión de la maestra (opción 2):** el Tema 10 queda reservado para **Ecuaciones**, y este pasa a
  ser el **Tema 11** (`tema-11-plano-cartesiano-area-y-perimetro.html`). No se sube hasta tener listo
  Ecuaciones, para que no quede un hueco en la lista.
- Cuando exista el Tema 10: agregarlo al índice antes del 11 y cambiar el enlace "Tema anterior" del
  Tema 11 (por ahora apunta al Tema 9).
- Nuevo **Tema 10. Ecuaciones** (`tema-10-ecuaciones.html`), a partir de la foto del apunte: 3 ejemplos
  (términos semejantes en ambos lados; con paréntesis y distributiva; con signo menos antes del
  paréntesis). Se corrigió el ejemplo 1 (decisión de la maestra): el apunte daba x = 10/3, pero
  4 + 14 = 18, así que 3x = 18 y x = 6. Los ejemplos 2 (x = −11/7) y 3 (x = −4) estaban bien.
- 4 Productos de 3 ejercicios (uno de cada tipo de ejemplo), con sus respuestas: algunas enteras,
  otras negativas y otras en fracción. Todas se comprobaron sustituyendo x en ambos lados.
- A petición de la maestra, en el Producto 3 se cambiaron de lugar los lados de las ecuaciones:
  ej. 2 → 4x + 5(2x + 3) = 2(3x − 5) + 1 y ej. 3 → 8 − 2(x − 5) = 10x − (4x − 3). Las respuestas
  no cambian (−3 y 15/8).
- Ya enlazado en el índice (antes del 11), y el "Tema anterior" del Tema 11 ahora lleva al Tema 10.
- Tema 11: se agregaron 4 Productos de 3 ejercicios (rectángulo, triángulo con la punta arriba del
  centro de la base, circunferencia con centro y un punto), más sus respuestas (área y perímetro, con
  π = 3.1416 y redondeo a 2 decimales). Algunos triángulos dan lados exactos (5 y 13) y otros con raíz
  (√73, √52).
- Temas 10 y 11 revisados, subidos por la maestra con GitHub Desktop y verificados en línea.
- Nuevo **Tema 12. Gráfica de una ecuación lineal** (`tema-12-grafica-de-una-ecuacion-lineal.html`),
  a partir de la foto del apunte (estaba correcto). Ejemplo 1: 9x − 3y + 12 = 0 → y = 3x + 4, la tabla
  con x = 1, 2, 3 y la gráfica de la recta. Se escribió "y = 3x + 4" sin el + inicial (estilo de libro).
  Nueva clase `table.tabla-xy` en `style.css` para la tabla de valores. Enlace de repaso al Tema 10.
- Tema 12 (actualizado): a petición de la maestra se dejaron solo **2 Productos** de 3 ejercicios. Cada
  Producto tiene pendientes positivas y negativas (3 y 3 en total). La maestra no tiene más ejemplos.
- Tema 12 (versión anterior): 4 Productos de 3 ecuaciones (forma ax + by + c = 0), con respuestas (y despejada + puntos
  para x = 1, 2, 3). Diversificados a petición de la maestra: pendientes positivas y negativas, y
  coeficientes de x y de y con signos variados. Todas verificadas sustituyendo en la ecuación original.
- Tema 12: a petición de la maestra, la gráfica del ejemplo se pasó al lado derecho (pasos y tabla a
  la izquierda) y se hizo más grande (hasta 480 px). En celular se acomoda debajo. Nuevas clases en
  `style.css`: `.ejemplo-dos-columnas` y `.grafica-card.grafica-grande`.
- Tema 12: la gráfica se rehízo con **cuadritos iguales en x y en y** (antes 1 unidad en x medía más
  que 1 unidad en y). Ahora cada número de los dos ejes está a la misma distancia, y se numeran todos
  (x de −3 a 5, y de −2 a 14). Por eso la gráfica es más alta que ancha.
  **Regla para gráficas futuras:** usar siempre la misma escala en los dos ejes.
- Tema 12 revisado y subido por la maestra con GitHub Desktop.
- La maestra no quiso un recordatorio a una hora fija (se borró la tarea programada). Prefiere que
  Claude se lo recuerde al abrir la próxima sesión, porque la ventana de git sigue apareciendo.
- Siguiente: Tema 13 (la maestra traerá el apunte).
- Pendiente (pedido por la maestra para el 2026-10-04): quitar la ventana de macOS que pide instalar
  las herramientas del comando git. La provocan los comandos `git` y `python3` que corre Claude
  (Xcode Command Line Tools no está instalado). Claude ya no los usará.

## 2026-10-05

- **Resuelto:** la ventana de macOS que pedía instalar las herramientas de git ya no aparece. La
  causa era que la app de Claude usaba el `git` de Apple (que no está instalado); se creó
  `~/.zprofile` para que use primero el git que trae GitHub Desktop. Confirmado por la maestra.
- Se empieza **Matemáticas 2**: falta que la maestra comparta el temario y el apunte del Tema 1.

- Nuevo tema de Matemáticas 2: **Rectas paralelas, perpendiculares y oblicuas**
  (`matematicas-2/rectas-paralelas-perpendiculares-y-oblicuas.html`). Va sin número porque aún no
  hay temario. Se quitó el aviso de "temario no cargado" del índice de Matemáticas 2.
- Contenido a partir de 2 fotos del apunte: Nota (las 3 reglas), Ejemplo 1 (paralelas, m = 2/3) y
  Ejemplo 2 (perpendiculares, 3/2 y −2/3), cada uno con su gráfica de comprobación (misma escala en
  x y en y, escalones de Δx y Δy). En el apunte del ejemplo 2 los nombres L1/L2 estaban invertidos
  en el encabezado; se usó L₁: 6x − 4y + 8 = 0 y L₂: 2x + 3y + 9 = 0, como en el resto del apunte.
- 4 Productos de 3 pares de rectas (en cada uno: una paralela, una perpendicular y una oblicua, en
  distinto orden), con respuestas (m₁, m₂ y el tipo). Incluyen "trampas" de oblicuas: pendientes
  3 y −3, y −5 y −1/5. Nuevas clases en `style.css`: `.dos-rectas` y `.conclusion-ejemplo`.

- Rectas paralelas…: a petición de la maestra, en los Productos los alumnos también hacen la **gráfica
  de comprobación** de las dos rectas. Las respuestas ahora incluyen b₁ y b₂ además de m₁ y m₂.

- Rectas paralelas…: a petición de la maestra quedan solo **2 Productos** visibles. Los otros 2 pasaron
  a una pestaña desplegable **"Productos extra"** (oculta hasta que se abre), con sus propias
  respuestas, también ocultas. Nueva regla en `style.css`: `details.productos-extra`.

- Rectas paralelas…: a petición de la maestra, cada ejemplo y su gráfica quedan en **una sola caja**.
  El título "Ejemplo 1"/"Ejemplo 2" va afuera de la caja, arriba a la izquierda, y dentro la parte de
  la gráfica solo dice "Comprobación". Instrucción de ejercicios acortada. Nuevas clases:
  `.titulo-fuera` y `.titulo-comprobacion`.

- **⚠️ INSTRUCCIÓN IMPORTANTE DE LA MAESTRA (para todos los temas):** cada ejemplo, con su desarrollo
  y su gráfica de comprobación, va en **una sola caja** para que los alumnos puedan **imprimir cada
  ejemplo en una hoja tamaño carta**. Al hacer ejemplos nuevos hay que cuidar que cada caja quepa
  en una hoja carta (no hacerla demasiado alta). El título "Ejemplo N" va afuera de la caja, arriba
  a la izquierda, con el mismo estilo morado de los títulos (`titulo-regla-signos titulo-fuera`).

- Ajuste de impresión en `style.css` (`@media print`), para todo el sitio: hoja carta, sin encabezado,
  migas, pie ni enlaces de repaso; las cajas de ejemplo y de Productos no se parten entre hojas; las
  gráficas grandes se imprimen con máximo 380 px de alto. Medido: Ejemplo 1 ≈ 845 px y Ejemplo 2 ≈ 896 px
  de alto, menos que los ≈ 943 px que caben en una hoja carta con márgenes de 1.5 cm.

- Revisión de impresión en Matemáticas 1: los temas 2, 3, 4, 5, 6, 7, 9, 10 y 12 ya caben (cada caja en
  una hoja carta). No cabían el 1, el 8 y el 11 (varios ejemplos en una sola caja muy alta).
- **Tema 11** separado en 3 cajas (Ejemplo 1, 2 y 3, con el título afuera). Ahora miden ≈ 630–695 px,
  y cada una cabe en una hoja carta. El contenido no cambió. Faltan los temas 8 y 1.

- **Tema 8** separado para imprimir: la caja de la Regla queda igual; los 7 ejemplos (cortos) se
  repartieron en 2 cajas, "Ejemplos 1 a 3" (≈ 650 px) y "Ejemplos 4 a 7" (≈ 550 px), con el título
  afuera. No se hizo una caja por ejemplo porque son muy cortos y se gastaría mucho papel. Falta el Tema 1.

- Tema 8 (ajuste pedido por la maestra): al imprimir, la Regla quedaba sola en una hoja. Ahora la Regla
  y los ejemplos 1 a 3 van en la misma caja ("Regla y ejemplos 1 a 3", ≈ 755 px), y los ejemplos 1 y 2 van
  uno al lado del otro. Nuevas clases: `.ejemplos-lado-a-lado` (en celular se acomodan uno debajo del
  otro) y `.titulo-separado` (mismo estilo que `.titulo-comprobacion`).

- **Tema 1** separado para imprimir: "Ejemplo 1. Con decimales" y "Ejemplo 2. Con números naturales",
  cada uno en su caja con el título afuera (antes había un solo h2 "Ejemplo"). En el ejemplo con decimales,
  suma, resta y multiplicación quedan en una columna a la izquierda y la división a la derecha (nueva clase
  `.columna-operaciones`), así mide ≈ 816 px en lugar de ≈ 1015. Naturales ≈ 666 px. Contenido sin cambios.
  Con esto, **todos los temas de Matemáticas 1 caben en hoja carta** (cada caja en una hoja).

- Página de inicio: la tarjeta de Matemáticas 2 pasó de "Próximamente" (gris) a activa (degradado morado-
  fucsia), porque ya tiene su primer tema.

- Todo lo de hoy fue subido por la maestra con GitHub Desktop (2 commits) y verificado en línea: el tema
  de Rectas paralelas, los títulos morados afuera de las cajas y la tarjeta activa de Matemáticas 2.

- **Iconito de la pestaña** (antes salía gris): cuadro con degradado morado-fucsia y π en blanco.
  Archivos `favicon.svg` y `favicon.png` (180 px, también para iPhone) en la raíz; se agregaron los
  `<link rel="icon">` a las 22 páginas. Las páginas nuevas deben llevar esas mismas 3 líneas.

## 2026-10-09

- **Mat 1, Tema 5 (Operaciones con enteros):** todas las divisiones (ley de signos, ejemplo 6 y
  Productos 1–4) pasaron de "a ÷ b" a fracción (`.fraccion`). El ejemplo ya no lleva numeración
  (se quitaron los `num-circulo`) y queda alineado a la izquierda (la maestra probó centrado y prefirió
  izquierda); así el primer ejercicio ya no se corta en el celular. Último ejercicio del ejemplo: el
  paso de abajo ahora es 3(−2)(−2) en vez de 3(+4).
- Tema 5, ejercicio 4 de los Productos (para diversificar): P2 −4(5 − 9) = +16 y P3 −7(−4 − 6) = +70
  (respuestas actualizadas). P1 y P4 se quedan como estaban, por decisión de la maestra.
- Tema 5, ejercicio 7: P3 ahora −2(−6)² = −72 y P4 ahora −4(10)³ = −4000 (respuestas actualizadas).
- **Mat 1, Tema 7 (Potencias):** en la primera caja se quitaron las reglas generales (aⁿ…) y quedan solo
  los ejemplos numéricos, para que el estudiante deduzca la regla; título de la caja: "Potencias". Se
  quitó la numeración de esa caja y de la de Ejemplo (alineado a la izquierda).
  Además: todas las divisiones (÷) del tema pasaron a fracción (caja Potencias, Ejemplo y Productos 1–3);
  signo + en los exponentes que cambian de lugar en la fracción (7⁺², 5⁺⁴, 3⁺⁴, 7⁺³, 7⁺⁴); nuevo ejemplo
  de fracción con exponente negativo: (2/3)⁻² = (3/2)⁺² = 9/4.
  Ejercicio nuevo en cada Producto (ahora es el 7; los demás se recorren): P1 (3/4)⁻² = 16/9,
  P2 (2/5)⁻³ = 125/8, P3 (1/6)⁻² = 36 (respuestas agregadas).
  Productos del Tema 7 en dos columnas (nueva clase `.dos-columnas` en `ol.lista-extra`, en style.css).
  El exponente cero estaba escrito con "º" (símbolo de ordinal, como en 1º) y en el celular salía al
  lado del número. Además, en el celular de la maestra no se veía el 4 de "⁻⁴". Solución: en el Tema 7
  TODOS los exponentes pasaron de caracteres especiales (², ⁻⁴…) a `<sup>` con números normales
  (p. ej. `7<sup>−4</sup>`), que se ven bien en cualquier celular. Preferir `<sup>` en temas nuevos.
  Ojo: dentro de `ol.lista-extra li` (que es flex) el `<sup>` no sube y 10⁰ parecía "100"; en
  `.dos-columnas` los `li` ahora son `display: block` y hay regla de tamaño/altura para `sup`.
- **Mat 1, Tema 8 (Radicales):** mismo problema en el celular (2¹⁰, 3¹² desalineados): todos los exponentes
  pasaron a `<sup>`. La regla de `sup` en Productos/Respuestas excluye `.indice` (índice del radical).
- **Mat 1, Tema 9 (Operaciones con polinomios):** el ejemplo ya no lleva numeración y se quitaron las
  líneas de regla de signos "(+)(−) = −" y "(−)(−) = +" debajo de los ejemplos 3 y 4. Todos los
  exponentes pasaron a `<sup>`. Nueva regla en style.css: los `li` de Productos que tienen `<sup>` son
  `display: block` (`li:has(sup:not(.indice))`), para que el exponente suba y no se pierdan espacios.
  Ejercicio 4 (división) de P2 y P4: se invirtieron los coeficientes para que el número solo se simplifique:
  P2 6a⁵b⁹c⁴ / −48a²b³c⁴ = −a³b⁶/8; P4 8m⁹n⁵p⁷ / 72m⁴n⁵p³ = m⁵p⁴/9 (respuestas actualizadas).
  Nuevo ejemplo (después del de división exacta): 5x⁶y⁴z³ / −20x²y³z³ = −x⁴y¹/4, con el paso 5/−20 = −1/4.
  Radicales con número entero en el radicando: ejemplo ∛(8x³y⁹z¹⁸) = 2x¹y³z⁶ (paso ∛(2³x³…), sin la nota "8=2³" por decisión de la maestra);
  ejercicio 6 de Productos: P1 ∛125… = 5a²b¹c⁴, P2 ⁴√16… = 2x²y¹z³, P3 ⁵√243… = 3a²b¹c³,
  P4 ∛−64… = −4x³y⁵z¹ (respuestas actualizadas).
  Después: en el ejemplo se quitaron los pasos (renglones de proceso) de multiplicación, divisiones,
  potencia y raíz — ya están en el Tema 7 y la maestra quiere que lo apliquen de memoria. Los ejemplos 1
  y 2 (suma y resta) conservan sus pasos; también se dejaron "5/−20 = −1/4" y "∛(2³x³y⁹z¹⁸)".
- Pendiente: la maestra revisará en su celular el exponente ⁴ del Tema 5 (Producto 1: (−2)⁴ y 3(−2)⁴);
  si no se ve, pasar a `<sup>`. Próxima sesión: temas de Matemáticas 2.
- **Mat 1, Tema 10 (Ecuaciones):** ejemplo centrado (clase `.centrado` en `.lista-ejemplo-vertical`, regla en
  style.css) y sin numeración; así el primer renglón de los ejemplos 2 y 3 cabe completo en el celular.
  Signo = alineado en la misma columna en todos los pasos (idea de balanza): cada renglón es
  `.fila` con `.lado-izq` / `.igual` / `.lado-der` dentro de `.ecuacion-alineada` (grid de 3 columnas).


<!-- Nueva entrada: agrega fecha (AAAA-MM-DD) y una lista breve de qué se hizo, qué se decidió y qué falta. -->

## 2026-10-12

- Nuevo tema de Matemáticas 2: **Representación de racionales p/q, q ≠ 0**
  (`matematicas-2/representacion-de-racionales.html`), a partir de una foto del apunte. Va sin número
  (aún no hay temario) y quedó enlazado en el índice de Matemáticas 2.
- Ejemplo con 14/10 en una tabla: figura (2 barras de 10 partes), fracción y fracción mixta (1 4/10),
  fracción equivalente, decimal (1.4 con la división), porcentaje (140 %) y recta (0 a 2, en décimos).
  Correcciones confirmadas por la maestra: el porcentaje es 140 % (en la foto decía 100 %), y la fracción
  equivalente queda 7/5, 28/20, 56/40. En los ejercicios, la idea es que los alumnos escriban el número
  que falta; en el ejemplo los números que faltaban van resaltados.
- En el celular, la tabla se acomoda en bloques (nombre arriba y resultado abajo). Nueva clase
  `table.tabla-representaciones` en style.css.
- Pendiente: la maestra sugirió "agregar una columna más" (falta aclarar si es otro ejemplo, más números
  en los Productos o una explicación) y decidir los Productos (en la foto, columnas con 10/3 y con la
  recta en 3/5 para completar).
- Rep. de racionales (pedido de la maestra): la tabla del ejemplo ahora tiene **3 columnas más** para
  completar, como en el apunte: a) dato 10/3 y 3 1/3; b) dato la recta (0 a 2 en quintos, punto en 3/5);
  c) dato solo la fracción equivalente 6/8, 3/__, __/16 (propuesta de Claude; respuestas 4 y 12).
  Las demás celdas quedan en blanco para que escriban. En el celular la tabla se desliza de lado
  (`.tabla-deslizable`); ya no se acomoda en bloques. La caja mide ≈ 680 px (cabe en hoja carta).
- Rep. de racionales: **Producto 1 y 2** (propuestos por Claude, a petición de la maestra), con la misma
  tabla de 4 columnas a)–d), cada una con un solo dato de inicio distinto, y sus respuestas (desplegables).
  P1: a) figura 7/4, b) decimal 0.8, c) porcentaje 250 %, d) recta en cuartos con punto en 5/4.
  P2: a) fracción mixta 2 1/4, b) equivalentes 9/6, 3/__, __/8, c) porcentaje 45 %, d) figura 2/5.
  En las rectas de los Productos el punto no lleva etiqueta (el alumno lee la fracción). Cada caja de
  Producto mide ≈ 580 px (cabe en hoja carta). Nueva clase: `.producto-tabla`.
- **Inicia la numeración de Matemáticas 2:** Representación de racionales es el **Tema 1** (archivo
  renombrado a `matematicas-2/tema-1-representacion-de-racionales.html`; título, migas y pestaña con
  "Tema 1."). En el índice va primero. Rectas paralelas… sigue sin número hasta que la maestra diga cuál le toca.
- Tema 1, Producto 2 a): ahora se da la fracción y la fracción mixta (9/4 , 2 1/4), como en el ejemplo;
  antes la fracción estaba en blanco.
- **Mat 2, Tema 2. Operaciones básicas con racionales** (`matematicas-2/tema-2-operaciones-basicas-con-racionales.html`),
  título elegido por la maestra (el apunte decía "Operaciones con fracciones"). Ejemplo de la foto en una caja:
  1) suma y resta −3/4 + 1/2 − 6/3 + 3/12 = −2, con tabla de mcm (4, 2, 3, 12 → 12) y amplificación resaltada;
  2) (3/2)(4/5) = 12/10 = 6/5; 3) división como fracción sobre fracción (−5/3 entre 4/6) = −30/12 = −15/6 = −5/2
  (nueva clase `.fraccion-doble`); 4) (2/5)<sup>2</sup> = 4/25; 5) ∛(−8/27) = ∛(−2³/3³) = −2¹/3¹ con tablas de
  factores — la maestra pidió dejarlo así, sin "= −2/3". Caja ≈ 560 px en computadora, ≈ 770 en celular.
  Enlazado en el índice como Tema 2. Pendiente: Productos 1 y 2.
- Tema 2, ejemplo 1 (pedido de la maestra): primero se escribe la operación tal cual
  (−3/4 + 1/2 − 6/3 + 3/12 =) y abajo el desarrollo (amplificación, etc.).
- Tema 2, ejemplo 2: se quitó el "÷ 2"; queda (3/2)(4/5) = 12/10 = 6/5.
- Tema 2: **4 Productos** visibles (pedido de la maestra; tema corto, sin gráfica), 5 ejercicios cada uno:
  suma/resta de 4 fracciones, multiplicación, división (fracción sobre fracción), potencia y raíz
  (cúbica, cuadrada, cúbica negativa y cuarta). Respuestas variadas (enteras 1, 4, −6; negativas; fracciones)
  y verificadas. Instrucción: "Resuelve y simplifica el resultado." Cada caja de Producto ≈ 305 px
  (cabe de sobra en hoja carta; las cajas no se parten al imprimir).
- Tema 1, **Producto 1** reacomodado para parecerse al ejemplo (pedido de la maestra): a) figura 7/4;
  b) fracción y fracción mixta 8/5 , 1 3/5; c) recta en cuartos con el punto en 5/4 (con etiqueta, como en
  el ejemplo); d) fracción equivalente 10/4 , 5/__ , __/8 (faltan 2 y 20; mismo patrón del ejemplo). Respuestas actualizadas.
  Producto 2 se queda con datos variados. La maestra vio "un error" en la fracción equivalente del
  Producto 2 (9/6 , 3/__ , __/8): quería que siga el patrón del ejemplo (simplificar y luego ampliar al doble del denominador): ahora es 9/6 , 3/__ , __/12 (faltan 2 y 18).
- Todo lo de hoy (Mat 2: Tema 1 y Tema 2) fue subido por la maestra con GitHub Desktop y revisado en línea.
- Pendiente: decidir el número de "Rectas paralelas, perpendiculares y oblicuas" (sigue sin número a
  propósito) y el siguiente tema de Matemáticas 2.
- **⚠️ INSTRUCCIÓN IMPORTANTE DE LA MAESTRA (para todos los temas):** el **Producto 1** debe ser **muy
  parecido al ejemplo** (mismo tipo de datos, en la misma posición y con el mismo patrón), para que el
  cambio sea pequeño y los alumnos puedan resolverlo. En los Productos siguientes se van metiendo
  cambios **poco a poco** (gradualmente), no todos de golpe.

## 2026-10-18

- Nueva sección **Admisión a Licenciatura** (carpeta `admision-licenciatura/`, pedido de la maestra), con su
  `index.html` igual que las demás materias (aviso de "temario todavía no cargado" y lista de temas vacía).
  Enlazada en la página principal como tarjeta "Próximamente", después de Problemas Interprepas.
  Pendiente: que la maestra suba el temario o material de esta sección.
- Admisión a Licenciatura: **Tema 1. Física** (`admision-licenciatura/tema-1-fisica.html`), pedido de la maestra.
  Por ahora es una página vacía con aviso de "contenido todavía no cargado"; ya está enlazada en la lista de
  temas de la sección (se quitó el aviso de "temario no cargado" del índice). Todo sigue solo en la computadora
  (la maestra no quiere subirlo todavía). Pendiente: el material de Física (ejemplos, ejercicios).
- La maestra eligió **Cinemática** como Tema 1 (de Física): el archivo se renombró a
  `admision-licenciatura/tema-1-cinematica.html` (ya no existe `tema-1-fisica.html`); en la lista dice
  "Física · Tema 1. Cinemática". Ejemplo: el problema de la gráfica distancia–tiempo del coche (foto de la
  maestra), dibujado en SVG con secciones I–IV, explicación de cómo leer la inclinación y tabla de respuesta
  (uniforme: II; acelerado: I y III; reposo: IV). No se copiaron las opciones A–D (la D venía cortada en la foto).
  Pendiente: Productos (ejercicios). Sigue sin subirse.
- Cinemática: el ejemplo del coche ahora es **Ejemplo 1**; se agregó **Ejemplo 2** (foto de la maestra):
  velocidad media del patinador, gráfica d–t con puntos (0,0), (5,8), (12,8), (15,16), dibujada con cuadrícula
  de misma escala (1 cuadrito = 1 s = 1 m). Pasos: 16 m ÷ 15 s ≈ 1.07 m/s; tabla de velocidades por tramo
  (1.6, 0, 2.67) y aviso de que la velocidad media no es el promedio de esas velocidades. Sin opciones A–D.

## 2026-10-18

- **Admisión a Licenciatura: nueva página "Física · Guía práctica"** (`admision-licenciatura/guia-practica-fisica.html`),
  enlazada en la lista de temas. Preguntas de opción múltiple que la maestra manda en capturas: el alumno da clic en
  A–D, la correcta se pinta morada y la elegida incorrecta fucsia (colores de la paleta, no verde/rojo), aparece una
  explicación corta y un botón "Intentar otra vez". Al imprimir no salen las explicaciones. Estilos nuevos al final de
  style.css (`.opciones`, `.opcion`, `.retro`, `.veredicto`). Para agregar una pregunta se copia un `<section>` y se
  cambia `data-correcta`.
  Pregunta 1: rapidez media (respuesta D). Pregunta 2: gráfica x–t del ferrocarril (respuesta C, velocidad constante),
  gráfica redibujada en SVG con cuadritos cuadrados (0.1 s × 5 m). Pendiente: la opción D de la pregunta 2 venía cortada.
  Pregunta 3: aceleración centrípeta del auto de prueba (a = v<sup>2</sup>/r = 625/20 = 31.25 m/s², respuesta B).
  Pregunta 4: encuentro de dos trenes (se acercan 45 + 60 = 105 km cada hora; 360 ÷ 105 ≈ 3.4 h, respuesta D).
  Pregunta 5: lancha en el río, misma dirección (8 + 2 = 10 m/s, respuesta D).
  Pregunta 6: piedra lanzada hacia arriba, tiempo hasta el punto más alto (39.2 ÷ 9.8 = 4.0 s, respuesta A).
  Pregunta 7: auto que arranca con a = 18 m/s², velocidad a los 2 s (0 + 18 · 2 = 36 m/s, respuesta D).
  Pregunta 8: caída libre sin fricción, la velocidad aumenta 9.8 m/s cada segundo (respuesta A).
  Pregunta 9: aceleración en caída libre, constante e igual a g (respuesta D).
  Pregunta 10: gráfica v–t (línea que baja hasta 0), redibujada en SVG. La opción D venía cortada; la maestra pidió que Claude la redactara: "Un lanzamiento vertical hacia arriba hasta que el cuerpo se detiene" (respuesta D).
  Pregunta 11: altura máxima del proyectil (80 · sen 30° = 40 m/s; 40² ÷ 20 = 80 m, respuesta A). La captura no
  traía la respuesta marcada; la calculó Claude.
  Pregunta 12: objeto que se deja caer desde 6.05 m (v² = 2 · 10 · 6.05 = 121; v = 11 m/s, respuesta C). La captura
  no traía la respuesta marcada; la calculó Claude y la maestra confirmó la C con otra captura.
- **Página principal reorganizada en dos cajas** (pedido de la maestra): caja **"Matemáticas"** (Mat 1–5, Optativa y
  Problemas Interprepas) y caja **"Guía de Admisión a Licenciatura"** con 8 materias: Matemáticas, Física, Biología,
  Historia de México, Literatura, Química, Geografía e Historia Universal. Estilo nuevo `.grupo-materias` /
  `.titulo-grupo` al final de style.css (caja lila suave con borde, tarjetas blancas dentro).
- **Carpetas nuevas**: una subcarpeta por materia dentro de `admision-licenciatura/` (`matematicas`, `fisica`,
  `biologia`, `historia-de-mexico`, `literatura`, `quimica`, `geografia`, `historia-universal`), cada una con su
  `index.html`. Física (Tema 1. Cinemática y Guía práctica) se movió a `admision-licenciatura/fisica/`; las demás
  muestran "ejercicios todavía no cargados". `admision-licenciatura/index.html` ahora muestra las 8 materias en
  tarjetas. Sigue sin subirse.
- **Cambio sobre lo anterior (pedido de la maestra): las materias quedan "ocultas"**. La página principal ya no
  muestra las cajas con todas las materias, solo **dos tarjetas grandes**: "Matemáticas" (abre la página nueva
  `matematicas.html`, con Mat 1–5, Optativa e Interprepas) y "Guía de Admisión a Licenciatura" (abre
  `admision-licenciatura/index.html`, con las 8 materias). Se quitaron los estilos `.grupo-materias`/`.titulo-grupo`
  y se agregó `.tarjetas-principales`. En el índice de cada materia de matemáticas el enlace de arriba ahora dice
  "← Volver a Matemáticas" (antes "Volver al inicio"). Sigue sin subirse (la maestra todavía no quiere).
- Las dos tarjetas de la página principal ya no llevan texto debajo: solo el título en letras grandes
  ("Matemáticas" y "Guía de Admisión a Licenciatura"), pedido de la maestra.
- Fin de la sesión del 2026-10-18. Pendientes: que la maestra confirme la respuesta de la Pregunta 11 de Física
  (proyectil, se puso A = 80 m); subir los cambios cuando ella lo decida (todo lo de hoy sigue solo en la computadora);
  agregar ejercicios de las demás materias de la Guía de Admisión.

## 2026-10-19

- **Mat 2, Tema 4. Razones, proporciones y porcentajes** (`matematicas-2/tema-4-razones-proporciones-y-porcentajes.html`),
  hecho a partir de la foto del apunte de la maestra: 4 ejemplos en una caja (proporción con comprobación, proporción
  directa con los discos, proporción inversa con los hombres y la barda "se invierten", descuento del 30% al televisor).
  4 Productos de 4 ejercicios cada uno (el Producto 1 sigue el mismo patrón que los ejemplos) con respuestas ocultas.
  Enlazado en `matematicas-2/index.html`. Falta que la maestra lo revise.
- **Tema 3. Jerarquía de operaciones con racionales**: la maestra todavía no tiene los ejercicios; aún no se agrega a la
  lista (pendiente preguntarle si lo pone ya con "ejercicios todavía no cargados").
- **Temario de Matemáticas 2 (completo, dictado por la maestra)**: 1. Representación de racionales;
  2. Operaciones básicas con racionales; 3. Jerarquía de operaciones con racionales; 4. Razones, proporciones y
  porcentajes; 5. Semejanza de triángulos; 6. Teorema de Tales; 7. Teorema de Pitágoras; 8. Trigonometría; 9. Ley de senos y cosenos; 10. Distancia entre dos puntos; 11. Pendiente y ordenada al origen; 12. Rectas paralelas y perpendiculares; 13. Estadística; 14. Estadística y gráficas. "Rectas
  paralelas, perpendiculares y oblicuas" = Tema 12.
- "Rectas paralelas, perpendiculares y oblicuas" ahora es el **Tema 12** (confirmado por la maestra): número agregado en
  la pestaña, el título, la ruta de arriba y la lista de Matemáticas 2. El nombre del archivo no cambió.
- La lista de Matemáticas 2 ahora muestra los 14 temas del temario. Los que todavía no tienen página (3, 5–11, 13, 14)
  aparecen como cajita punteada con "(Próximamente)" (estilo nuevo `li.tema-pendiente` en style.css); al hacer cada
  página, cambiar ese `<li>` por un enlace normal. Pendiente: material (fotos) de cada tema.
- **Temario de Matemáticas 3 (la maestra empezó a dictarlo)**: 1. Operaciones con polinomios; 2. Productos notables.
  Ojo: ya existe `matematicas-3/tema-1-funciones-y-relaciones.html` ("Tema 1. Funciones y relaciones: la prueba de la
  recta vertical"); falta que la maestra diga qué número le toca. Mat 1 ya tiene "Tema 9. Operaciones con polinomios".
  La maestra confirmó que Operaciones con polinomios de Mat 3 lleva material propio, más avanzado (no copiar el de Mat 1).
- **"Funciones y relaciones: la prueba de la recta vertical" se movió de Mat 3 a Mat 4** (pedido de la maestra), sin
  número porque aún no sabe en qué posición queda: ahora es `matematicas-4/funciones-y-relaciones.html`, enlazada desde
  `matematicas-4/index.html`. La lista de Mat 3 ahora muestra Tema 1. Operaciones con polinomios y Tema 2. Productos
  notables como "(Próximamente)".
- La maestra **confirmó la respuesta de la Pregunta 11 de Física** (proyectil, A = 80 m). Va a subir todos los cambios.
- Mat 2, Tema 4: la maestra subió los cambios. Después pidió reordenar los Productos 3 y 4. **Producto 3**: porcentaje,
  proporción, inversa, directa (el orden que ella dio). **Producto 4**: inversa, porcentaje, directa, proporción (orden
  elegido por Claude para variar). Respuestas reordenadas igual. Falta subirlo.
- La maestra revisó en internet el nuevo orden del Tema 4 y ya se ve. **Regla nueva para todos los temas**: el
  Producto 1 sigue el orden del ejemplo; en los Productos siguientes (3 y 4) los tipos de ejercicio van revueltos, en un
  orden distinto en cada uno, para que el alumno analice y no conteste en automático.
- **Audios de estudio para la maestra (no son parte del sitio, no se suben)**: con la voz "Paulina" de la Mac (`say`).
  Historia de México en `~/Audios Historia de Mexico/` (01 La Nueva España, 02 La Independencia, 03 México
  independiente) e Historia Universal en `~/Audios Historia Universal/` (01 La Historia, 02 Revoluciones burguesas,
  03 Pensamiento y movimientos del siglo XIX, 04 Capitalismo y socialismo, 05 El mundo actual; la maestra dijo que son
  todos los temas). Cada carpeta tiene `guiones/` con el texto, que puede servir de base para las guías de la página.
  Pendiente: hacer la guía de Historia de México / Universal para subirla.
- La maestra pasó los audios a su celular por WhatsApp.
- Fin de la sesión del 2026-10-19. Pendientes: subir los cambios de Mat 3 (lista con Temas 1 y 2 "Próximamente"),
  Mat 4 ("Funciones y relaciones" sin número) y esta bitácora; material (fotos) de los temas que faltan en Mat 2 y
  Mat 3; número de "Funciones y relaciones" en Mat 4; guías de Historia para la Guía de Admisión.

## 2026-10-24

- **Mat 2, Tema 10. Distancia entre dos puntos** (foto de la maestra): nueva página
  `matematicas-2/tema-10-distancia-entre-dos-puntos.html`, ya enlazada en la lista de Matemáticas 2 (dejó de ser
  "Próximamente"). Lleva la caja de la Fórmula con su dibujo del triángulo, el Ejemplo 1 (P₁(1, 2), P₂(4, 6), d = 5)
  con su gráfica en la misma caja, Productos 1 y 2 visibles y 2 Productos extra ocultos, con respuestas.
  Producto 1 sigue el patrón del ejemplo (coordenadas positivas, resultado exacto); el Producto 2 agrega negativos;
  los Productos extra revuelven el orden e incluyen dos resultados que no son exactos (√13 ≈ 3.61 y √29 ≈ 5.39) —
  falta que la maestra confirme si los quiere así. Estilos nuevos en style.css: `.segmento` (rayita sobre P₁P₂),
  `.formula-distancia` y `.dato-etiquetado` (x₁, y₁ arriba de cada número). Falta subirlo.
- La vista previa local (`.claude/launch.json`) ahora usa `/usr/bin/ruby` en vez de python3, porque python3 abre la
  ventana de instalar herramientas de Apple; ruby viene con la Mac y no la abre.
- La maestra pidió manejar los Productos extra del Tema 10 como **Producto 3 y Producto 4**, visibles (ya no ocultos),
  con sus respuestas en la misma pestaña "Respuestas" que los Productos 1 y 2. Le gustaron los Productos que hizo Claude.
- La maestra confirmó que le gusta que la dificultad suba poco a poco de un Producto al siguiente (en el Tema 10: positivos → negativos → orden revuelto y resultados no exactos). Aplicarlo así en los temas nuevos.
- La maestra subió el Tema 10 de Mat 2 a GitHub (2026-10-24). Comprobado en internet: la página, los 4 Productos, los estilos y el enlace en la lista de Mat 2 ya se ven. `.claude/launch.json` se quedó sin subir (es archivo de trabajo de Claude).
- Mat 2, Tema 11 renombrado (pedido de la maestra) a "Ecuación general a partir de la gráfica" (antes "Pendiente y ordenada al origen") (sigue como Próximamente). Falta subirlo.
- **Mat 2, Tema 11. Ecuación general a partir de la gráfica** (foto de la maestra): nueva página
  `matematicas-2/tema-11-ecuacion-general-a-partir-de-la-grafica.html`, enlazada en la lista de Mat 2. Ejemplo en una
  caja: gráfica a la izquierda (b = −3, escalones +4 y −3) y pasos a la derecha hasta 4x + 3y + 9 = 0. Ejercicios: cada
  uno es una gráfica chiquita (3 por Producto, pedido de la maestra); Productos 1 y 2 visibles y 2 Productos extra
  ocultos (también pedido por ella). Respuestas con m, b, y = mx + b y la ecuación general (con x positiva).
  Estilos nuevos en style.css: `.una-columna`, `.graficas-ejercicio`, `.numero`, `.pasos-lado`. Falta subirlo.
- Tema 11: en la explicación del ejemplo la maestra pidió "se avanza −3 (Δx)" en vez de "3 a la izquierda" (usar el signo, no la dirección).
- Tema 11: la maestra notó que en las gráficas de los Productos los puntos no caían en cruces de la cuadrícula. Causa: la cuadrícula estaba recorrida medio cuadrito. Corregido en las 12 gráficas; ahora los puntos quedan en coordenadas enteras.
- La maestra subió el Tema 11 y ya se ve en internet (tardó unos minutos en aparecer). Fin de la sesión del 2026-10-24. Pendientes: decidir si el Tema 12 usa signos en los escalones ("se avanza +3", "−2"); confirmar la forma de la ecuación general con pendiente positiva (x positiva); fotos de los temas que faltan (Mat 2: 3, 5–9, 13, 14; Mat 3). Esta entrada de la bitácora todavía no está subida.

## 2026-11-03

- **Apartado de exámenes con contraseña**: carpeta `cuadernos/`, sin enlaces desde el resto del sitio y con `noindex`. Las páginas van cifradas: sin la contraseña no se puede leer su contenido. Cada versión tiene una hoja para imprimir, en cajas por tema, y una hoja resuelta para calificar. Formato inspirado en el ejemplo de una amiga de la maestra.
- La maestra mandó las cuatro versiones de un examen de Matemáticas 1. Las copias sin cifrar, el programa que arma las hojas y el que las cifra están en `~/Examenes-originales`, fuera de este repositorio. **Nunca copiar esos archivos aquí ni subirlos.** Después de cambiar un examen, hay que volver a cifrar con `/usr/bin/ruby ~/Examenes-originales/cifrar.rb`.
- **No escribir en esta bitácora los ejercicios ni las respuestas de los exámenes**, porque este archivo es público. Las dudas de lectura de las fotos se le pasaron a la maestra en el chat; algunas siguen sin confirmar.
- Es provisional: sirve para que la maestra califique e imprima. Cuando termine, se harán los exámenes definitivos de AntonyMathClass.
- En la Mac de la maestra las páginas abiertas desde la carpeta no cargaban el diseño de archivos aparte (causa no confirmada), por eso el diseño va dentro de cada examen.
- Exámenes: la maestra vio que al imprimir el examen salía muy grande y en dos hojas. Se compactó la letra y los espacios solo para impresión; en una prueba con Chrome cada versión ya sale en una hoja carta. Falta que ella lo confirme en su impresión y volver a cifrar.
- Exámenes: la maestra confirmó que abierto en Chrome el examen se imprime en una sola hoja. Para imprimir, usar Chrome. Falta volver a cifrar y subirlo.
- La maestra subió los exámenes cifrados. Comprobado en internet: `cuadernos/` pide contraseña, las páginas revisadas no muestran ejercicios legibles y la página principal no enlaza a ellos. Esta entrada todavía no está subida. Pendiente: que confirme las dudas de lectura de las fotos; si algo cambia, corregir en `~/Examenes-originales`, volver a cifrar y subir.
- Exámenes: la maestra encontró al calificar un dato mal leído de la foto en un ejercicio de jerarquía de la versión C. Corregido en la copia original; falta volver a cifrar y subirlo.

## 2026-11-10

- **Guía de Admisión, Historia de México: nueva Guía práctica** (`admision-licenciatura/historia-de-mexico/guia-practica-historia-de-mexico.html`), con el mismo formato que la de Física (opciones, veredicto y explicación corta). Enlazada en la lista de la materia; se quitó el aviso de "todavía no están cargados". Pregunta 1: tropas de Cortés (subtema "Descubrimiento y conquista militar y espiritual de México"). La maestra mandó la captura del reactivo solo con el inciso C (derrota de Narváez, marcado incorrecto); los incisos A, B y D y la respuesta (B, alianza con los tlaxcaltecas) los propuso Claude a pedido de ella. Falta subirlo.
- Guía práctica de Historia de México, Pregunta 2: capitulación (reactivo dictado por la maestra con incisos Capitulación, Cédula Real, Requerimiento, Encomienda; después pidió cambiar los incisos y Claude puso Bula papal, Merced real, Capitulación, Repartimiento; respuesta C). Ella escribió "y aprobarlos"; Claude puso "y poblarlos"; ella contestó "Es correcto, debe decir probarlos" y Claude lo tomó como confirmación de "poblarlos" (después lo confirmó: "poblarlos").
- Guía práctica de Historia de México, Pregunta 3: evangelización de los indígenas (captura de la maestra con los cuatro incisos, sin la respuesta marcada; Claude puso como correcta la B, misión y congregación; falta que ella la confirme con su sistema). Después pidió redactarla con otras palabras: Claude cambió el enunciado y los cuatro incisos (misma idea, misma respuesta B); la explicación conserva los términos del reactivo original. Falta subirlo.
- Fin de la sesión del 2026-11-10. La Guía práctica de Historia de México lleva 3 preguntas y no está subida (tampoco el cambio en la lista de la materia ni esta bitácora). Pendientes: que la maestra confirme en su sistema la respuesta de la Pregunta 3; seguir agregando reactivos; exámenes: volver a cifrar y subir la corrección de la versión C. Falta subirlo.

## 2026-11-11

- **Guía de Admisión, Historia Universal: nueva Guía práctica** (`admision-licenciatura/historia-universal/guia-practica-historia-universal.html`), con el mismo formato que la de Historia de México. Enlazada en la lista de la materia; se quitó el aviso de "todavía no están cargados". Pregunta 1: mercantilismo (captura de la maestra, reactivo 17 de su sistema, con los cuatro incisos y sin la respuesta marcada; Claude puso como correcta la D y redactó la explicación; texto del reactivo tal como venía). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 2: despotismo ilustrado (captura de la maestra solo con el enunciado y el inciso D, Enciclopedia, marcado incorrecto; los incisos A Reforma, B Contrarreforma y C Ilustración, y la respuesta C, los propuso Claude; falta que ella los confirme o mande los incisos reales). Falta subirlo.
- Pregunta 2 de Historia Universal: la maestra confirmó que se quedan los incisos propuestos por Claude (Reforma, Contrarreforma, Ilustración, Enciclopedia). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 3: causas de la Independencia de las Trece Colonias (captura de la maestra, reactivo 23 de su sistema, con los cuatro incisos tal como venían y sin la respuesta marcada; Claude puso como correcta la B y redactó la explicación). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 4: Guerra de los Siete Años como causa externa (captura de la maestra, reactivo 24 de su sistema, con los cuatro incisos; en la captura estaba seleccionada la B, sin veredicto; Claude puso como correcta la A, Trece Colonias, y se lo avisó; el enunciado venía cortado y Claude completó "de la"; falta que ella confirme la respuesta). Falta subirlo.
- Pregunta 4 de Historia Universal: la maestra confirmó que su sistema marcó la B como incorrecta (coincide con la A que puso Claude; el sistema no le mostró cuál es la correcta). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 5: causas externas de la Independencia de las Trece Colonias (captura de la maestra solo con el enunciado y los enunciados I a IV, sin incisos ni respuesta; los incisos A "I y II", B "I y IV", C "II y III", D "III y IV" y la respuesta B los propuso Claude; falta que ella los confirme o mande los reales). Falta subirlo.
- Pregunta 5 de Historia Universal: la maestra confirmó que se quedan los incisos propuestos por Claude (I y II, I y IV, II y III, III y IV). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 6: documento con el que Gran Bretaña reconoció la independencia de Estados Unidos (captura de la maestra solo con el enunciado, sin incisos ni respuesta; los incisos A Declaración de Independencia, B Constitución de los Estados Unidos, C Tratado de París y D Tratado de Utrecht, y la respuesta C, los propuso Claude; falta que ella los confirme o mande los reales). Falta subirlo.
- Pregunta 6 de Historia Universal: la maestra confirmó que se quedan los incisos propuestos por Claude (Declaración de Independencia, Constitución de los Estados Unidos, Tratado de París, Tratado de Utrecht). Falta subirlo.
- La maestra pidió subir a GitHub; Claude le dio los pasos de GitHub Desktop (5 archivos; sin `.claude/launch.json` ni `.DS_Store`). Falta que confirme que lo subió y revisar en internet.
- Guía práctica de Historia Universal, Pregunta 7: Congreso como aportación política de las Trece Colonias (captura de la maestra solo con el enunciado, sin incisos ni respuesta; los incisos A Haití, B Brasil, C México y D Canadá, y la respuesta C, los propuso Claude; falta que ella los confirme o mande los reales). Falta subirlo.
- Pregunta 7 de Historia Universal: la maestra pidió no subirla hasta revisar los incisos en su sistema. Claude la quitó de la página (la guía queda con 6 preguntas). Pendiente: cuando ella mande los incisos reales, volver a agregarla.
- La maestra mandó otro reactivo de Historia Universal (dos causas internas de la Revolución Francesa, con dos espacios en blanco y sin incisos). Claude no lo agregó a la página: le dio la respuesta probable en el chat y le pidió los incisos de su sistema. Pendiente.
- Guía práctica de Historia Universal, nueva Pregunta 7: causas internas de la Revolución Francesa (captura de la maestra, reactivo 34 de su sistema, con los puntos I a IV y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, II y IV, y redactó la explicación). Ocupa el número 7 que dejó libre la pregunta del Congreso, que sigue pendiente. Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 8: Haití y la Revolución Francesa como antecedentes (captura de la maestra solo con el enunciado; ella pidió que Claude propusiera los incisos: A las Trece Colonias, B Hispanoamérica, C África, D Asia; respuesta B). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 9: relacionar países con libertadores (captura de la maestra con las dos listas y solo el inciso C, que ella eligió, sin veredicto visible; Claude lo dejó como correcto, C, y propuso los incisos A, B y D con el orden revuelto; falta que ella los confirme). Falta subirlo.
- Guía práctica de Historia Universal, Pregunta 10: personaje de la independencia de Chile, Argentina y Perú (captura de la maestra solo con el enunciado; los incisos A Simón Bolívar, B Francisco Miranda, C José de San Martín y D Miguel Hidalgo y Costilla, y la respuesta C, los propuso Claude; falta que ella los confirme, igual que los de la Pregunta 9). Falta subirlo.
- Pregunta 10 de Historia Universal: la maestra pidió que Claude generara los incisos; se quedan los propuestos.

## 2026-11-15

- **Guía de Admisión, Literatura: nueva Guía práctica** (`admision-licenciatura/literatura/guia-practica-literatura.html`), con el mismo formato que las de Historia, pero **sin explicación** (la maestra lo pidió así: solo aparece si acertó y el botón de intentar otra vez). Enlazada en la lista de la materia; se quitó el aviso de "todavía no están cargados". Pregunta 1: relacionar fragmentos de una oración con sujeto, objeto directo, objeto indirecto y complemento circunstancial (captura de la maestra con el enunciado, las dos listas y solo el inciso A, que ella eligió; Claude lo verificó como correcto y propuso los incisos B, C y D con el orden revuelto, y redactó la instrucción "Relaciona cada fragmento…" porque no venía en la captura; falta que ella los confirme o mande los reales). Falta subirlo.
- Pregunta 1 de Literatura: la maestra confirmó que se quedan los incisos propuestos por Claude. Claude también le mostró en el chat un mapa conceptual de las partes de la oración (sujeto: núcleo y modificadores; predicado: núcleo, objeto directo, objeto indirecto y complemento circunstancial); no está en el sitio, falta que ella diga si lo quiere en la página. Falta subirlo.
- Pregunta 1 de Literatura: **mapa conceptual "Para repasar: partes de la oración"** dentro de la pregunta; aparece después de contestar, junto con el veredicto (la maestra lo eligió entre 4 opciones: caja que se abre, siempre visible, después de contestar, página aparte). Usa otra oración de ejemplo propuesta por Claude para no dar la respuesta ("La joven maestra explica pacientemente las lecciones a sus alumnos."); falta que la maestra la revise. Estilos nuevos en `style.css` (`.mapa-oracion`, `.mapa-rama`…): sujeto en morado, predicado en fucsia; en celular las dos ramas quedan una debajo de la otra. Falta subirlo (archivos: la guía de Literatura, la lista de Literatura, `style.css` y esta bitácora).
- Guía práctica de Literatura, Pregunta 2: relacionar la estructura de un texto argumentativo (presentación del tema, tesis, argumentación, conclusión) con cinco ideas sobre los antibióticos (captura de la maestra con las dos listas y solo el inciso C, I: a – II: e – III: d – IV: b, que su sistema marcó incorrecto; sin la instrucción ni los demás incisos). Sin explicación, como la Pregunta 1. Claude puso como correcta la B (I: c – II: d – III: a – IV: e), dejó la C de la captura como incorrecta y propuso la instrucción y los incisos A y D. Pendiente: que la maestra confirme la respuesta en su sistema (si sale incorrecta, la alternativa es con la "b" en la argumentación: I: c – II: d – III: b – IV: e). Falta subirlo.
- Pregunta 2 de Literatura: la maestra confirmó que la B (I: c – II: d – III: a – IV: e) es la correcta. Se quedan la instrucción y los incisos propuestos. Falta subirlo.
- **Guía de Admisión, Matemáticas: nueva Guía práctica** (`admision-licenciatura/matematicas/guia-practica-matematicas.html`), con el mismo formato que la de Literatura, **sin explicación** (así lo pidió la maestra). Enlazada en la lista de la materia; se quitó el aviso de "todavía no están cargados". Pregunta 1: cuál expresión representa una identidad, (x − 6) al cuadrado (captura de la maestra con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, x al cuadrado − 12x + 36). Exponentes con `<sup>`. Falta subirlo.
- Guía práctica de Matemáticas (admisión), Pregunta 2: cuál expresión es una ecuación (captura de la maestra, reactivo 3 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, 9x/5 = 27x/5, que solo se cumple con x = 0). Sin explicación. Fracciones y raíz con las clases `fraccion` y `radical` del sitio. Falta subirlo.
- Pregunta 10 de Historia Universal (personaje de la independencia de Chile, Argentina y Perú): la maestra mandó captura de su sistema donde eligió "B) Simón Bolívar" y le salió incorrecto; coincide con la respuesta de la guía (C, José de San Martín). En su sistema Bolívar es el inciso B y en la guía es el A; Claude ofreció intercambiar A y B para que coincida, falta que ella decida. La página no se cambió.
- Guía práctica de Matemáticas (admisión), Pregunta 3: completar el binomio de Newton (a + b) a la sexta (captura de la maestra, reactivo 3 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, 20b³a³; 6b⁵a). Sin explicación. Falta subirlo.
- Pregunta 3 de Matemáticas (admisión): **triángulo de Pascal "Para repasar"** dentro de la pregunta; aparece después de contestar, igual que el mapa conceptual de Literatura. La maestra lo pidió solo, sin explicación: renglones 0 a 6, con el renglón 6 resaltado en morado. Estilos nuevos en `style.css` (`.pascal`, `.pascal-fila`). En el chat Claude le explicó también la diferencia entre ecuación e identidad y cómo se desarrolla (a − b) a la n (signos alternados); eso no está en el sitio. Falta subirlo.
- Guía práctica de Matemáticas (admisión), Pregunta 4: rango de la función f(x) = x al cuadrado − 4 (captura de la maestra, reactivo 10 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, y ≥ −4). Sin explicación. En el chat Claude le explicó cómo sacar el rango de cualquier función; eso no está en el sitio. La guía lleva 4 preguntas. Falta subirlo.
- Guía práctica de Matemáticas (admisión), Pregunta 5: cuál gráfica representa una función inyectiva (captura de la maestra, reactivo 15 de su sistema; los cuatro incisos son gráficas y la D salía cortada). Sin explicación; correcta la C (recta y = x). Claude dibujó las cuatro gráficas en SVG con cuadrícula cuadrada de −5 a 5 en los dos ejes: A onda tipo seno, B parábola y = x al cuadrado, C recta y = x, D **reconstruida** como una cúbica que sube, baja y vuelve a subir (cruza el eje x en −1, 0 y 1) porque en la captura solo se veía la parte de arriba; falta que la maestra la compare con la de su sistema o mande la captura completa. Estilos nuevos en `style.css` (`.opciones-graficas`: incisos con gráfica, dos por renglón y uno por renglón en celular). La guía lleva 5 preguntas. Falta subirlo.
- Pregunta 5 de Matemáticas (función inyectiva, con gráficas): la maestra pidió eliminarla ("esa no", "elimina"). Claude la quitó de la página; la guía queda con 4 preguntas. Los estilos `.opciones-graficas` se quedaron en `style.css` por si se vuelve a usar un reactivo con gráficas como incisos.
- Guía práctica de Matemáticas (admisión), nueva Pregunta 5: cuál expresión corresponde a una función implícita (captura de la maestra, reactivo 16 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, x al cuadrado − 3xy − y al cuadrado = 1). Sin explicación. La guía lleva 5 preguntas. Falta subirlo.
- Guía práctica de Matemáticas (admisión), Pregunta 6: dominio y rango de f(x) = ln(x − 1) (captura de la maestra, reactivo 1 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, D: (1, ∞); R: (−∞, ∞)). Sin explicación. La maestra solo dijo "agrega la pregunta", sin decir en cuál guía; Claude la puso en esta por ser la de Matemáticas de admisión. La guía lleva 6 preguntas. Falta subirlo.
- Pregunta 6 de Matemáticas (dominio y rango de ln(x − 1)): la maestra pidió eliminarla ("cancela", "sí, elimínala"). Claude la quitó de la página; la guía queda con 5 preguntas.
- Guía práctica de Matemáticas (admisión), nueva Pregunta 6: dominio y rango de f(x) = e a la x, menos 1 (captura de la maestra, reactivo 3 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, D: (−∞, ∞); R: (−1, ∞)). Sin explicación. La guía lleva 6 preguntas. Falta subirlo.

## 2026-11-16

- **Subido a GitHub** por la maestra (guías prácticas de Literatura y Matemáticas de admisión, preguntas nuevas de Historia Universal, `style.css` y bitácora). Claude revisó en internet: la guía de Matemáticas muestra 6 preguntas (la 6 es la de e a la x, menos 1, correcta la B) y la de Literatura muestra 2. Esta entrada de la bitácora queda pendiente de subir en el siguiente push.
- Guía práctica de Física (admisión), Pregunta 13: gotas de agua en ingravidez, aceleración en el movimiento rectilíneo uniforme (captura de la maestra, reactivo 2 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; la maestra mandó solo la captura, sin decir qué hacer, y Claude la agregó; puso como correcta la C, cero, y redactó la explicación como en las demás preguntas de Física). La guía lleva 13 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 14: desplazamiento total al caminar 2 m al este y 2 m al norte (captura de la maestra, reactivo 3 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; mandó solo la captura y Claude la agregó; puso como correcta la C, raíz de 8 metros al noreste, y redactó la explicación con Pitágoras). Raíces con la clase `radical` del sitio. La guía lleva 14 preguntas. Falta subirlo.
- Pregunta 13 de Física (gotas de agua, aceleración cero): **repaso "Para repasar: velocidad y aceleración"** dentro de la pregunta; aparece después de contestar, debajo de la explicación (la maestra lo pidió así, con lo que Claude le explicó en el chat). Dos columnas con los estilos del mapa de Literatura (`.mapa-ramas`: velocidad en morado, aceleración en fucsia; sin estilos nuevos): qué mide, fórmula, unidades y pregunta que responde; debajo, el ejemplo del auto (20 m/s constante, de 0 a 20 m/s en 4 s, frenar de 20 m/s a 0 en 5 s) y el aviso del avión a 900 km/h. No se incluyó lo de la aceleración centrípeta. Falta subirlo.
- Pregunta 14 de Física (desplazamiento 2 m al este y 2 m al norte): **repaso "Para repasar: los puntos cardinales en el plano"** dentro de la pregunta; aparece después de contestar, debajo de la explicación. La maestra preguntó cómo es el plano de este, oeste, norte y sur y escribió "esto lo metas en la guía"; Claude lo entendió como que sí lo quería en la página (falta que ella lo confirme; si quiso decir que no, se quita). Dibujo en SVG con cuadrícula cuadrada (1 cuadrito = 1 m): norte arriba, sur abajo, este a la derecha, oeste a la izquierda, las cuatro direcciones intermedias, el camino de la pregunta en morado y el desplazamiento √8 m en fucsia. Sin estilos nuevos (`.mapa-oracion` y `.grafica-card`). Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 15: dos personas recorren la misma distancia en el mismo tiempo de manera constante (captura de la maestra solo con el enunciado, sin incisos ni respuesta; ella pidió que se agregara con los incisos propuestos por Claude: A misma aceleración distinta de cero, B misma rapidez, C misma masa, D parten del mismo punto; respuesta B; explicación redactada por Claude). La guía lleva 15 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 16: enunciado que describe el concepto de rapidez (captura de la maestra, reactivo 7 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, cantidad escalar, distancia entre tiempo, y redactó la explicación). Único cambio al texto: "llevo" se escribió "llevó", con acento. La guía lleva 16 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 17: carrera de la liebre y la tortuga, ventaja en pasos para empatar (captura de la maestra, reactivo 9 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, 100/3, y redactó la explicación). Fracciones con la clase `fraccion` del sitio. En el chat Claude le explicó qué es una cantidad escalar y una vectorial; eso no está en el sitio. La guía lleva 17 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 18: relacionar aceleración media y velocidad media con su definición (captura de la maestra con las dos listas y los cuatro incisos tal como venían; ella tenía elegida la A, I: a – II: d, sin veredicto visible; Claude la verificó como correcta y redactó la explicación). La instrucción no salía en la captura; Claude puso "Relaciona cada concepto con su definición." (falta que la maestra la confirme o mande la real). La guía lleva 18 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 19: automóviles p, q, z y w, cuál tiene mayor aceleración (captura de la maestra con el enunciado y solo el inciso A, "p mantiene su rapidez de 130 km/h", que ella eligió y su sistema marcó como no correcto; sin los demás incisos). Claude propuso los incisos B (q), C (z) y D (w) con la misma redacción del A, puso como correcta la B (q: 60 km/h por minuto, contra 30 de z, 20 de w y cero de p) y redactó la explicación. Pendiente: que la maestra confirme los incisos o mande los reales (el orden en su sistema puede ser otro). La guía lleva 19 preguntas. Falta subirlo.
- La maestra pidió subir los cambios; Claude le dio los pasos de GitHub Desktop (2 archivos: la guía de Física y la bitácora). Luego ella escribió "las preguntas de la 13 a 19 con sus repasos, y con sus repasos"; Claude no entendió si quería repaso en todas (solo la 13 y la 14 tienen) y se lo preguntó; quedó sin respuesta. Pendiente.
- Guía práctica de Física (admisión), Pregunta 20: automóvil a 72 km/h que frena y se detiene en 4 s, aceleración y distancia (captura de la maestra, reactivo 13 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, a = −5 m/s², d = 40 m, y redactó la explicación). Cambios al texto: "Cual" con acento y "Km" en minúscula. La guía lleva 20 preguntas. Falta subirlo.
- **Subido a GitHub** por la maestra: preguntas 13 a 19 de Física con sus dos repasos. Claude revisó en internet: la guía de Física muestra 19 preguntas y los 2 cuadros "Para repasar". Con eso quedó aclarado su mensaje de "las preguntas de la 13 a 19 con sus repasos" (se refería a lo que subió, no a agregar más repasos). **Falta subir:** la Pregunta 20 (automóvil que frena) y las últimas notas de la bitácora.
- En el chat Claude le explicó por qué en la Pregunta 20 la distancia es velocidad promedio por tiempo (se divide entre 2 porque es el promedio de la velocidad inicial y la final); eso no está en el sitio.
- Guía práctica de Física (admisión), Pregunta 21: aceleración de la motocicleta a los 2 s, con gráfica de velocidad contra tiempo (captura de la maestra, reactivo 14 de su sistema, con el enunciado, la gráfica y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, 2.5 m/s², y redactó la explicación con la pendiente). Gráfica dibujada en SVG con cuadritos cuadrados (cada uno 2 s a lo ancho y 5 m/s a lo alto), copiando la original: recta por los puntos (2, 0), (4, 5), (6, 10), (8, 15), (10, 20), (12, 25), (14, 30) y el eje horizontal dibujado a la altura de −5 m/s. La guía lleva 21 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 22: canica que resbala por una pendiente de 30° sin fricción, rapidez después de 3.6 m (captura de la maestra, reactivo 15 de su sistema, con el enunciado, los datos de "Considera" y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, 6 m/s, y redactó la explicación: a = g · sen 30° = 5 m/s², v al cuadrado = 2 · 5 · 3.6 = 36). La guía lleva 22 preguntas. Falta subirlo.
- En el chat Claude le explicó por qué en el plano inclinado se usa el seno (altura = distancia · sen 30°; caída libre como caso de 90°) y la diferencia entre rapidez final y velocidad final; eso no está en el sitio. Claude ofreció un cuadro "Para repasar" con pistas para leer los reactivos (parte del reposo, se detiene, mantiene su rapidez); la maestra no contestó.
- Guía práctica de Física (admisión), Pregunta 23: gráfica de velocidad contra tiempo de un cuerpo en trayectoria rectilínea, de 40 m/s a −40 m/s en 8 s (captura de la maestra, reactivo 16 de su sistema, con el enunciado, la gráfica y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, en los primeros 4 s recorre 80 m, y redactó la explicación). Gráfica dibujada en SVG con cuadritos cuadrados (cada uno 1 s a lo ancho y 10 m/s a lo alto), copiando la original, con las líneas punteadas hacia el punto (8, −40). La guía lleva 23 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 24: promedio de velocidad de un pájaro que va a 2 m/s y aumenta 1 m/s cada segundo durante 10 s (captura de la maestra con el enunciado y solo el inciso D, 12 m/s, que ella eligió, sin veredicto visible ni los demás incisos). Claude puso como correcta la B, 7 m/s (velocidad final 12, promedio (2 + 12) ÷ 2), dejó el D de la captura como incorrecto y propuso los incisos A 6 m/s, B 7 m/s y C 10 m/s; redactó la explicación. Pendiente: que la maestra confirme los incisos o mande los reales (igual que los de la Pregunta 19). La guía lleva 24 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 25: en dinámica, un objeto cambia su estado de movimiento solamente si… (captura de la maestra, reactivo 4 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, fuerza diferente de cero generada por otro cuerpo, y redactó la explicación con la primera ley de Newton). Primera pregunta de dinámica de la guía. La guía lleva 25 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 26: fuerza paralela al movimiento aplicada a un carrito que viaja a velocidad constante, qué provoca (captura de la maestra, reactivo 5 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, un cambio en su estado de movimiento, y redactó la explicación). La guía lleva 26 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 27: piedra lanzada hacia arriba, cuántas y cuáles fuerzas actúan en su máxima altura (captura de la maestra con el enunciado y solo el inciso D, "Dos, la gravitatoria y la del impulso inicial y van disminuyendo", que ella eligió, sin veredicto visible ni los demás incisos). Claude puso como correcta la B, "Una, la gravitatoria", dejó el D de la captura como incorrecto y propuso los incisos A (Ninguna, porque la piedra está en reposo), B y C (Dos, la gravitatoria y la del impulso inicial y están en equilibrio); redactó la explicación. Pendiente: que la maestra confirme los incisos o mande los reales (igual que los de las Preguntas 19 y 24). La guía lleva 27 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 28: bloque que se desliza hacia abajo por un plano inclinado con velocidad constante, relación entre el bloque y la fuerza (captura de la maestra, reactivo 8 de su sistema, con el enunciado, la imagen y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, la fuerza neta sobre el bloque es cero, y redactó la explicación). Imagen dibujada en SVG copiando la original: triángulo del plano inclinado, bloque sobre la rampa y flecha paralela a la rampa hacia abajo, con los colores del sitio. La guía lleva 28 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 29: triángulo de fuerzas a, b y c, cuál suma de vectores se cumple (captura de la maestra, reactivo 11 de su sistema, con el enunciado, la figura y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, a + c = b, y redactó la explicación). Figura dibujada en SVG copiando la original: a sube por el lado izquierdo, c va de la punta de a hacia la derecha y b va del inicio de a al mismo punto donde termina c. Estilo nuevo en `style.css` (`.vec`: letra con flechita arriba para escribir vectores). La guía lleva 29 preguntas. Falta subirlo (ahora también `style.css`).
- Guía práctica de Física (admisión), Pregunta 30: esquema de las fuerzas sobre una pelota después de ser lanzada verticalmente, sin fricción del aire (captura de la maestra, reactivo 12 de su sistema; los cuatro incisos son dibujos de la pelota con flechas, sin la respuesta marcada). Claude dibujó los cuatro en SVG copiando la captura: A una flecha hacia abajo, B flecha larga hacia arriba y corta hacia abajo, C flecha corta hacia arriba y larga hacia abajo, D una flecha hacia arriba; puso como correcta la A y redactó la explicación. Usa los estilos `.opciones-graficas` que habían quedado en `style.css` (incisos con dibujo, dos por renglón). La guía lleva 30 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 31: cuerdas CA y CB perpendiculares que sostienen un objeto de 5 kg, tensión en CA si en CB es de 30 N (captura de la maestra, reactivo 15 de su sistema, con el enunciado, el dato de g, la figura y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, 40 N, y redactó la explicación: peso 50 N, triángulo 30-40-50). Figura dibujada en SVG copiando la original: techo con rayas, puntos A y B, cuerdas T1 (morado) y T2 (fucsia) en ángulo recto en C, línea horizontal por C y el objeto de 5 kg colgando. La guía lleva 31 preguntas. Falta subirlo.
- Guía práctica de Física (admisión), Pregunta 32: dos personas jalan una caja con 600 N cada una a 45° de la dirección del movimiento, fuerza total (captura de la maestra, reactivo 16 de su sistema, con el enunciado, los datos de "Considera" y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, 848.6 N, y redactó la explicación). Nota: con cos 45° = 0.707 la cuenta da 848.4 N (2 · 600 · 0.707) y el inciso dice 848.6; es el más cercano (el valor exacto es 848.5) y la explicación lo aclara como redondeo. La guía lleva 32 preguntas.
- La maestra subió las preguntas 20 a 32 de Física con GitHub Desktop (junto con `style.css` y la bitácora). Claude verificó en https://antonymathclass.github.io que la guía de Física ya muestra las 32 preguntas y que el estilo de los vectores con flechita (`.vec`) está publicado. Sigue pendiente que la maestra confirme los incisos propuestos por Claude en las preguntas 19, 24 y 27, y la instrucción de la 18.
- Guía práctica de Historia Universal (admisión), Pregunta 11: primer movimiento de lucha obrera caracterizado por la violencia contra las máquinas (captura de la maestra con el enunciado y solo el inciso que ella eligió, "B) Liberalismo", que es incorrecto). Claude puso como correcta la C, Ludismo, redactó la explicación y propuso los incisos A (Cartismo), C (Ludismo) y D (Anarquismo); la maestra aprobó esos incisos y la respuesta.
- Guía práctica de Historia Universal (admisión), Pregunta 12: completar "El ___ buscaba la destrucción de las máquinas; el ___ se orientaba a la lucha política; y el ___ promovía la toma de decisiones de forma colectiva" (captura de la maestra, reactivo 5 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, ludismo – cartismo – cooperativismo, y redactó la explicación). La guía lleva 12 preguntas. Falta subirlo.
- Guía práctica de Matemáticas (admisión), Pregunta 7: lugar geométrico de los puntos que equidistan de F (−5, 2) y de la recta x = 3 (parábola; captura de la maestra, reactivo 1 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, (y − 2)^2 = −16x − 16). Sin explicación en la página, como las demás de esta guía; la explicación se dio solo en el chat. La guía lleva 7 preguntas.
- La maestra subió con GitHub Desktop la Pregunta 7 de Matemáticas y las preguntas 11 y 12 de Historia Universal. Claude verificó en https://antonymathclass.github.io que Matemáticas ya muestra 7 preguntas e Historia Universal 12 (tardó cerca de un minuto en actualizarse).
- **Nueva guía práctica de Geografía (admisión)** en `admision-licenciatura/geografia/guia-practica-geografia.html`, enlazada desde el `index.html` de Geografía (se quitó el aviso de "todavía no están cargados"). Misma estructura y script que las demás guías. Pregunta 1: relacionar las ramas de la Geografía (humana, física, biológica) con su objeto de estudio (captura de la maestra con las dos listas y solo el inciso C, "I: c – II: a – III: b", que ella eligió, sin veredicto visible ni los demás incisos). Claude la verificó como correcta, propuso los incisos A (I: a – II: c – III: b), B (I: b – II: a – III: c) y D (I: c – II: b – III: a) y redactó la explicación. En la captura el inciso b salía cortado ("con la socieda…"); se completó como "sociedad". Pendiente: que la maestra confirme los incisos o mande los reales. La guía lleva 1 pregunta. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 2: si en Londres (GMT 0) son las 17:00 hrs, qué hora es en Tijuana (GMT −8) (captura de la maestra, reactivo 11 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, 09:00 hrs, y redactó la explicación: se restan 8 horas porque Tijuana está al oeste). La guía lleva 2 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 3: "La ________ estudia los factores biológicos del paisaje natural" (captura de la maestra solo con el enunciado, sin incisos ni respuesta). Claude propuso los incisos A climatología, B biogeografía, C geomorfología y D hidrografía, puso como correcta la B y redactó la explicación. Pendiente: que la maestra confirme los incisos o mande los reales (igual que los de la Pregunta 1). La guía lleva 3 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 4: teoría que explica cómo se crea y modifica el relieve por el movimiento de las placas (captura de la maestra, reactivo 15 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, Tectónica global, y redactó la explicación, distinguiéndola de la deriva continental). La guía lleva 4 preguntas. Falta subirlo.
- La maestra aprobó los incisos que Claude propuso en las Preguntas 1 y 3 de Geografía ("sí, déjalo así"); ya no quedan pendientes en esa guía.
- Guía práctica de Geografía (admisión), Pregunta 5: contacto entre las placas Norteamericana y de Cocos en las costas de Guerrero (captura de la maestra, reactivo 16 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, subducción, y redactó la explicación). La guía lleva 5 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 6: sismo y tsunami de Japón (11 de marzo de 2011) en el Cinturón de Fuego del Pacífico, tipo de límite entre placas (captura de la maestra, reactivo 17 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, convergente o subducción, y redactó la explicación). La guía lleva 6 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 7: "Cordillera formada por sismos de alta intensidad debido a la subducción de placas tectónicas" (captura de la maestra solo con el enunciado, sin incisos ni respuesta). Claude propuso los incisos A Cordillera de los Andes, B Cordillera del Himalaya, C Montes Urales y D Sierra Madre Oriental, puso como correcta la A (Andes, ejemplo clásico de subducción: Nazca bajo la Sudamericana) y redactó la explicación. Pendiente: que la maestra confirme (en su sistema la respuesta podría ser otra, por ejemplo la Sierra Madre del Sur). La guía lleva 7 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 8: fenómenos característicos de las placas convergentes de corteza terrestre y marina (captura de la maestra, reactivo 21 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, sismicidad y vulcanismo, y redactó la explicación). La guía lleva 8 preguntas. Sigue pendiente que la maestra confirme la Pregunta 7. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 9: montañas que sirven de límite entre Europa y Asia (captura de la maestra, reactivo 22 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, Urales, y redactó la explicación). La guía lleva 9 preguntas. Sigue pendiente que la maestra confirme la Pregunta 7. Falta subirlo.
- La maestra aprobó los incisos y la respuesta (A, Cordillera de los Andes) que Claude propuso en la Pregunta 7 de Geografía. Ya no quedan pendientes en esa guía.
- Guía práctica de Geografía (admisión), Pregunta 10: sistema montañoso de América paralelo a la costa del Atlántico (captura de la maestra, reactivo 23 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, Montes Apalaches, y redactó la explicación). La guía lleva 10 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 11: estados que forman parte de la llanura costera del Pacífico (captura de la maestra, reactivo 24 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, Sinaloa y Nayarit, y redactó la explicación). La guía lleva 11 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 12: "La ________ se localiza en el centro de México" (captura de la maestra, reactivo 25 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, Meseta de Anáhuac, y redactó la explicación). La guía lleva 12 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 13: actividades que frecuentemente se practican en las zonas montañosas (captura de la maestra, reactivo 26 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, minera y forestal, y redactó la explicación). La guía lleva 13 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 14: recurso natural que se obtiene en la llanura costera de Guerrero Negro (captura de la maestra solo con el enunciado, sin incisos ni respuesta). Claude propuso los incisos A petróleo, B sal, C cobre y D gas natural, puso como correcta la B (sal) y redactó la explicación. Nota: el enunciado dice "Baja California", pero Guerrero Negro está en Baja California Sur (junto al límite con Baja California); se dejó como venía y se le avisó a la maestra. Pendiente: que la maestra confirme los incisos. La guía lleva 14 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 15: distribución correcta de los principales minerales preciosos, industriales y energéticos en el mundo (captura de la maestra, reactivo 33 de su sistema, con los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, China – oro, Australia – bauxita y Estados Unidos – carbón, y redactó la explicación). El enunciado salía cortado a la derecha ("…preciosos, industrial… mundo."); Claude lo completó como "industriales y energéticos en el mundo" (falta que la maestra lo confirme). La guía lleva 15 preguntas. Falta subirlo.
- La maestra aprobó los incisos que Claude propuso en la Pregunta 14 de Geografía (Guerrero Negro, sal).
- La maestra confirmó el enunciado completado de la Pregunta 15 de Geografía ("…preciosos, industriales y energéticos en el mundo"). Ya no quedan pendientes en esa guía.
- Guía práctica de Geografía (admisión), Pregunta 16: países con mayor producción de cobre en la cordillera de los Andes (captura de la maestra, reactivo 34 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, Chile y Perú, y redactó la explicación). La guía lleva 16 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 17: país de África con una de las mayores producciones y reservas de coltán (captura de la maestra, reactivo 35 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, República Democrática del Congo, y redactó la explicación). Único cambio al texto: "Zimbawe" se escribió "Zimbabue", como se escribe en español. La guía lleva 17 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 18: por qué el agua es un asunto de "Seguridad Nacional" (captura de la maestra, reactivo 36 de su sistema, con el enunciado y los cuatro incisos tal como venían; ella tenía elegida la D, sin veredicto visible; Claude la verificó como correcta, "genera conflictos por su posesión", y redactó la explicación). La guía lleva 18 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 19: actividad económica que consume el mayor porcentaje de agua en el mundo (captura de la maestra, reactivo 37 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la C, agricultura, y redactó la explicación: cerca del 70 % agricultura, 20 % industria, 10 % uso doméstico). La guía lleva 19 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 20: fase del ciclo hidrológico que influye directamente en la erosión fluvial (captura de la maestra, reactivo 39 de su sistema, con el enunciado y los cuatro incisos tal como venían; ella tenía elegida la D, precipitación, sin veredicto visible). Claude puso como correcta la B, escurrimiento (la erosión fluvial la hacen los ríos, que son agua que escurre), y redactó la explicación aclarando por qué no es la precipitación. Pendiente: que la maestra confirme. La guía lleva 20 preguntas. Falta subirlo.
- Guía práctica de Geografía (admisión), Pregunta 21: principal sistema fluvial que comunica al Atlántico con el interior de América del Norte (captura de la maestra, reactivo 42 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la B, Los Grandes Lagos – San Lorenzo, y redactó la explicación). La guía lleva 21 preguntas. Sigue pendiente que la maestra confirme la respuesta de la Pregunta 20. Falta subirlo.
- La maestra volvió a mandar el enunciado de la Pregunta 21 de Geografía (sin incisos); Claude no la duplicó.
- Guía práctica de Geografía (admisión), Pregunta 22: sistema fluvial que comunica a Europa occidental con Europa oriental (captura de la maestra, reactivo 43 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, Rhin – Danubio, y redactó la explicación). La guía lleva 22 preguntas. Sigue pendiente que la maestra confirme la respuesta de la Pregunta 20. Falta subirlo.
- La maestra confirmó la B (escurrimiento) como respuesta de la Pregunta 20 de Geografía. Ya no quedan pendientes en esa guía.
- Guía práctica de Geografía (admisión), Pregunta 23: uno de los ríos más importantes para la cultura china (captura de la maestra, reactivo 44 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la D, Amarillo, y redactó la explicación). La guía lleva 23 preguntas. Se agregó mientras la maestra subía las 22 anteriores: falta subir esta.
- Guía práctica de Geografía (admisión), Pregunta 24: ríos de Mesopotamia que desembocan en el Golfo Pérsico (captura de la maestra, reactivo 45 de su sistema, con el enunciado y los cuatro incisos tal como venían, sin la respuesta marcada; Claude puso como correcta la A, Tigris y Éufrates, y redactó la explicación). Único cambio al texto: "Tígris" se escribió "Tigris", sin acento. La guía lleva 24 preguntas. Falta subirlo.
