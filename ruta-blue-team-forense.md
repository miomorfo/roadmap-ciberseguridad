# 🔵🔍 Ruta Blue Team y forense

Esta página es para ti si lo que más te llamó la atención fue **defender, investigar incidentes y entender cómo funcionan los ataques**. No reemplaza las etapas: te dice **en qué fijarte dentro de cada una** y **qué hacer después** para practicar como lo hace un analista de verdad.

---

## ¿Qué hacen realmente?

**Blue Team** es el equipo que defiende. **Forense digital** es la parte que investiga *qué pasó* después de un ataque. Están tan conectadas que en la industria se habla de **DFIR** (*Digital Forensics and Incident Response*, "forense digital y respuesta a incidentes").

Un caso típico se ve así:

1. 🚨 **Llega una alerta:** "Un computador de contabilidad se está conectando a un sitio raro a las 3 de la mañana".
2. 🔎 **Investigar:** ¿es un ataque de verdad o una falsa alarma? Se revisan los **registros** (*logs*): quién entró, a qué hora, qué programas se ejecutaron, con qué sitios se comunicó.
3. 🧩 **Reconstruir la historia:** ¿cómo entró el atacante? (¿un correo de phishing?) ¿qué hizo? ¿qué se llevó? Se arma una **línea de tiempo**.
4. 🛑 **Contener:** desconectar el equipo, bloquear la cuenta, cerrar la puerta por donde entró.
5. 📝 **Informar:** escribir qué pasó, qué evidencia se encontró y cómo evitar que se repita.

Es trabajo de **detective**: mirar pistas, hacerse preguntas y no quedarse con la primera respuesta.

### Lo que más se usa en este trabajo

- **Entender redes:** cómo se comunican los computadores (por eso la Etapa 2 es clave).
- **Entender Windows y Linux por dentro:** dónde quedan las huellas de lo que pasó.
- **Leer registros (logs):** mucho texto con fechas, horas y eventos donde hay que encontrar lo raro.
- **Tomar notas y escribir claro:** un hallazgo no sirve si no lo puedes explicar.
- **Inglés:** las herramientas, los informes y las alertas están en inglés.

---

## Cómo recorrer las etapas con este enfoque

### Etapa 1 · Curiosear
- La parte de **phishing** es trabajo real de Blue Team: la mayoría de los incidentes empiezan con un correo falso. Tómatela en serio.
- En el curso de Cisco, pon especial atención a los módulos sobre **ataques, amenazas y cómo se protegen las organizaciones**.

### Etapa 2 · Cómo funciona todo por dentro
- Esta es **la etapa más importante para ti**. No la apures.
- Dedícale atención extra a las salas de **redes** (cómo viaja la información) y de **Windows** (la mayoría de las empresas usa Windows, así que ahí ocurren la mayoría de los incidentes).
- **Bandit** te sirve mucho: buscar información escondida entre muchos archivos con comandos (`grep`, `find`) es casi lo mismo que buscar algo raro entre miles de registros.

### Etapa 3 · Primeros retos
- En CyLab Security Academy, **después de General Skills, ve directo a Forensics**. Esa es tu categoría.
- **Cryptography** te sirve de apoyo. **Web** y **Reverse Engineering** puedes dejarlas para más adelante o saltarlas.
- Usa **CyberChef** seguido: en forense se usa para decodificar textos sospechosos.

---

## 🧪 Siguiente nivel: practicar como analista

Cuando hayas terminado (o casi) las etapas 2 y 3, sigue con esto, en este orden.

### 1 · Salas defensivas gratis en TryHackMe

TryHackMe tiene muchas salas de defensa que se hacen **en el navegador**, con las herramientas ya instaladas en el computador virtual.

- **Empieza por phishing**, porque ya lo conoces de la Etapa 1:
  - **Phishing Analysis Fundamentals:** aprendes las partes de un correo y dónde se esconden las pistas.
  - **Phishing Emails in Action:** analizas correos de phishing reales.
- Después, usa el buscador de salas con palabras como **SOC**, **forensics**, **incident response**, **Wireshark** o **logs**, y **filtra por gratis (*Free*) y fácil (*Easy*)**.
- El camino completo **SOC Level 1** es justo lo que te interesa, pero **la mayor parte es de pago**. Haz primero todas las salas gratis que encuentres de ese camino. Solo si te encanta y quieres seguir, conversa sobre si vale la pena pagar.

