# Etapa 3 · Primeros retos (jugar a hackear, legalmente)

**Objetivo:** resolver retos prácticos de seguridad.

---

## ¿Qué es un CTF?

**CTF = Capture The Flag ("captura la bandera").** Son desafíos en los que tienes que encontrar un texto secreto (la bandera o *flag*) escondido en algún lado: en un archivo, una página web, un mensaje cifrado, una imagen… Una bandera se ve más o menos así: `picoCTF{h0la_mund0}`. Cuando la encuentras, la copias, la pegas en la página del reto y ganas puntos.

Cada reto es como un mini misterio. Hay de varios tipos. Apréndete los nombres en inglés, porque así aparecen en todas las plataformas:

| Categoría | De qué se trata | Si te gusta, quizás te va… |
|---|---|---|
| **General Skills** (habilidades generales) | Uso básico de la terminal y herramientas | (para todos, empieza aquí) |
| **Cryptography** (criptografía) | Descifrar mensajes secretos | acertijos y lógica |
| **Web Exploitation** (web) | Encontrar fallas en páginas web | ataque ético () |
| **Forensics** (forense) | Encontrar pistas escondidas en archivos e imágenes | forense y defensa () |
| **Reverse Engineering** (ingeniería inversa) | Desarmar programas para ver cómo funcionan por dentro | ataque o análisis de malware |

---

## Plataforma principal: CyLab Security Academy (ex picoCTF)

[cylabacademy.org](https://cylabacademy.org)

Es una plataforma gratuita de la Universidad Carnegie Mellon (Estados Unidos), pensada para estudiantes que recién empiezan. Antes se llamaba picoCTF. Cambió de nombre en 2026, pero es el mismo equipo y los mismos retos. Por eso, en internet vas a encontrar mucha información con el nombre antiguo, y las banderas todavía pueden empezar con `picoCTF{`.

Está en inglés. Las descripciones de los retos suelen ser cortas, así que son una buena práctica: léelas en inglés y busca solo las palabras que te traben.

### Paso 1 · Crea tu cuenta

1. En [cylabacademy.org](https://cylabacademy.org), aprieta **Sign Up** (registrarse).
2. Completa el formulario. Elige un nombre de usuario que no sea tu nombre real completo.
3. Te va a llegar un correo de confirmación. Ábrelo y haz clic en el link para activar la cuenta. *(Si no llega, revisa la carpeta de spam).*
4. Entra a la plataforma en [learn.cylabacademy.org](https://learn.cylabacademy.org).

### Paso 2 · Lee el "CTF Primer"

Es una guía introductoria que explica lo básico: la terminal, la criptografía y otros conceptos. Léela antes de los retos y vuelve a ella cuando te trabes.

### Paso 3 · Conoce la webshell (tu terminal en el navegador)

Muchos retos se resuelven con comandos de Linux. Para eso, la plataforma te da una webshell: una terminal Linux que funciona dentro del navegador, así que no tienes que instalar nada en Windows.

- La encuentras en el panel **Webshell** de la plataforma, o directamente en [webshell.cylabacademy.org](https://webshell.cylabacademy.org).
- Para entrar, usa el mismo usuario y contraseña de tu cuenta.
- Igual que en Bandit, cuando escribes la contraseña no aparece nada en la pantalla. Escríbela igual y aprieta Enter.
- **Para pegar en la webshell usa `Ctrl + Shift + V`** (con `Ctrl + V` solo no funciona).

### Paso 4 · Cómo se ve un reto

Entra a la **Challenge Library** (biblioteca de retos). Cada reto tiene:

- **Título y puntos:** los de pocos puntos son los más fáciles.
- **Descripción:** te cuenta el misterio y qué tienes que hacer.
- A veces, un archivo para descargar o un link a una página.
- **Hints (pistas):** un botón que te da una ayuda si te trabas.
- **Un recuadro para la bandera:** ahí pegas la bandera que encontraste y aprietas **Submit** (enviar).

### Paso 5 · Bajar un archivo del reto a la webshell

Muchos retos te dan un archivo para analizar con comandos. Para tenerlo en la webshell:

1. En la página del reto, haz clic derecho sobre el link del archivo → **Copiar dirección del vínculo** (o *Copiar dirección del enlace*).
2. En la webshell escribe `wget` y un espacio, pega el link con `Ctrl + Shift + V` y aprieta Enter. Va a quedar algo así:

   ```
   wget https://direccion-del-archivo
   ```

3. Escribe `ls` y Enter: vas a ver el archivo descargado.
4. Para ver qué tiene adentro, escribe `cat` seguido del nombre del archivo, por ejemplo `cat flag`.

### Paso 6 · Por dónde empezar

1. Busca la guía "Beginner's Guide to the Challenge Library": reúne los retos más amigables para principiantes. Si no la encuentras, filtra la biblioteca por General Skills y ordénala por menos puntos.
2. Resuelve unos 10 retos de General Skills.
3. Después prueba Cryptography y Forensics (suelen ser las más amigables).
4. Recién entonces mira Web Exploitation.

La plataforma también organiza mini competencias durante el año. Cuando tengas más práctica, puedes participar en alguna.

---

## Una herramienta útil: CyberChef

[gchq.github.io/CyberChef](https://gchq.github.io/CyberChef/)

Es una página para transformar y decodificar textos sin escribir comandos. Pegas un texto raro a la izquierda, arrastras una "receta" (por ejemplo, *From Base64*) al centro y ves el resultado a la derecha. Te va a servir mucho en los retos de Cryptography. Funciona completa en el navegador.

## Complemento: TryHackMe "Cyber Security 101"

Si te gustó TryHackMe en la Etapa 2, sigue con el camino Cyber Security 101 (búscalo en el menú de *Learning Paths* de TryHackMe). Ahí vas a probar un poco de todo (defensa, ataque, herramientas) con salas guiadas. De nuevo: haz las gratis y salta las de pago.

## Si te trabas

- Si llevas un buen rato sin avanzar, primero usa el botón de **Hints**.
- Si con las pistas no basta, busca un *writeup*: una explicación escrita por otra persona de cómo resolvió el reto. Busca en Google el nombre del reto + "picoCTF writeup" (por el nombre antiguo, ahí está casi todo). Léelo hasta el punto donde te trabaste, ciérralo e intenta seguir sola.

---

## Para decidir si sigues de la Etapa 3

1. ¿Te pasó que se te fue el tiempo resolviendo un reto?
2. ¿Qué categoría disfrutaste más?
3. ¿Te imaginas haciendo cosas así (o parecidas) como trabajo?

- Si te gustó: sigue con la [Etapa 4](04-etapa-4-elegir-camino.md)
- Si te gustó más o menos: sigue practicando un tiempo antes de decidir.
- Si no te gustó: revisa igual la Etapa 4. Hay áreas menos técnicas.
