Parte 1
# 6/8/2026 17:41 dia 1 OSI:
Pasted image 20260814095423.png Comandos introducidos con éxito Reparación de errores con IA Instalación de paquetes que faltaban Creación de atajo que al solo poner letra C y pulsar intro limpia la terminal (lo mismo que clear) 6/8/2026 18:41 dia 1OSI: 1h de estudio acumulada 
##7/8/2026 6:22 día 2 OSI:
Ashell tiene página en github para ponerle todo lo que le falta mediante comandos y es personalizable todo pestañas imagen cursor https://github.com/holzschu/a-shell También existe ashell mini SSH para conectar equipos transferir archivos por terminal Comandos SSH para conectar por SSH https://www.ssh.com/academy/ssh/command 7:04 haré 2 ronda para aplicar lo aprendido 7:17 vuelvo a empezar empiezo con https://github.com/holzschu/a-shell](https://github.com/holzschu/a-shell) en safari Abro ashell introduzco help en ashell el resultado es [Documents]$ help a-Shell is a terminal emulator for iOS, with many Unix commands: ls, pwd, tar, mkdir, grep....
a-Shell can do most of the things you can do in a terminal, locally on your iPhone or iPad. You can redirect command output to a file with ">" (append with ">>") and you can pipe commands with "|".
	•	customize appearance with config
	•	pickFolder: open, bookmark and access a directory anywhere (another app, iCloud, WorkingCopy, file providers...)
	•	newWindow: open a new window
	•	exit: close the current window
	•	All your files, including configuration files (.bashrc, .profile, .ssh/...) are in ~/Documents/
	•	Files created by Shortcuts are in ~shortcuts/
	•	a-Shell executes the ~/Documents/.profile and ~/Documents/.bashrc files for each new window
	•	single-finger swipe scrolls the terminal and selects text, two-fingers swipe sends arrows.
	•	Edit files with vim and pico.
	•	Transfer files with curl, tar, scp and sftp.
	•	Clone repositories and do version control with lg2 (similar to git)
	•	Install more commands with "pkg"
	•	Process files with python3, lua, jsc, clang, pdflatex, lualatex.
	•	Open files in other apps with open, play sound and video with play, preview with view.
	•	For network queries: nslookup, ping, host, whois, ifconfig...
	•	bookmark the current directory with "bookmark " and access it later with "cd ~name" or "jump ".
	•	showmarks: show current list of bookmarks
	•	renamemark, deletemark: change list of bookmarks
User guide: https://bianshen00009.gitbook.io/a-guide-to-a-shell/ Support: e-mail (another_shell@icloud.com), Bluesky (@a-shell-ios.bsky.social), github (https://github.com/holzschu/a-shell/issues) and Discord (https://discord.gg/cvYnZm69Gy).
For a full list of commands, type help -l [~Downloads]$ A continuación config en ashell Y después config . en ambos pasa lo mismo [~Downloads]$ config usage: config [-s font size][-n font name][-b background color][-f foreground color][-c cursor color][-dgpr] [~Downloads]$ config . [~Downloads]$ Tengo que aprender a configurarlo La personalización de ashell depende del archivo profile así que midificando este personalizo ashell Para más https://bianshen00009.gitbook.io/a-guide-to-a-shell/ Para compilar ashell Descargar módulo entero y submodulos: git submodule update --init --recursive Descargar todos los frameworks de XC: downloadFrameworks.sh Esto descargará los frameworks estándar de Apple (en xcfs/.build/artefacts/xcfs , con control de checksum). Existen demasiadas bibliotecas y frameworks de Python (más de 2000) disponibles para descargar automáticamente. Puedes eliminarlas en el paso de "Incorporar" del proyecto, o compilar las que desees Necesitarás las herramientas de línea de comandos de Xcode, si aún no las tienes sudo xcode-select -- install Siguiendo en HTML ejecuto úname -a en ashell la salida es la siguiente: [~Downloads]$ uname -a Darwin localhost 25.6.0 Darwin Kernel Version 25. 6.0: Sat Jul 11 15:46:45 PDT 2026; root:xnu-12377 .162.13~2/RELEASE_ARM64_T8140 iPhone17,3 [~Downloads]$ A continuación introduzco el siguiente comando del HTML SSH-keygen: [~Downloads]$ ssh-keygen Generating public/private rsa key pair. Enter file in which to save the key (/private/var /mobile/Containers/Data/Application/8F8B8576-BB74 -4EA9-A54E-FB51B92576DB/Documents/.ssh/id_rsa): 7:53 sigo con ssh ~Downloads]$ ssh-keygen Generating public/private rsa key pair. Enter file in which to save the key (/private/var /mobile/Containers/Data/Application/8F8B8576-BB74 -4EA9-A54E-FB51B92576DB/Documents/.ssh/id_rsa): 1 Reply is: 1. Enter passphrase (empty for no passphrase): Enter same passphrase again: Your identification has been saved in 1 Your public key has been saved in 1.pub The key fingerprint is: SHA256:Y40hjNg9MKhrmt8XdN/vtIHEwddeTYJPisWWfACuM1 c mobile@localhost The key's randomart image is: +---[RSA 3072]----+ | .o .+.+. .| | .o . .B o+.| | .. o = . .+E=. +| |. .o.=.o.o...| | . . .S.o.o .| |.. .. =.... | |o. . ..o | |o . . ..o | | .. .. .o | +----[SHA256]-----+ [~Downloads]$ 7:55 hago captura de pantalla para tener la imagen generada de ssh 8:00 añado la foto aquí IMG_4316.jpeg Pasted image 20260807080326.jpg Código dentro de fotos 8:05 sigo y procedo a aprender el modelo OSI https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/ Mando el HTML a Gemini para que ponga botones de copiado rápido No hace falta al final por qué funciona bien el HTML OSI protocolos | Capa | Nombre | Función Principal | Protocolos / Elementos | Enfoque en Ciberseguridad | | :---: | :--- | :--- | :--- | :--- | | 7 | Aplicación | Interfaz directa con software y usuario final. | HTTP, HTTPS, SMTP, DNS | Ataques DDoS Capa 7(HTTP Floods, agotamiento de recursos del servidor). | | 6 | Presentación | Traducción, formato, compresión y cifrado/descifrado. | TLS/SSL, ASCII, Base64 | Vulnerabilidades en algoritmos de cifrado, desinteligibilidad de datos. | | 5 | Sesión | Apertura, mantenimiento y cierre de sesiones de comunicación. | RPC, Sockets, SMB | Secuestro de sesión (Session Hijacking), ataques Replay. | | 4 | Transporte | Transmisión de datos segmento a segmento (fiable o rápida). | TCP, UDP | SYN Floods, Port Scanning (escaneo de puertos TCP/UDP). | | 3 | Red | Enrutamiento y direccionamiento lógico entre redes. | IP, ICMP, Routers | IP Spoofing, Ping Floods (ICMP DDoS), manipulación de tablas de rutas. | | 2 | Enlace de Datos | Transferencia de tramas entre nodos de la misma red local. | Ethernet, MAC, Switches | ARP Spoofing, MAC Flooding, ataques VLAN Hopping. | | 1 | Física | Transmisión física de bits brutos sobre el medio. | Cables RJ45, Fibra, Radio | Intercepción de señal (Eavesdropping*), Jamming de Wi-Fi, corte físico. |
https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/ OSI:El modelo OSI se puede ver como un lenguaje universal para la conexión de las redes de equipos. Se basa en el concepto de dividir un sistema de comunicación en siete capas abstractas, cada una apilada sobre la anterior. Para capas ver foto de capas 
  Ataques ddos: https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ Ataques a la capa de aplicación se dirigen a la capa 7: https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/
Internet no sigue OSI Cada capa es específica y se comunica con las otras Internet no sigue estrictamente OSI (sigue cerca paquetes de internet) OSI útil para resolver problemas OSi ayuda a desglosar problema y a identificar causa Si problema reduce 1 capa no se hace trabajo innecesario Informe de seguridad https://www.cloudflare.com/lp/security-signals-report/2026/ C7-interactúa datos usuario apps no forman parte de capa la capa de aplicación es responsable de los protocolos y la manipulación de datos de los que depende el software para presentar datos significativos al usuario Protocolos de capa de app incluyen HTTP y SMTP C6-responsable de preparar datos para app para capa de app Hace que datos se preparen para apps Responsable de traducción cifrado y comprensión de datos c6 traduce datos en sintaxis para que receptor 
### 6:22 8/8/2026 día 3 OSI:
6:22 a 8:40 2:18h Total acumuladas h: 3:18h
#### 8:56 9/8/2026 día 4 OSI:
6:22 8:56 total día 2:34 Acumuladas 5:52
Ver opciones de configuración visual (fuente, colores, cursor)
config
Modificar tamaño de fuente (-s) y color de fondo (-b)
config -s 14 -b black
Editar el archivo de perfil para persistir aliases y variables de entorno
pico ~/Documents/.profile
o con vim:
vim ~/Documents/.profile
Alias rápidos
alias c='clear' alias ll='ls -la' alias h='help'
Mostrar mensaje de bienvenida
echo "a-Shell cargado correctamente."
Generar clave RSA estándar de 3072 bits
ssh-keygen
Conectarse a un servidor remoto mediante SSH
ssh usuario@direccion_ip -p 22
Conectarse especificando una clave privada personalizada
ssh -i ~/.ssh/1 usuario@direccion_ip
🔗 Referencias y Enlaces de Interés
 a-Shell GitHub: https://github.com/holzschu/a-shell
 Guía de usuario a-Shell: https://bianshen00009.gitbook.io/a-guide-to-a-shell/
 SSH Command Reference: https://www.ssh.com/academy/ssh/command
 Aprender Modelo OSI (Cloudflare): https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/
 Ataques DDoS Capa 7: https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/
""| Capa | Nombre | Función Principal | Protocolos / Elementos | Enfoque en Ciberseguridad | | :---: | :--- | :--- | :--- | :--- | | 7 | Aplicación | Interfaz directa con software y usuario final. | HTTP, HTTPS, SMTP, DNS | Ataques DDoS Capa 7(HTTP Floods, agotamiento de recursos del servidor). | | 6 | Presentación | Traducción, formato, compresión y cifrado/descifrado. | TLS/SSL, ASCII, Base64 | Vulnerabilidades en algoritmos de cifrado, desinteligibilidad de datos. | | 5 | Sesión | Apertura, mantenimiento y cierre de sesiones de comunicación. | RPC, Sockets, SMB | Secuestro de sesión (Session Hijacking), ataques Replay. | | 4 | Transporte | Transmisión de datos segmento a segmento (fiable o rápida). | TCP, UDP | SYN Floods, Port Scanning (escaneo de puertos TCP/UDP). | | 3 | Red | Enrutamiento y direccionamiento lógico entre redes. | IP, ICMP, Routers | IP Spoofing, Ping Floods (ICMP DDoS), manipulación de tablas de rutas. | | 2 | Enlace de Datos | Transferencia de tramas entre nodos de la misma red local. | Ethernet, MAC, Switches | ARP Spoofing, MAC Flooding, ataques VLAN Hopping. | | 1 | Física | Transmisión física de bits brutos sobre el medio. | Cables RJ45, Fibra, Radio | Intercepción de señal (Eavesdropping), Jamming de Wi-Fi, corte físico. |
+-------------------------------------------------------------+ | Capa 7: APLICACIÓN --> HTTP, HTTPS, SMTP, DNS, FTP, SSH | +-------------------------------------------------------------+ | Capa 6: PRESENTACIÓN --> TLS/SSL, JSON, XML, JPEG (Cifrado)| +-------------------------------------------------------------+ | Capa 5: SESIÓN --> NetBIOS, RPC, Sockets | +-------------------------------------------------------------+ | Capa 4: TRANSPORTE --> TCP, UDP | +-------------------------------------------------------------+ | Capa 3: RED --> IPv4, IPv6, ICMP, IPsec (Routers) | +-------------------------------------------------------------+ | Capa 2: ENLACE DATOS --> Ethernet, Wi-Fi, MAC, Switches | +-------------------------------------------------------------+ | Capa 1: FÍSICA --> Cables, Fibra, Señales de Radio | +-------------------------------------------------------------+
######8:56 10/8/2026 día 6 OSI:
2:34 día 10:13:10 h termine Total acumuladas Hago copia de seguridad hacia notas Notas no aparece en compartir así que en el PC Mac sincronizo el móvil con PC Creo HTML nuevo sincronizado actualizado Y sincronizo Obsidian entre Mac y iPhone con iCloud Buscaré cómo hacer copia de seguridad 12:51 7/8/2026. 16:05 todo listo para jornada siguiente atajo echo y archivo HTML en app Documents en descargas/hack/ y en iCloud Todo sincronizado además ahora el HTML tiene una pestaña llamada guía de referencia donde pego todo lo que apunto en Obsidian y lo indexa y ofrece en forma de índice que al tocar se despliega con botones de copiado rápido y enlaces clicables La pestaña estudiar tiene una checklist de 3 que cuando se completa ofrece los 3 siguientes pasos desplegables con referencias comandos webs y demás 16:23 lo dejé en https://www.cloudflare.com/es-es/learning/ddos/glossary/open-systems-interconnection-model-osi/ 6 Capa de presentación Leer 1 capa 7 y pasar a Documents el HTML capa 6 apuntar todo en obsidian Día 6 10/8/2026 17:40 empiezo a estudiar OSI: [Documents]$ openssl s_client -connect google.com:443 openssl: command not found [Documents]$ openssl version which openssl Modifico el atajo para incluir ashell-mini El 1 comando no funciona así que voy a la web https://www.cloudflare.com/es-es/learning/ddos/glossary/open-systems-interconnection-model-osi/ para aprender capa 7 y 6 el objetivo del día es la 6 el primero más concretamente tls SSL formatos crifrados Me pongo a ello Osi modelo conceptual creado por organizacion estandarización permite sistemas conecten estándar da estándar para conectar lenguaje universal para conexion divide sistema en 7 capas 7 app láyer: Human-computer interaction layer, where applications can access the network services 6 presentation layer:Ensures that data is in a usable format and is where data encryption occurs 5 sesión layer:Maintains connections and is responsible for controlling ports and sessions 4 transport layer:Transmits data using transmission protocols including TCP/UDP 3 network layer:Decides which physical path the data will take 2 data link layer:Defines the format of data on the network 1 physical layer:Transmits raw bit stream over the physical medium
	7.	Capa de aplicación (Application Layer): Capa de interacción entre el usuario y el ordenador, donde las aplicaciones pueden acceder a los servicios de red.
6.Capa de presentación (Presentation Layer): Garantiza que los datos estén en un formato utilizable y es donde se realiza el cifrado de los datos.
5.Capa de sesión (Session Layer): Mantiene las conexiones y se encarga de controlar los puertos y las sesiones.
4.Capa de transporte (Transport Layer): Transmite los datos utilizando protocolos de transmisión, incluidos TCP/UDP.
3.Capa de red (Network Layer): Decide qué ruta física seguirán los datos.
2.Capa de enlace de datos (Data Link Layer): Define el formato de los datos en la red.
1.Capa física (Physical Layer): Transmite el flujo de bits sin procesar a través del medio fisico 7 → Aplicación 6 → Presentación 5 → Sesión 4 → Transporte 3 → Red 2 → Enlace de datos 1 → Física 7-6-5 → Aplicación, datos y sesiones 4 → TCP/UDP 3 → IP/routing 2 → Ethernet/MAC 1 → Señales/cables/Wi-Fi físico Cada osi función comunica capas Los ddos a osi capas específicas https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ Ataques a capa de app https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/ Ataques app capa 7 ataques capa ptrotoclo 3 y 4 Osi desglosar problema e identificar causa Problema-capa-evita trabajo Las 7 capas: 7:app 6:presentación 5:sesión 4:transporte 3:red 2:enlace de datos 1:física 
###### 17:40 10/8/2026 Día 6 OSI:
Hoy 1:12h acumuladas 9:28h
####### 6:47 11/8/2026 día 7 OSI:
traceroute 8.8.8.8 Comand not found en Ashell mini Procedo a investigar cómo arreglarlo: ChatGPT introduzco: traceroute 8.8.8.8 Comand not found Ashell mini Dame el comando para que cualquier comando funcione en Ashell- mini y no de problemas Responde: Con comandos Procedo a arreglarlo Hoy toca la capa 3 y finalizar las 7: #######Capa 7:Aplicacion:

