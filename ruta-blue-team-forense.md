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

## 📝 Ejercicio opcional: tu primer informe

En Blue Team, **saber explicar lo que encontraste es tan importante como encontrarlo**. Cuando termines una sala o un laboratorio que te haya gustado, intenta escribir un resumen corto (media página) respondiendo:

1. **¿Qué pasó?** (en 2 o 3 frases, como si se lo contaras a alguien que no sabe de computadores)
2. **¿Cómo lo descubriste?** (qué evidencia miraste)
3. **¿Cómo se pudo haber evitado?**

Si te animas, escríbelo en inglés: así es como se escriben los informes en la industria.

---

## 🛠️ Herramientas que vas a escuchar

No tienes que instalar ninguna. Las vas a usar **dentro de las salas y laboratorios**, en el navegador. Así sabrás de qué te hablan:

| Herramienta | Para qué sirve |
|---|---|
| **Wireshark** | Ver, uno por uno, los "paquetes" de información que viajaron por una red. Sirve para descubrir con quién se comunicó un computador infectado. |
| **Splunk / ELK** | Son **SIEM**: juntan los registros de muchos sistemas en un solo lugar y permiten buscar entre millones de eventos. |
| **Autopsy** | Revisar el disco de un computador para encontrar archivos borrados, historial y otras huellas. |
| **Volatility** | Analizar la memoria RAM de un computador, donde quedan rastros de programas maliciosos que estaban corriendo. |
| **CyberChef** | Decodificar y transformar textos sospechosos (ya lo conoces de la Etapa 3). |

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
