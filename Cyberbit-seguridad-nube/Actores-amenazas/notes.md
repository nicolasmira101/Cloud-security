# Actores de amenazas

## APT35

- APT35, también conocido como Charming Kitten o Fósforo, ha estado presente desde 2014.
- Realizaron una campaña de espionaje a través de las redes sociales, una de las más sofisticadas, organizadas por actores iraníes.
- En 2019, apuntaron a instituciones académicas en EE. UU., Francia y el Medio Oriente.
- En 2020, se dirigieron a organizaciones de investigación médica en Israel y EE. UU.
- En 2021, abusaron de las vulnerabilidades del servidor Microsoft Exchange (ProxyShell).
- Charming Kitten atacó a investigadores médicos, particularmente en oncología, genética y neurología, usando phishing con temas sensibles.
- Han realizado campañas altamente dirigidas, como "BadBlood", utilizando temas sensibles como armas nucleares de Israel.
- Han atacado a periodistas y activistas que informan sobre temas en el Medio Oriente.
- Utilizan backdoors PowerShell como PowerLess Backdoor para ejecutar comandos.
- Explotaron la vulnerabilidad Log4Shell/Log4j en enero de 2022, aprovechando la situación antes de que las organizaciones parcharan sus sistemas afectados.
- Recientemente, se observó a Charming Kitten usando Hyperscrape para extraer correos electrónicos.
- Hyperscrape se utiliza para recolectar información de disidentes iraníes y se ha descubierto que descarga datos de Google TakeOut.
  
## Lockbit

<p align="center">
  <img src="https://media.licdn.com/dms/image/D5622AQHN8gs-3HFp1Q/feedshare-shrink_800/0/1698731494971?e=2147483647&v=beta&t=mI-oASPx21We5kAvtFkURHu0i0e-yRwLYcE_pmOoLaA"/>
</p>

- Responsable de más de un tercio de los ataques de ransomware entre la segunda mitad del año anterior y el primer trimestre de 2023.
- Surgió en septiembre de 2019 y se convirtió en el grupo más activo en 2022 tras la desaparición del grupo Conti.
- Más de 1500 registros de anuncios de víctimas en la plataforma SOCRadar y más de 300 víctimas anunciadas en el primer trimestre de 2023.
- Atento reportó una pérdida de $42.1 millones en 2021 debido a un ataque de LockBit, con $34.8 millones en pérdida de ingresos y $7.3 millones en gastos de mitigación.
- Capacidad para atacar sistemas Windows, Linux, VMware ESXi y posiblemente sistemas MacOS, ARM, FreeBSD, MIPS y SPARC.
- Utiliza Ransomware-as-a-Service (RaaS) desde enero de 2020, empleando tácticas como doble extorsión y reclutamiento de insiders.
- Borra archivos de registro y sombras de volumen, emplea encriptación híbrida AES y RSA.
- Enfoque en entidades gubernamentales, educativas y de emergencia.
- Ganancias aproximadas de $91 millones en EE. UU. desde 2020.
- Tipica operación de LockBit

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2023/04/lockbit-operation-scheme.png"/>
</p>
  
## Lazarus

- Lazarus Group es un grupo de ciberataque que se cree tiene vínculos con Corea del Norte.
- Se les ha atribuido una serie de operaciones cibernéticas desde principios de la década de 2000.
- Sus actividades están centradas en operaciones financieras fraudulentas.
- Utilizan malware personalizado, ataques de ingeniería social y técnicas de evasión.
- Han utilizado malware como "Trojan.Fastcash", diseñado específicamente para manipular sistemas de pagos internacionales.
- Ciclo de vida del ataque

<p align="center">
  <img src="https://hub.packtpub.com/wp-content/uploads/2018/10/APT38-Attack-Lifecycle.png"/>
</p>

- Han atacado instituciones financieras, criptomonedas y empresas de tecnología.
- Se estima que han robado más de 100 millones de dólares a través de sus ataques a diferentes instituciones financieras.
- Han llevado a cabo múltiples ataques notables, como el de WannaCry.
- Realizan una planificación previa a sus ataques, que pueden involucrar meses de vigilancia y reconocimiento de sus objetivos.

