# Documentación de Inagent

Este repositorio contiene la documentación oficial de **Inagent**, construida con Mintlify. Incluye guías de uso, conceptos principales, configuración de canales, herramientas, bases de conocimiento, supervisión, reportes, facturación y referencia de API.

## Estructura del proyecto

- `docs.json`: configuración principal de Mintlify, navegación, marca, tabs y enlaces globales.
- `index.mdx`: página inicial de la documentación.
- `getting-started/`: guías iniciales, quickstart, checklist de producción y glosario.
- `core/`: conceptos centrales de equipos, agentes, contactos, herramientas, conocimiento, guardrails y publicación.
- `tools/`: documentación de herramientas como handoff humano, API REST y código.
- `knowledge/`: fuentes de conocimiento nativas y externas.
- `channels/`: configuración de canales como voz, WhatsApp, Webchat, Instagram, Facebook Messenger, SMS e Inconnect.
- `supervision/`, `conversation-history/`, `reporting/` y `billing/`: módulos operativos y administrativos.
- `api-reference/`: introducción, endpoints, eventos y especificación OpenAPI en `api-reference/openapi.json`.
- `images/`, `logo/`, `favicon.png`: recursos estáticos.
- `snippets/`: fragmentos MDX reutilizables.

## Desarrollo local

Instala la CLI de Mintlify si todavía no está disponible:

```bash
npm i -g mint
```

Ejecuta la vista previa desde la raíz del repositorio, donde está `docs.json`:

```bash
mint dev
```

La documentación local se sirve normalmente en:

```text
http://localhost:3000
```

Si la vista previa falla o el comportamiento parece desactualizado, actualiza la CLI:

```bash
mint update
```

## Flujo de trabajo recomendado

1. Edita o crea páginas `.mdx` en la carpeta temática correspondiente.
2. Si agregas una página nueva, incorpórala en `docs.json` para que aparezca en la navegación.
3. Ejecuta `mint dev` y revisa manualmente las páginas modificadas.
4. Verifica que los enlaces internos no generen 404.
5. Para cambios de API, valida que `api-reference/openapi.json` siga siendo JSON válido.

## Convenciones de contenido

- Usa nombres de archivo en kebab-case, por ejemplo `production-checklist.mdx`.
- Mantén frontmatter al inicio de cada página con `title` y, cuando aporte contexto, `description`.
- Reutiliza componentes Mintlify existentes como `Card`, `Columns`, `info` y `tip`.
- Mantén el contenido en español para páginas de producto, salvo que estés actualizando una página que ya esté en inglés.
- Guarda imágenes inspeccionables en `images/` o `logo/`; evita incrustar recursos grandes directamente en MDX.

## Publicación

Mintlify despliega los cambios desde el repositorio conectado mediante su integración de GitHub. Los cambios enviados a la rama principal se publican automáticamente según la configuración del proyecto en Mintlify.

## Recursos

- [Documentación de Mintlify](https://mintlify.com/docs)
- [Mintlify CLI en npm](https://www.npmjs.com/package/mint)
