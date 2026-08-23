## Configuración de la variable

> [!WARNING]
> Esta variable es necesaria para que el sistema funcione correctamente.

Si no creas esta variable o modificas su estructura, el sistema puede dejar de funcionar.

### Crear la variable

En la aplicación Bot Designer For Discord (BDFD) debes crear una variable con exactamente estos datos.

**Nombre de la variable**

``configFines_Spark``

**Valor de la variable**

```json 
{
  "channel_logs": "1540898891883610233",
  "fines": [],
  "limit_fines": 15
}
```

## Configuración del canal de logs

Debes cambiar únicamente la ID:

```1540898891883610233```

por la ID del canal de logs de tu servidor.

**Por ejemplo:**

```json  
{
  "channel_logs": "ID_DE_TU_CANAL_DE_LOGS",
  "fines": [],
  "limit_fines": 15
}
```

> [!CAUTION]
> No cambies ninguna otra parte del JSON.

Solamente reemplaza la ID del canal de logs.

No modifiques "fines", "limit_fines" ni los nombres de las propiedades.

Si modificas la estructura del JSON, puedes provocar errores y hacer que el sistema no funcione correctamente.

---

### ¿Por qué el límite es de 15 multas?

En esta versión del sistema, el límite está establecido en 15 multas por usuario.

Esto se debe a que las multas se muestran mediante un menú de selección de Discord, y el sistema utiliza un máximo de 15 opciones para mostrar las multas.

Por esta razón, la variable utiliza:

``"limit_fines": 15``

No se agregaron más opciones en esta versión porque el sistema actual utiliza este menú para seleccionar y consultar las multas.

> [!NOTE]
> Este límite corresponde a la versión actual del sistema. En una futura versión se podría utilizar otra forma de mostrar las multas para permitir una cantidad mayor.

---

### ¿Cómo obtener la ID del canal?

Para obtener la ID de un canal necesitas activar el Modo Desarrollador de Discord.

Si no sabes cómo activarlo, puedes ver mi video donde explico cómo hacerlo: https://youtube.com/shorts/0kAOtT9RIn4

También puedes unirte a mi servidor de Discord si necesitas ayuda: https://discord.gg/eSUZFWwajw

Antes de continuar

Asegúrate de que:

- [ ] Creaste la variable "configFines_Spark".
- [ ] Utilizaste exactamente el JSON proporcionado.
- [ ] Cambiaste únicamente la ID del canal de logs.
- [ ] La ID corresponde al canal donde el bot guardará los registros.
- [ ] No modificaste ninguna otra parte del JSON.

> [!IMPORTANT]
> Esta variable es obligatoria. Si no la agregas correctamente, el sistema no funcionará.