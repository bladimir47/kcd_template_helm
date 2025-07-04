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

Dentro de cada carpeta se encuentra un ejemplo completo para practicar y observar el uso de Helm.

```bash
.
├── base/                 # Proyecto HELM que solo tiene las apliaciones a lanzar de ejemplo
├── for/                  # Proyecto HELM que contiene los archivos para ejecutar el range
└── if/                   # Proyecto HELM que contiene los archivos para ejecutar el if
```

## 📁 Estructura de Archivos

Dentro de cada carpeta hay una estructura como la siguiente:

```bash
.
├── templates/
│   └── deployment.yaml   # Contiene la lógica con if y range
│   └── service.yaml   # Contiene la lógica con if y range
├── values.yaml           # Define la lista de apps
└── Chart.yaml            # Información básica del chart
```

---

## 💻 Comandos

```bash
#Crear un proyecto
helm create kcd 

#Instalar un proyecto de HELM en Kubernetes
helm install kcd2025 .

#Actualizar un despliegue 
helm upgrade kcd2025 .
#Si actualizamos es despliegue con cambios en values
helm upgrade kcd2025 . -f Values.yaml

#Si queremos ver como HELM genera los archivos enviados a Kubernetes
helm template .

```

## 📚  Recursos

[KUBERNETES](https://kubernetes.io/docs/home/)

[HELM](https://helm.sh/)

[MINIKUBE](https://minikube.sigs.k8s.io/docs/start)

[KCD GUATEMALA 2025](https://community.cncf.io/events/details/cncf-kcd-guatemala-presents-kcd-antigua-guatemala-2025/)