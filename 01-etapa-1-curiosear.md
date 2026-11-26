# Etapa 1 · Curiosear

**Objetivo:** entender los peligros más comunes de internet protegiendo tus propias cuentas. Lo que aprendas aquí te sirve aunque no sigas con la ciberseguridad.

> Los menús de las apps y páginas cambian seguido. Si algún paso no calza exactamente con lo que ves, busca en Google, por ejemplo, "activar verificación en dos pasos Instagram", y sigue la guía más reciente.

---

## 1 · Tu propia seguridad (práctica real, en tus cuentas)

Haz estas misiones una por una.

### Misión A · ¿Se filtraron tus datos?

Cuando a una empresa le roban su base de datos, los correos y contraseñas de sus usuarios pueden terminar circulando en internet. A eso se le llama filtración.

1. Entra a [haveibeenpwned.com](https://haveibeenpwned.com). Es un sitio confiable y conocido que junta las filtraciones públicas. Está en inglés, pero es muy simple: es una buena primera práctica.
2. Escribe tu correo en el recuadro y aprieta **Check**.
3. Vas a ver uno de dos resultados:
   - **"Good news — no pwnage found!"**: tu correo no aparece en filtraciones conocidas.
   - **"Oh no — pwned!"**: tu correo aparece en una o más filtraciones. Es muy común.
4. Si sale rojo, baja en la página. Vas a ver la lista de filtraciones con el nombre de cada sitio y qué datos se filtraron (por ejemplo, *Email addresses, Passwords*).
5. **Qué hacer:** si en alguna dice Passwords, cambia la contraseña de ese sitio y la de cualquier otro sitio donde uses la misma. Las misiones B y C te ayudan con eso.

### Misión B · Entender los gestores de contraseñas

**El problema:** casi todos usamos la misma contraseña (o parecidas) en todos lados. Si se filtra una, se pueden meter a todas tus cuentas. Y nadie puede recordar 30 contraseñas largas y distintas.

**La solución:** un gestor de contraseñas es como una caja fuerte digital. Guarda todas tus contraseñas cifradas y tú solo tienes que recordar una: la contraseña maestra, que abre la caja.

#### Cómo funcionan

- **Generan contraseñas** largas y al azar por ti, como `q7#Lm!2vRz9@pXw4`. No tienes que inventarlas ni recordarlas.
- **Las rellenan solas** cuando entras a un sitio, desde el computador y desde el celular.
- **Te avisan** si una contraseña está repetida, es débil o apareció en una filtración.
- Las guardan cifradas: aunque alguien robara el archivo, sin la contraseña maestra no puede leer nada.

#### Tipos que existen

| Tipo | Ejemplos | Ventaja | A tener en cuenta |
|---|---|---|---|
| **Los que vienen en el navegador o el teléfono** | Gestor de contraseñas de Google (Chrome/Android), el de Edge, Llavero de iCloud (Apple) | Ya los tienes, no hay que instalar nada | Funcionan mejor dentro del mismo ecosistema (todo Google, todo Apple, etc.) |
| **Apps dedicadas** | Bitwarden, 1Password, Proton Pass, KeePassXC | Funcionan en cualquier navegador y teléfono, y tienen más funciones | Hay que instalarlas. Algunas son gratis y otras son de pago |

No hay uno "correcto". Lo importante es la idea: contraseñas distintas y largas para cada sitio, guardadas en un lugar seguro.

#### Para investigar

1. Revisa si tu navegador ya está guardando contraseñas. En Chrome: *Configuración* → *Autocompletar y contraseñas* → *Gestor de contraseñas*. En Edge: *Configuración* → *Perfiles* → *Contraseñas*. ¿Qué tienes guardado? ¿Te avisa de contraseñas repetidas o filtradas?
2. Busca en YouTube "qué es un gestor de contraseñas" y compara 2 o 3 opciones. ¿Cuál te parece más cómoda?
3. Si decides usar uno, cambia primero las contraseñas de tus cuentas más importantes (correo, Instagram, banco) por contraseñas nuevas generadas por el gestor.

**Sea cual sea el que elijas:** la contraseña maestra (o la de tu cuenta de Google o Apple, si usas el del navegador o el teléfono) es la llave de todo. Que sea larga, por ejemplo una frase de 4 o 5 palabras sin relación entre sí, y no la uses en ningún otro lado. En muchos gestores, si la olvidas, nadie puede recuperarla.

### Misión C · Verificación en dos pasos (2FA)

Con esto, para entrar a tu cuenta no basta la contraseña: también se necesita un código que llega a tu celular. Si alguien roba tu contraseña, igual no puede entrar, porque no tiene tu teléfono.

Actívala en estas tres cuentas (los nombres de los menús pueden variar un poco):

| Cuenta | Dónde se activa |
|---|---|
| **Gmail / Google** | Entra a [myaccount.google.com](https://myaccount.google.com) → **Seguridad** → **Verificación en 2 pasos** → sigue los pasos |
| **Instagram** | Tu perfil → menú ** (arriba a la derecha) → Centro de cuentas → Contraseña y seguridad → Autenticación en dos pasos** |
| **WhatsApp** | **Configuración** (o *Ajustes*) → **Cuenta** → **Verificación en dos pasos** → crea un PIN de 6 números que no olvides |

Algunas apps te dan códigos de respaldo al activarla. Guárdalos en un lugar seguro (en tu gestor de contraseñas o en un papel en tu casa): sirven para entrar si pierdes el celular.

Pregunta para pensar: ¿por qué esto hace tan difícil que te roben la cuenta?

### Misión D · Revisa los permisos de tus apps

Muchas apps piden acceso a tu ubicación, micrófono o cámara aunque no lo necesiten.

- **Android:** *Ajustes* → *Seguridad y privacidad* (o *Privacidad*) → **Administrador de permisos**. *(El nombre cambia un poco según la marca del teléfono).*
- **iPhone:** *Ajustes* → **Privacidad y seguridad** → entra a *Localización*, *Micrófono* y *Cámara*.

Revisa la lista. ¿Una app de linterna con acceso a tu ubicación? ¿Un juego con acceso al micrófono? Quítale el permiso.

---

## 2 · Aprender a detectar engaños (phishing)

El phishing son mensajes falsos (correos, SMS, WhatsApp) que se hacen pasar por alguien confiable, como un banco, Correos de Chile o Netflix, para que hagas clic en un link y entregues tus datos. Es el ataque más común del mundo.

### Las señales de alerta

| Señal | Ejemplo |
|---|---|
| **Urgencia o miedo** | "Tu cuenta será bloqueada en 24 horas" |
| **El remitente no calza** | Dice "Banco Estado", pero el correo es `soporte@bancoestado-seguro.xyz` |
| **El link lleva a otro lado** | El texto dice una cosa, pero el enlace real va a otra página |
| **Te piden datos** | Contraseñas, claves, códigos que te llegan por SMS. Ninguna empresa seria te los pide |
| **Premios o regalos** | "Ganaste un iPhone, solo paga el envío" |

### Cómo revisar un link sin hacer clic

- **En el computador:** pon el mouse encima del link sin hacer clic. Abajo a la izquierda del navegador aparece la dirección real.
- **En el celular:** mantén el dedo apretado sobre el link (sin soltarlo rápido) y aparece la dirección.
- **Fíjate en la parte final del dominio**, justo antes de la primera `/`. En `bancoestado.cl.verificar-cuenta.com`, el sitio real es verificar-cuenta.com, no BancoEstado.

### Misiones

1. **Haz el quiz de phishing de Google** → [phishingquiz.withgoogle.com](https://phishingquiz.withgoogle.com). Te muestra 8 correos y tienes que decidir cuáles son falsos. Al final te explica cada uno.
   - Te va a pedir un nombre y un correo: es solo para que los ejemplos se vean más reales. Puedes inventarlos.
   - La dirección del quiz se ve rara, pero es de Google. Es un buen ejemplo de por qué hay que revisar los dominios con atención.
2. **Revisa tu carpeta de spam.** Busca 3 correos sospechosos (sin hacer clic en nada adentro) y, para cada uno, identifica qué señales de la tabla tiene.
3. **Busca en Google** "estafas por SMS Chile" o "estafas WhatsApp Chile" y lee 2 o 3 noticias. ¿Cómo engañan a la gente?

---

## 3 · Un curso cortito con certificado

**Cisco** es una de las empresas de redes más grandes del mundo. Su plataforma educativa, Networking Academy (NetAcad), tiene cursos gratuitos.

**"Introduction to Cybersecurity"**: [netacad.com/courses/introduction-to-cybersecurity](https://www.netacad.com/courses/introduction-to-cybersecurity)

1. Entra al link y aprieta el botón para empezar (*Get Started* o similar).
2. Crea una cuenta gratis con tu correo.
3. **Elige el idioma.** El curso está disponible en español y en inglés. Como es el primer curso, puedes hacerlo en español para entender bien los conceptos. Si te sientes capaz, hazlo en inglés para ir aprendiendo el vocabulario. Para cambiar el idioma, busca el selector (un ícono de globo o un menú que dice *English*).
4. El curso tiene módulos con lecturas cortas, videos y preguntas de práctica. Avanza de a uno.
5. Al final hay una evaluación. Si la apruebas, te dan un certificado y una insignia digital que puedes poner en tu CV o en LinkedIn.

No pide conocimientos previos.

---

## Para decidir si sigues de la Etapa 1

1. ¿Disfrutaste las misiones, o las sentiste como tarea?
2. ¿Te dio curiosidad saber cómo funcionan los ataques por dentro?
3. ¿Le contaste a alguien algo que aprendiste?

- Si te gustó: sigue con la [Etapa 2](02-etapa-2-como-funciona.md)
- Si te gustó más o menos: prueba el comienzo de la Etapa 2. La parte práctica es distinta a esta.
- Si no te gustó: puedes quedarte aquí. Lo aprendido te sirve para protegerte.
