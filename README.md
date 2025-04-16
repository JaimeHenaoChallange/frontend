# Frontend Service

Este repositorio contiene el código fuente del servicio frontend para la aplicación.

## Requisitos previos

- Node.js (versión 18 o superior)
- Docker (opcional, para construir la imagen)
- Kubernetes (opcional, para despliegue)

## Instalación local

1. Clona este repositorio:
   ```bash
   git clone https://github.com/JaimeHenaoChallange/frontend.git
   cd frontend
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Inicia el servidor de desarrollo:
   ```bash
   npm start
   ```

4. El servidor estará disponible en `http://localhost:3000`.

## Construcción de la imagen Docker

1. Construye la imagen Docker:
   ```bash
   docker build -t jaimehenao8126/frontend:latest .
   ```

2. Ejecuta el contenedor:
   ```bash
   docker run -p 80:80 jaimehenao8126/frontend:latest
   ```

## Despliegue en Kubernetes

1. Asegúrate de que `kubectl` y `helm` estén configurados correctamente.
2. Aplica el Helm Chart:
   ```bash
   helm install frontend ./helm-charts/frontend
   ```

3. Verifica el estado del despliegue:
   ```bash
   kubectl get pods
   ```

## Integración con ArgoCD

Este repositorio está configurado para ser gestionado por ArgoCD. Asegúrate de que ArgoCD esté instalado y configurado en tu clúster de Kubernetes.

- Archivo de configuración de ArgoCD: `argocd/frontend-app.yaml`

## Contacto

Para preguntas o soporte, contacta a [Jaime Henao](mailto:jaime@example.com).
