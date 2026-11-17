# Repositorio IA

Este repositorio reúne dos actividades de programación y un proyecto interactivo de exploración espacial realizado para el curso.

## Contenido

### `IA-semana1/` — Ordenar tres valores

`IA_semana1.txt` contiene un ejercicio de lógica condicional en JavaScript. Compara tres números (`a`, `b` y `c`) y muestra sus valores de menor a mayor mediante una cadena de condiciones `if/else`.

### `IA-semana2/` — Análisis de una decisión con IA

`riwi-tres-cupos-borrador.txt` documenta una actividad sobre la asignación de tres cupos de acompañamiento entre ocho estudiantes ficticios. Incluye:

- La situación, las notas, la asistencia y las circunstancias de cada estudiante.
- Dos consultas a una IA y las selecciones justificadas para cada una.
- Una comparación de cómo cambia la recomendación al conocer los recursos y el objetivo del programa.
- Observaciones sobre los datos utilizados, las suposiciones de la IA y la información adicional que habría sido útil solicitar.
- Una reflexión sobre la importancia de definir criterios y revisar las recomendaciones de la IA.

### `proyecto-IA/agujero-negro-lab/` — Event Horizon

Laboratorio interactivo de exploración espacial y gravedad relativista. Incluye una portada, un simulador 3D del espacio y recursos de audio, texturas y datos astronómicos.

La portada está en `index.html`; el simulador, en `simulador.html`. El archivo `event_horizon_viaje_interactivo_hacia_un_agujero_negro.html` conserva el enlace de entrada antiguo. La documentación específica, con navegación y parámetros disponibles, está en [`proyecto-IA/agujero-negro-lab/README.md`](proyecto-IA/agujero-negro-lab/README.md).

#### Abrir el proyecto

Se necesita Python 3 para iniciar un servidor local. Desde la raíz de este repositorio:

```powershell
python -m http.server 8000 --directory "proyecto-IA/agujero-negro-lab"
```

Después, abre <http://localhost:8000/> en un navegador moderno. El simulador requiere conexión a Internet para cargar sus bibliotecas y recursos externos, y un navegador compatible con WebGL. No requiere instalar paquetes ni compilar el proyecto.

#### Estructura del laboratorio

```text
proyecto-IA/agujero-negro-lab/
├── index.html                         Portada
├── simulador.html                     Interfaz del simulador
├── event_horizon_viaje_interactivo_hacia_un_agujero_negro.html
├── README.md                          Documentación del laboratorio
├── assets/
│   ├── inicio.css                     Estilos de la portada
│   ├── data/stars.json                Catálogo de estrellas
│   ├── audio/
│   │   ├── earth.mp3
│   │   ├── gargantua.mp3
│   │   ├── jupiter.mp3
│   │   ├── pulsar.mp3
│   │   ├── sun.mp3
│   │   └── genesis/
│   │       ├── cassiopeia-a.mp3
│   │       ├── centro-galactico.mp3
│   │       ├── nebulosa-carina.mp3
│   │       └── pilares-creacion.mp3
│   └── textures/
│       ├── earth_atmos_2048.jpg
│       ├── earth_clouds_1024.png
│       ├── earth_lights_2048.png
│       ├── earth_normal_2048.jpg
│       ├── earth_specular_2048.jpg
│       ├── europa.jpg
│       ├── jupiter.jpg
│       ├── mars.jpg
│       ├── mercury.jpg
│       ├── moon.jpg
│       ├── moon_1024.jpg
│       ├── neptune.jpg
│       ├── pluto.jpg
│       ├── saturn.jpg
│       ├── sun.jpg
│       ├── titan.jpg
│       ├── uranus.jpg
│       └── venus_atmosphere.jpg
├── css/
│   └── simulador.css                  Estilos del simulador
└── js/
    ├── main.js                        Inicio y animación
    ├── state.js                       Estado global
    ├── audio/
    │   ├── engine.js
    │   └── genesis-sound.js
    ├── config/
    │   ├── missions.js
    │   ├── moons.js
    │   └── targets.js
    ├── cosmos/
    │   ├── bigbang.js
    │   ├── compare.js
    │   ├── cosmos.js
    │   ├── nav.js
    │   ├── orrery.js
    │   ├── stars.js
    │   └── tour.js
    ├── genesis/
    │   ├── data.js
    │   ├── director.js
    │   ├── events-v3.js
    │   ├── events.js
    │   ├── fx.js
    │   ├── particles.js
    │   └── postfx.js
    ├── scene/
    │   ├── core.js
    │   ├── lens.js
    │   ├── materials.js
    │   ├── moon-textures.js
    │   ├── sky.js
    │   └── bodies/
    │       ├── mars-weather.js
    │       ├── moons.js
    │       ├── pulsar-blackhole.js
    │       ├── pulsar-physics.js
    │       ├── saturn-jupiter.js
    │       └── solar-system.js
    ├── surface/
    │   ├── descent.js
    │   ├── journey.js
    │   ├── sites.js
    │   └── surface.js
    └── ui/
        ├── controls.js
        ├── icons.js
        ├── missions.js
        ├── moon-focus.js
        ├── nasa.js
        └── telemetry.js
```

Los módulos del simulador se cargan desde `simulador.html`. En conjunto implementan la escena 3D, los astros y sus lunas, el audio, las misiones, la telemetría, las vistas del cosmos, los efectos del Génesis y las experiencias de aterrizaje y viaje.
