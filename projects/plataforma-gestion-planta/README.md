# Plataforma de gestión de planta

Sistema web interno que centraliza la operación diaria de la planta. Lo diseñé, desarrollé y desplegué desde cero.

## Qué hace, por área

- **Producción:** control de operaciones (ensamble, estampado, láser, moldeo, verificación de rosca) y matrices de polivalencia por nivel (A1–A4).
- **Calidad y mantenimiento:** auditorías, control documental y gestión de equipos.
- **Logística y planeación:** picking, control de inventario, listas operativas y seguimiento de producción.
- **RH y seguridad:** expedientes de personal, registro de entrenamientos y control de accesos en caseta.
- **Indicadores:** dashboards en tiempo real por área.

## Stack

Python (Flask, SQLAlchemy, Waitress) · PostgreSQL · HTML / CSS / JavaScript · ReportLab · openpyxl

## Funcionalidades clave

Control de acceso basado en roles (RBAC), auditoría mediante logs, carga masiva desde Excel, generación automatizada de formatos en PDF y respaldos programados de la base de datos.

## Estado

En producción, con acceso estable para personal operativo, caseta y pantallas Andon.

> Por ser un sistema interno de la empresa, aquí se describe en términos generales. El código interno no se publica en este repo.