## Vice Society

- Vice Society surgió en 2021 y ha atacado organizaciones de todos los tamaños.
- Realizan cacería de grandes presas y emplean la táctica de doble extorsión: cifrado y robo de datos.
- A diferencia de otros grupos, no operan como un servicio de ransomware.
- Se cree que son una organización criminal con base en Rusia.
- En 2022, Vice Society fue el grupo más activo, con 39 ataques a la industria educativa.
- La educación fue una de las industrias más afectadas por el ransomware.
- Inicialmente, explotaban la vulnerabilidad PrintNightmare.
- Usaban ransomware de terceros, pero ahora han desarrollado su propio ransomware, "PolyVice".
- En diciembre de 2021, atacaron sistemas de operaciones de tiendas en el Reino Unido, cerrando muchas tiendas de Spar.
- En mayo de 2022, atacaron a Eskenazi Health en Indianápolis y al Waikato Region Health Board en Nueva Zelanda.
- En octubre de 2022, filtraron datos de estudiantes del LAUSD.

## ALPHV BlackCat

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2023/07/dark-web-profile-blackcat-ransomware-768x432.png"/>
</p>

- Es un grupo de ransomware conocido por ser el primero en usar el lenguaje de programación Rust.
- El grupo anunció su programa de afiliados RaaS (Ransomware-as-a-Service) en un foro de la dark web en diciembre de 2021.
- El grupo obtiene acceso inicial a sistemas objetivo mediante credenciales de usuario robadas o aprovechando vulnerabilidades conocidas en Microsoft Exchange.
- Una vez dentro, comprometen cuentas de usuario y administrador en AD para establecer objetos de directiva de grupo maliciosos (GPOs).
- Deshabilitan medidas de seguridad al eliminar software antivirus y obtienen cuentas de dominio utilizando herramientas como [AdFind](https://www.hackplayers.com/2015/05/analiza-la-informacion-de-tu-da-con-adfind.html) y [ADRecon](https://github.com/adrecon/ADRecon)
- Emplean la triple extorsión, donde además de robar datos sensibles antes de cifrar los archivos de la víctima y amenazar con su publicación (doble extorsión), amenazan con lanzar un ataque de denegación de servicio distribuido (DDoS) si no se cumplen sus demandas.

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2023/02/blackcat-infection-chain.jpg"/>
</p>

-  Implementar la autenticación multifactor (MFA) como requisito de acceso podría bloquear puntos de entrada comprometidos.
-  Mantener copias de seguridad fuera de línea es crucial al lidiar con ransomware.

## Lapsus$

- Grupo relativamente nuevo que ha llamado la atención mundial con ataques de alto perfil y métodos poco convencionales.
- Atacaron el Ministerio de Salud de Brasil, borrando 50 terabytes de datos.
- Luego apuntaron a empresas como CORREIOS, Claro, Impresa (Portugal), NVIDIA, Samsung, Ubisoft, Microsoft, y Okta.
- Exigió a NVIDIA eliminar la función LHR y liberar los controladores de GPU para Windows, Mac y Linux.
- Publicaron códigos fuente de Bing, Bing Map y Cortana de Microsoft en su canal de Telegram.
- Violación de Okta, ganando control total sobre las cuentas administrativas.
- TTPs:

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*tqGosO-G1oK_pgjc9Do9fA@2x.png"/>
</p>

- Lapsus$ no busca ocultar sus acciones, anuncia ataques en redes sociales y busca publicar filtraciones.
- Las defensas sólidas, MFA basado en token y protocolos de respuesta a incidentes son vitales.

## Tropical Scorpius

- Cuba es un ransomware basado en C++, utilizado por el grupo Cuba Ransomware en ataques de doble extorsión.
- Utilizan Cuba junto a un sitio de filtración de datos que publica información extraída de sistemas comprometidos.
- Apareció por primera vez a fines de 2019 afectando varias máquinas.
- Aunque se hace alusión a Cuba en imágenes y el nombre del grupo es Cuba, se presume una asociación con Rusia debido al uso del idioma ruso en el sitio de filtración de datos y durante negociaciones.
- El 4 de febrero, el ransomware afectó los Servicios de Transferencia Automática de Fondos (AFTS) en Seattle.
- El FBI informó que en diciembre de 2021, el grupo comprometió al menos 49 entidades en cinco sectores críticos, incluyendo finanzas, gobierno, salud, manufactura y tecnología.

<p align="center">
  <img src="https://socradar.io/wp-content/uploads/2022/03/stages-of-a-cuba-ransomware-attack--1024x512.png"/>
</p>

- Cuba Ransomware se asocia con Hancitor downloader para acceder a redes comprometidas.
- Utilizan Cobalt Strike para ejecutar scripts, realizar escaladas de privilegios y explorar redes comprometidas.
- Emplean herramientas como Netping y Protoping para escanear y recopilar información de la red.
- Utilizan acceso remoto y backdoors como Ficker Stealer o SystemBC para moverse lateralmente en la red.
  
## Cozy Bear

- Se asocia con agencias de inteligencia rusas, específicamente identificado como APT29.
- Poseen capacidades avanzadas para llevar a cabo ataques altamente dirigidos, como el ataque a la cadena de suministro de SolarWinds.
- Presumiblemente dirigido por el Servicio de Inteligencia Exterior de Rusia (SVR).
- Infiltraron la red del Comité Nacional Demócrata en 2015, causando una violación de datos detectada en 2016.
- Están detrás de operaciones como Operation Ghost, afectando al Ministerio de Asuntos Exteriores de algunos países europeos.
- Se les vincula con el malware WellMess utilizado en ataques a institutos de investigación de vacunas contra COVID-19.
- Utilizan plataformas de redes sociales y servicios en línea para comunicarse durante sus actividades maliciosas.
- Se valen de aplicaciones como Notion y sistemas como LegisWrite y eTrustEx para atacar a organizaciones estatales en la Unión Europea.
- Recientemente han empleado chats de Microsoft Teams para realizar ataques de ingeniería social.
- Aprovecharon una vulnerabilidad de WinRAR en ataques a embajadas europeas.
- También explotan vulnerabilidades críticas como [CVE-2018-13379](https://nvd.nist.gov/vuln/detail/CVE-2018-1337) de Fortinet FortiOS y otras.

## APT40

- Grupo patrocinado por China
- Desde al menos 2013, este actor ha apoyado los esfuerzos de modernización naval de China.
- También se ha observado un enfoque en países estratégicamente importantes para la Iniciativa del Cinturón y Ruta de la Seda
- APT40 utiliza una variedad de técnicas para el compromiso inicial, como explotación de servidores web, campañas de phishing y compromisos estratégicos en la web.
- Ciclo de vida del ataque:

<p align="center">
  <img src="https://ics-cert.kaspersky.com/wp-content/uploads/sites/6/2020/04/3-2.png"/>
</p>

- Utilizan malware como AIRBREAK, FRESHAIR y BEACON para penetrar los sistemas.
- Utilizan backdoors y herramientas como web shells para mantener el control en el entorno comprometido.
- Implica recopilar y transferir información, usando herramientas como rar.exe para comprimir y cifrar datos antes de la exfiltración.

## Earth Preta

- En noviembre de 2022, se reveló una gran campaña de phishing iniciada por Earth Preta, también conocido como Mustang Panda.
- La campaña apuntó a varios países de la región de Asia-Pacífico (APAC) a través de correos electrónicos de spear-phishing.
- Se identificó a entidades gubernamentales como uno de los principales objetivos del grupo.
- Desde principios de 2023, se observaron nuevos vectores de ataque utilizados por el grupo, como MIROGO y QMAGENT.
- Se descubrió un nuevo dropper llamado TONEDROP que libera el malware TONEINS y TONESHELL en diferentes regiones.
- Los documentos señuelo están escritos en birmano y contienen temas controvertidos entre países.
- Utilizan correos electrónicos de spear-phishing con enlaces de Google Drive para distribuir archivos maliciosos.
  
