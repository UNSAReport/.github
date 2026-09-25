# UNSAReport

Ecosistema de herramientas para la generación automatizada de informes de laboratorio, gestión de paquetes y diapositivas de presentación diseñadas para estudiantes y docentes de la Universidad Nacional de San Agustín (UNSA).

> [!NOTE]
> La suite UNSAReport ha consolidado su desarrollo en una arquitectura de monorepo centralizada en **[UNSAReport2](https://github.com/UNSAReport/UNSAReport2)**, unificando las herramientas CLI/TUI, servicios de registro, autenticación y plataformas web en un único lugar.

Escribe informes académicos elegantes y reproducibles en segundos usando [Typst](https://typst.app/), sin lidiar con plantillas complejas de LaTeX ni formateo manual en Word. La herramienta principal de línea de comandos es **`unsarep`**.

---

## Plataforma y Recursos

- **Plataforma Web**: Disponible en **[unsareport.ynoacamino.tech](https://unsareport.ynoacamino.tech/)** para explorar paquetes y plantillas oficiales o de la comunidad, gestionar credenciales y autenticar flujos de trabajo.
- **Seguimiento del proyecto**: Consulta el progreso actual y la planificación en el [tablero de la organización](https://github.com/orgs/UNSAReport/projects/1/views/1).

---

## Repositorios

### Repositorios activos

| Repositorio | Descripción |
|-------------|-------------|
| [**UNSAReport2**](https://github.com/UNSAReport/UNSAReport2) | **Monorepo principal del ecosistema.** Alberga el código base unificado: el CLI y TUI (`unsarep`), la plataforma web, el servicio de registro de paquetes, autenticación y la plataforma de diapositivas. |
| [**packages**](https://github.com/UNSAReport/packages) | **Biblioteca de componentes y plantillas.** Aloja y gestiona los componentes oficiales bajo el scope `@unsareport` (ej. `@unsareport/epis-lab`, temas y utilidades para Typst). |
| [**skills**](https://github.com/UNSAReport/skills) | **Skills para agentes de IA.** Habilidades e instrucciones para agentes de desarrollo compatibles con Claude Code, Cursor, OpenCode, Codex y más de 67 herramientas. |
| [**.github**](https://github.com/UNSAReport/.github) | **Configuración organizacional.** Perfil institucional de la organización en GitHub, plantillas compartidas y directrices globales. |

### Repositorios archivados y deprecados

Los siguientes repositorios han completado su ciclo de vida o han sido consolidados dentro del monorepo [UNSAReport2](https://github.com/UNSAReport/UNSAReport2):

| Repositorio | Estado / Razón |
|-------------|----------------|
| [**UNSAReport**](https://github.com/UNSAReport/UNSAReport) | CLI v1 original en Go. Reemplazado por la arquitectura y nuevas capacidades de `UNSAReport2`. |
| [**tui**](https://github.com/UNSAReport/tui) | Interfaz de terminal y CLI. Integrado en el directorio `tui/` de `UNSAReport2`. |
| [**registry**](https://github.com/UNSAReport/registry) | Servicio de registro estilo npm. Integrado en el directorio `registry/` de `UNSAReport2`. |
| [**auth**](https://github.com/UNSAReport/auth) | Servicio de autenticación centralizada. Integrado en el directorio `auth/` de `UNSAReport2`. |
| [**UNSASlides**](https://github.com/UNSAReport/UNSASlides) | Plataforma en la nube para diapositivas interactivas. Integrada en el directorio `slides/` de `UNSAReport2`. |
| [**website**](https://github.com/UNSAReport/website) | Portal web y frontend de la plataforma. Integrado en el directorio `web/` de `UNSAReport2`. |
| [**templates**](https://github.com/UNSAReport/templates) | Implementación anterior del catálogo de plantillas. Reemplazado por los paquetes del scope `@unsareport` en `components`. |

---

## Guía rápida con `unsarep`

Genera, edita en tiempo real y compila tu primer informe de laboratorio:

### 1. Inicializar la estructura del informe
Crea un nuevo proyecto a partir de un paquete de plantilla oficial (por ejemplo, `@unsareport/epis-lab`):

```bash
unsarep docs init @unsareport/epis-lab --report lab-01 --yes
cd lab-01
```

### 2. Vista previa en vivo mientras escribes
Inicia el compilador continuo para actualizar el PDF al instante cada vez que guardes tus archivos `.typ`:

```bash
unsarep docs watch lab-01
```

### 3. Compilar el PDF final de entrega
Genera el PDF de producción definitivo:

```bash
unsarep docs build lab-01
```

Para conocer todas las opciones de instalación (binarios precompilados, flakes de Nix o compilación desde el código fuente), visita el [README de UNSAReport2](https://github.com/UNSAReport/UNSAReport2#instalación).

---

## Contribuciones, Errores y Sugerencias

¡Las contribuciones de la comunidad son bienvenidas!

- **Reportar un error o solicitar funcionalidades**: Abre una issue en el repositorio correspondiente (para incidencias del CLI, la web o los servicios, utiliza el gestor de issues de [UNSAReport2](https://github.com/UNSAReport/UNSAReport2/issues)).
- **Proponer nuevos paquetes o plantillas**: Si deseas proponer o mejorar componentes para tu facultad o curso, consulta el repositorio [components](https://github.com/UNSAReport/components).
- **Desarrollo y Pull Requests**: Revisa la guía técnica en [CONTRIBUTING.md](https://github.com/UNSAReport/UNSAReport2/blob/main/CONTRIBUTING.md) para levantar el entorno local de desarrollo y ejecutar pruebas.

---

## 📄 Licencia

Este repositorio institucional está distribuido bajo la licencia [GNU Affero General Public License v3.0](LICENSE). Cada repositorio individual del ecosistema cuenta con su propia licencia específica (consulta el archivo `LICENSE` en cada uno).