### 2 · CyberDefenders: investigar incidentes de verdad

👉 [cyberdefenders.org](https://cyberdefenders.org)

Es una plataforma **hecha solo para Blue Team**. Funciona distinto a los CTF de la Etapa 3: en vez de buscar una bandera, **te entregan la evidencia de un incidente** (capturas de tráfico de red, registros, imágenes de discos) y tienes que **responder preguntas** sobre qué pasó: ¿por dónde entró el atacante? ¿a qué hora? ¿qué archivo usó?

- Crea una cuenta gratis y entra a la sección de **labs** (laboratorios).
- Usa el filtro de **Free Labs** (gratis) y dificultad **Easy**. Los que dicen *Premium* son de pago.
- Elige laboratorios que **funcionen en el navegador**. Algunos piden descargar archivos y usar programas instalados en tu computador: esos sáltalos por ahora.
- ⚠️ Es **más difícil** que TryHackMe y menos guiado. Si te pierdes, vuelve a las salas de TryHackMe y regresa después. Es normal.

### 3 · Más adelante (cuando lo anterior te quede fácil)

- **Blue Team Labs Online** → [blueteamlabs.online](https://blueteamlabs.online). Tiene retos defensivos gratis, pero la misma plataforma dice que **no está pensada para principiantes totales** y varios retos requieren programas instalados. Déjalo para después.
- **Hack The Box** también tiene una sección defensiva, con retos forenses llamados *Sherlocks*.

---

## 🛠️ Herramientas que vas a usar

Al principio las vas a usar **dentro de las salas y laboratorios**, en el navegador, sin instalar nada. Más adelante puedes tenerlas en tu propio computador (ver la sección siguiente).

### Herramientas principales

| Herramienta | Para qué sirve | ¿Dónde funciona? |
|---|---|---|
| **Wireshark** | Ver, uno por uno, los "paquetes" de información que viajaron por una red. Sirve para descubrir con quién se comunicó un computador infectado. | Windows, Linux, Mac |
| **Sysinternals** | Conjunto de herramientas gratuitas de Microsoft para ver qué está pasando dentro de Windows: qué programas corren, qué se ejecuta al encender, qué conexiones hay abiertas. Las más conocidas son *Process Explorer* y *Autoruns*. | Windows |
| **Autopsy** | Revisar el disco de un computador para encontrar archivos borrados, historial de navegación y otras huellas. | Windows, Linux |
| **Volatility** | Analizar la memoria RAM de un computador, donde quedan rastros de programas maliciosos que estaban corriendo. | Linux, Windows (por terminal) |
| **Splunk / ELK** | Son **SIEM**: juntan los registros de muchos sistemas en un solo lugar y permiten buscar entre millones de eventos. Los vas a practicar en TryHackMe. | Servidores (se usan desde el navegador) |
| **CyberChef** | Decodificar y transformar textos sospechosos (ya lo conoces de la Etapa 3). | Navegador |

### Comandos de Linux que más se usan en forense

Muchos ya los conoces de Bandit. En Blue Team se usan para revisar registros y archivos sospechosos:

| Comando | Para qué sirve |
|---|---|
| `grep` | Buscar una palabra dentro de archivos (por ejemplo, una IP sospechosa en miles de líneas de registro) |
| `less`, `head`, `tail` | Leer archivos largos de a poco, ver el comienzo o el final (`tail -f` muestra en vivo lo que se va agregando a un registro) |
| `sort`, `uniq -c` | Ordenar y contar repeticiones (por ejemplo, qué IP intentó entrar más veces) |
| `wc -l` | Contar líneas |
| `find` | Buscar archivos por nombre, fecha o tamaño |
| `file` | Saber qué tipo de archivo es realmente (aunque le hayan cambiado la extensión) |
| `strings` | Ver el texto legible escondido dentro de un archivo o programa |
| `sha256sum` | Calcular el **hash** (la "huella digital") de un archivo, para compararlo con bases de datos de malware conocido |

---

## 🧰 Tu propio laboratorio (opcional, para más adelante)

Cuando ya te sientas cómoda con las salas y quieras practicar en tu propio computador, puedes armar un **laboratorio**: un espacio en tu computador para usar herramientas sin riesgo.

> ⚠️ **Antes de instalar nada:** esto es opcional. Todo lo de las etapas funciona en el navegador. Arma tu laboratorio solo cuando sientas que lo necesitas, y pide ayuda si algo no te queda claro.

### Opción 1 · Linux dentro de Windows con WSL (la más fácil)

**WSL** (*Windows Subsystem for Linux*) es una función oficial de Windows que permite tener **Linux funcionando dentro de Windows**, sin máquinas virtuales. Es la forma más simple de practicar comandos de Linux en tu propio computador.

- Se instala desde la **terminal de Windows como administrador** con un solo comando, o desde la **Microsoft Store**.
- Puedes elegir qué Linux instalar: **Ubuntu** (el más común para empezar) o **Kali Linux**.
- 📖 Guía oficial de Microsoft (en inglés): [learn.microsoft.com/windows/wsl/install](https://learn.microsoft.com/windows/wsl/install)
- 📖 Guía oficial para Kali en WSL: [kali.org/docs/wsl](https://www.kali.org/docs/wsl/)

### ¿Y Kali Linux?

**Kali Linux** es el Linux más famoso en ciberseguridad. Viene con cientos de herramientas ya instaladas. Hay que saber dos cosas:

- Está pensado principalmente para **ataque ético** (pentesting). Tiene algunas herramientas forenses, pero no es su foco.
- **Es útil para aprender igual**: practicar Linux, conocer las herramientas que usan los atacantes (para defenderte, hay que entender cómo atacan) y seguir guías, porque muchas usan Kali.
- ⚠️ Algunos antivirus detectan herramientas de Kali como "peligrosas", porque son herramientas de ataque. Es normal, pero tenlo en cuenta.
- 📖 Documentación oficial (en inglés): [kali.org/docs](https://www.kali.org/docs/)

Para tu área, la opción más especializada es la siguiente.

### Opción 2 · Máquinas virtuales (para Linux especializados)

Una **máquina virtual** es un computador completo "de mentira" que funciona dentro de tu computador, en una ventana. Si algo sale mal, la borras y listo: tu Windows no se ve afectado.

**Programas para crear máquinas virtuales (elige uno):**
- **VirtualBox** → [virtualbox.org](https://www.virtualbox.org): gratis y de código abierto.
- **VMware Workstation Pro**: gratis para uso personal. Se descarga desde el portal de Broadcom (la empresa dueña de VMware), que pide crear una cuenta y es un poco enredado.

**Linux especializados para Blue Team y forense:**

| Sistema | Qué es |
|---|---|
| **SIFT Workstation** | Creado por **SANS**, una de las instituciones de formación en ciberseguridad más reconocidas del mundo. Es gratis y viene con cientos de herramientas forenses ya instaladas. Es **el más recomendado para forense**. Se descarga como máquina virtual desde [sans.org/tools/sift-workstation](https://www.sans.org/tools/sift-workstation) (pide crear una cuenta gratis en SANS). |
| **REMnux** | Linux especializado en **analizar malware**. Para más adelante, cuando ya tengas base → [remnux.org](https://remnux.org) |
| **Security Onion** | Plataforma completa de monitoreo de red, como un "SOC en una caja". Es avanzada y necesita un computador con bastantes recursos. Para mucho más adelante. |

⚠️ **Antes de instalar una máquina virtual:**
- Necesitas **espacio en disco**: la de SIFT, por ejemplo, pesa casi 9 GB solo para descargar.
- Necesitas **memoria RAM** suficiente, porque vas a tener dos sistemas funcionando a la vez.
- Puede que haya que activar la **virtualización** en la configuración del computador (la BIOS). Si un programa te dice que la virtualización está desactivada, busca cómo activarla para el modelo de tu computador.

### Herramientas que puedes instalar directo en Windows

Si no quieres máquinas virtuales todavía, estas funcionan directo en Windows y son seguras:

- **Wireshark** → [wireshark.org](https://www.wireshark.org). Para practicar, la página de Wireshark tiene **capturas de ejemplo** que puedes abrir y analizar sin riesgo.
- **Sysinternals** → busca "Sysinternals Suite" en el sitio de Microsoft. Prueba *Process Explorer* para ver qué programas están corriendo en tu propio computador.

### 🚨 Reglas de seguridad para tu laboratorio

1. **Nunca descargues malware real en tu computador**, aunque sea "para analizarlo". Eso se hace en entornos preparados por profesionales. Las salas de TryHackMe y CyberDefenders ya traen la evidencia lista, de forma segura.
2. **Descarga herramientas solo de sus páginas oficiales.** Una herramienta de seguridad descargada de un sitio cualquiera puede venir con virus.
3. **Una máquina virtual no es una burbuja perfecta.** Es mucho más segura que tu Windows, pero no es infalible.
4. **Solo analiza tus propios equipos** o lo que te entreguen las plataformas de práctica (la regla de ética de la Etapa 0 sigue valiendo).

---

## 📚 Guías y recursos para seguir aprendiendo

Todos en inglés y gratuitos:

- **SANS Cheat Sheets y Posters** → busca "SANS DFIR posters". Son hojas de resumen que usan los profesionales, con los comandos y los lugares donde buscar evidencia. Hay una específica para SIFT.
- **Documentación de Kali** → [kali.org/docs](https://www.kali.org/docs/). Muy completa, explica la instalación paso a paso.
- **Canales de YouTube:**
  - **13Cubed:** forense digital, explicado con mucho detalle.
  - **John Hammond:** análisis de malware, CTF y casos reales.
  - **NetworkChuck:** muy amigable para principiantes (Linux, redes, Kali).
- **Linux Journey** → [linuxjourney.com](https://linuxjourney.com): guía para aprender Linux desde cero, por temas.

---

## 🇬🇧 Vocabulario Blue Team

| Inglés | Qué significa |
|---|---|
| **Alert** | Aviso automático de que algo sospechoso pasó |
| **Log** | Registro: anotación automática de un evento (un inicio de sesión, un error, una conexión) |
| **Incident** | Incidente: un problema de seguridad confirmado |
| **Triage** | Revisar alertas rápido para decidir cuáles son importantes |
| **False positive** | Falsa alarma: la alerta saltó, pero no era un ataque |
| **IOC** (*Indicator of Compromise*) | Pista que indica un ataque: una dirección IP maliciosa, un nombre de archivo, un dominio raro |
| **PCAP** | Archivo con una grabación del tráfico de una red |
| **Threat** / **Threat actor** | Amenaza / el atacante (persona o grupo) |
| **Malware** | Programa malicioso |
| **Timeline** | Línea de tiempo de lo que pasó |
| **Evidence** / **Artifact** | Evidencia / huella que queda en un sistema |
| **Containment** | Contención: aislar el problema para que no se extienda |
| **MITRE ATT&CK** | Un catálogo público de las técnicas que usan los atacantes. Los analistas lo usan como "diccionario" para describir qué hizo el atacante |
| **DFIR** | *Digital Forensics and Incident Response*: forense digital y respuesta a incidentes |

## 📺 Para mirar

Busca en YouTube, **en inglés**:
- **"day in the life of a SOC analyst"**
- **"what is digital forensics"**
- **"incident response explained"**

Fíjate en qué hacen durante el día y si te imaginas ahí.

---

## 🚦 Semáforo de esta ruta

1. Cuando investigaste un caso (en una sala o un laboratorio), ¿te dieron ganas de seguir hasta entender qué pasó?
2. ¿Disfrutaste más **detectar** (Blue Team, SOC) o **reconstruir lo que pasó** (forense)?
3. ¿Te imaginas revisando alertas y registros como trabajo?

- 🟢 → Sigue con TryHackMe y CyberDefenders, y conversa sobre opciones de estudio formal (está en la [Etapa 4](04-etapa-4-elegir-camino.md)).
- 🟡 → Prueba la otra mitad: si hiciste más de Blue Team, prueba forense, o al revés.
- 🔴 → Mira las otras áreas de la [Etapa 4](04-etapa-4-elegir-camino.md). Quizás lo tuyo esté en otro lado, y está bien.
