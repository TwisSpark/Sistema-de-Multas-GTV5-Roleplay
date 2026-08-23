## Sistema de Multas — GTV5 / Roleplay

Un sistema de multas para Discord pensado principalmente para servidores de GTA V Roleplay, pero diseñado para que pueda adaptarse a diferentes tipos de comunidades y sistemas de administración.

La idea es sencilla: ofrecer un sistema de multas funcional, organizado y fácil de adaptar, especialmente para quienes necesitan uno pero no saben cómo desarrollarlo desde cero.

«¿Buscabas un sistema de multas para tu servidor? Quizás por fin lo encontraste.»

---

### ¿Qué incluye?

La versión base cuenta con las siguientes funciones:

- Crear multas mediante ``/add_fine``

- Consultar las multas de un usuario mediante ``/see_fines``

- Mostrar la información completa de cada multa.

- Límite de hasta 15 multas por usuario.

- Eliminación de multas mediante botones.

- Sistema de permisos para consultar y eliminar multas.

- Registro de acciones mediante un canal de logs.

- Información configurable de cada multa.

- Compatible con comandos Slash y Prefix para la consulta de multas.

---

### Información de las multas

La información principal de cada multa se encuentra en una variable configurable del sistema.

**Por defecto, contiene:**

```js 
$var[info;
**Ciudadano:** <@$var[userID]>
**Oficial:** $var[authorID]
**Infracción:** $var[infracción]
**Monto:** $numberSeparator[$message[monto];,]
**Estado:** $var[estado]
**Fecha:** <t:$getTimestamp:D>
]
```

Esta parte está pensada para que puedas modificarla según las necesidades de tu servidor.

Puedes cambiar, agregar o quitar información de acuerdo con el sistema de Roleplay que utilices.

La información incluida por defecto representa los datos básicos que normalmente necesita una multa:

- Ciudadano
- Oficial
- Infracción
- Monto
- Estado
- Fecha

---

**Comandos**

``/add_fine``

Permite registrar una nueva multa.

Este comando utiliza Slash Commands, ya que el sistema necesita diferentes opciones para registrar correctamente la información de la multa.

---

``/see_fines``

Permite consultar las multas registradas de un usuario.

Puede utilizarse mediante:

- Slash Command
- Prefix Command

Desde el panel de multas también es posible seleccionar una multa específica para consultar sus detalles.

Si el usuario cuenta con los permisos necesarios, podrá eliminar la multa mediante el botón correspondiente.

---

### Eliminación de multas

No existe un comando independiente como ``/delete_fine``.

La eliminación se realiza mediante los botones disponibles dentro del sistema:

- Desde la información de una multa.

- Desde el mensaje correspondiente en el canal de logs.

Esto permite mantener el sistema más sencillo y evita tener un comando adicional que no resulta necesario.

---

### Sistema de almacenamiento

Este sistema utiliza una forma diferente de almacenar la información.

En lugar de guardar toda la información de cada multa directamente en variables de BDFD, el sistema utiliza mensajes de Discord en el canal de logs como almacenamiento de la información.

Las variables de BDFD almacenan principalmente información necesaria para localizar y administrar esos registros, como:

- ID del canal de logs.
- IDs de los mensajes utilizados para almacenar las multas.
- Cantidad de multas registradas.

Cuando el sistema necesita consultar una multa, puede localizar el mensaje correspondiente y obtener de allí la información almacenada.

> [!WARNING]
> ⚠️ **IMPORTANTE:**
NO BORRES EL CANAL DE LOGS NI LOS MENSAJES QUE ENVÍA EL BOT EN ESE CANAL.

El sistema utiliza esos mensajes para almacenar la información de las multas.

Si eliminas el canal de logs o los mensajes utilizados por el sistema, las multas pueden dejar de funcionar correctamente y el sistema puede romperse.

Si necesitas limpiar el canal de logs, asegúrate primero de comprender cómo funciona el almacenamiento del sistema.

---

### Personalización

Este sistema está pensado para ser adaptado.

Puedes modificar la información que aparece en las multas para ajustarla a las reglas y necesidades de tu servidor.

Por ejemplo, puedes agregar información relacionada con:

- Código penal.
- Tipo de infracción.
- Departamento policial.
- Identificación del oficial.
- Estado de la multa.
- Información adicional del ciudadano.
- Cualquier otro dato que necesite tu sistema.

La versión incluida en este repositorio utiliza únicamente la información básica necesaria para mantener el sistema sencillo y fácil de modificar.

---

### Compatibilidad

El sistema está desarrollado utilizando:

- Bot Designer For Discord (BDFD)
- BDScript 2

Está pensado principalmente para servidores de GTA V Roleplay, pero no está limitado exclusivamente a este tipo de servidores.

Puedes adaptar el sistema a cualquier comunidad que necesite administrar multas o infracciones mediante Discord.

---

### Código gratuito y abierto

Este proyecto es gratuito y público.

Puedes utilizarlo, modificarlo y adaptarlo a las necesidades de tu servidor.

Si realizas modificaciones importantes, mejoras el sistema o decides publicar nuevamente una versión modificada del proyecto, debes mantener a TwisSpark como autor original.

No es necesario que mantengas exactamente el mismo sistema, pero sí debes reconocer que el proyecto original fue creado por:

***TwisSpark***

Por ejemplo:

```«Original system created by TwisSpark. Modified and improved by [Tu nombre].»```

La idea es que otras personas puedan mejorar el proyecto sin eliminar el reconocimiento de quien creó la versión original.

---

### ¿Quieres una nueva versión?

Esta es solamente la versión base del sistema.

Si recibo suficiente apoyo y sugerencias de la comunidad, puedo desarrollar futuras versiones con nuevas funciones y mejoras.

Si quieres proponer una función o sugerencia para futuras versiones, es necesario que formes parte de mi servidor de Discord para poder revisar las propuestas y recibir feedback de la comunidad.

---

### Autor

***TwisSpark***

Desarrollador y creador original del sistema.

Si encuentras un error, tienes una sugerencia o quieres proponer una mejora, puedes contactar conmigo a través de mi comunidad.

---

### ¿Te sirvió?

Si este sistema te ayudó, puedes apoyar el proyecto dejando una estrella en el repositorio.

Y si lo modificas o mejoras, recuerda mantener a TwisSpark como autor original.

> «Espero que este sistema sea justo lo que estabas buscando.»