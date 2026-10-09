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
- **Mat 1, Tema 10 (Ecuaciones):** ejemplo centrado (clase `.centrado` en `.lista-ejemplo-vertical`, regla en
  style.css) y sin numeración; así el primer renglón de los ejemplos 2 y 3 cabe completo en el celular.
  Signo = alineado en la misma columna en todos los pasos (idea de balanza): cada renglón es
  `.fila` con `.lado-izq` / `.igual` / `.lado-der` dentro de `.ecuacion-alineada` (grid de 3 columnas).


<!-- Nueva entrada: agrega fecha (AAAA-MM-DD) y una lista breve de qué se hizo, qué se decidió y qué falta. -->
