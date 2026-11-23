# Etapa 2 · Cómo funciona todo por dentro

🎯 **Objetivo:** entender lo básico de **internet, las redes y los computadores**. No se puede proteger (ni atacar) lo que no se entiende.

> 🧘 Esta es la etapa más "de estudio". Si se pone pesada, intercala con un reto de la Etapa 3 para no perder la motivación.

---

## Plataforma principal: TryHackMe

👉 [tryhackme.com](https://tryhackme.com): crea una cuenta gratis.

TryHackMe funciona por **"salas" (rooms)**: lecciones cortas con explicación y preguntas, y muchas incluyen un computador virtual que se abre en el navegador, así que no tienes que instalar nada.

- Empieza por el camino **"Pre Security"**: está hecho para personas sin conocimientos previos.
- Muchas salas introductorias son **gratis**. Si te topas con una de pago, sáltala y sigue con la siguiente.
- La cuenta gratis tiene un límite diario de uso del computador virtual (más o menos una hora).
- Está en inglés. Si se te hace difícil, usa el traductor del navegador sin culpa.

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
