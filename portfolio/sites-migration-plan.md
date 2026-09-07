# Plan de migración desde ChatGPT Sites a GitHub

Este documento organiza la migración de proyectos actualmente desplegados en ChatGPT Sites hacia repositorios privados de GitHub, manteniendo una capa pública de portafolio para reclutadores.

## Objetivo

Para cada producto:

1. conservar el código fuente completo en un repositorio privado;
2. eliminar o externalizar secretos y configuración sensible;
3. documentar arquitectura, stack y decisiones técnicas;
4. mantener una demo pública cuando corresponda;
5. publicar solamente evidencia segura para reclutadores.

## Proyectos

| Proyecto | Estado del producto | Código en GitHub | Destino recomendado | Showcase público |
|---|---|---|---|---|
| Tu Casa Pro | Desplegado | Pendiente recuperar de Sites | `tucasapro-app` privado | Sí, alta prioridad |
| Terixia | Desplegado | Pendiente recuperar de Sites | `terixia-web` privado | Sí, alta prioridad |
| Café Moreno | Desplegado | Pendiente recuperar de Sites | `cafe-moreno-web` privado | Sí |
| Manufacturas Mego | Desplegado | Pendiente recuperar de Sites | `manufacturas-mego-web` privado | Opcional |
| Verixia | Desplegado | Ya existe privado | Mantener privado | Sí |
| LM Dotaciones | Desplegado | Ya existe privado | Mantener privado | Sí |
| Tambit | Proyecto privado | Ya existe privado | Mantener privado | Case study técnico |

## Checklist por repositorio

### 1. Recuperación

- obtener todos los archivos fuente del Site;
- conservar estructura de carpetas;
- identificar framework y runtime;
- identificar dependencias y lockfile;
- separar archivos generados de archivos fuente.

### 2. Seguridad antes del primer push

No subir:

- `.env` o variantes;
- API keys o tokens;
- claves de Supabase u otros proveedores que no sean publicables;
- credenciales de correo;
- webhooks privados;
- datos de clientes;
- exports de bases de datos;
- cookies o sesiones;
- archivos con secretos históricos.

Crear cuando aplique:

- `.gitignore`;
- `.env.example` sin valores reales;
- documentación de variables requeridas;
- configuración por entorno.

### 3. Calidad técnica

- `README.md` con propósito, arquitectura y ejecución local;
- comandos de instalación, desarrollo, lint, test y build;
- estructura de carpetas explicada;
- manejo de errores;
- validación de entradas;
- responsive y accesibilidad básica;
- eliminar archivos temporales y código muerto.

### 4. Evidencia para reclutadores

Cada proyecto público/showcase debería mostrar:

- problema de negocio;
- solución construida;
- rol y responsabilidad;
- arquitectura;
- tecnologías;
- capturas del producto;
- decisiones técnicas relevantes;
- resultados o impacto cuando existan;
- link a demo.

## Prioridad

1. Tu Casa Pro
2. Terixia
3. Verixia
4. LM Dotaciones
5. Café Moreno
6. Tambit
7. Manufacturas Mego

## Regla de publicación

El código completo no tiene que ser público para demostrar experiencia. Si un proyecto contiene lógica comercial, integraciones sensibles o información de terceros, se mantiene privado y se presenta mediante un case study o un repositorio showcase aislado.
