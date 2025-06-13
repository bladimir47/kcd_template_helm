# 📦 Proyecto Helm: Ejemplo con `if`, `range` y despliegue de múltiples apps

Este proyecto es una plantilla Helm personalizada para desplegar múltiples aplicaciones (`apps`) de forma dinámica, usando lógica condicional (`if`) y bucles (`range`) en los templates.

---

## 🛠️ Requisitos

- Kubernetes instalado (local o en la nube)
- Helm 3+
- Acceso a un cluster configurado (por ejemplo, con `kubectl config view`)
- Docker (opcional, si construirás tus propias imágenes)

---

## 🚀 ¿Qué hace este proyecto?

Este Helm chart permite definir múltiples aplicaciones en el `values.yaml` y generar automáticamente un `Deployment` y `Service`.

Esto permite tener un solo archivo `.yaml` dinámico para múltiples componentes.

---

## 📁 Estructura de Archivos

```bash
.
├── charts/               # (subcharts, si los usas)
├── templates/
│   └── deployment.yaml   # Contiene la lógica con if y range
│   └── service.yaml   # Contiene la lógica con if y range
├── values.yaml           # Define la lista de apps
└── Chart.yaml            # Información básica del chart

---

## 📁 Comandos
Comandos