Única interactúa usuario (software) dependen de C7 para iniciar software cliente no C7 C7 protocolos manipulación datos depende datos usuario C7 incluye HTTP-(https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) SMTP-(https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) protocolo correo permite comunicaciones (https://www.cloudflare.com/learning/email-security/what-is-email/) ######Capa 6:Presentación:

Responsable datos usar capa app los preparan consumo apps responsable de traducción cifrado y compresión (https://www.cloudflare.com/learning/ssl/what-is-encryption/) Dos conectados puede usar distintos codificadores responsable traducir entrantes receptor si cifrada responsable cifrado emisor y decodificar receptor para app legible comprime datos de C7 antes enviar a C5 más velocidad/eficiencia comunicación/minimizacion datos transferidos #####Capa 5: Sesión:

Responsable apertura/cierre 2 dispositivos tiempo entre apertura/cierre-sesion garantiza abierta datos cambiando después cierra para no desaprovechar recursos sincroniza datos utilizando control ####Capa 4: Transporte:

Responsable cifrada (extremo a extremo)toma sesión y divide en trozos pequeños (segmentos) responsable rearmar segmentos para construir datos para sesion responsable flujo y errores flujo-velocidad-conexión rápida control errores y garantiza recibidos y si no solicita (https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/) (https://www.cloudflare.com/learning/ddos/glossary/user-datagram-protocol-udp/) ###Capa 3: Red:

Responsable transferencia redes si dispositivos se encuentran en red la capa no necesaria divide segmentos en unidades pequeñas paquetes(https://www.cloudflare.com/learning/network-layer/what-is-a-packet/) los junta en receptor La capa busca la ruta para datos a destino [enrutamiento] (https://www.cloudflare.com/learning/network-layer/what-is-routing/) Protocolos incluyen ip Protocolo control Internet (ICMP), el Protocolo grupo Internet (IGMP) paquete IPsec## ##Capa2:Enlace datos: **** Similar a 3 excepto que capa enlace facilita datos dos de red(misma) la 2 coje paquetes y divide en partes pequeñas (tramas) Responsable control flujo y control errores comunicaciones red (transporte solo control flujo y errores ) # Capa 1: Física :

 Esquioo físico en datos (cables y conmutadores)-(https://www.cloudflare.com/learning/network-layer/what-is-a-network-switch/) Datos en bits 1 y 0 dispositivos estar acuerdo a convención a convención a 1 y 0 (bits) en dispositivos Transmisión en osi: Datos atravesar 7 capas en orden en emisor y receptor # #######7:23 11/8/2026 día 7 OSI: como están sin acabar las 7 capas sigo por encima de capa 3 para acabar 7:53 11/8/2026 descanso 8:31 he editado esta nota en el descanso para asegurar que refleja bien los días 1/2/3 las h de estudio y que lleva orden en todo aparte de que esté documentada 8:32 sigo terminando capa 6 y termino capa 7 Total acumuladas h:hasta ahora 9:46 procedo a marcar conceptos y dias dia 7 empiezo: 6:47 Termino:1204 Horas día 6:51 Acumuladas 16:19h Falta: Terminal para Mac y iPhone sincronizada # ########5:18 12/8/2026 día 8 capa red direccionamiento subnetting ICMP https://www.google.com/search?client=firefox-b-m&q=capa%20red%20direccionamiento%20subnetting%20ICMP%20 Welcome to Alpine!
You can install packages with: apk add 
You may change this message by editing /etc/motd.
localhost:~# traceroute 8.8.8.8 traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 46 byte packets 1traceroute: sendto: Socket is connected localhost:~# localhost:~# arp -a arp: can't open '/proc/net/arp': No such file or directory localhost:~# localhost:~# tcpdump -i any -c 10 -n -ash: tcpdump: not found localhost:~# Capa 3 Red (IP / Direccionamiento / Subnetting / ICMP) Capa 3: se encarga del direccionamiento lógico y del enrutamiento de paquetes de datos a través de diferentes redes interconectadas usa protocolos ip icmp para mover dirección de origen a destino Protocolo IP: Dirección lógica identifica únicamente cada dispositivo en una red IPv4 e IPv6 versiones en uso v4 32 y v6 128 (bits) Encapsulamiento: añade info origen/destino a paquete Direccionamiento/Subnetting: Red/host:ip dividida entre red y equipo Máscara de su red:que parte de ip es de red y cuál de host Subnetting:divide red en redes para mejorar rendimiento y seguridad Protocolo ICMP: Control y errores:informa sobre ellos con mensajes Herramienta Ping: usa ICMP para comprobar conexión con (PC) Herramienta Traceroute:enseña ruta de paquetes en routers 5:54 termino 1 tarea del día localhost:~# arp -a arp: can't open '/proc/net/arp': No such file or directory localhost:~# Capa 1 Física & Capa 2 Enlace (Ethernet / Direcciones MAC / ARP) https://www.google.com/search?client=firefox-b-m&q=Capa%201%20F%C3%ADsica%20%26%20Capa%202%20Enlace%20%28Ethernet%20%2F%20Direcciones%20MAC%20%2F%20ARP%29 Ethernet usa mac para mandar datos a red local Mac fija (estática)ip cambia (dinámica) ARP une ip con Mac para hablar en la red 06:03 Comienzo descanso/Termino descanso 6;07 - 4 minutos de descanso Ethernet/Mac: Ethernet:estándar que conecta (pcs)en red por cable/señañes Mac:viene de fábrica es un código de 48 bits no cambia e identifica el equipo,es una tarjeta que identifica Protocolo ARP: Arp:un PC pregunta quien tiene la ip correcta a la red Respuesta:el PC con esa ip responde con Mac Tabla caché: PC tardan respuestas para no preguntar qué envían localhost:~# tcpdump -i any -c 10 -n -ash: tcpdump: not found localhost:~# https://www.google.com/search?client=firefox-b-m&q=Captura%20y%20An%C3%A1lisis%20de%20Tr%C3%A1fico%20de%20Red%20%28Wireshark%20%26%20Tcpdump Captura y Análisis de Tráfico de Red Wireshark tcpdump: Herramientas para captura/analisis de red tcpdump es capturador en línea de comandos para servidores whireshark es gráfica/ avanzada y examina paquetes se usan juntos para análisis en whireshark Uso tcpdump: Capturar: tcpdump -i eth0 Guardar: tcpdump -i eth0 -w captura.pcap Filtrar puertos: tcpdump -i eth0 port 80 Uso wireshark Seleccionar: elige tarjeta res y pulsar botón Filtros visualización: IP/HTTP … Seguir TCP: clic en paquete y reconstruye la charla completa de sesión 6:55 hago pausa para reparar terminal 7:06 termino de arreglar terminal continuo Total tiempo no estudiado: 15 minutos 7:12 instalo todo a iSH para evitar fallos localhost:~# curl -I https://example.com HTTP/2 200 date: Wed, 12 Aug 2026 05:14:44 GMT content-type: text/html server: cloudflare last-modified: Sat, 08 Aug 2026 02:07:29 GMT allow: GET, HEAD accept-ranges: bytes age: 4946 cf-cache-status: HIT cf-ray: a29cff89dc05f771-MAD
localhost:~# Fundamentos OWASP Top 10 & Pentesting Web https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=AOlV&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnt_medfkAcFtbiCaiablEO6aJQaxg%3A1786511845349&udm=50&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiCgrefq5qWAxVkygIHHUsSJrYQ2J8OegQIDhAE&biw=393&bih=651&dpr=3&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1
https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=3iQq&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnuPZ4nCUp_5sdYQYUWr7jIeSvGShw%3A1786512757600&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiSorbSrpqWAxVG7LsIHaQdF0AQ2J8OegQIDhAE&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1&udm=50&biw=393&bih=651&dpr=3 OWASP:Top 10 guía https://owasp.org/Top10/2021/es/ Recoge 10 riesgos críticos en apps web Pentesting web es simular/descubrir/mitigar vulnerabilidades antes Las graves: organizado en frecuencia/impacto A01:2021-acceso roto: Usuarios van a datos/funciones fuera de permiso A02:2021-Falla criptográfica: Exposición de datos por cifrado/algoritmo A03:2021-Inyección: Datos enviados a intérprete comandos involuntarios A04:2021-Diseño inseguro: Errores/arquitectura/diseño de app que no se arreglan A05:2021-Configuración seguridad incorrecta: Sistemas por defecto servicios/mensajes de error con detalle A06:2021-Componentes: Hackeables que usan librerías/framewroks/software con fallos A07:2021Fallos: identificación/autentificacion Permite fuerza/robo por la gestión de keys (contraseñas) A08:2021-Fallos integridad de software/datos: Código/datos sin ver origen A09:2021-Fallos en registro/supervisión de seguridad: No registrar criticos(eventos)impide detectar ataques A10:2021-Falsificación solicitudes servidor (SSRF): App/web manipulada para hacer peticiones a servidores Metodología de Pentesting Web: 1 Reconocimiento: Recopila información sobre objetivo/activa 2 Escaneo y Análisis: Saber por dónde entrar con herramientas 3 Explotación (Gain Access): Aprovecha vulnerabilidades 4 Post-explotación: Mide impacto de fallo analiza datos comprometidos o escala privilegios. 5 Reporte: Crear informe para desarrollador/ejecutivo/gerencia y dice la solución https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=3iQq&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnuPZ4nCUp_5sdYQYUWr7jIeSvGShw%3A1786512757600&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiSorbSrpqWAxVG7LsIHaQdF0AQ2J8OegQIDhAE&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1&udm=50&biw=393&bih=651&dpr=3 Herramientas pentester: Se unan entornos/ herramientas Kali SO para seguridad tiene muchas herramientas Burp Owasp proxis para analizar/modificar/repetir HTTP (entre navegador y servidor) Nmap escáner para abiertos/ejecucion (puertos) Dirsearch/Gobuster para directorios/archivos en servidor OWASP Juice Shop vulnerable para hacking segura 8:18 12/8/2026 acabo de estudiar Empeze a las 5:18 Total h hoy 3h Acumuladas 19:19 h
########7:08 13/8/2026 dia 8 Scripting Bash & Python para Automatización Terminal
localhost:~# python3 -m http.server 8080 -ash: python3: not found localhost:~# https://www.py4e.com/ Python para todos: Materiales https://www.py4e.com/lessons Conferencias https://www.youtube.com/watch?v=UjeNA_JtXME&list=PLlRFEj9H3Oj7Bp8-DfGpfAfDBiblRfl5p&index=1 Libro https://www.py4e.com/book.php También en: coursera https://www.coursera.org/specializations/python Edx https://www.edx.org/bio/charles-severance Freecodecamp https://www.youtube.com/watch?v=8DvywoWv6fI Certificados gratuitos para estudiantes y personal de la universidad de Míchigan https://online.umich.edu/series/python-for-everybody/ Si inicias sesión te unes a un mundo libre curso online con calificaciones asignaciones/foros/insignias por tus esfuerzos se toman en serio la privacidad se puede revisar política para detalles https://www.py4e.com/privacy Todo esto se puede usar https://www.py4e.com/tsugi/cc/ IMS también herramientas IMS la clave/secreto https://www.py4e.com/tsugi/admin/key/index.php el código/diapositivas/contenido está en https://github.com/csev/py4e puedes hacer lo que quieras con el mismo puedes traducir el sitio publicarlo (instrucciones traducción github) https://github.com/csev/py4e/blob/master/TRANSLATION.md la web usa Tsugi http://www.tsugi.org/ para aprender si quieres colaborar http://www.tsugi.org/ https://www.py4e.com/ python3 -m http.server 8080 Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ... Hardening Unix/Linux & Auditoría de Archivos de Log tail -f /var/log/syslog no funciona en ishell Con otros comandos localhost:~# echo "[INFO] Sistema iniciado" > prueba.log tail -f prueba.log INFO] Sistema iniciado localhost:~# python3 -m http.server 8080 Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ... Ishell es solo en inglés [https://www.cisecurity.org/cis-benchmarks/] 8:31 descanso CIS configuraciones para productos son expertos/esfuerzo/consenso mundial ayudan a sistemas contra amenazas Puntos de referencia https://learn.cisecurity.org/benchmarks Nuevo? https://www.cisecurity.org/cis-benchmarks-overview Benchmarks/puntos https://fast.wistia.com/embed/medias/s1abjx9h37/ encuentra lo que buscas tecnología/subcategoria/filtar(jopcional)/CIS/accede a todo esto en la web https://www.cisecurity.org/cis-benchmarks a unos 7 mm del inicio de la web en cuadro azul Construye kits https://www.cisecurity.org/cis-securesuite/cis-securesuite-build-kit-content descarga referencias v2.0.0 https://learn.cisecurity.org/benchmarks A fondo https://www.cisecurity.org/benchmark/alibaba_cloud Adaptar https://www.cisecurity.org/cis-securesuite CIS Benchmarks https://www.cisecurity.org/cis-benchmarks Arista Networks https://www.cisecurity.org/benchmark/arista_networks Azure Linux https://www.cisecurity.org/benchmark/azure_linux BIND https://www.cisecurity.org/benchmark/bind Bottlerocket https://www.cisecurity.org/benchmark/bottlerocket Check Point Firewall https://www.cisecurity.org/benchmark/checkpoint_firewall Cisco https://www.cisecurity.org/benchmark/cisco CockroachDB https://www.cisecurity.org/benchmark/cockroachdb Debian Linux https://www.cisecurity.org/benchmark/debian_linux DigitalOcean https://www.cisecurity.org/benchmark/digitalocean DISA STIG https://www.cisecurity.org/benchmark/stig_bm Docker https://www.cisecurity.org/benchmark/docker Everpure https://www.cisecurity.org/benchmark/everpure Extreme Networks https://www.cisecurity.org/benchmark/extreme_networks F5 https://www.cisecurity.org/benchmark/f5 Fortinet https://www.cisecurity.org/benchmark/fortinet FreeBSD https://www.cisecurity.org/benchmark/freebsd Google Android https://www.cisecurity.org/benchmark/google_android Google Chrome https://www.cisecurity.org/benchmark/google_chrome Google ChromeOS https://www.cisecurity.org/benchmark/google_chromeos Google Cloud Computing Platform https://www.cisecurity.org/benchmark/google_cloud_computing_platform Google Workspace https://www.cisecurity.org/benchmark/google_workspace HPE Aruba Networking https://www.cisecurity.org/benchmark/hpe_aruba_networking IBM AIX https://www.cisecurity.org/benchmark/ibm_aix IBM Cloud Foundations https://www.cisecurity.org/benchmark/ibm_cloud_foundations IBM Db2 https://www.cisecurity.org/benchmark/ibm_db2 IBM i https://www.cisecurity.org/benchmark/ibm_i IBM WebSphere https://www.cisecurity.org/benchmark/ibm_websphere IBM Z System https://www.cisecurity.org/benchmark/ibm_z_system Juniper https://www.cisecurity.org/benchmark/juniper Kubernetes https://www.cisecurity.org/benchmark/kubernetes Linux Mint https://www.cisecurity.org/benchmark/linux_mint LXD https://www.cisecurity.org/benchmark/lxd MariaDB https://www.cisecurity.org/benchmark/mariadb Microsoft 365 https://www.cisecurity.org/benchmark/microsoft_365 Microsoft Azure https://www.cisecurity.org/benchmark/azure Microsoft Dynamics 365 Power Platform https://www.cisecurity.org/benchmark/dynamics_365_power_platform Microsoft Exchange Server https://www.cisecurity.org/benchmark/exchange_server Microsoft IIS https://www.cisecurity.org/benchmark/iis Microsoft Intune Apple iOS, iPadOS, macOS https://www.cisecurity.org/benchmark/intune_apple Microsoft Intune for Microsoft Windows https://www.cisecurity.org/benchmark/intune_windows Microsoft Office https://www.cisecurity.org/benchmark/microsoft_office Microsoft SharePoint https://www.cisecurity.org/benchmark/sharepoint Microsoft SQL Server https://www.cisecurity.org/benchmark/sql_server Microsoft Web Browser https://www.cisecurity.org/benchmark/microsoft_web_browser Microsoft Windows Desktop https://www.cisecurity.org/benchmark/windows_desktop Microsoft Windows Server https://www.cisecurity.org/benchmark/windows_server MongoDB https://www.cisecurity.org/benchmark/mongodb Mozilla Firefox https://www.cisecurity.org/benchmark/mozilla_firefox NGINX https://www.cisecurity.org/benchmark/nginx OceanBase https://www.cisecurity.org/benchmark/oceanbase OPNsense https://www.cisecurity.org/benchmark/opnsense Oracle Cloud Infrastructure https://www.cisecurity.org/benchmark/oracle_cloud Oracle Database https://www.cisecurity.org/benchmark/oracle_database Oracle Linux https://www.cisecurity.org/benchmark/oracle_linux Oracle MySQL https://www.cisecurity.org/benchmark/oracle_mysql Oracle Solaris https://www.cisecurity.org/benchmark/oracle_solaris Palo Alto Networks https://www.cisecurity.org/benchmark/palo_alto_networks pfSense Firewall https://www.cisecurity.org/benchmark/pfsense PostgreSQL https://www.cisecurity.org/benchmark/postgresql Red Hat Enterprise Linux https://www.cisecurity.org/benchmark/red_hat_enterprise_linux Robot Operating System (ROS) https://www.cisecurity.org/benchmark/ros Rocky Linux https://www.cisecurity.org/benchmark/rocky_linux Safari Browser https://www.cisecurity.org/benchmark/safari SingleStore https://www.cisecurity.org/benchmark/singlestore Snowflake https://www.cisecurity.org/benchmark/snowflake Software Supply Chain Security https://www.cisecurity.org/benchmark/software_supply_chain_security Sophos https://www.cisecurity.org/benchmark/sophos SUSE Linux Enterprise Server https://www.cisecurity.org/benchmark/suse_linux Talos Linux https://www.cisecurity.org/benchmark/talos_linux Tencent Cloud https://www.cisecurity.org/benchmark/tencent_cloud Ubuntu Linux https://www.cisecurity.org/benchmark/ubuntu_linux Visual Studio https://www.cisecurity.org/benchmark/visual_studio VMware https://www.cisecurity.org/benchmark/vmware Wind River Linux https://www.cisecurity.org/benchmark/wind_river_linux YugabyteDB https://www.cisecurity.org/benchmark/yugabytedb 9:11 termino estudiar Total h hoy 1:56 minutos Acumuladas 21:15h a dia 8 Creado nuevo HTML Que funciona en Mac y iPhone Vale para todo Creado con Gemini 11:08 actualizados foto y nombre en RRSS Procedo a colgar apuntes de Obsidian
Parte 2
 # #########06:04 14/82026 día 9 Capa 6: Presentación & Capa 7: Aplicación Welcome to Alpine! You can install packages with: apk add  You may change this message by editing /etc/motd. localhost:~# curl -Iv https://cloudflare.com
	•	Trying 104.16.132.229:443...
	•	Failed to set TCP_KEEPIDLE on fd 5
	•	Failed to set TCP_KEEPINTVL on fd 5
	•	Connected to cloudflare.com (104.16.132.229) port 443 (#0)
	•	ALPN: offers h2,http/1.1
	•	TLSv1.3 (OUT), TLS handshake, Client hello (1):
	•	CAfile: /etc/ssl/certs/ca-certificates.crt
	•	CApath: none
	•	TLSv1.3 (IN), TLS handshake, Server hello (2):
	•	TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
	•	TLSv1.3 (IN), TLS handshake, Certificate (11):
	•	TLSv1.3 (IN), TLS handshake, CERT verify (15):
	•	TLSv1.3 (IN), TLS handshake, Finished (20):
	•	TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
	•	TLSv1.3 (OUT), TLS handshake, Finished (20):
	•	SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
	•	ALPN: server accepted h2
	•	Server certificate:
	•	subject: CN=cloudflare.com
	•	start date: Jul 8 21:47:39 2026 GMT
	•	expire date: Oct 6 22:47:27 2026 GMT
	•	subjectAltName: host "cloudflare.com" matched cert's "cloudflare.com"
	•	issuer: C=US; O=Google Trust Services; CN=WE1
	•	SSL certificate verify ok.
	•	using HTTP/2
	•	h2h3 [:method: HEAD]
	•	h2h3 [:path: /]
	•	h2h3 [:scheme: https]
	•	h2h3 [:authority: cloudflare.com]
	•	h2h3 [user-agent: curl/8.0.1]
	•	h2h3 [accept: /]
	•	Using Stream ID: 1 (easy handle 0xf7b52170)HEAD / HTTP/2 Host: cloudflare.com Ataques Ddos https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/ Van a la capa de app de internet para parar el flujo web/servicio Que es? https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ Los de C7 son un tipo de mal comportamiento que apunta a la capa superior de OSI https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/ Donde solicitudes https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/ son efectivas por consumo de recursos aparte de red https://www.cloudflare.com/learning/ddos/dns-amplification-ddos-attack/https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/ Cómo funcionan? La efectividad de los Ddos viene de la cantidad de recursos El consumo de recursos entre cliente/servidor Los datos son mínimos El servidor que recibe solicitud de cliente debe realizar consultas de BBDD o API para producir web Cuando disparidad magnifica el resultado es dispositivos apuntando a una sola propiedad como ataque https://www.cloudflare.com/learning/ddos/what-is-a-ddos-botnet/(Ddos) El servicio colapsa y provoca Ddos https://www.cloudflare.com/learning/ddos/glossary/denial-of-service/ El tráfico en casos ataca API con C7 para dejarlo fuera del sistema Por qué es difícil detenerlos? Difícil distinguir ataque/normal (trafico) sobre todo en capas de apps (como bot et para ataque)https://www.cloudflare.com/learning/ddos/http-flood-ddos-attack/ Contra servidor victima cada bot realiza solicitudes de red el tráfico no se falsifica https://www.cloudflare.com/learning/ddos/glossary/ip-spoofing/ y parece normal Requieren estrategia con capacidad de límite de tráfico según reglas Varían 07:01 Ahora procedo a terminar lo que dejé ayer incompleto lo dejo en https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/ Sección como funcionan y dentro de ella en varían Y sigo por donde lo dejé ayer Lo dejo en referencias de macOS de ayer Horas hoy 1:18 Acumuladas 22:33h Día 9 8:40 actualizado Día siguiente solo estudiar 
##########7:39 16/8/2026 Día 10 Fundamentos de Redes / TCP-IP
https://www.google.com/search?client=firefox-b-m&q=Fundamentos%20de%20Redes%20%2F%20TCP-IP#lfId=ChxjMe Conjunto de reglas que se usan para internet Divide envío en 4 Las 4 Capa de app la más cercana a la persona que la usa Donde viven apps ( web correo …) Nombres fáciles ( webs) Capa de transporte Controla viaje datos Usa TCP para no errores/llege bien Usa UDP para rapidez (videos llamadas) Capa de red/ internet Pone dirección a cada dato Usa ip para destino Capa de acceso a la red/enlace Maneja conexión Pasa datos por cable/wifi/fibra Conceptos clave IP número único que identifica aparato en red Paquetes datos grandes se hacen pequeños(paquetes) viajan mejor y se juntan al llegar Reglas/Protocolos acuerdos de las máquinas para entenderse siempre Protocolos/puertos de TCP/IP https://www.youtube.com/watch?v=WSMcAY-Lmjc Análisis de Tráfico en Wireshark Whireshark es libre Captura y ve datos de red Ayurda fallos revisa seguridad y entiende a equipos Empieza a usarla https://www.wireshark.org/ Para tráfico Elige red abre app y selecciona tu tarjeta Capturar datos pulsa botón y graba datos Filtrar la vista usa filtros HTTP/dns/ip.addr/ para ver Revisar capas clickea paquete y ve sus detalles divididos Fundamentos de captura/analisis de paquetes https://www.youtube.com/watch?v=I7zlZ1bQuQQ Consejos La captura poco tiempo abierta Filtros claros Ahorra tiempo con nombres de protocolos Cuidado con privacidad no compartas Escaneo de Puertos con Nmap Fundamentos de Redes y Protocolos (TCP/IP, DNS, HTTP)[PENDIENTE] https://www.google.com/search?client=firefox-b-m&q=Fundamentos%20de%20Redes%20y%20Protocolos%20%28TCP%2FIP%2C%20DNS%2C%20HTTP%29%0A%5BPENDIENTE%5D#lfId=ChxjMe Son reglas que hacen que aparatos hablen entre sí TCP/IP envía datos ordenados DNS cambia nombres por IP HTTP mueve entre servidor/navegador TCP/IP IP da dirección a aparato para red TCP parte mensajes ( en paquetes) los cuida y junta (al final) Conexión segura crea ruta antes de datos para no pérdidas DNS Traductor cambia nombres(Google)a IP Directorios usa servidores mundiales para encontrar dirección(rapido) Caché guarda respuestas(del pasado) en el pc/aparato para abrir con velocidad HTTP Base es peticiones y respuestas pides/devuelve Métodos principales GET lee datos POST envía datos Códigos avisan (200 si todo ok 404 si web no está …)
Parte 1
# 6/8/2026 17:41 dia 1 OSI:
Pasted image 20260814095423.png Comandos introducidos con éxito Reparación de errores con IA Instalación de paquetes que faltaban Creación de atajo que al solo poner letra C y pulsar intro limpia la terminal (lo mismo que clear) 6/8/2026 18:41 dia 1OSI: 1h de estudio acumulada 
##7/8/2026 6:22 día 2 OSI:
Ashell tiene página en github para ponerle todo lo que le falta mediante comandos y es personalizable todo pestañas imagen cursor https://github.com/holzschu/a-shell También existe ashell mini SSH para conectar equipos transferir archivos por terminal Comandos SSH para conectar por SSH https://www.ssh.com/academy/ssh/command 7:04 haré 2 ronda para aplicar lo aprendido 7:17 vuelvo a empezar empiezo con https://github.com/holzschu/a-shell](https://github.com/holzschu/a-shell) en safari Abro ashell introduzco help en ashell el resultado es [Documents]$ help a-Shell is a terminal emulator for iOS, with many Unix commands: ls, pwd, tar, mkdir, grep....
a-Shell can do most of the things you can do in a terminal, locally on your iPhone or iPad. You can redirect command output to a file with ">" (append with ">>") and you can pipe commands with "|".
	•	customize appearance with config
	•	pickFolder: open, bookmark and access a directory anywhere (another app, iCloud, WorkingCopy, file providers...)
	•	newWindow: open a new window
	•	exit: close the current window
	•	All your files, including configuration files (.bashrc, .profile, .ssh/...) are in ~/Documents/
	•	Files created by Shortcuts are in ~shortcuts/
	•	a-Shell executes the ~/Documents/.profile and ~/Documents/.bashrc files for each new window
	•	single-finger swipe scrolls the terminal and selects text, two-fingers swipe sends arrows.
	•	Edit files with vim and pico.
	•	Transfer files with curl, tar, scp and sftp.
	•	Clone repositories and do version control with lg2 (similar to git)
	•	Install more commands with "pkg"
	•	Process files with python3, lua, jsc, clang, pdflatex, lualatex.
	•	Open files in other apps with open, play sound and video with play, preview with view.
	•	For network queries: nslookup, ping, host, whois, ifconfig...
	•	bookmark the current directory with "bookmark " and access it later with "cd ~name" or "jump ".
	•	showmarks: show current list of bookmarks
	•	renamemark, deletemark: change list of bookmarks
User guide: https://bianshen00009.gitbook.io/a-guide-to-a-shell/ Support: e-mail (another_shell@icloud.com), Bluesky (@a-shell-ios.bsky.social), github (https://github.com/holzschu/a-shell/issues) and Discord (https://discord.gg/cvYnZm69Gy).
For a full list of commands, type help -l [~Downloads]$ A continuación config en ashell Y después config . en ambos pasa lo mismo [~Downloads]$ config usage: config [-s font size][-n font name][-b background color][-f foreground color][-c cursor color][-dgpr] [~Downloads]$ config . [~Downloads]$ Tengo que aprender a configurarlo La personalización de ashell depende del archivo profile así que midificando este personalizo ashell Para más https://bianshen00009.gitbook.io/a-guide-to-a-shell/ Para compilar ashell Descargar módulo entero y submodulos: git submodule update --init --recursive Descargar todos los frameworks de XC: downloadFrameworks.sh Esto descargará los frameworks estándar de Apple (en xcfs/.build/artefacts/xcfs , con control de checksum). Existen demasiadas bibliotecas y frameworks de Python (más de 2000) disponibles para descargar automáticamente. Puedes eliminarlas en el paso de "Incorporar" del proyecto, o compilar las que desees Necesitarás las herramientas de línea de comandos de Xcode, si aún no las tienes sudo xcode-select -- install Siguiendo en HTML ejecuto úname -a en ashell la salida es la siguiente: [~Downloads]$ uname -a Darwin localhost 25.6.0 Darwin Kernel Version 25. 6.0: Sat Jul 11 15:46:45 PDT 2026; root:xnu-12377 .162.13~2/RELEASE_ARM64_T8140 iPhone17,3 [~Downloads]$ A continuación introduzco el siguiente comando del HTML SSH-keygen: [~Downloads]$ ssh-keygen Generating public/private rsa key pair. Enter file in which to save the key (/private/var /mobile/Containers/Data/Application/8F8B8576-BB74 -4EA9-A54E-FB51B92576DB/Documents/.ssh/id_rsa): 7:53 sigo con ssh ~Downloads]$ ssh-keygen Generating public/private rsa key pair. Enter file in which to save the key (/private/var /mobile/Containers/Data/Application/8F8B8576-BB74 -4EA9-A54E-FB51B92576DB/Documents/.ssh/id_rsa): 1 Reply is: 1. Enter passphrase (empty for no passphrase): Enter same passphrase again: Your identification has been saved in 1 Your public key has been saved in 1.pub The key fingerprint is: SHA256:Y40hjNg9MKhrmt8XdN/vtIHEwddeTYJPisWWfACuM1 c mobile@localhost The key's randomart image is: +---[RSA 3072]----+ | .o .+.+. .| | .o . .B o+.| | .. o = . .+E=. +| |. .o.=.o.o...| | . . .S.o.o .| |.. .. =.... | |o. . ..o | |o . . ..o | | .. .. .o | +----[SHA256]-----+ [~Downloads]$ 7:55 hago captura de pantalla para tener la imagen generada de ssh 8:00 añado la foto aquí IMG_4316.jpeg Pasted image 20260807080326.jpg Código dentro de fotos 8:05 sigo y procedo a aprender el modelo OSI https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/ Mando el HTML a Gemini para que ponga botones de copiado rápido No hace falta al final por qué funciona bien el HTML OSI protocolos | Capa | Nombre | Función Principal | Protocolos / Elementos | Enfoque en Ciberseguridad | | :---: | :--- | :--- | :--- | :--- | | 7 | Aplicación | Interfaz directa con software y usuario final. | HTTP, HTTPS, SMTP, DNS | Ataques DDoS Capa 7(HTTP Floods, agotamiento de recursos del servidor). | | 6 | Presentación | Traducción, formato, compresión y cifrado/descifrado. | TLS/SSL, ASCII, Base64 | Vulnerabilidades en algoritmos de cifrado, desinteligibilidad de datos. | | 5 | Sesión | Apertura, mantenimiento y cierre de sesiones de comunicación. | RPC, Sockets, SMB | Secuestro de sesión (Session Hijacking), ataques Replay. | | 4 | Transporte | Transmisión de datos segmento a segmento (fiable o rápida). | TCP, UDP | SYN Floods, Port Scanning (escaneo de puertos TCP/UDP). | | 3 | Red | Enrutamiento y direccionamiento lógico entre redes. | IP, ICMP, Routers | IP Spoofing, Ping Floods (ICMP DDoS), manipulación de tablas de rutas. | | 2 | Enlace de Datos | Transferencia de tramas entre nodos de la misma red local. | Ethernet, MAC, Switches | ARP Spoofing, MAC Flooding, ataques VLAN Hopping. | | 1 | Física | Transmisión física de bits brutos sobre el medio. | Cables RJ45, Fibra, Radio | Intercepción de señal (Eavesdropping*), Jamming de Wi-Fi, corte físico. |
https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/ OSI:El modelo OSI se puede ver como un lenguaje universal para la conexión de las redes de equipos. Se basa en el concepto de dividir un sistema de comunicación en siete capas abstractas, cada una apilada sobre la anterior. Para capas ver foto de capas 
  Ataques ddos: https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ Ataques a la capa de aplicación se dirigen a la capa 7: https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/
Internet no sigue OSI Cada capa es específica y se comunica con las otras Internet no sigue estrictamente OSI (sigue cerca paquetes de internet) OSI útil para resolver problemas OSi ayuda a desglosar problema y a identificar causa Si problema reduce 1 capa no se hace trabajo innecesario Informe de seguridad https://www.cloudflare.com/lp/security-signals-report/2026/ C7-interactúa datos usuario apps no forman parte de capa la capa de aplicación es responsable de los protocolos y la manipulación de datos de los que depende el software para presentar datos significativos al usuario Protocolos de capa de app incluyen HTTP y SMTP C6-responsable de preparar datos para app para capa de app Hace que datos se preparen para apps Responsable de traducción cifrado y comprensión de datos c6 traduce datos en sintaxis para que receptor 
### 6:22 8/8/2026 día 3 OSI:
6:22 a 8:40 2:18h Total acumuladas h: 3:18h
#### 8:56 9/8/2026 día 4 OSI:
6:22 8:56 total día 2:34 Acumuladas 5:52
Ver opciones de configuración visual (fuente, colores, cursor)
config
Modificar tamaño de fuente (-s) y color de fondo (-b)
config -s 14 -b black
Editar el archivo de perfil para persistir aliases y variables de entorno
pico ~/Documents/.profile
o con vim:
vim ~/Documents/.profile
Alias rápidos
alias c='clear' alias ll='ls -la' alias h='help'
Mostrar mensaje de bienvenida
echo "a-Shell cargado correctamente."
Generar clave RSA estándar de 3072 bits
ssh-keygen
Conectarse a un servidor remoto mediante SSH
ssh usuario@direccion_ip -p 22
Conectarse especificando una clave privada personalizada
ssh -i ~/.ssh/1 usuario@direccion_ip
🔗 Referencias y Enlaces de Interés
 a-Shell GitHub: https://github.com/holzschu/a-shell
 Guía de usuario a-Shell: https://bianshen00009.gitbook.io/a-guide-to-a-shell/
 SSH Command Reference: https://www.ssh.com/academy/ssh/command
 Aprender Modelo OSI (Cloudflare): https://www.cloudflare.com/es-es/learning/network-layer/what-is-the-osi-model/
 Ataques DDoS Capa 7: https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/
""| Capa | Nombre | Función Principal | Protocolos / Elementos | Enfoque en Ciberseguridad | | :---: | :--- | :--- | :--- | :--- | | 7 | Aplicación | Interfaz directa con software y usuario final. | HTTP, HTTPS, SMTP, DNS | Ataques DDoS Capa 7(HTTP Floods, agotamiento de recursos del servidor). | | 6 | Presentación | Traducción, formato, compresión y cifrado/descifrado. | TLS/SSL, ASCII, Base64 | Vulnerabilidades en algoritmos de cifrado, desinteligibilidad de datos. | | 5 | Sesión | Apertura, mantenimiento y cierre de sesiones de comunicación. | RPC, Sockets, SMB | Secuestro de sesión (Session Hijacking), ataques Replay. | | 4 | Transporte | Transmisión de datos segmento a segmento (fiable o rápida). | TCP, UDP | SYN Floods, Port Scanning (escaneo de puertos TCP/UDP). | | 3 | Red | Enrutamiento y direccionamiento lógico entre redes. | IP, ICMP, Routers | IP Spoofing, Ping Floods (ICMP DDoS), manipulación de tablas de rutas. | | 2 | Enlace de Datos | Transferencia de tramas entre nodos de la misma red local. | Ethernet, MAC, Switches | ARP Spoofing, MAC Flooding, ataques VLAN Hopping. | | 1 | Física | Transmisión física de bits brutos sobre el medio. | Cables RJ45, Fibra, Radio | Intercepción de señal (Eavesdropping), Jamming de Wi-Fi, corte físico. |
+-------------------------------------------------------------+ | Capa 7: APLICACIÓN --> HTTP, HTTPS, SMTP, DNS, FTP, SSH | +-------------------------------------------------------------+ | Capa 6: PRESENTACIÓN --> TLS/SSL, JSON, XML, JPEG (Cifrado)| +-------------------------------------------------------------+ | Capa 5: SESIÓN --> NetBIOS, RPC, Sockets | +-------------------------------------------------------------+ | Capa 4: TRANSPORTE --> TCP, UDP | +-------------------------------------------------------------+ | Capa 3: RED --> IPv4, IPv6, ICMP, IPsec (Routers) | +-------------------------------------------------------------+ | Capa 2: ENLACE DATOS --> Ethernet, Wi-Fi, MAC, Switches | +-------------------------------------------------------------+ | Capa 1: FÍSICA --> Cables, Fibra, Señales de Radio | +-------------------------------------------------------------+
######8:56 10/8/2026 día 6 OSI:
2:34 día 10:13:10 h termine Total acumuladas Hago copia de seguridad hacia notas Notas no aparece en compartir así que en el PC Mac sincronizo el móvil con PC Creo HTML nuevo sincronizado actualizado Y sincronizo Obsidian entre Mac y iPhone con iCloud Buscaré cómo hacer copia de seguridad 12:51 7/8/2026. 16:05 todo listo para jornada siguiente atajo echo y archivo HTML en app Documents en descargas/hack/ y en iCloud Todo sincronizado además ahora el HTML tiene una pestaña llamada guía de referencia donde pego todo lo que apunto en Obsidian y lo indexa y ofrece en forma de índice que al tocar se despliega con botones de copiado rápido y enlaces clicables La pestaña estudiar tiene una checklist de 3 que cuando se completa ofrece los 3 siguientes pasos desplegables con referencias comandos webs y demás 16:23 lo dejé en https://www.cloudflare.com/es-es/learning/ddos/glossary/open-systems-interconnection-model-osi/ 6 Capa de presentación Leer 1 capa 7 y pasar a Documents el HTML capa 6 apuntar todo en obsidian Día 6 10/8/2026 17:40 empiezo a estudiar OSI: [Documents]$ openssl s_client -connect google.com:443 openssl: command not found [Documents]$ openssl version which openssl Modifico el atajo para incluir ashell-mini El 1 comando no funciona así que voy a la web https://www.cloudflare.com/es-es/learning/ddos/glossary/open-systems-interconnection-model-osi/ para aprender capa 7 y 6 el objetivo del día es la 6 el primero más concretamente tls SSL formatos crifrados Me pongo a ello Osi modelo conceptual creado por organizacion estandarización permite sistemas conecten estándar da estándar para conectar lenguaje universal para conexion divide sistema en 7 capas 7 app láyer: Human-computer interaction layer, where applications can access the network services 6 presentation layer:Ensures that data is in a usable format and is where data encryption occurs 5 sesión layer:Maintains connections and is responsible for controlling ports and sessions 4 transport layer:Transmits data using transmission protocols including TCP/UDP 3 network layer:Decides which physical path the data will take 2 data link layer:Defines the format of data on the network 1 physical layer:Transmits raw bit stream over the physical medium
	7.	Capa de aplicación (Application Layer): Capa de interacción entre el usuario y el ordenador, donde las aplicaciones pueden acceder a los servicios de red.
6.Capa de presentación (Presentation Layer): Garantiza que los datos estén en un formato utilizable y es donde se realiza el cifrado de los datos.
5.Capa de sesión (Session Layer): Mantiene las conexiones y se encarga de controlar los puertos y las sesiones.
4.Capa de transporte (Transport Layer): Transmite los datos utilizando protocolos de transmisión, incluidos TCP/UDP.
3.Capa de red (Network Layer): Decide qué ruta física seguirán los datos.
2.Capa de enlace de datos (Data Link Layer): Define el formato de los datos en la red.
1.Capa física (Physical Layer): Transmite el flujo de bits sin procesar a través del medio fisico 7 → Aplicación 6 → Presentación 5 → Sesión 4 → Transporte 3 → Red 2 → Enlace de datos 1 → Física 7-6-5 → Aplicación, datos y sesiones 4 → TCP/UDP 3 → IP/routing 2 → Ethernet/MAC 1 → Señales/cables/Wi-Fi físico Cada osi función comunica capas Los ddos a osi capas específicas https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ Ataques a capa de app https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/ Ataques app capa 7 ataques capa ptrotoclo 3 y 4 Osi desglosar problema e identificar causa Problema-capa-evita trabajo Las 7 capas: 7:app 6:presentación 5:sesión 4:transporte 3:red 2:enlace de datos 1:física 
###### 17:40 10/8/2026 Día 6 OSI:
Hoy 1:12h acumuladas 9:28h
####### 6:47 11/8/2026 día 7 OSI:
traceroute 8.8.8.8 Comand not found en Ashell mini Procedo a investigar cómo arreglarlo: ChatGPT introduzco: traceroute 8.8.8.8 Comand not found Ashell mini Dame el comando para que cualquier comando funcione en Ashell- mini y no de problemas Responde: Con comandos Procedo a arreglarlo Hoy toca la capa 3 y finalizar las 7: #######Capa 7:Aplicacion:

Única interactúa usuario (software) dependen de C7 para iniciar software cliente no C7 C7 protocolos manipulación datos depende datos usuario C7 incluye HTTP-(https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) SMTP-(https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) protocolo correo permite comunicaciones (https://www.cloudflare.com/learning/email-security/what-is-email/) ######Capa 6:Presentación:

Responsable datos usar capa app los preparan consumo apps responsable de traducción cifrado y compresión (https://www.cloudflare.com/learning/ssl/what-is-encryption/) Dos conectados puede usar distintos codificadores responsable traducir entrantes receptor si cifrada responsable cifrado emisor y decodificar receptor para app legible comprime datos de C7 antes enviar a C5 más velocidad/eficiencia comunicación/minimizacion datos transferidos #####Capa 5: Sesión:

Responsable apertura/cierre 2 dispositivos tiempo entre apertura/cierre-sesion garantiza abierta datos cambiando después cierra para no desaprovechar recursos sincroniza datos utilizando control ####Capa 4: Transporte:

Responsable cifrada (extremo a extremo)toma sesión y divide en trozos pequeños (segmentos) responsable rearmar segmentos para construir datos para sesion responsable flujo y errores flujo-velocidad-conexión rápida control errores y garantiza recibidos y si no solicita (https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/) (https://www.cloudflare.com/learning/ddos/glossary/user-datagram-protocol-udp/) ###Capa 3: Red:

Responsable transferencia redes si dispositivos se encuentran en red la capa no necesaria divide segmentos en unidades pequeñas paquetes(https://www.cloudflare.com/learning/network-layer/what-is-a-packet/) los junta en receptor La capa busca la ruta para datos a destino [enrutamiento] (https://www.cloudflare.com/learning/network-layer/what-is-routing/) Protocolos incluyen ip Protocolo control Internet (ICMP), el Protocolo grupo Internet (IGMP) paquete IPsec## ##Capa2:Enlace datos: **** Similar a 3 excepto que capa enlace facilita datos dos de red(misma) la 2 coje paquetes y divide en partes pequeñas (tramas) Responsable control flujo y control errores comunicaciones red (transporte solo control flujo y errores ) # Capa 1: Física :

 Esquioo físico en datos (cables y conmutadores)-(https://www.cloudflare.com/learning/network-layer/what-is-a-network-switch/) Datos en bits 1 y 0 dispositivos estar acuerdo a convención a convención a 1 y 0 (bits) en dispositivos Transmisión en osi: Datos atravesar 7 capas en orden en emisor y receptor # #######7:23 11/8/2026 día 7 OSI: como están sin acabar las 7 capas sigo por encima de capa 3 para acabar 7:53 11/8/2026 descanso 8:31 he editado esta nota en el descanso para asegurar que refleja bien los días 1/2/3 las h de estudio y que lleva orden en todo aparte de que esté documentada 8:32 sigo terminando capa 6 y termino capa 7 Total acumuladas h:hasta ahora 9:46 procedo a marcar conceptos y dias dia 7 empiezo: 6:47 Termino:1204 Horas día 6:51 Acumuladas 16:19h Falta: Terminal para Mac y iPhone sincronizada # ########5:18 12/8/2026 día 8 capa red direccionamiento subnetting ICMP https://www.google.com/search?client=firefox-b-m&q=capa%20red%20direccionamiento%20subnetting%20ICMP%20 Welcome to Alpine!
You can install packages with: apk add 
You may change this message by editing /etc/motd.
localhost:~# traceroute 8.8.8.8 traceroute to 8.8.8.8 (8.8.8.8), 30 hops max, 46 byte packets 1traceroute: sendto: Socket is connected localhost:~# localhost:~# arp -a arp: can't open '/proc/net/arp': No such file or directory localhost:~# localhost:~# tcpdump -i any -c 10 -n -ash: tcpdump: not found localhost:~# Capa 3 Red (IP / Direccionamiento / Subnetting / ICMP) Capa 3: se encarga del direccionamiento lógico y del enrutamiento de paquetes de datos a través de diferentes redes interconectadas usa protocolos ip icmp para mover dirección de origen a destino Protocolo IP: Dirección lógica identifica únicamente cada dispositivo en una red IPv4 e IPv6 versiones en uso v4 32 y v6 128 (bits) Encapsulamiento: añade info origen/destino a paquete Direccionamiento/Subnetting: Red/host:ip dividida entre red y equipo Máscara de su red:que parte de ip es de red y cuál de host Subnetting:divide red en redes para mejorar rendimiento y seguridad Protocolo ICMP: Control y errores:informa sobre ellos con mensajes Herramienta Ping: usa ICMP para comprobar conexión con (PC) Herramienta Traceroute:enseña ruta de paquetes en routers 5:54 termino 1 tarea del día localhost:~# arp -a arp: can't open '/proc/net/arp': No such file or directory localhost:~# Capa 1 Física & Capa 2 Enlace (Ethernet / Direcciones MAC / ARP) https://www.google.com/search?client=firefox-b-m&q=Capa%201%20F%C3%ADsica%20%26%20Capa%202%20Enlace%20%28Ethernet%20%2F%20Direcciones%20MAC%20%2F%20ARP%29 Ethernet usa mac para mandar datos a red local Mac fija (estática)ip cambia (dinámica) ARP une ip con Mac para hablar en la red 06:03 Comienzo descanso/Termino descanso 6;07 - 4 minutos de descanso Ethernet/Mac: Ethernet:estándar que conecta (pcs)en red por cable/señañes Mac:viene de fábrica es un código de 48 bits no cambia e identifica el equipo,es una tarjeta que identifica Protocolo ARP: Arp:un PC pregunta quien tiene la ip correcta a la red Respuesta:el PC con esa ip responde con Mac Tabla caché: PC tardan respuestas para no preguntar qué envían localhost:~# tcpdump -i any -c 10 -n -ash: tcpdump: not found localhost:~# https://www.google.com/search?client=firefox-b-m&q=Captura%20y%20An%C3%A1lisis%20de%20Tr%C3%A1fico%20de%20Red%20%28Wireshark%20%26%20Tcpdump Captura y Análisis de Tráfico de Red Wireshark tcpdump: Herramientas para captura/analisis de red tcpdump es capturador en línea de comandos para servidores whireshark es gráfica/ avanzada y examina paquetes se usan juntos para análisis en whireshark Uso tcpdump: Capturar: tcpdump -i eth0 Guardar: tcpdump -i eth0 -w captura.pcap Filtrar puertos: tcpdump -i eth0 port 80 Uso wireshark Seleccionar: elige tarjeta res y pulsar botón Filtros visualización: IP/HTTP … Seguir TCP: clic en paquete y reconstruye la charla completa de sesión 6:55 hago pausa para reparar terminal 7:06 termino de arreglar terminal continuo Total tiempo no estudiado: 15 minutos 7:12 instalo todo a iSH para evitar fallos localhost:~# curl -I https://example.com HTTP/2 200 date: Wed, 12 Aug 2026 05:14:44 GMT content-type: text/html server: cloudflare last-modified: Sat, 08 Aug 2026 02:07:29 GMT allow: GET, HEAD accept-ranges: bytes age: 4946 cf-cache-status: HIT cf-ray: a29cff89dc05f771-MAD
localhost:~# Fundamentos OWASP Top 10 & Pentesting Web https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=AOlV&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnt_medfkAcFtbiCaiablEO6aJQaxg%3A1786511845349&udm=50&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiCgrefq5qWAxVkygIHHUsSJrYQ2J8OegQIDhAE&biw=393&bih=651&dpr=3&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1
https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=3iQq&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnuPZ4nCUp_5sdYQYUWr7jIeSvGShw%3A1786512757600&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiSorbSrpqWAxVG7LsIHaQdF0AQ2J8OegQIDhAE&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1&udm=50&biw=393&bih=651&dpr=3 OWASP:Top 10 guía https://owasp.org/Top10/2021/es/ Recoge 10 riesgos críticos en apps web Pentesting web es simular/descubrir/mitigar vulnerabilidades antes Las graves: organizado en frecuencia/impacto A01:2021-acceso roto: Usuarios van a datos/funciones fuera de permiso A02:2021-Falla criptográfica: Exposición de datos por cifrado/algoritmo A03:2021-Inyección: Datos enviados a intérprete comandos involuntarios A04:2021-Diseño inseguro: Errores/arquitectura/diseño de app que no se arreglan A05:2021-Configuración seguridad incorrecta: Sistemas por defecto servicios/mensajes de error con detalle A06:2021-Componentes: Hackeables que usan librerías/framewroks/software con fallos A07:2021Fallos: identificación/autentificacion Permite fuerza/robo por la gestión de keys (contraseñas) A08:2021-Fallos integridad de software/datos: Código/datos sin ver origen A09:2021-Fallos en registro/supervisión de seguridad: No registrar criticos(eventos)impide detectar ataques A10:2021-Falsificación solicitudes servidor (SSRF): App/web manipulada para hacer peticiones a servidores Metodología de Pentesting Web: 1 Reconocimiento: Recopila información sobre objetivo/activa 2 Escaneo y Análisis: Saber por dónde entrar con herramientas 3 Explotación (Gain Access): Aprovecha vulnerabilidades 4 Post-explotación: Mide impacto de fallo analiza datos comprometidos o escala privilegios. 5 Reporte: Crear informe para desarrollador/ejecutivo/gerencia y dice la solución https://www.google.com/search?q=Fundamentos+OWASP+Top+10+%26+Pentesting+Web&client=firefox-b-m&hs=3iQq&sca_esv=dcd8ef552bf1ab14&sxsrf=APpeQnuPZ4nCUp_5sdYQYUWr7jIeSvGShw%3A1786512757600&fbs=ABfTbFUDadgeu2mn4mYJ8iEZ1GUDYA5WktO3cDixokzCf5xEYfEenJNN_g8p_oGWd2oCAgAwmmPxPzsmC4uzlcuIAIV8ckjQHwv4DlHcviKbiurq8fJ5hKIrSR_c4mV7rQIno1q3hEU4yEAYddydoSlFSI2OagQC7B6KtdXPoGSD_ajZX8vXbAuZcaxG4wmS2KOjpqB0bzUO&aep=1&ntc=1&cs=1&sa=X&ved=2ahUKEwiSorbSrpqWAxVG7LsIHaQdF0AQ2J8OegQIDhAE&mstk=AUtExfC9lTn6DJLAjJ5AaJCpZnEwcpxKYHYoGvT6DAHI9nAzL06cCf9ifz3btJPdssCUejFLUJsbB6xeCQmMot3l9j-IBadZUhvCHLrlbsPMy9Z768K4yrOhrR2J7OvExuGD8p7bVpVTw2CBdPuIzoEr-gg3WR97mWsy45w&csuir=1&udm=50&biw=393&bih=651&dpr=3 Herramientas pentester: Se unan entornos/ herramientas Kali SO para seguridad tiene muchas herramientas Burp Owasp proxis para analizar/modificar/repetir HTTP (entre navegador y servidor) Nmap escáner para abiertos/ejecucion (puertos) Dirsearch/Gobuster para directorios/archivos en servidor OWASP Juice Shop vulnerable para hacking segura 8:18 12/8/2026 acabo de estudiar Empeze a las 5:18 Total h hoy 3h Acumuladas 19:19 h
########7:08 13/8/2026 dia 8 Scripting Bash & Python para Automatización Terminal
localhost:~# python3 -m http.server 8080 -ash: python3: not found localhost:~# https://www.py4e.com/ Python para todos: Materiales https://www.py4e.com/lessons Conferencias https://www.youtube.com/watch?v=UjeNA_JtXME&list=PLlRFEj9H3Oj7Bp8-DfGpfAfDBiblRfl5p&index=1 Libro https://www.py4e.com/book.php También en: coursera https://www.coursera.org/specializations/python Edx https://www.edx.org/bio/charles-severance Freecodecamp https://www.youtube.com/watch?v=8DvywoWv6fI Certificados gratuitos para estudiantes y personal de la universidad de Míchigan https://online.umich.edu/series/python-for-everybody/ Si inicias sesión te unes a un mundo libre curso online con calificaciones asignaciones/foros/insignias por tus esfuerzos se toman en serio la privacidad se puede revisar política para detalles https://www.py4e.com/privacy Todo esto se puede usar https://www.py4e.com/tsugi/cc/ IMS también herramientas IMS la clave/secreto https://www.py4e.com/tsugi/admin/key/index.php el código/diapositivas/contenido está en https://github.com/csev/py4e puedes hacer lo que quieras con el mismo puedes traducir el sitio publicarlo (instrucciones traducción github) https://github.com/csev/py4e/blob/master/TRANSLATION.md la web usa Tsugi http://www.tsugi.org/ para aprender si quieres colaborar http://www.tsugi.org/ https://www.py4e.com/ python3 -m http.server 8080 Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ... Hardening Unix/Linux & Auditoría de Archivos de Log tail -f /var/log/syslog no funciona en ishell Con otros comandos localhost:~# echo "[INFO] Sistema iniciado" > prueba.log tail -f prueba.log INFO] Sistema iniciado localhost:~# python3 -m http.server 8080 Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ... Ishell es solo en inglés [https://www.cisecurity.org/cis-benchmarks/] 8:31 descanso CIS configuraciones para productos son expertos/esfuerzo/consenso mundial ayudan a sistemas contra amenazas Puntos de referencia https://learn.cisecurity.org/benchmarks Nuevo? https://www.cisecurity.org/cis-benchmarks-overview Benchmarks/puntos https://fast.wistia.com/embed/medias/s1abjx9h37/ encuentra lo que buscas tecnología/subcategoria/filtar(jopcional)/CIS/accede a todo esto en la web https://www.cisecurity.org/cis-benchmarks a unos 7 mm del inicio de la web en cuadro azul Construye kits https://www.cisecurity.org/cis-securesuite/cis-securesuite-build-kit-content descarga referencias v2.0.0 https://learn.cisecurity.org/benchmarks A fondo https://www.cisecurity.org/benchmark/alibaba_cloud Adaptar https://www.cisecurity.org/cis-securesuite CIS Benchmarks https://www.cisecurity.org/cis-benchmarks Arista Networks https://www.cisecurity.org/benchmark/arista_networks Azure Linux https://www.cisecurity.org/benchmark/azure_linux BIND https://www.cisecurity.org/benchmark/bind Bottlerocket https://www.cisecurity.org/benchmark/bottlerocket Check Point Firewall https://www.cisecurity.org/benchmark/checkpoint_firewall Cisco https://www.cisecurity.org/benchmark/cisco CockroachDB https://www.cisecurity.org/benchmark/cockroachdb Debian Linux https://www.cisecurity.org/benchmark/debian_linux DigitalOcean https://www.cisecurity.org/benchmark/digitalocean DISA STIG https://www.cisecurity.org/benchmark/stig_bm Docker https://www.cisecurity.org/benchmark/docker Everpure https://www.cisecurity.org/benchmark/everpure Extreme Networks https://www.cisecurity.org/benchmark/extreme_networks F5 https://www.cisecurity.org/benchmark/f5 Fortinet https://www.cisecurity.org/benchmark/fortinet FreeBSD https://www.cisecurity.org/benchmark/freebsd Google Android https://www.cisecurity.org/benchmark/google_android Google Chrome https://www.cisecurity.org/benchmark/google_chrome Google ChromeOS https://www.cisecurity.org/benchmark/google_chromeos Google Cloud Computing Platform https://www.cisecurity.org/benchmark/google_cloud_computing_platform Google Workspace https://www.cisecurity.org/benchmark/google_workspace HPE Aruba Networking https://www.cisecurity.org/benchmark/hpe_aruba_networking IBM AIX https://www.cisecurity.org/benchmark/ibm_aix IBM Cloud Foundations https://www.cisecurity.org/benchmark/ibm_cloud_foundations IBM Db2 https://www.cisecurity.org/benchmark/ibm_db2 IBM i https://www.cisecurity.org/benchmark/ibm_i IBM WebSphere https://www.cisecurity.org/benchmark/ibm_websphere IBM Z System https://www.cisecurity.org/benchmark/ibm_z_system Juniper https://www.cisecurity.org/benchmark/juniper Kubernetes https://www.cisecurity.org/benchmark/kubernetes Linux Mint https://www.cisecurity.org/benchmark/linux_mint LXD https://www.cisecurity.org/benchmark/lxd MariaDB https://www.cisecurity.org/benchmark/mariadb Microsoft 365 https://www.cisecurity.org/benchmark/microsoft_365 Microsoft Azure https://www.cisecurity.org/benchmark/azure Microsoft Dynamics 365 Power Platform https://www.cisecurity.org/benchmark/dynamics_365_power_platform Microsoft Exchange Server https://www.cisecurity.org/benchmark/exchange_server Microsoft IIS https://www.cisecurity.org/benchmark/iis Microsoft Intune Apple iOS, iPadOS, macOS https://www.cisecurity.org/benchmark/intune_apple Microsoft Intune for Microsoft Windows https://www.cisecurity.org/benchmark/intune_windows Microsoft Office https://www.cisecurity.org/benchmark/microsoft_office Microsoft SharePoint https://www.cisecurity.org/benchmark/sharepoint Microsoft SQL Server https://www.cisecurity.org/benchmark/sql_server Microsoft Web Browser https://www.cisecurity.org/benchmark/microsoft_web_browser Microsoft Windows Desktop https://www.cisecurity.org/benchmark/windows_desktop Microsoft Windows Server https://www.cisecurity.org/benchmark/windows_server MongoDB https://www.cisecurity.org/benchmark/mongodb Mozilla Firefox https://www.cisecurity.org/benchmark/mozilla_firefox NGINX https://www.cisecurity.org/benchmark/nginx OceanBase https://www.cisecurity.org/benchmark/oceanbase OPNsense https://www.cisecurity.org/benchmark/opnsense Oracle Cloud Infrastructure https://www.cisecurity.org/benchmark/oracle_cloud Oracle Database https://www.cisecurity.org/benchmark/oracle_database Oracle Linux https://www.cisecurity.org/benchmark/oracle_linux Oracle MySQL https://www.cisecurity.org/benchmark/oracle_mysql Oracle Solaris https://www.cisecurity.org/benchmark/oracle_solaris Palo Alto Networks https://www.cisecurity.org/benchmark/palo_alto_networks pfSense Firewall https://www.cisecurity.org/benchmark/pfsense PostgreSQL https://www.cisecurity.org/benchmark/postgresql Red Hat Enterprise Linux https://www.cisecurity.org/benchmark/red_hat_enterprise_linux Robot Operating System (ROS) https://www.cisecurity.org/benchmark/ros Rocky Linux https://www.cisecurity.org/benchmark/rocky_linux Safari Browser https://www.cisecurity.org/benchmark/safari SingleStore https://www.cisecurity.org/benchmark/singlestore Snowflake https://www.cisecurity.org/benchmark/snowflake Software Supply Chain Security https://www.cisecurity.org/benchmark/software_supply_chain_security Sophos https://www.cisecurity.org/benchmark/sophos SUSE Linux Enterprise Server https://www.cisecurity.org/benchmark/suse_linux Talos Linux https://www.cisecurity.org/benchmark/talos_linux Tencent Cloud https://www.cisecurity.org/benchmark/tencent_cloud Ubuntu Linux https://www.cisecurity.org/benchmark/ubuntu_linux Visual Studio https://www.cisecurity.org/benchmark/visual_studio VMware https://www.cisecurity.org/benchmark/vmware Wind River Linux https://www.cisecurity.org/benchmark/wind_river_linux YugabyteDB https://www.cisecurity.org/benchmark/yugabytedb 9:11 termino estudiar Total h hoy 1:56 minutos Acumuladas 21:15h a dia 8 Creado nuevo HTML Que funciona en Mac y iPhone Vale para todo Creado con Gemini 11:08 actualizados foto y nombre en RRSS Procedo a colgar apuntes de Obsidian
Parte 2
 # #########06:04 14/82026 día 9 Capa 6: Presentación & Capa 7: Aplicación Welcome to Alpine! You can install packages with: apk add  You may change this message by editing /etc/motd. localhost:~# curl -Iv https://cloudflare.com
	•	Trying 104.16.132.229:443...
	•	Failed to set TCP_KEEPIDLE on fd 5
	•	Failed to set TCP_KEEPINTVL on fd 5
	•	Connected to cloudflare.com (104.16.132.229) port 443 (#0)
	•	ALPN: offers h2,http/1.1
	•	TLSv1.3 (OUT), TLS handshake, Client hello (1):
	•	CAfile: /etc/ssl/certs/ca-certificates.crt
	•	CApath: none
	•	TLSv1.3 (IN), TLS handshake, Server hello (2):
	•	TLSv1.3 (IN), TLS handshake, Encrypted Extensions (8):
	•	TLSv1.3 (IN), TLS handshake, Certificate (11):
	•	TLSv1.3 (IN), TLS handshake, CERT verify (15):
	•	TLSv1.3 (IN), TLS handshake, Finished (20):
	•	TLSv1.3 (OUT), TLS change cipher, Change cipher spec (1):
	•	TLSv1.3 (OUT), TLS handshake, Finished (20):
	•	SSL connection using TLSv1.3 / TLS_AES_256_GCM_SHA384
	•	ALPN: server accepted h2
	•	Server certificate:
	•	subject: CN=cloudflare.com
	•	start date: Jul 8 21:47:39 2026 GMT
	•	expire date: Oct 6 22:47:27 2026 GMT
	•	subjectAltName: host "cloudflare.com" matched cert's "cloudflare.com"
	•	issuer: C=US; O=Google Trust Services; CN=WE1
	•	SSL certificate verify ok.
	•	using HTTP/2
	•	h2h3 [:method: HEAD]
	•	h2h3 [:path: /]
	•	h2h3 [:scheme: https]
	•	h2h3 [:authority: cloudflare.com]
	•	h2h3 [user-agent: curl/8.0.1]
	•	h2h3 [accept: /]
	•	Using Stream ID: 1 (easy handle 0xf7b52170)HEAD / HTTP/2 Host: cloudflare.com Ataques Ddos https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/ Van a la capa de app de internet para parar el flujo web/servicio Que es? https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/ Los de C7 son un tipo de mal comportamiento que apunta a la capa superior de OSI https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/ Donde solicitudes https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/ son efectivas por consumo de recursos aparte de red https://www.cloudflare.com/learning/ddos/dns-amplification-ddos-attack/https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/ Cómo funcionan? La efectividad de los Ddos viene de la cantidad de recursos El consumo de recursos entre cliente/servidor Los datos son mínimos El servidor que recibe solicitud de cliente debe realizar consultas de BBDD o API para producir web Cuando disparidad magnifica el resultado es dispositivos apuntando a una sola propiedad como ataque https://www.cloudflare.com/learning/ddos/what-is-a-ddos-botnet/(Ddos) El servicio colapsa y provoca Ddos https://www.cloudflare.com/learning/ddos/glossary/denial-of-service/ El tráfico en casos ataca API con C7 para dejarlo fuera del sistema Por qué es difícil detenerlos? Difícil distinguir ataque/normal (trafico) sobre todo en capas de apps (como bot et para ataque)https://www.cloudflare.com/learning/ddos/http-flood-ddos-attack/ Contra servidor victima cada bot realiza solicitudes de red el tráfico no se falsifica https://www.cloudflare.com/learning/ddos/glossary/ip-spoofing/ y parece normal Requieren estrategia con capacidad de límite de tráfico según reglas Varían 07:01 Ahora procedo a terminar lo que dejé ayer incompleto lo dejo en https://www.cloudflare.com/learning/ddos/application-layer-ddos-attack/ Sección como funcionan y dentro de ella en varían Y sigo por donde lo dejé ayer Lo dejo en referencias de macOS de ayer Horas hoy 1:18 Acumuladas 22:33h Día 9 8:40 actualizado Día siguiente solo estudiar 
##########7:39 16/8/2026 Día 10 Fundamentos de Redes / TCP-IP
https://www.google.com/search?client=firefox-b-m&q=Fundamentos%20de%20Redes%20%2F%20TCP-IP#lfId=ChxjMe Conjunto de reglas que se usan para internet Divide envío en 4 Las 4 Capa de app la más cercana a la persona que la usa Donde viven apps ( web correo …) Nombres fáciles ( webs) Capa de transporte Controla viaje datos Usa TCP para no errores/llege bien Usa UDP para rapidez (videos llamadas) Capa de red/ internet Pone dirección a cada dato Usa ip para destino Capa de acceso a la red/enlace Maneja conexión Pasa datos por cable/wifi/fibra Conceptos clave IP número único que identifica aparato en red Paquetes datos grandes se hacen pequeños(paquetes) viajan mejor y se juntan al llegar Reglas/Protocolos acuerdos de las máquinas para entenderse siempre Protocolos/puertos de TCP/IP https://www.youtube.com/watch?v=WSMcAY-Lmjc Análisis de Tráfico en Wireshark Whireshark es libre Captura y ve datos de red Ayurda fallos revisa seguridad y entiende a equipos Empieza a usarla https://www.wireshark.org/ Para tráfico Elige red abre app y selecciona tu tarjeta Capturar datos pulsa botón y graba datos Filtrar la vista usa filtros HTTP/dns/ip.addr/ para ver Revisar capas clickea paquete y ve sus detalles divididos Fundamentos de captura/analisis de paquetes https://www.youtube.com/watch?v=I7zlZ1bQuQQ Consejos La captura poco tiempo abierta Filtros claros Ahorra tiempo con nombres de protocolos Cuidado con privacidad no compartas Escaneo de Puertos con Nmap Fundamentos de Redes y Protocolos (TCP/IP, DNS, HTTP)[PENDIENTE] https://www.google.com/search?client=firefox-b-m&q=Fundamentos%20de%20Redes%20y%20Protocolos%20%28TCP%2FIP%2C%20DNS%2C%20HTTP%29%0A%5BPENDIENTE%5D#lfId=ChxjMe Son reglas que hacen que aparatos hablen entre sí TCP/IP envía datos ordenados DNS cambia nombres por IP HTTP mueve entre servidor/navegador TCP/IP IP da dirección a aparato para red TCP parte mensajes ( en paquetes) los cuida y junta (al final) Conexión segura crea ruta antes de datos para no pérdidas DNS Traductor cambia nombres(Google)a IP Directorios usa servidores mundiales para encontrar dirección(rapido) Caché guarda respuestas(del pasado) en el pc/aparato para abrir con velocidad HTTP Base es peticiones y respuestas pides/devuelve Métodos principales GET lee datos POST envía datos Códigos avisan (200 si todo ok 404 si web no está …) Linux Essentials y Administración de Terminal https://www.google.com/search?q=Linux+Essentials+y+Administraci%C3%B3n+de+Terminal&client=firefox-b-m&hs=3a7&sca_esv=4a7eb2b0844aa6f7&sxsrf=APpeQnstkALvVXd5mRRmbZF-qbmA6V2WnA%3A1786867245972&ei=LW6Bavr9OsCoi-gP58PfwAw&biw=393&bih=651&oq=Linux+Essentials+y+Administraci%C3%B3n+de+Terminal&gs_lp=EhNtb2JpbGUtZ3dzLXdpei1zZXJwIi5MaW51eCBFc3NlbnRpYWxzIHkgQWRtaW5pc3RyYWNpw7NuIGRlIFRlcm1pbmFsMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSPYOUABYAHACeAGQAQCYAQCgAQCqAQC4AQPIAQCYAgKgAhKYAwCIBgGQBgiSBwEyoAcAsgcAuAcAwgcHMC4xLjAuMcgHC4AIAQ&sclient=mobile-gws-wiz-serp#lfId=ChxjMe Abarca fundamentos de S.O.(Libre) uso de comandos gestion de archivos permisos de seguridad y administración de usuarios/procesos Es punto avalado por organizaciones Linux Professional Institute Conceptos claves Filosofía libre/open source Entender/software libre/licencias/estructura( ubuntu debían fedora) Estructura directorios Familiaridad con arbol de directorios /etc / var / home / bin …etc Usuarios y grupos Creación de usuarios y control de privilegios Comandos básicos pwd directorio actual ls archivos/carpetas en directorio cd cambia de directorio cp/mv copian mueven renombran archivos o carpetas rm elimina ficheros o directorios mkdir/touch crean directorios (nuevos)o archivos (vacíos) Administración Permisos de archivos de lectura/escritura/ejecucion chmod chown Gestión de procesos visualizar/controlar tareas ps top kill Redes y paquetes Ver interfaces de red con ip gestión/instalación de apps por paquetes apt dnf video introductorio https://www.youtube.com/watch?v=EOONp491bis 10:34 16:8:2026 día 10 Hoy 3:55h Acumuladas 26:28 h
###########6:02 17/8/2026 dia 11 Criptografía/Seguridad
Welcome to Alpine!
You can install packages with: apk add 
You may change this message by editing /etc/motd.
localhost:~# apk add openssl fetch http://apk.ish.app/v3.14-2023-05-19/community/x86/APKINDEX.tar.gz (1/1) Installing openssl (1.1.1t-r2) Executing busybox-1.33.1-r8.trigger OK: 240 MiB in 77 packages localhost:~# openssl enc -aes-256-cbc -salt -in fi le.txt -out file.enc Can't open file.txt for reading, No such file or directory 4160736388:error:02001002:system library:fopen:No such file or directory:crypto/bio/bss_file.c:69:fopen('file.txt','rb') 4160736388:error:2006D080:BIO routines:BIO_new_file:no such file:crypto/bio/bss_file.c:76: localhost:~# [https://www.openssl.org/ Misión todos deben tener herramientas de seguridad/privacidad, quien de donde sea O si/no tiene credenciales, son derecho fundamental. La misión https://openssl-mission.org/ Biblioteca OpenSSL https://openssl-library.org/ Castillo de Boyncy https://www.bouncycastle.org/ Cryplib https://cryptlib.com/ OpenSSL.org Biblioteca Misión Comunidades Corporación Fundación Proyectos Conferencia Nmap y Shodan localhost:~# nmap -A -T4 <target_ip> -ash: syntax error: unexpected newline localhost:~# [https://www.shodan.io/] 6:44 dentro de shodan 6:46 descanso para tomar algo 6:52 elimino ashel-mini del atajo y de las apps ejecutándose solo con ishell me vale dejo ishell El atajo es así Abrir archivos app Abrir spotify Abrir reloj Abrir notas de voz Abrir notas Abrir Obsidian Abrir Chrome Abrir opera Abrir firefox Abrir Safari Abrir Documents Abrir iSH 6:55 sigo con mi descanso Shodan es motor de búsqueda de dispositivos conectados a Internet es excelente para encontrar webs Si quieres medir los países más conectados /saber V Microsoft más popular/encontrar servidores que controlan malware/vulnerabilidad/hosts posiblemente afectados los buscadores no responden a esas preguntas Coge info de todos los dispositivos conectados a internet Shodan consulta para obtener info disponible públicamente Los dispositivos indexados varían de pequeños a enormes( de PC a centrales nucleares) Índice de shodan la mayoría de datos se cogen de banners metadatos sobre software ejecutándose en un dispositivo puede ser info sobre software de servidor/opciones admitidas/mensaje de bienvenida/… que cliente desea saber antes del usar servidor Ejemplo banner ftp 220 kcg.cz FTP server (Version 6.00LS) ready. Dice nombre de servidor tipo version Para HTTP el banner es HTTP/1.0 200 OK Date: Tue, 16 Feb 2010 10:03:04 GMT Server: Apache/1.3.26 (Unix) AuthMySQL/2.20 PHP/4.1.2 mod_gzip/1.3.19.1a mod_ssl/2.8.9 OpenSSL/0.9.6g Last-Modified: Wed, 01 Jul 1998 08:51:04 GMT ETag: "135074-61-3599f878" Accept-Ranges: bytes Content-Length: 97 Content-Type: text/html La info se aplica a áreas Seguridad de red vigila todo lo conectado a internet Investigación mercado descubre productos usados reales Riesgo cibernético incluye exposición de proveedores como métrica de riesgo IOT sigue usando dispositivos inteligentes Seguimiento ramsomware mide dispositivos afectados (cuántos) 7:24 17/8/2026 Termino de Estudiar 1:10:28 hms hoy Acumuladas 27:38 h Para mañana terminaré shodan y empezaré nmap
###########6:47 18/8/2026 Día 11 terminar shodan y empezar nmap
localhost:~# nmap -A -T4 192.168.1.62 Starting Nmap 7.91 ( https://nmap.org ) at 2026-08-18 04:55 UTC NSE: failed to initialize the script engine: could not locate nse_main.lua stack traceback:[C]: in ? QUITTING! localhost:~# https://help.shodan.io/the-basics/what-is-shodan Seguimiento de ramsomware cuantos dispositivos afectados Casos de uso variados Shodan garantiza info precisa/consistente/actualizada en aparatos conectados a internet Cada uno decide su interés Shodan vs google El 1 rastrea internet y el 2 www Internet es una red mundial que conecta dispositivos y permite intercambiar datos. www es (World Wide Web): sistema de páginas y recursos que funciona sobre Internet, accesible mediante navegadores. Aún así la www es una pequeña porción de lo conectado Objetivo shodan dar imagen entera de internet Diferencia es que shodan explora internet y Google wwww Aun así www es una pequeña parte de lo conectado Objetivo shodan 3 líneas arriba A diferencia de Google shodan necesita que entiendas sintaxis de consulta búsqueda ejemplo no se puede entrar en planta de energía y esperar resultados Shodan para ingenieros/desarrolladores para máximo provecho de datos Otra diferencia es que shodan necesita que comprendas sintaxis de consulta de búsqueda ejemplo no se puede ingresar a planta de energía y esperar resultados Nmap localhost:~# nmap connect 192.168.1.62 Starting Nmap 7.91 ( https://nmap.org ) at 2026-08-18 05:42 UTC Failed to resolve "connect". route_dst_netlink: cannot create AF_NETLINK socket: Invalid argument https://nmap.org/ Rediseñado compatible con móviles También en https://npcap.com/ https://seclists.org/ https://insecure.org/ https://sectools.org/ Nmap V7.90 lanzado con Npcap V1.0.0 junto a mejoras de rendimiento/corrección de errores/mejora de funciones lanzamiento https://seclists.org/nmap-announce/2020/1 Descargas https://nmap.org/download.html H estudio hoy 1:09 Acumuladas 28:47 h
############13:39 19/8/2026 Día 12
Continuo con Nmap por donde lo dejé Que es Nmap descargas Después de más de 7 años de desarrollo 170 prelanzamientos anunciamos la V1.00 de npcap anuncio de lanzamiento https://seclists.org/nmap-announce/2020/0 Descarga https://nmap.org/npcap/ Lanzado Nmap 7.80 para Defcom 27 notas de la versión https://seclists.org/nmap-announce/2019/0 descarga https://nmap.org/download.html Nmap cumple 20 años en 2017 celébralo https://nmap.org/p51-11.html #Nmap20 https://twitter.com/hashtag/Nmap20 V7.50 disponible (Nmap) notas https://seclists.org/nmap-announce/2017/3 descarga https://nmap.org/download.html Nuevo proyecto icons of the web https://nmap.org/favicon/ collage interactivo de 5 gigapixeles de sitios más importantes de internet Nmap usado en 2 películas para hackear el cerebro de Matt Damon en Elyseum https://nmap.org/movies/#elysium y para lanzar misiles nucleares en GIJOE:Represalia https://nmap.org/movies/#gijoe Nmap V6.40 con 14 nuevos scripts NSE https://nmap.org/book/vscan.html firmas https://nmap.org/book/vscan.html SO https://nmap.org/book/osdetect.html y Versiones https://nmap.org/book/vscan.html Continua con las Versiones hacia abajo y continúa… Los que no vieron Defcon pueden ver Fyodor y David Fifield demostrando poder de Nmap https://nmap.org/presentations/BHDC10/ explore los favicons https://nmap.org/favicon Guía oficial de Nmap https://nmap.org/book/ Nmap es gratis y de código abierto https://nmap.org/npsl/ para auditar/descubrir redes de seguridad Muchos lo encuentran útil para el inventario de red/gestión de horarios/actualización de servicio/seguimiento de actividad en host o servicio utiliza paquetes ip sin procesar novedosamente para saber hosts disponibles en red servicios(nombre y versión) están en hosts que SO y V del SO Tipos de filtros/paquetes/cortafuegos están en uso y más cosas Diseñado para escanear rápidamente grandes redes funciona contra hosts se ejecuta en todos los SO paquetes disponibles para Linux Windows y macOS Trae interfaz gráfica avanzada y visor https://nmap.org/zenmap/ herramienta flexible de datos dirección/depuracion https://nmap.org/ncat/ utilidad para comparar resultados https://nmap.org/ndiff/ Herramienta de generación de paquetes/analisis de respuesta https://nmap.org/nping/ Sirve para descubrir redes y auditorías de seguridad útil para inventario de red/gestión de horarios de actualización de servicio/seguimiento tiempo de actividad del host o servicio Usa paquetes ip sin procesar novedosamente para saber hosts disponibles en red qué servicios están dando con Nombre y versión ofrecen hosts que SO están ejecutando filtros/paquetes/firewall en uso y más También contra hosts individuales se ejecuta en todos los SO Windows Linux Mac incluye interfaz gráfica de usuario avanzada y visor de resultados (Zenmap)flexible para transferencia de datos redireccion y depuración NCAT compara resultados de escaneo Ndiff genera paquetes y análisis de respuesta (Nping) Nmap es: Flexible https://nmap.org/book/man-port-scanning-techniques.html https://nmap.org/book/osdetect.htmlhttps://nmap.org/book/vscan.html https://nmap.org/docs.html Potente Portátil Fácil Gratis https://nmap.org/download.html https://nmap.org/data/COPYING Bien documentado https://nmap.org/docs.html Compatible https://nmap.org/#lists https://seclists.org/nmap-dev https://nmap.org/book/man-bugs.htmlhttps://seclists.org/nmap-hackers http://facebook.com/nmap http://twitter.com/nmap http://freenode.net/http://www.efnet.org/ Aclamado https://nmap.org/nmap_inthenews.html Popular 14:46 termino Horas hoy 1:05 Acumuladas 29:52h
############ 6:56 20/8/2026 Dia 13 Hacking Web &
OWASP Top 10 localhost:~# https://owasp.org/Top10/2021/es/ -ash: https://owasp.org/Top10/2021/es/: not found https://cleanuri.com/E6ke4Y Hacking Web disciplina de ciberseguridad que busca identificar explorar y mitigar fallos en webs la comunidad la usa como referencia principal el Owasp top 10 es una lista de 10 riesgos https://owasp.org/Top10/2021/es/ 10 vulnerabilidades críticas de Owasp 10 A01 control de acceso roto Que es falla Ataque cambiar URL (id123 por id124)para ver perfiles ajenos (idor) H hoy 21:30 mins Acumuladas h totales 30:13:30 h
#############5:51 21/8/2026 Día 14
Hacking Web & OWASP Top 10 continuo https://cleanuri.com/E6ke4Y …A01 prevención basta con implementar políticas de denegación por defecto y verificaciones de permisos (petición) A02 Fallos criptográficos Qué es exposición/proteccion deficiente de datos Ataque cojer HTTP sin cifrar o contraseñas con MD5(función criptográfica de hash que transforma cualquier cantidad de datos en un valor fijo de 128 bits, normalmente representado como una cadena hexadecimal de 32 caracteres) Prevención cifrar todo usando algoritmos fuertes AES (sistema de cifrado que convierte tus datos en información ilegible para protegerlos de personas no autorizadas) A03 inyección Que es envío no confiable de datos a un intérprete que ejecuta como comandos inesperados también SQL(lenguaje que permite consultar, modificar y organizar datos almacenados en bases de datos) SQLi (es una técnica de ataque que introduce código SQL malicioso en una aplicación para manipular o acceder a datos de su base de datos) y XSS(vulnerabilidad que permite inyectar código JavaScript malicioso en una página web para que se ejecute en el navegador de otros usuarios) Ataque código sql en formulario de login para evitar autenticación Prevención usar consultas parametricas (dependen de uno o varios parámetros o valores que pueden cambiar) A04 Diseño inseguro Qué es defectos en la arquitectura del programa antes del código Ataque diseño de flujo que recupera contraseña y permite adivinar preguntas de seguridad sin límites de tiempo Prevención identificar posibles ataques desde el principio y diseñar el programa con medidas de seguridad para evitarlos A05 Configuración incorrecta de seguridad Que es falta de endurecimiento en servidores o apps web XML(formato de texto que organiza y almacena datos usando etiquetas para que diferentes sistemas puedan entenderlos) XXE(vulnerabilidad en la que un atacante manipula un archivo XML para conseguir que el servidor acceda o revele información que debería estar protegida) Ataque acceso a consolas admin con contraseñas (sin cambiar ) o leer mensajes de error detallados que revelan BBDD Prevención quitar funciones innecesarias y auditar configuración de servidores(automática) A06 Componentes vulnerables y obsoletos Que es uso de cosas antiguas que tienen fallos públicos conocidos Ataque tomar control del servidor aprovechando lo del punto amterior Prevención usar herramientas de análisis (composición de software) y actualizar parches A07 Fallos de identificación y autenticación Que es debilidades para validar identidad Ataque fuerza bruta para contraseñas débiles por falta de bloqueo Prevención contraseñas complejas y 2FA(autenticación de doble factor) A08 Fallos de integridad de software y datos Que es código/infraestructura que no protegen contra manipulaciones Ataque modificar objeto en serie de las cookies de navegador para subir privilegios a admin Prevención firmar archivos verificar artefactos A09 Fallos de registro y monitorización de seguridad Qué es no poder detectar/alertar/registrar actividades sospechosas en el momento Ataque alguien vulnera sistema durante un tiempo sin que nadie sospeche Prevención centralizar logs de server establecer sistemas automáticos de respuesta ante incidentes A10 Falsificación de solicitudes del lado del servidor Que es fallo cuando app web procesa URL remota Ataque obligar al server web a realizar peticiones HTTP hacia su red interna para ver puertos ocultos Prevención crear listas blancas de permitidos e ignorar lo demás 7:01 termino Horas hoy 1:05 Acumuladas 31:18 h
############## 6:47 24/8/2026 Día 15 Entornos Virtuales y Laboratorios (UTM / Linux)
localhost:~# uname -a && cat /etc/os-release Linux localhost 4.20.69-ish SUPER AWESOME May 20 2023 23:41:32 i686 Linux NAME="Alpine Linux" ID=alpine VERSION_ID=3.14.3 PRETTY_NAME="Alpine Linux v3.14" HOME_URL="https://alpinelinux.org/" BUG_REPORT_URL="https://bugs.alpinelinux.org/" localhost:~# https://docs.getutm.app/ Utm emulador de sistema con todas las funciones y host de MV(iOS y Mac OS) Páginas ordenadas de más a menos importante se recomienda usar páginas para aprender a usar UTM en la documentación hay: Macos indica que la próxima sección o frase aplica solo a UTM en macOS iOS igual que macOS Wip indica secciones que no han cambiado y deben hacerlo Desobrecado secciones que refieren a características que pueden eliminarse en actualización futura y no deben usarse. Linux https://cleanuri.com/80lQ48 es un SO abierto y gratis el núcleo se llama kernel controla hardware y permite que funcionen las apps administra computadoras servicios web móviles y supercomputadoras Análisis de Tráfico y Captura de Paquetes https://www.tcpdump.org/ Tcdump potente analizador de paquetes en línea de comandos y libpcap biblioteca portátil C/C++ para captura tráfico red 7:19 termino H hoy 29:33 mins Acumuladas total 31:47 h
############### 14:45 25/8/2026 Día 16
Certificado Cisco — Introduction to Cybersecurity https://www.netacad.com/courses/introduction-to-cybersecurity Introducción a la ciberseguridad explora este mundo y mira por qué está preparado para el Es gratis 6h 7 labs desde principiante a ritmo propio recibe insignias por logros aprenderás privacidad confidencialidad de datos ciberseguridad vulnerabilidades de red las mejores prácticas cibernéticas a detectar amenazas Procedo a registrarme 15:00 ya registrado y en web https://www.netacad.com/es/courses/introduction-to-cybersecurity?courseLang=es-XL Web del certificado para mañana H hoy 22:16 minutos Acumuladas total 32:09:16 h Certificado Cisco — Networking Basics https://www.netacad.com/courses/networking-basics?courseLang=es-XL Networking Basics introduce los fundamentos de las redes informáticas y explica cómo funcionan las redes. Es gratis, online y a ritmo propio. Certificado Cisco — Networking Basics https://www.netacad.com/courses/networking-basics?courseLang=es-XL Networking Basics introduce los fundamentos de las redes informáticas y explica cómo funcionan las redes. Es gratis, online y a ritmo propio. 22 h 13 labs Nivel principiante Aprenderás fundamentos de redes, dispositivos de red, medios de transmisión, protocolos, direccionamiento y funcionamiento de las redes. También trabajarás con conceptos prácticos para configurar y comprender redes pequeñas. Procedo a registrarme Web del certificado para mañana https://www.netacad.com/courses/networking-basics?courseLang=es-XL Certificado Fortinet — NSE 1: Cybersecurity https://training.fortinet.com/ NSE 1: Cybersecurity introduce los fundamentos de la ciberseguridad y el panorama actual de amenazas. Es gratis, online y a ritmo propio. Aprenderás amenazas actuales, actores maliciosos, tipos de ataques, fundamentos de ciberseguridad y buenas prácticas de seguridad. Certificado Fortinet — NSE 1: Cybersecurity https://training.fortinet.com/ NSE 1: Cybersecurity introduce los fundamentos de la ciberseguridad y el panorama actual de amenazas. Es gratis, online y a ritmo propio. Aprenderás amenazas actuales, actores maliciosos, tipos de ataques, fundamentos de ciberseguridad y buenas prácticas de seguridad. Para conseguir la certificación: Completar el curso online y realizar el test. Procedo a registrarme Web del certificado para mañana https://training.fortinet.com/ Certificado Fortinet — NSE 2: Cybersecurity https://training.fortinet.com/ NSE 2: Cybersecurity introduce los fundamentos de los Next Generation Firewalls (NGFW). Es gratis, online y a ritmo propio. Aprenderás qué son los firewalls de nueva generación, sus características principales y cómo ayudan a proteger las redes. Curso: Introduction to Next Generation Firewall Para conseguir la certificación: Completar el curso online y realizar el test.Procedo a registrarme Web del certificado para mañana https://training.fortinet.com/ Certificado Fortinet — NSE 3: FortiGate Operator https://training.fortinet.com/ NSE 3: FortiGate Operator introduce la operación de los dispositivos FortiGate. Es online y a ritmo propio. Aprenderás las funciones principales de FortiGate, operaciones básicas, configuración y gestión de dispositivos de seguridad Fortinet. Para conseguir la certificación: Completar el curso FortiGate Operator y superar el examen NSE 3. Procedo a registrarme Web del certificado para mañana https://training.fortinet.com/ Certificado IBM — Cybersecurity Fundamentals https://www.ibm.com/training/badge/cybersecurity-fundamentals Cybersecurity Fundamentals proporciona una introducción a los conceptos fundamentales de ciberseguridad. Es online y gratuito. Aprenderás: Ciberataques Criptografía Estrategias de seguridad Amenazas Buenas prácticas Fundamentos de ciberseguridad Casos prácticos Duración aproximada: 6 h Procedo a registrarme Web del certificado para mañana https://www.ibm.com/training/badge/cybersecurity-fundamental
################10:16 26/8/2926 día 17
Certificado 1 introducción a la ciberseguridad de Cisco https://www.netacad.com/courses/introduction-to-cybersecurity empiezo el certificado y si lo termino hoy bien si no mañana o otro dia Hecho hoy 18:05 mins Acumuladas total 32:05 h Deje el certificado sin terminar después de la batería de preguntas se cuelga la web o safari y la abriré en Firefox o otro navegador ya probado en Firefox funcional de momento También modifiqué el HTML de estudio para que tenga mandelbrots y otras animaciones y sonidos y editado este documento para que refleje certeza/verdad ahora desde el HTML tengo total control de lo que veo en el HTML dejo el certificado en punto 1.1.3 Actualización H hoy 28:05 mins Acumuladas 32:15 h
################## Día 18 dedicados 7:47 minutos 3:45 am
05:09 27/8/2026 día 18 continuo con el certificado introducción a la ciberseguridad de cisco Acumuladas h 32:22 h 16:38 vuelvo al certificado Lo dejo en el 1.2 a más 16:48 Acumuladas h 32:32 h A ver si termino el certificado 
################### 11:30 28/82026 día 19 sigo con el 1 certificado la parte 1.2
Lo dejo en 1.2.6 a las 11:45 H hoy 14:50 mins Acumuladas 32:46 h 12:50 me quedo en 1.5 H hoy 29:89 mins Acumuladas 33:01 h
####################9:47 29/8/2026 Día 20 introducción a la ciberseguridad de cisco
me quedo en 2.2.3 https://www.netacad.com/courses/introduction-to-cybersecurity H hoy 18:08 mins Acumuladas 33:19 h 21:53 me quedo en el 2.2.6 He estado 6 mins Total acumuladas 33:25 h
##################### 6:33 30/8/2026 Día 21 continuo con el 1 certificado investigación de seguridad https://bugs.chromium.org/p/project-zero/issues/list?can=1&redir=1
Lo dejo en el 3.1 H hoy 39 mins Acumuladas h 34:04 
#####################11:23 31/8/2026 Día 22 sigo con el certificado
Ma quedo en 3.1.9 H hoy 22 mins Acumuladas 34:26 h 17:03 sigo estudiando donde lo dejé 17:14 lo dejo en 3.4 Acumuladas 34:40h 21:03 empiezo a estudiar otra tanda Lo dejo en 5.1.1 he estudiado 36 mins Acumuladas 35:16 h 12:07 1/9/2026 Día 23 sigo con el 1 certificado 12:52 suspendo el examen varias veces y me tomo un descanso 12:54 empiezo a hacerlo otra vez 13:01 he estado 38 minutos y rondo el 40/50 % de el 70 que pide el examen solución descansar e intentarlo por la tarde Acumuladas h 35:54h 13:35 he estado 5 minutos más y no paso del umbral del 40/50% Acumuladas 35:59 h Como no pasó del 40/50% de aprobar después de la siesta 5 minutos por vídeo Módulo 1 — Introducción a la ciberseguridad https://www.youtube.com/watch?v=1S0vshMFCrM  Módulo 2 — Ataques, conceptos y técnicas https://www.youtube.com/watch?v=c5nleVufrbI Módulo 3 — Protegiendo sus datos y su privacidad https://www.youtube.com/watch?v=Krzxuq2F0cA Módulo 4 — Protegiendo a la organización https://www.youtube.com/watch?v=sNu8mOJATPE Módulo 5 — Tu futuro en ciberseguridad [https://www.youtube.com/watch?v=uaNv9KtIE7Q] https://www.youtube.com/watch?v=uaNv9KtIE7Q Orden para después de la siesta: 1 → 2 → 3 → 4 → 5 → examen.


7:13 2/9/2026 dia 24 voy por el 5 vídeo y voy a por el Examen del 1 certificado hoy no mido tiempo pues la prioridad es aprobar 8:31 introducción a la ciberseguridad aprobado con 80% Guardado en Documents y archivos Total h hoy 1:18h Acumuladas 37:17 h Compro Cnpen y me formaré hasta poder hacerlo HTML modificado para cubrir con éxito Cnpen ahora muestra cuando migrar a recurso o pestaña con acceso directo

16:20 4/9/2026 Día 25 CNpen TCP/IP + red en profundidad: diferenciar claramente ARP, ICMP, TCP/UDP, DNS y HTTP y diagnosticar una comunicación con captura localhost:~# ip addr && ip route && ss -tulpn ip: socket(AF_NETLINK,3,0): Invalid argument localhost:~# Enlaces CNPEN # 🔐 CNPen — Enlaces
1. CNPen — Página oficial
https://secops.group/
2. Exam Portal — Acceso al examen
https://candidate.speedexam.net/
3. Recuperación de contraseña
https://candidate.speedexam.net/forgotpassword.aspx?site=thesecopsgroup https://www.rfc-editor.org/ Rfc solicitud de comentario documentos que describen estándares de internet especificaciones técnicas, protocolos, procedimientos, investigación y otra información relacionada con Internet y sistemas conectados a Internet El 1 Rfc en 1969 por steve crocker para organizar notas relacionadas con el desarrollo de ARPANET allanó camino para internet moderno los posteriores establecieron muchos de los fundamentos técnicos de Internet ahora todo el mundo desarrolla Rfc para documentar trabajo técnico, compartir información y estandarizar tecnologías de Internet No todos son estándar de internet pueden tener diferentes estados y pueden ser publicados a través de varias corrientes Entender esto junto con las relaciones entre ellos ayuda a determinar qué representa en particular y cómo leerlo una vez publicado el contenido no cambia si es necesario cambiar algo se publica uno nuevo (Rfc) relaciones entre RFC, incluidas actualizaciones y obsoleciones, se registran en los metadatos de RFC también se pueden presentar los errores encontrados después de publicarlo Participar en creación de Rfc https://www.ietf.org/participate/get-started/ También puedes unirte al grupo de trabajo https://datatracker.ietf.org/wg/ Como leer Rfc utilizan terminología/convenciones que pueden no ser familiares para todos antes de confiar mejor observar metadatos y documento verificar estado flujo si es obsoleto o actualizado y si se han reportado errores RFC STREAMS La corriente de RFC identifica proceso a través del cual se produjo el documento. Hay cinco flujos de RFC:
	•	El Grupo de Trabajo de Ingeniería de Internet(IETF) produce normas de protocolo, mejores prácticas actuales y documentos informativos. Esta es la única corriente que crea estándares de Internet.
	•	El Grupo de Trabajo de Investigación en Internet (IRTF) se centra en cuestiones de investigación a largo plazo relacionadas con Internet.
	•	El tablero de arquitectura de Internet (IAB) proporciona una dirección técnica de largo alcance para el desarrollo de Internet.
	•	Presentaciones Independientes Los RFC se publican fuera de los procesos oficiales de la IETF, IAB e IRTF, pero son relevantes para la comunidad de Internet.
	•	Editorial Los RFC son producidos por el Grupo de Trabajo de la Serie RFC (RSWG) y documentar las políticas de publicación de los RFC. Los RFC que se publicaron antes de que existiera cualquier flujo se etiquetan como "Corriente de legado" en lugar de un nombre de flujo. EStado RFC Dice que tipo de documento es no asume algo estándar de internet por que haya sido publicado como Rfc El estado cambia con el tiempo https://www.rfc-editor.org/status-changes/ Los Rfc estándares usan los siguientes estados Estándar propuesto. especificación de Estándar Propuesto es generalmente estable, resuelto opciones de diseño conocidas, se cree es bien entendida, ha recibido revisión significativa de comunidad y parece disfrutar de interés de la comunidad para ser valioso. Sin embargo, la experiencia adicional podría dar como resultado un cambio o la retracción de la especificación antes de que avance. Proyecto de norma. etapa intermedia que ya no se utiliza para nuevos estándares. Estándar de Internet. se caracteriza por alto grado de madurez técnica y por creencia generalmente sostenida de que protocolo o servicio especificado proporciona beneficio significativo a la comunidad de Internet. Otros estados de RFC son: Informativo. especificación "informativa" para información general de comunidad de Internet, no representa consenso o recomendación de comunidad de Internet. RFC 2026, Sección 4.2.2 Experimental. denota una especificación parte de esfuerzo de investigación o desarrollo. Se publica para información general de comunidad técnica Internet y como registro de archivo de obra. RFC 2026, Sección 4.2.1 Históricodescribe una tecnología que ya no está en uso o ya no se recomienda para su uso se le asigna el estado "histórico". Mejores Prácticas Actuales (BCP). Los BCP tienen doble rol: uno documentar los procesos de IETF según acordado por la comunidad de la IETF, y el otro se explica en RFC 2026, Sección 5 "ya que Internet está compuesto por redes operadas gran variedad de organizaciones, con diversos objetivos reglas, un buen servicio al usuario requiere que los operadores y administradores de Internet sigan pautas comunes para las políticas y operaciones". Desconocido. Los RFC que se publicaron antes de que se introdujeran los estados (antes de RFC 1128) se considera tienen un estado desconocido, y un puñado se aplicó los estados retroactivamente. Subserie Rfc ETF Y BCP me quedo aquí en https://www.rfc-editor.org/series/rfc/ H hoy 43 mins Acumuladas h 38h 

17:33 5/9/2026 Día 26 continuo con Rfc Subserie Rfc:std y bcp A algunos Rfc se les asignan idénticadores en una Subserie de Rfc son o STD(Estándar de Internet) y BCP (Mejor Práctica Actual) No todos pertenecen a Subserie identificador de subserie da forma estable de identificar estándar de Internet o práctica de actualidad recomendada, incluso cuando RFC que la definen cambian. Cuando un RFC en subserie está obsoleto, puede reemplazarse por un RFC más nuevo mientras el identificador STD o BCP sigue siendo el mismo.
	•	identificadores STD se asignan a los estándares de Internet. Una ETS (Equipo de Trabajo de Seguridad) puede consistir en un RFC o un grupo RFC juntos especifican protocolo/tecnología en particular.
	•	identificadores BCP se asignan a mejores prácticas actuales. Un BCP puede consistir un RFC o grupo RFC que describen proceso IETF (organización de estándares de Internet) particular o conjunto de pautas recomendadas. significa que (un número de) STD o BCP y un número RFC sirven para cosas distintas:número RFC identifica permanentemente un documento publicado mientras que identificador STD o BCP puede continuar identificando estándar o práctica a medida que cambian sus RFC definitivos Relaciones y cambios de RFC RFC forman gran cuerpo de documentos relacionados, y las especificaciones a menudo se desarrollan con el tiempo. Debido a texto de un RFC publicado nunca cambia, las revisiones/reemplazos se publican como nuevos RFC. Es posible que vea las relaciones:
	•	Actualizaciones:Este RFC realiza cambios sustanciales en los RFC enumerados aquí posible que deba leer esas RFC junto con esta para entender la especificación completa.
	•	Actualizado por:Este RFC modificado sustancialmente por los RFC enumerados aquí. posible que debe leer RFC más recientes para entender la especificación/práctica actual.
	•	Obsoletos:RFC que reemplaza a los RFC enumerados aquí. Los RFC más antiguos siguen siendo parte de archivo permanente de la serie RFC, pero este RFC generalmente debe usarse para comprender la especificación o práctica actual.
	•	Obsoleto por:Este RFC ha sido reemplazado por los RFC enumerados aquí. Para entender la especificación o práctica actual, generalmente debe leer las RFC que la obsoleto. Cuando está tratando de determinar la especificación actual para un protocolo o tecnología, verificar estas relaciones es una parte importante de la lectura de un RFC.
Errata
Los errores descubiertos después de que se publica un RFC se manejan a través del proceso de errata de la serie RFC en lugar de cambiar el RFC publicado.
Cuando un RFC ha reportado erratas, se enumeran en la sección Errata de la barra lateral en la página del RFC. Errata con un estado verificado ha sido revisado y se ha determinado que es preciso. Consulte la página RFC Errata para obtener más información sobre el proceso.
Las erratas no se incorporan a las versiones TXT, PDF o XML de una RFC. Aparecen en la versión de visualización en este sitio y en la versión HTML descargable que incluye específicamente erratas.
Si está utilizando un RFC para implementar un protocolo o necesita información técnica precisa, es una buena idea comprobar si hay errata verificada 18:05 h hoy 27 mins me queda parte por resumir Acumuladas 38h 27 mins

18:03 6/9/2026 Día 27 resumo lo que queda de Rfc y lo termino total h hoy 7 minutos Acumuladas 38:34 h

8:00 7/9/2026 Día 28 Fundamentos de redes y TCP/ip localhost:~# ip addr && ip route && ss -tuln ip: socket(AF_NETLINK,3,0): Invalid argument https://www.wireshark.org/docs/ Wireshark manual de usuario https://www.wireshark.org/download/docs/wsug_html.zip Manual de línea de comandos https://www.wireshark.org/docs/man-pages/ Filtro de pantalla https://www.wireshark.org/docs/dfref/ Notas de lanzamiento https://www.wireshark.org/docs/relnotes/ Avisos de seguridad https://www.wireshark.org/security/ Documentación del desarrollador https://www.wireshark.org/download/docs/wsdg_html.zip TCP ip y Rfc localhost:~# curl -I https://www.google.es HTTP/2 200 content-type: text/html; charset=ISO-8859-1 content-security-policy-report-only: object-src 'none';base-uri 'self';script-src 'nonce-azepEjTEPHynRL7Ookydww' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp accept-ch: Sec-CH-Prefers-Color-Scheme p3p: CP="This is not a P3P policy! See g.co/p3phelp for more info." date: Mon, 07 Sep 2026 06:15:19 GMT server: gws x-xss-protection: 0 x-frame-options: SAMEORIGIN expires: Mon, 07 Sep 2026 06:15:19 GMT cache-control: private set-cookie: AEC=AdJVEatGND5O3X8JeHq4UyhQfiEUqXKlyn95tKgy-crM7yaXdjfbe4tg; expires=Sat, 06-Mar-2027 06:15:19 GMT; path=/; domain=.google.es; Secure; HttpOnly; SameSite=lax set-cookie: Secure-ENID=36.SE=AKL8jmnoe71EcF-sNwuYZDwd2M9UVmBJ_nTesGvcmAalznj7CUoUsFrureFR9RHErP_pGpMyqRgPO_tyIl8-6PcZdOKrkKXQrw--gnrs9ef-4S6P3wE9_sO6VJCu-fwrS35ffxAZgwJQ7l-Pf47oXPje5ICjVP-6sJi5Wl_BAOaqDsW2frADT6WGyDtuXZ2YG7BwcI9WiISsz0xsvksTgpUd-twza-gMPmRbqHpPHaLsmZxKNC6OQrMs; expires=Thu, 07-Oct-2027 22:33:37 GMT; path=/; domain=.google.es; Secure; HttpOnly; SameSite=lax alt-svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000 Guía de usuario de wireshark https://www.wireshark.org/docs/wsug_html_chunked/ 1.1. ¿Qué es Wireshark? Wireshark es analizador paquetes red. presenta los datos de paquetes capturados con mayor detalle posible. Wireshark es gratuito es de código abierto de los mejores analizadores de paquetes 1.1.1. propósitos previstos/razones de uso: administradores red usan solucionar problemas red ingenieros seguridad red usan examinar los problemas seguridad ingenieros control calidad usan verificar aplicaciones de red desarrolladores usan depurar implementaciones protocolo Los demás (gente) usa para aprender protocolos de red Wireshark puede ser útil 1.1.2. CARACTERÍSTICAS que ofrece Disponible UNIX/Windows. Captura datos de paquetes de red. Abra archivos con datos de paquetes capturados con tcpdump/WinDump/Wireshark y otros programas captura paquetes. Importar archivos de texto con volcados hexadecales de datos de paquetes. Mostrar paquetes con info de protocolo detallada. Guardar datos capturados. Exporte paquetes en varios formatos de archivo Filtra paquetes según muchos criterios. Busca paquetes en muchos criterios. Colorea en función de los filtros. Crea estadísticas y más cosas Para ver su poder úsalo 1.1.3. Captura vivo desde varios medios de red diferentes puede capturar tráfico de varios tipos medios red, tambien Ethernet, LAN inalámbrica, Bluetooth, USB etc. Los específicos medios admitidos pueden estar limitados por factores, hardware/sistema operativo etc Puede encontrar una descripción general de los tipos de medios compatibles en [https://wiki.wireshark.org/CaptureSetup/NetworkMedia] 1.1.4. Importar archivos de otros programas puede abrir capturas de paquetes desde gran número de apps de captura. Para una lista de formatos de entrada, consulte la sección 5.2.2, "Formatos de archivo de entrada". 1.1.5. Exportar archivos para otros programas puede guardar paquetes en muchos formatos, incluidos usados por otras apps de captura. Para una lista de formatos de salida, consulte la sección 5.3.2, "Formatos de archivo de salida". 1.1.6. disectores de protocolo Hay disectores de protocolo (o decodificadores) para gran cantidad de protocolos: consulte la sección B.5.3, "Carpeta temporal de Windows". 1.1.7. de código abierto proyecto de código abierto, se publica bajo la GNU (GPL). Puede usarlo en cualquier número de ordenadores que desee, sin preocuparse por claves de licencia o tarifas etc .todo el código fuente está disponible gratuitamente bajo la GPLPor ello es muy fácil para personas agregar protocolos ya sean complementos/integrados en la fuente 1.1.8. Lo que no es Wireshark no proporciona:
	•	no es sistema de detección de intrusiones Sin embargo, si pasan cosas extrañas, podría ayudarte a saber que pasa
	•	no manipulará cosas en red, solo "mide” cosas de red. no envía paquetes/ni otras cosas activas (excepto resolución nombre de dominio,eso se puede desactivar). Descarga de wireshark https://www.wireshark.org/download.html
	3.	Requisitos del sistema Los que necesita depende del entorno y del tamaño del archivo de captura analizandose |Nota(https://www.wireshark.org/docs/wsug_html_chunked/images/note.svg)|Las redes ocupadas significan grandes capturas| |Una red ocupada produce archivos de captura grandes. Capturar en una red de 100 megabits pudiese producir cientos de megabytes de datos/captura Un PC con procesador rápido mucha memoria y espacio en disco siempre es una buena idea. Si Wireshark se queda sin memoria, se bloqueará. [https://wiki.wireshark.org/KnownBugs/OutOfMemory]para detalles y soluciones. Aunque utiliza un proceso separado para capturar el análisis es de un solo hilo y no se beneficiará mucho de los sistemas multinúcleo. 1.3.1. Microsoft Windows debe admitir cualquier versión del SO que aún esté dentro de su vida útil (https://windows.microsoft.com/en-us/windows/lifecycle). En el momento de escribir esto incluye Windows 11, 10, Server 2022, Server 2019 y Server 2016. También requiere lo siguiente:
	•	tiempo de ejecución de Universal C. incluido en Windows 10/Windows Server 2019 se instala automáticamente en V anteriores si Windows Update está habilitado. De lo contrario, debe instalar KB2999226 o KB3118401.
	•	Cualquier procesador moderno de 64 bits Intel/arm
	•	500 MB de RAM 
	•	500 MB de espacio en disco 
	•	Se recomienda resolución de 1280 × 1024 o superior.hará uso deHiDPI o Retina si están disponibles. Los usuarios avanzados encontrarán útiles varios monitores.
	•	Una tarjeta de red compatible para capturar
	•	Ethernet. (https://wiki.wireshark.org/CaptureSetup/Ethernet) y descarga de Ethernet para ver los problemas que pueden afectar a su entorno.
	•	802.11. (https://wiki.wireshark.org/CaptureSetup/WLAN#Windows). Capturar información sin procesar de 802.11 puede ser difícil sin un equipo especial.
	•	Otros medios. Consulte [https://wiki.wireshark.org/CaptureSetup/NetworkMedia] V anteriores de Windows fuera de soporte no son compatibles. 
	•	Wireshark 4.6 fue la última rama de lanzamiento en admitir oficialmente Windows 10, versión 1809 y Windows Server 2019. Consulte la sección el ciclo de vida de wireshark (https://www.wireshark.org/docs/wsug_html_chunked/ChIntroReleaseLifeCycle.html 1.3.2. macOS compatible con macOS 11 y versiones posteriores. las versiones compatibles de macOS dependen de bibliotecas de terceros y de los requisitos de Apple.
	•	Wireshark 4.4 fue la última rama de lanzamiento compatible con macOS 11. Consulte la sección del ciclo de vida de la versión de Wireshark
1.3.3. UNIX, Linux y BSD
se ejecuta en la mayoría de los SO UNIX y similares a UNIX, Linux y BSD. Los requisitos del sistema deben ser comparables a las especificaciones enumeradas anteriormente para Windows. Los paquetes binarios están disponibles para la mayoría de las distribuciones de Unices y Linux, incluidas las siguientes plataformas:
	•	Linux Alpine
	•	Arch Linux
	•	Ubuntu canónico
	•	Debian GNU/Linux
	•	BSD gratis
	•	Gentoo Linux
	•	HP-UX
	•	NetBSD
	•	OpenPKG
	•	Oracle Solaris
	•	Red Hat Enterprise Linux / CentOS / Fedora Si un paquete binario no está disponible para su plataforma, puede descargar la fuente e intentar construirla. Por favor, informe de sus experiencias a wireshark-dev[AT]wireshark.org. 10:17 paro por hoy H hoy 1:32 h Acumuladas 40:06 h

11:30 8/9/2026 Día 29 Empiezo la nueva sección programación 1 ejecutar phyton3 Print para imprimir en pantalla print (“hola mundo”) hola mundo Guardar texto como variable nombre = 'David' localhost:~# phyton3 -ash: phyton3: not found localhost:~# python3 Python 3.9.16 (main, Dec 10 2022, 13:47:19) [GCC 10.3.1 20210424] on linux Type "help", "copyright", "credits" or "license" for more information.
print ("hola mundo") hola mundo nombre=david Traceback (most recent call last): File "", line 1, in  NameError: name 'david' is not defined nombre='david' exit Use exit() or Ctrl-D (i.e. EOF) to exit exit() localhost:~# Ahora comando localhost:~# curl -I https://google.es HTTP/2 301 location: https://www.google.es/ content-type: text/html; charset=UTF-8 content-security-policy-report-only: object-src 'none';base-uri 'self';script-src 'nonce-dxcYmyGrC75M-x7jiZ5qtQ' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp date: Tue, 08 Sep 2026 09:49:05 GMT expires: Thu, 08 Oct 2026 09:49:05 GMT cache-control: public, max-age=2592000 server: gws content-length: 219 x-xss-protection: 0 x-frame-options: SAMEORIGIN alt-svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000 localhost:~# https://www.rfc-editor.org/ El hogar oficial de las RFC ¿Qué es un RFC?
Últimas RFC
	•	RFC 10042: Intercambio de claves híbridas post-cuántica/tradicional con el mecanismo de encapsulación de claves basado en la celosía del módulo para su uso en SSH INFORMACIONAL
	•	RFC 10038: Distribución del enrutamiento de segmentos a través del localizador IPv6 (SRv6) usando DHCPv6 ESTÁNDAR PROPUESTO
	•	RFC 10037: Extensión del Protocolo de Acceso a Datos de Registro (RDAP) para valores de tiempo de vida (TTL) de DNS ESTÁNDAR PROPUESTO
Más información sobre las RFC
	•	¿Qué es un RFC? Una introducción a las RFC, las organizaciones que las producen y las convenciones comunes en la serie
	•	Errata en RFC Comprender errores y correcciones en las RFC
	•	Acerca del editor de RFC El editor de RFC publica y archiva las RFC oficiales
Examinar RFC
	•	Estándares Protocolos y servicios estables o maduros
	•	Mejores prácticas actuales Directrices comunes para políticas, operaciones o procedimientos
	•	Descargar RFC Descargue, refleje u obtenga un feed de RFC
	•	Examinar todas las RFC
Empieza a participar
	•	[Grupo de Trabajo de Ingeniería de Internet](https://www.ietf.org/ Normas de protocolo, mejores prácticas actuales, documentos experimentales e informativos
	•	Grupo de trabajo de investigación en Internet Cuestiones de investigación relacionadas con Internet
	•	[Junta de Arquitectura de Internet](https://www.iab.org/ Dirección técnica a largo plazo para el desarrollo de Internet
	•	Envíos independientes Cómo funciona el flujo de envío independiente. https://www.wireshark.org/docs/wsug_html_chunked/ Total h hoy 27 mins Acumuladas h 40:33h

15:54 9/9/2026 Día 30 Programación localhost:~# python3 Python 3.9.16 (main, Dec 10 2022, 13:47:19) [GCC 10.3.1 20210424] on linux Type "help", "copyright", "credits" or "license" for more information.
edad = 38 tcpdump -i any -c 20 -n tcpdump: socket: Invalid argument Total h hoy 14 mins Acumuladas 40:47 h

11:53 11/9/2026 Día 31 programación enteros edad = 38 localhost:~# python3 Python 3.9.16 (main, Dec 10 2022, 13:47:19) [GCC 10.3.1 20210424] on linux Type "help", "copyright", "credits" or "license" for more information.
edad = 38 https://translate.google.com/translate?sl=en&tl=es&u=https://www.wireshark.org/docs/wsug_html/ 6 mins Acumuladas 40:53h

11:19 14/9/2026 Día 32 Wireshark/Tcdump localhost:~# tcpdump -i any -c 20 -n tcpdump: socket: Invalid argument localhost:~# https://www.wireshark.org/docs/wsug_html/ Instalación de Wireshark en macOS https://www.wireshark.org/download.html IMG_5601.png Menú para acciones Barra de herramientas principal da acceso a cosas de uso frecuente La barra de herramientas de filtro permite seleccionar que paquetes muestra El panel de la lista de paquetes resumen de cada paquete capturado El panel de detalles del paquete muestra paquete seleccionado en el panel de la lista El panel de bytes del paquete muestra datos de paquete seleccionado en el panel lista… Panel de diagrama de paquetes muestra diagrama del paquete seleccionado en lista La barra de estado muestra info actual sobre la app y datos capturados Guardar paquetes capturados archivo guardar o archivo guardar como No todo se guarda como los paquetes caídos Wireshark — Resumen de estudio
	1.	Capturar paquetes ¿Qué es? Capturar paquetes consiste en registrar los datos que circulan por una red. Cada paquete contiene información sobre una comunicación, como su origen, destino y protocolo. Qué tengo que aprender
	•	☐ Abrir Wireshark y elegir la interfaz de red correcta (Wi-Fi o Ethernet).
	•	☐ Iniciar una captura de paquetes.
	•	☐ Identificar paquetes TCP, UDP, DNS, HTTP y HTTPS.
	•	☐ Reconocer la IP de origen y la IP de destino.
	•	☐ Saber qué puerto utiliza cada comunicación.
	•	☐ Detener y guardar una captura. Ejemplo Si visitas una página web, Wireshark puede mostrar comunicaciones entre tu ordenador y los servidores de esa página. Objetivo: aprender a ver qué ocurre en una red y reconocer los diferentes tipos de tráfico
	1.	Analizar credenciale ¿Qué es? Analizar credenciales consiste en estudiar cómo se transmiten los datos de autenticación, como usuarios y contraseñas, dentro de una comunicación de red. Qué tengo que aprender
	•	☐ Entender qué son las credenciales: usuario, contraseña, tokens y cookies.
	•	☐ Diferenciar HTTP de HTTPS.
	•	☐ Saber por qué HTTP sin cifrar puede exponer información sensible.
	•	☐ Reconocer métodos de autenticación como Basic Auth.
	•	☐ Utilizar filtros para localizar tráfico HTTP.
	•	☐ Usar Follow → TCP Stream para reconstruir una comunicación.
	•	☐ Entender por qué HTTPS protege el contenido frente a la captura de tráfico. Ejemplo educativo En una red de laboratorio propia, puedes capturar una comunicación HTTP de prueba y comprobar si los datos de autenticación viajan sin cifrar. Importante: no captures ni intentes obtener contraseñas de otras personas. Utiliza siempre tráfico propio o un laboratorio autorizado. Diferencia entre los dos puntos | | | |---|---| |Punto|Qué aprendo| |1. Capturar paquetes|Ver y registrar el tráfico de una red.| |2. Analizar credenciales|Comprender cómo se transmiten y protegen los datos de inicio de sesión.| Orden recomendado
	1.	Aprender a capturar paquetes.
	2.	Reconocer los protocolos de red.
	3.	Estudiar el análisis de autenticación.
	4.	Practicar en un laboratorio controlado Meta final: saber capturar y analizar tráfico de red con Wireshark, entendiendo qué información es visible y cómo el cifrado protege las comunicaciones. H hoy 25.31 mins Acumuladas 41:18 h
#################################6:30 15/9/2026 Día 33 Nmap manual
localhost:~# nmap -sV -sC 192.168.1.62 Starting Nmap 7.91 ( https://nmap.org ) at 2026-09-15 04:32 UTC NSE: failed to initialize the script engine: could not locate nse_main.lua stack traceback: [C]: in ? QUITTING! localhost:~# https://nmap.org/book/ https://nmap.org/book/host-discovery.html Cap 3 descubrimiento del host El primer paso es reducir todo a unas pocas ip en una lista de host él escaneo ea lento e innecesario los admin de red están interesados en host que lleve un servicio. Mientras que los auditores pueden preocuparse por una ip. El admin está cómodo solo con Ping ICMP(Protocolo de Mensajes de Control de Internet) para encontrar host en red interna. Nmap ofrece amplia variedad de opciones se puede omitir el paso del ping con escaneo de lista -sL o desactivado el Ping -Pn o TCP SYN/ACK, UDP e ICMP multipuerto. Syn: significa Synchronize (sincronizar). Es una bandera (flag) del protocolo TCP que se utiliza para iniciar una conexión entre dos dispositivos. En Nmap, SYN es especialmente importante porque permite descubrir puertos abiertos sin completar una conexión TCP normal. Ack: significa Acknowledgment (confirmación o reconocimiento). Es una bandera (flag) del protocolo TCP que indica que se ha recibido correctamente un paquete o que se confirma un número de secuencia Todo esto es usado para demostrar que una ip está activa(usada por host o dispositivo) En ocasiones solo pequeño porcentaje direcciones IP son activas en un momento dado
Nmap — Host Discovery + Parsing NSE Output
1. Host Discovery
Host Discovery significa descubrimiento de hosts. Es el proceso de identificar qué dispositivos están activos en una red antes de escanear sus puertos. Nmap envía sondas a las direcciones IP y analiza las respuestas.
Comando principal
nmap -sn 192.168.1.0/24
	•	-sn: descubrimiento de hosts, sin escanear puertos.
	•	192.168.1.0/24: rango de IPs de la red.
Descubrir un host
nmap -sn 192.168.1.1
Tipos de sondas
ICMP Echo
nmap -PE 192.168.1.1
Envía una petición ICMP Echo.
TCP SYN
nmap -PS80 192.168.1.1
Envía una sonda TCP SYN al puerto 80.
TCP ACK
nmap -PA80 192.168.1.1
Envía una sonda TCP ACK al puerto 80.
UDP
nmap -PU53 192.168.1.1
Envía una sonda UDP al puerto 53.
ARP
nmap -PR 192.168.1.0/24
Realiza descubrimiento ARP en redes Ethernet.
Omitir Host Discovery
nmap -Pn 192.168.1.1
Omite el descubrimiento y trata el host como activo.
Conceptos importantes
	•	ICMP: protocolo de control de red. Puede utilizarse para comprobar conectividad.
	•	SYN: bandera TCP utilizada para iniciar una conexión.
	•	ACK: bandera TCP utilizada para confirmar la recepción.
	•	ARP: protocolo utilizado para resolver direcciones IP a direcciones MAC en redes locales.
	•	Firewall: puede bloquear las sondas y hacer que un equipo activo parezca no responder.

2. NSE — Nmap Scripting Engine
NSE significa Nmap Scripting Engine. Permite ejecutar scripts que amplían las capacidades de Nmap. Los scripts pueden recopilar información de servicios, detectar configuraciones y realizar comprobaciones de seguridad autorizadas.
Ejecutar scripts por defecto
nmap -sV --script default 192.168.1.1
	•	-sV: detección de versiones de servicios.
	•	--script default: ejecuta los scripts de la categoría default.
Ayuda de scripts
nmap --script-help default
Muestra información sobre la categoría de scripts.
Ayuda de un script concreto
nmap --script-help http-title
Muestra la ayuda del script http-title.
Ejecutar http-title
nmap -sV --script http-title 192.168.1.1
Obtiene información sobre el título de una página web HTTP si el servicio está disponible.
Ejecutar scripts HTTP
nmap --script "http-*" 192.168.1.1
Ejecuta scripts cuyo nombre coincide con http-*. Utilízalo solo en sistemas autorizados.
3. Parsing NSE Output
Parsing significa analizar y extraer información de la salida de Nmap y de sus scripts NSE. Ejemplo de salida:
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH
80/tcp open  http    Apache
Datos que podemos extraer
Campo	Ejemplo
Puerto	22
Estado	open
Servicio	ssh
Versión	OpenSSH
Ejemplo de salida NSE
| http-title:
|   Site title: Mi servidor
El parser puede extraer:
http-title → Mi servidor

4. Guardar resultados de Nmap
Salida normal
nmap -sV --script default -oN resultado.txt 192.168.1.1
Guarda la salida normal en resultado.txt.
Salida XML
nmap -sV --script default -oX resultado.xml 192.168.1.1
Guarda la salida en XML, útil para procesarla con programas o scripts.
Salida Grepable
nmap -sV --script default -oG resultado.gnmap 192.168.1.1
Guarda la salida en formato grepable.
5. Parsear XML con Python
Este código extrae las IPs y los estados de los puertos de un XML generado por Nmap.
import xml.etree.ElementTree as ET

tree = ET.parse("resultado.xml")
root = tree.getroot()

for host in root.findall("host"):
    address = host.find("address")
    if address is not None:
        print("IP:", address.get("addr"))

    for port in host.findall("./ports/port"):
        state = port.find("state")
        print(
            port.get("portid"),
            state.get("state") if state is not None else "unknown"
        )

6. Comandos esenciales de Nmap
Host Discovery
nmap -sn 192.168.1.0/24
Escaneo SYN
nmap -sS 192.168.1.1
Escaneo ACK
nmap -sA 192.168.1.1
Detección de servicios
nmap -sV 192.168.1.1
Scripts NSE
nmap --script default 192.168.1.1
Guardar XML
nmap -oX resultado.xml 192.168.1.1
## 7. Estados de puertos
| Estado | Significado |
|---|---|
| `open` | Hay una aplicación escuchando en el puerto. |
| `closed` | El puerto es accesible, pero no hay aplicación escuchando. |
| `filtered` | Un firewall u otro filtro impide determinar el estado. |
| `unfiltered` | El puerto es accesible, pero el escaneo no determina si está abierto o cerrado. |
**Importante:** En un escaneo ACK, `unfiltered` no significa necesariamente que el puerto esté abiert
## 8. Checklist de estudio
### Host Discovery
- [ ] Saber qué es Host Discovery.
- [ ] Dominar `nmap -sn`.
- [ ] Entender ICMP.
- [ ] Entender SYN.
- [ ] Entender ACK.
- [ ] Conocer `-PE`.
- [ ] Conocer `-PS`.
- [ ] Conocer `-PA`.
- [ ] Conocer `-PU`.
- [ ] Conocer `-PR`.
- [ ] Entender `-Pn`.
### NSE y Parsing
- [ ] Saber qué es NSE.
- [ ] Ejecutar scripts con `--script`.
- [ ] Consultar scripts con `--script-help`.
- [ ] Entender `-sV`.
- [ ] Guardar resultados con `-oN`.
- [ ] Guardar resultados con `-oX`.
- [ ] Guardar resultados con `-oG`.
- [ ] Entender qué significa parsear.
- [ ] Extraer IPs y puertos de un XML.
- [ ] Interpretar `open`, `closed`, `filtered` y `unfiltered`.
## Resumen para memorizar
> **Host Discovery:** descubre qué dispositivos están activos.
>
> **NSE:** amplía Nmap con scripts.
>
> **Parsing NSE Output:** extrae y analiza la información que devuelven Nmap y sus scripts.
## Práctica segura
Utiliza estos comandos en tu propia red o en laboratorios autorizados.
H hoy 38 minutos 
Acumuladas h 41:56 h
# #####################################
5:55 18/8/2026 Día 34 Programación HTTP …

-ash: pyrhon3: not found
localhost:~# python3
Python 3.9.16 (main, Dec 10 2022, 13:47:19) 
[GCC 10.3.1 20210424] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> edad = int('38')
>>> 
>>> # Comprobación
>>> print(edad)resultado = 38 + 2
  File "<stdin>", line 1
    print(edad)resultado = 38 + 2
               ^
SyntaxError: invalid syntax
>>> 
>>> # Comprobación
>>> print(resultado)resultado = 38 + 2
  File "<stdin>", line 1
    print(resultado)resultado = 38 + 2
                    ^
SyntaxError: invalid syntax
>>> 
>>> # Comprobación
>>> localhost:~# curl -I https://google.es
HTTP/2 301 
location: https://www.google.es/
content-type: text/html; charset=UTF-8
content-security-policy-report-only: object-src 'none';base-uri 'self';script-src 'nonce-D7uvz_H3rXYVtswROOKWcg' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
date: Fri, 18 Sep 2026 03:59:44 GMT
expires: Sun, 18 Oct 2026 03:59:44 GMT
cache-control: public, max-age=2592000
server: gws
content-length: 219
x-xss-protection: 0
x-frame-options: SAMEORIGIN
alt-svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000
localhost:~# 
https://developer.mozilla.org/es/docs/Web/HTTP
# HTTP — Hypertext Transfer Protocol
![HTTP](https://upload.wikimedia.org/wikipedia/commons/5/5b/HTTP_logo.svg)
## 1. ¿Qué es HTTP?
HTTP (Hypertext Transfer Protocol) es un protocolo de la capa de aplicación utilizado para transmitir documentos hipermedia, como HTML, entre clientes y servidores web.
### Características
- Capa: Aplicación.
- Modelo: Cliente-servidor.
- Funcionamiento: Petición → Respuesta.
- Estado: Sin estado (stateless).
- Transporte habitual: TCP/IP.
- HTTPS: HTTP protegido mediante TLS.
### Modelo cliente-servidor
1. El cliente (navegador) establece una conexión.
2. Realiza una petición HTTP.
3. El servidor procesa la petición.
4. Devuelve una respuesta HTTP.
### Protocolo sin estado
HTTP es stateless: cada petición es independiente. El servidor no conserva automáticamente el estado entre peticiones.
Las cookies y otros mecanismos permiten mantener información entre peticiones.
### Transporte
HTTP se utiliza habitualmente sobre TCP. HTTP/3 utiliza QUIC sobre UDP.
## 2. Flujo HTTP
```mermaid
sequenceDiagram
    participant C as Cliente / Navegador
    participant S as Servidor Web
    C->>S: Petición HTTP
    S->>S: Procesa la petición
    S-->>C: Respuesta HTTP
    C->>C: Renderiza el recurso
3. Generalidades de HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Overview HTTP permite solicitar páginas HTML, imágenes, CSS, JavaScript y otros recursos.
Petición
GET /index.html HTTP/1.1
Host: ejemplo.com
Respuesta
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 1250
4. Cookies HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Cookies RFC 6265: https://datatracker.ietf.org/doc/html/rfc6265 Las cookies son pequeños datos que el servidor puede enviar al navegador y que este devuelve en peticiones posteriores.
	•	Set-Cookie: establece una cookie.
	•	Cookie: envía una cookie.
	•	Expires / Max-Age: duración.
	•	Domain: dominio.
	•	Path: ruta.
	•	Secure: envío mediante HTTPS.
	•	HttpOnly: impide el acceso desde JavaScript.
	•	SameSite: controla el envío entre sitios.
Ejemplo
HTTP/1.1 200 OK
Set-Cookie: session=abc123; Secure; HttpOnly; SameSite=Lax
GET /perfil HTTP/1.1
Host: ejemplo.com
Cookie: session=abc123
5. Caché HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Caching La caché almacena copias de recursos para evitar descargarlos de nuevo. Ventajas:
	•	Reduce el tiempo de carga.
	•	Disminuye el tráfico.
	•	Reduce peticiones al servidor.
Cabeceras
Cabecera	Función
Cache-Control	Reglas de caché
Expires	Fecha de caducidad
ETag	Identificador de versión
Last-Modified	Última modificación
If-None-Match	Validación mediante ETag
If-Modified-Since	Validación por fecha
Ejemplo
GET /style.css HTTP/1.1
Host: ejemplo.com
If-None-Match: "abc123"
HTTP/1.1 304 Not Modified
6. CORS
Cross-Origin Resource Sharing. Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/CORS CORS permite que un servidor indique qué otros orígenes pueden acceder a sus recursos desde un navegador. Un origen está formado por:
	•	Esquema.
	•	Host.
	•	Puerto.
Ejemplo
Origen A:
https://dominioa.ejemplo
Solicita un recurso a:
Origen B:
https://dominiob.foo/imagen.jpg
Cabeceras
Access-Control-Allow-Origin: https://dominioa.ejemplo
Access-Control-Allow-Methods: GET, POST
Access-Control-Allow-Headers: Content-Type
Conceptos:
	•	Same-Origin Policy.
	•	Preflight.
	•	OPTIONS.
	•	Access-Control-Allow-Origin.
	•	Access-Control-Allow-Methods.
	•	Access-Control-Allow-Headers.
7. Sugerencias de cliente HTTP
Documentación: https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Client_hints Las Client Hints son cabeceras que permiten al servidor solicitar información sobre el dispositivo, red y preferencias del cliente para adaptar los recursos enviados.
8. Evolución de HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Evolution_of_HTTP | Versión | Característica | |---|---| | HTTP/0.9 | Peticiones simples | | HTTP/1.0 | Cabeceras y respuestas completas | | HTTP/1.1 | Conexiones persistentes | | HTTP/2 | Multiplexación y mejoras | | HTTP/3 | HTTP sobre QUIC |
9. Mensajes HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Messages
Petición HTTP/1.x
GET /index.html HTTP/1.1
Host: ejemplo.com
User-Agent: Mozilla/5.0
Accept: text/html
Partes:
	1.	Línea de petición.
	2.	Cabeceras.
	3.	Línea vacía.
	4.	Cuerpo opcional.
Respuesta HTTP
HTTP/1.1 200 OK
Content-Type: text/html
<html>
  <body>
    Hola
  </body>
</html>
10. La típica sesión HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Session
flowchart TD
    A["Navegador"] --> B["Resuelve el dominio"]
    B --> C["Conecta con el servidor"]
    C --> D["Envía petición HTTP"]
    D --> E["Servidor procesa"]
    E --> F["Devuelve respuesta HTTP"]
    F --> G["Navegador interpreta"]
11. Gestión de conexiones HTTP/1.x
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Guides/Connection_management_in_HTTP_1.x Conceptos:
	•	Conexiones persistentes.
	•	Reutilización de conexiones TCP.
	•	Cierre de conexiones.
	•	Rendimiento y latencia.
12. Cabeceras HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers Las cabeceras describen el recurso o el comportamiento del cliente y servidor. Ejemplos:
	•	Host.
	•	Content-Type.
	•	Content-Length.
	•	User-Agent.
	•	Cookie.
	•	Authorization.
	•	Cache-Control.
	•	Set-Cookie. Registro IANA: https://www.iana.org/assignments/message-headers/message-headers.xhtml#perm-headers RFC 4229: https://tools.ietf.org/html/rfc4229
13. Métodos HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods | Método | Uso | |---|---| | GET | Obtener un recurso | | POST | Enviar datos | | OPTIONS | Consultar capacidades | | DELETE | Solicitar eliminar | | TRACE | Diagnóstico |
Enlaces específicos
GET: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods/GET POST: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods/POST OPTIONS: https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods/OPTIONS DELETE: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods/DELETE TRACE: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods/TRACE
14. Códigos de estado HTTP
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Status | Código | Significado | |---|---| | 1xx | Informativo | | 2xx | Petición correcta | | 3xx | Redirección | | 4xx | Error del cliente | | 5xx | Error del servidor | Ejemplos:
	•	200 OK: correcto.
	•	201 Created: recurso creado.
	•	301 Moved Permanently: redirección permanente.
	•	302 Found: redirección temporal.
	•	304 Not Modified: utilizar copia en caché.
	•	400 Bad Request: petición incorrecta.
	•	401 Unauthorized: autenticación requerida.
	•	403 Forbidden: acceso denegado.
	•	404 Not Found: recurso no encontrado.
	•	500 Internal Server Error: error del servidor.
15. CSP — Content Security Policy
Documentación: https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers/Content-Security-Policy CSP permite controlar qué recursos puede cargar una página, como scripts, imágenes y estilos.
Ejemplo
Content-Security-Policy: default-src 'self'
16. Herramientas y recursos
Firefox Developer Tools
https://firefox-source-docs.mozilla.org/devtools-user/index.html Herramientas para inspeccionar y depurar páginas web.
Network Monitor
https://firefox-source-docs.mozilla.org/devtools-user/network_monitor/index.html Permite inspeccionar peticiones, respuestas, cabeceras y recursos.
Mozilla Observatory
https://observatory.mozilla.org/ Herramienta para revisar aspectos de seguridad y configuración web.
RedBot
https://redbot.org/ Herramienta para comprobar cabeceras de caché.
Cómo trabajan los navegadores
https://web.dev/howbrowserswork/ Explica el funcionamiento interno de los navegadores y el flujo de peticiones HTTP.
17. Seguridad web de Mozilla
https://infosec.mozilla.org/guidelines/web_security Consejos para desarrollar aplicaciones web seguras.
18. Referencias completas
https://developer.mozilla.org/es/docs/Web/HTTP#referencias https://developer.mozilla.org/es/docs/Web/HTTP#herramientas_y_recursos
19. Checklist de estudio
	•	Entender cliente-servidor.
	•	Comprender stateless.
	•	Estudiar peticiones y respuestas.
	•	Aprender métodos HTTP.
	•	Aprender códigos de estado.
	•	Estudiar cabeceras.
	•	Estudiar cookies.
	•	Estudiar caché.
	•	Comprender CORS.
	•	Comprender CSP.
	•	Practicar con Network Monitor.
	•	Leer la documentación general de HTTP.
20. Comandos de práctica
curl — Petición GET
curl -i https://example.com
Ver solo cabeceras
curl -I https://example.com
Especificar método
curl -X OPTIONS https://example.com
Enviar una cabecera
curl -H "Accept: text/html" https://example.com
Enviar datos POST
curl -X POST -d "usuario=david" https://example.com
Usar únicamente contra sistemas propios o autorizados.
21. Qué debes dominar
	•	Qué es HTTP.
	•	Diferencia entre HTTP y HTTPS.
	•	Qué es una petición.
	•	Qué es una respuesta.
	•	Métodos GET y POST.
	•	Códigos 200, 301, 302, 304, 400, 401, 403, 404 y 500.
	•	Cabeceras.
	•	Cookies.
	•	Caché.
	•	CORS.
	•	CSP.
	•	Network Monitor.
	•	curl. H hoy 16 mins Total acumuladas 42:12h 6:39 Voy a resumir el texto copiado pegado 6:43 hay poco que resumir 9:25 21/9/2026 Dia 35 labs localhost:~# curl -I https://elhacker.net HTTP/2 200 date: Mon, 21 Sep 2026 07:24:57 GMT content-type: text/html; charset=iso-8859-1 x-frame-options: SAMEORIGIN referrer-policy: same-origin feature-policy: geolocation 'self' strict-transport-security: max-age=31536000 x-xss-protection: 1; mode=block server: cloudflare cf-cache-status: DYNAMIC report-to: {"group":"cf-nel","max_age":604800,"endpoints":[{"url":"https://a.nel.cloudflare.com/report/v4?s=j8IwTp%2FD5hOwp5mM7%2Br%2FHzOGlPsccmO7RDUO%2BM%2BuZjyVpB8roMpi0VNxy8vanJ6I2LLjK0PhdZUbZHgDim5y33zlv0fvKgdBAExNk0XSup6awZVfWrMFCQO%2BLSeplg%3D%3D"}]} nel: {"report_to":"cf-nel","success_fraction":0.0,"max_age":604800} expect-ct: max-age=86400, enforce x-content-type-options: nosniff cf-ray: a3e7554d3904e55b-MAD alt-svc: h3=":443"; ma=86400 localhost:~# Lab https://0a7f00b1036ee624838eb6c80058007b.web-security-academy.net/ Total hoy 10 minutos acumuladas 42:22 
###^^^^^^10:04 1/10/2026 Día 36
Empiezo a estudiar para cnpen 17 puntos y programación OSINT es localizar, evaluar y relacionar información disponible públicamente En pentesting, el objetivo convertir datos varios dominios, DNS, tecnologías, nombres o metadatos— en información útil para definir superficie ataque sin interactuar de forma indebida con sistemas. La parte crítica es verificación: fuente pública no es automáticamente correcta. Contrasta datos, registra procedencia y separa hechos comprobados de hipótesis. El resultado esperado es inventario de información útil y trazable. https://tryhackme.com/room/ohsint También se pueden extraer metadatos de fotos de RRSS para obtener info. Que info? Exif tools extrae metadatos se carga el archivo y aparecen los metadatos nombre directorio tiempos permisos lectura escritura … avatar de usuario propietario de la imagen Es importante limpiar metadatos de imágenes y archivos Con todo esto se pueden hacer informes También está la web wigle es para redes de todo tipo incluso de telefonía bluethoot …almacena información no contraseñas usadas más 2 apps para mejores informes (puzzle) En osint cada dato por separado no vale mucho pero todos juntos son el puzzle valen oro se puede localizar con wigle donde “vive” cada wifi wigle hace de todo es una web no un programa Los datos sacados de las apps se usan para informes Usar el extractor de metadatos combinado con Google para contestar al laboratorio de https://tryhackme.com/room/ohsint Buscar la wifi y terminar el lab B4:5D:50:AA:86:41 H hoy 54 mins Acumuladas 43:16h
###^^^^^^^12:00 2/10/2026 Día 37
Terminar el lab y el punto 1 de cnpen del HTML https://tryhackme.com/room/ohsint Buscando en Google el nombre de usuario que da exif tools encontré casi toda la información para contestar solo me falta 1 que es la contraseña la pista dice que está en el código fuente hoy respondí a estas What is the SSID of the WAP he connected to? Correct Answer What is his personal email address? Correct Answer What site did you find his email address on? Correct Answer Where has he gone on holiday? Correct Solo queda la contraseña también modifique el HTML de estudio ya que no copiaba Enel PC Mac los enlaces ahora ya si 1h 9 minutos para todo y 16 minutos de estudio y práctica dentro de esa hora nueve minutos H hoy 16 minutos por los problemas de copiado Acumuladas 43:32h 16:17 voy a volver a incluir firefox en el atajo de estudio y al final no hay que mirar el código de la web de TryHackMe si no el de la web de wordpress de OWoodflint Ya está laboratorio completado estaba dando problemas la web la contraseña estaba bien pennYDr0pper.! Tiempo echado 30 minutos + o - Acumuladas 44:02 h 8:57 3/10/2026 día 38 terminar punto 1 cnpen Inglés normal e inglés técnico completado del día 
Python localhost:~# python3 --version Python 3.9.16 localhost:~# mkdir -p ~/python-ciberseguridad/ejer cicio01 localhost:~# cd ~/python-ciberseguridad/ejercicio0 1 localhost:~/python-ciberseguridad/ejercicio01# nan o python01.py localhost:~/python-ciberseguridad/ejercicio01# pyt hon3 python01.py Objetivo: mi-lab IP: 192.168.50.20 Puertos: [22, 80, 443] <class 'str'> <class 'str'> <class 'list'> localhost:~/python-ciberseguridad/ejercicio01# nan localhost:~/python-ciberseguridad/ejercicio01# nan o python01.py localhost:~/python-ciberseguridad/ejercicio01# pyt hon3 python01.py Objetivo: laboratorio de linusin IP: 192.168.50.20 Puertos: [22, 80, 443] <class 'str'> <class 'str'> <class 'list'> localhost:~/python-ciberseguridad/ejercicio01# Me dispongo a hacer el portfolio por la tarde H hoy 23 mins Acumuladas 44:25h 11:18 informe para el portfolio Lab de https://tryhackme.com/room/ohsint 1 Introducción ohsint es un laboratorio de osint El objetivo es apartir de los metadatos de una foto responder una serie de preguntas (Investigar una persona o entidad) 2 Herramientas usadas firefox y Safari navegadores y exif tools extractor de metadatos 3 Preguntas y como las solucione
	1.	What is this user’s avatar of? — ¿De qué es el avatar del usuario? Solución buscar el nombre de usuario en Google y sale el gatito pongo cat en el campo
	2.	What city is this person in? — ¿En qué ciudad está esta persona? Busco en internet las coordenadas GPS de la foto ( los metadatos se ven con exif tools)y a partir de ahí con Google maps y Google veo en qué ciudad está
	3.	What is the SSID of the WAP he connected to? — ¿Cuál es el SSID del punto de acceso Wi-Fi al que se conectó?al buscar en Google el nombre de usuario sale una cuenta de x y esa cuenta de x sale la bssid Y como wigle no me dejaba registrarme busque en Google el nombre de ssid
	4.	What is his personal email address? — ¿Cuál es su correo electrónico personal?sale en github del usuario 
	5.	What site did you find his email address on? — ¿En qué sitio encontraste su correo?github
	6.	Where has he gone on holiday? — ¿Dónde se ha ido de vacaciones? Me fijé y las letras coincidían con New York fue cierto 
	7.	What is the person’s password? — ¿Cuál es la contraseña de la persona? Para esto desde el ordenador en el código de la web de wordpress del usuario estaba metida la password ( pero no era visible estuve un buen rato) 4 Técnicas usadas Análisis de metadatos, investigación de identidad,búsqueda en fuentes,geolocalización,análisis web y investigación 5 Cosas aprendidas Extracción de metadatos, análisis web,una pequeña información puede dar lugar a una gran investigación nadie está a salvo en internet si no limpia sus metadatos antes de subir fotos o vídeos a RRSS 6 Conclusion el lab me ha enseñado técnicas de osint y que hay que borrar metadatos antes de compartir fotos. A partir de una imagen he resuelto 7 preguntas incluyendo coordenadas GPS y avatar y email datos sensibles 7 Evidencia IMG_6046.pngIMG_6045.png
