# FoodGo - CI/CD Demo

Proyecto de demostración de CI/CD con GitHub Actions y Azure DevOps Boards.

## Características

- Pipeline automatizado de CI/CD con GitHub Actions
- Integración con Azure DevOps Work Items
- Automatización del flujo: PR → Merge → Pipeline → Work Item Done

## Tecnología

- GitHub Actions (CI/CD)
- Azure DevOps Boards (Gestión de proyectos)
- Git para control de versiones

## Flujo de Trabajo

1. Crear Work Item en Azure DevOps
2. Crear rama feature con cambios
3. Abrir Pull Request en GitHub
4. Mergear PR a main
5. GitHub Actions ejecuta pipeline automáticamente
6. Work Item se actualiza a "Done"

## Funcionalidades Implementadas

- Sistema de validación de pedidos
- Verificación de disponibilidad de productos
- Control de stock en tiempo real

## Documentación

Ver `GUIA_DEMO.md` para instrucciones completas de configuración y presentación.
