# Etapa 2 · Cómo funciona todo por dentro

🎯 **Objetivo:** entender lo básico de **internet, las redes y los computadores**. No se puede proteger (ni atacar) lo que no se entiende.

> 🧘 Esta es la etapa más "de estudio". Si se pone pesada, intercala con un reto de la Etapa 3 para no perder la motivación.

---

## Plataforma principal: TryHackMe

👉 [tryhackme.com](https://tryhackme.com)

TryHackMe es una plataforma para aprender ciberseguridad practicando. Funciona por **salas** (*rooms*): lecciones cortas con explicación y preguntas. Las salas se agrupan en **caminos** (*paths*), que son como cursos completos.

### Paso 1 · Crea tu cuenta

1. Entra a [tryhackme.com](https://tryhackme.com) y aprieta **Sign up** (registrarse). Puedes usar tu cuenta de Google o un correo.
2. Te va a hacer algunas preguntas sobre tu experiencia. Responde que eres principiante.

### Paso 2 · Abre el camino "Pre Security"

👉 Link directo: [tryhackme.com/path/outline/presecurity](https://tryhackme.com/path/outline/presecurity)

Está hecho para personas **sin ningún conocimiento previo**. Vas a ver una lista de salas agrupadas por tema. Hazlas en orden.

### Paso 3 · Cómo funciona una sala

1. Abre una sala. Si aparece el botón **Join Room** (unirse a la sala), apriétalo.
2. La sala está dividida en **tareas** (*Task 1, Task 2…*). Haz clic en cada una para abrirla.
3. Cada tarea tiene una explicación y, al final, una o más **preguntas**. Escribe tu respuesta en el recuadro y aprieta **Submit** (enviar). Si está bien, se pone verde ✅.
4. Si una pregunta dice **"No answer needed"** (no necesita respuesta), solo aprieta el botón para marcarla como completada.
5. Algunas tareas tienen un botón verde **Start Machine** o **Start AttackBox**. Eso enciende un **computador virtual**: un computador que existe en internet y que usas desde el navegador. Aparece al lado de las instrucciones (la pantalla se divide en dos).
   - No se instala nada en tu computador y **no puedes romper nada**: si algo sale mal, lo apagas y lo vuelves a encender.
   - La cuenta gratis tiene un límite diario de uso del computador virtual (más o menos una hora).

### Paso 4 · Gratis y de pago

Muchas salas introductorias son **gratis**. Las de pago tienen un candado o dicen **Premium** o **Subscribers**. Si te topas con una, **sáltala** y sigue con la siguiente. No necesitas pagar nada.

### Paso 5 · El inglés

TryHackMe está en inglés, y aquí empieza en serio la práctica del idioma. Lee las explicaciones en inglés y busca solo las palabras que no entiendas. Te va a costar al principio, pero en pocas salas vas a notar que las palabras se repiten. Revisa los consejos y el vocabulario en [El inglés en ciberseguridad](ingles.md).

⚠️ Si alguna vez usas el traductor del navegador, recuerda que puede romper los comandos y nombres de archivos. Lo que aparece en **recuadros grises** se escribe siempre **tal cual, en inglés**.

### Qué vas a ver (en simple)

| Tema | Pregunta que responde |
|---|---|
| **Cómo funciona internet** | ¿Qué pasa cuando escribo una página y aprieto Enter? |
| **Redes** | ¿Cómo se "hablan" los computadores? ¿Qué es una IP? |
| **Cómo funciona la web** | ¿Qué es un servidor? ¿Qué es HTTP? |
| **Linux** | ¿Cómo uso un computador solo escribiendo comandos? |
| **Windows por dentro** | ¿Dónde guarda las cosas y cómo maneja los usuarios? |

## Orden sugerido

1. Salas de redes e internet de Pre Security.
2. Salas de Linux. Aquí empieza lo entretenido.
3. Salas de web y Windows, y luego el juego **Bandit** (abajo).

💡 En la sección de Linux vas a usar por primera vez la **terminal**: una ventana donde le das órdenes al computador escribiendo, en vez de usar el mouse. Al principio se ve intimidante, pero son pocas palabras que se repiten mucho (`ls` para ver archivos, `cd` para moverte entre carpetas, `cat` para leer un archivo…). Las salas te las enseñan una por una.

## 🎮 Bonus: OverTheWire · Bandit

👉 [overthewire.org/wargames/bandit](https://overthewire.org/wargames/bandit/)

Es un juego por niveles en el que, para pasar al siguiente, tienes que encontrar una contraseña escondida usando comandos de Linux. Es como un *escape room* en la terminal.

- Empieza cuando hayas hecho las salas de Linux.
- La meta no es terminarlo, sino **llegar al nivel 10 o 15**.
- Si te trancas, buscar pistas está permitido (pero inténtalo un rato antes de buscarlas).

### ¿Cómo se juega? (lee esto antes de abrir la página)

A diferencia de TryHackMe, Bandit **no se juega en el navegador**. La página solo tiene las instrucciones de cada nivel. Para jugar, te conectas desde tu computador a un servidor Linux que está en internet, y lo controlas escribiendo comandos.

Esa conexión se hace con **SSH**: un programa que te deja usar otro computador a distancia, de forma segura, solo con texto. Es como abrir una ventana a un computador que está en otra parte del mundo.

La buena noticia: **Windows 10 y 11 ya traen SSH**. No tienes que instalar nada.

#### Paso 1 · Abre la terminal de Windows

Aprieta la tecla **Windows**, escribe **Terminal** (o **PowerShell**) y ábrela. Vas a ver una ventana negra o azul con un texto parecido a `PS C:\Users\TuNombre>`. Ahí se escriben los comandos.

#### Paso 2 · Conéctate al nivel 0

Copia este comando, pégalo en la terminal y aprieta **Enter**:

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Qué significa cada parte:

| Parte | Qué es |
|---|---|
| `ssh` | El programa para conectarse |
| `bandit0` | El usuario con el que entras (el nivel 0) |
| `bandit.labs.overthewire.org` | La dirección del servidor del juego |
| `-p 2220` | El "puerto", o sea, por qué puerta entrar. **No lo olvides**, sin esto no funciona |

#### Paso 3 · Las preguntas que te va a hacer

1. **La primera vez** va a aparecer un mensaje largo que termina en `Are you sure you want to continue connecting (yes/no)?`. Es normal: te pregunta si confías en ese servidor. Escribe **`yes`** y aprieta Enter.
2. Luego va a aparecer un dibujo grande con letras y te va a pedir `password:`. Para el nivel 0 la contraseña es **`bandit0`**.
3. ⚠️ **Cuando escribes la contraseña no aparece nada en la pantalla**: ni letras ni asteriscos. No está pegado, es una medida de seguridad. Escríbela igual y aprieta Enter.

Si todo salió bien, vas a ver algo como `bandit0@bandit:~$`. **¡Estás dentro de un servidor Linux!** 🎉 Desde aquí funcionan los mismos comandos que practicaste en TryHackMe (`ls`, `cat`, `cd`…).

#### Paso 4 · Pasar de nivel

1. En la página de Bandit, lee las instrucciones del **Level 0 → Level 1**. Ahí te dice dónde está escondida la contraseña del siguiente nivel.
2. Cuando la encuentres, **cópiala y guárdala** en un bloc de notas. Las vas a necesitar si quieres volver otro día.
3. Sal del servidor escribiendo **`exit`**.
4. Conéctate de nuevo, pero ahora como `bandit1`, y usa la contraseña que encontraste:

```
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Y así sucesivamente: `bandit2`, `bandit3`… Cada nivel te da la llave del siguiente.

#### 💡 Trucos útiles

- **Pegar en la terminal:** `Ctrl + V` o **clic derecho**.
- **Copiar desde la terminal:** selecciona el texto con el mouse y aprieta `Ctrl + C` (o clic derecho).
- **Repetir un comando anterior:** usa la flecha **↑** del teclado.
- **Si escribes mal la contraseña**, solo te la vuelve a pedir. Inténtalo de nuevo con calma.
- **Si aparece `Connection refused` o se queda pegado**, revisa que pusiste `-p 2220` al final.
- **Si no te deja escribir nada en la terminal**, aprieta `Ctrl + C` para cancelar lo que estaba haciendo.

---

## 🚦 Semáforo de la Etapa 2

1. Cuando algo te funcionó en la terminal, ¿sentiste satisfacción?
2. ¿Hubo algún tema que quisiste investigar más por tu cuenta?
3. ¿Qué te aburrió más? (Anótalo: también dice mucho sobre qué camino podría ser el tuyo)

- 🟢 → [Etapa 3: retos](03-etapa-3-primeros-retos.md)
- 🟡 → Toma una pausa y vuelve. A veces la cabeza necesita descansar para que todo encaje.
- 🔴 → Si lo técnico definitivamente no es lo tuyo, mira la parte de **Gestión y normas** en la [Etapa 4](04-etapa-4-elegir-camino.md). Hay ciberseguridad con mucho menos de terminal.

---

[← Volver al inicio](README.md)
