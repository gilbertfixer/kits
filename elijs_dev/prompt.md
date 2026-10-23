# Prompts de IA: revisión de seguridad antes de lanzar

*Kit gratuito · homenaje no oficial a Eli.js (@elijs_dev) · basado en https://x.com/elijs_dev/status/2113047772454883420*
*Prompts redactados de cero para este kit; no reproducen los originales.*

Úsalos dentro de tu proyecto (editor o agente con acceso al código), uno cada vez y en este orden.

## 0. Instrucción de arranque (pégala primero)
```
Vas a revisar la seguridad de este proyecto en varias rondas. En cada ronda:
solo informe, sin cambiar código. Cada hallazgo con archivo y línea, riesgo
(alto/medio/bajo) y cómo lo aprovecharía alguien. Si no estás seguro, dilo.
```

## 1. Secretos
```
Busca claves, tokens y contraseñas en todo el repositorio. Para cada uno: dónde
está, si ese código llega al navegador y qué podría hacer alguien con él.
Revisa también variables con prefijo público y si .env está ignorado por git.
```

## 2. Reglas de la base de datos
```
Supón que un atacante tiene la clave pública de mi base de datos y hace
peticiones directas. Tabla por tabla: ¿qué podría leer, crear, editar o borrar?
Propón las reglas mínimas para que cada usuario solo toque lo suyo.
```

## 3. Propiedad de recursos (IDOR)
```
Haz una tabla con todas las rutas y acciones de servidor: ruta, método, ¿pide
sesión?, ¿comprueba que el recurso es de quien lo pide?, ¿usa un id del
cliente en lugar de la sesión? Explica el caso más grave paso a paso.
```

## 4. Validación de entradas
```
Localiza todo lo que entra del usuario (formularios, parámetros, cuerpo de
peticiones, archivos). Dime si se valida en el servidor y qué inyección sería
posible. Propón un esquema de validación con la librería que ya use el proyecto.
```

## 5. Abuso y costes
```
Lista los endpoints que cuestan dinero o son sensibles (IA, correos, SMS,
login, registro, recuperación). ¿Tienen límite de uso? ¿Cuánto podría costar
un bot que los llame miles de veces? Propón límites por usuario e IP.
```

## 6. Pagos y webhooks
```
Sigue el flujo de pago de principio a fin. ¿Quién decide que un usuario es de
pago? ¿Se verifica la firma del webhook? ¿Qué pasa si llega dos veces, si hay
reembolso o cancelación? Cuéntame cómo alguien conseguiría acceso sin pagar.
```

## 7. Autenticación y sesiones
```
Revisa cómo se guardan contraseñas y sesiones, cuándo caducan, si cerrar
sesión las invalida en el servidor, si «olvidé mi contraseña» revela qué
correos existen y si hay rutas protegidas solo en el frontend.
```

## 8. Revisión final de lanzamiento
```
Con todo lo anterior, dame: los 5 riesgos reales más graves, dependencias
vulnerables (ejecuta la auditoría del gestor de paquetes), cabeceras de
seguridad que faltan, errores que filtran datos internos y un plan:
hoy / esta semana / puede esperar. Explícalo para alguien no experto.
```

> Aviso: primera capa de revisión. No sustituye una auditoría profesional.
