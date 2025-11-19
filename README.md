# 🧱 Arquitectura de Microservicios -- Proyecto Final

Este repositorio actúa como el **contenedor principal** del proyecto de
arquitectura de microservicios.\
Aquí se integran los diferentes microservicios desarrollados
individualmente, cada uno alojado en su propio repositorio de GitHub, y
referenciados en este proyecto mediante **Git Submodules**.

El repositorio principal permite:

-   Centralizar todos los servicios del sistema.
-   Mantener independencia entre los microservicios.
-   Facilitar la ejecución local mediante `docker-compose`.
-   Organizar y documentar la arquitectura general.

------------------------------------------------------------------------

## 📂 Estructura del repositorio

La estructura del proyecto luce de la siguiente manera:

    microservices-architecture-project/
    ├── api-gateway-micro/              # Submódulo: API Gateway del sistema
    ├── gestion-perfil-micro/           # Servicio de gestión de perfiles
    ├── notifications-service-micro/    # Servicio de notificaciones
    ├── orquestador-solicitudes-micro/  # Orquestador de solicitudes
    ├── health-check-app-micro/         # Servicio de health-check
    ├── automation-tests/               # Pruebas automatizadas del sistema
    ├── cicdjenkins/                    # Configuración de CI/CD con Jenkins
    ├── jwtmanual-taller1-micro/        # Servicio relacionado con autenticación JWT
    ├── observability/                  # Observabilidad: logs, métricas, dashboards
    ├── docker-compose.yml              # Composición del sistema completo
    └── README.md

------------------------------------------------------------------------

## 🔗 Microservicios incluidos

Cada microservicio se mantiene en su propio repositorio independiente.\
Este repositorio los incluye únicamente como **referencias**, lo cual
permite:

-   mantener su autonomía
-   conservar su historial individual
-   actualizarlos de forma independiente

Para sincronizarlos cuando se actualicen individualmente:

``` bash
git submodule update --remote
```

------------------------------------------------------------------------

## 🛠️ Configuración del Proyecto

### 📥 Clonar este repositorio con todos los microservicios

``` bash
git clone --recurse-submodules https://github.com/tuusuario/microservices-architecture-project.git
```

Si ya lo clonaste sin submódulos:

``` bash
git submodule update --init --recursive
```

------------------------------------------------------------------------

## 🔄 Actualización de submódulos

Actualizar un solo microservicio:

``` bash
git submodule update --remote nombre-del-submodulo
```

Actualizar todos los microservicios:

``` bash
git submodule update --remote --merge
```

Guardar cambios:

``` bash
git add .
git commit -m "Update submodules"
git push
```

------------------------------------------------------------------------

## 🐳 Ejecución del sistema con Docker Compose

``` bash
docker-compose up --build
```

------------------------------------------------------------------------

## 🧩 ¿Por qué usar submódulos en este proyecto?

-   Mantiene los microservicios desacoplados\
-   Evita mezclar múltiples repositorios\
-   Facilita integraciones y despliegues\
-   Sigue buenas prácticas de arquitectura de microservicios

------------------------------------------------------------------------

## 🧑‍🤝‍🧑 Equipo de Trabajo

Proyecto desarrollado para la asignatura **Arquitectura de
Microservicios**.

**Desarrollado por:**

- [Miguel Angel Mira Ortega](https://github.com/MiguelA05)
- [Santiago Quintero Uribe](https://github.com/Tourment0412)
- [Juan Manuel Isaza Vergara](https://github.com/JUANMANUELUQ)
- [Andrés Felipe Zuñiga Zuluaga](https://github.com/AndresZunigaZ2005)



------------------------------------------------------------------------

## 📘 Notas finales

-   El repositorio principal **no modifica** los repos individuales
-   Eliminarlos aquí **no afecta** los repositorios externos
-   Cada microservicio puede seguir evolucionando autónomamente

