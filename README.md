# 🌤️ Proyecto: Aplicación Web en PHP — Clima con Open-Meteo  
**ITI UTN — Tarea: Despliegue con Docker + Kubernetes local**  

> ✅ Aplicación web básica que consulta clima en tiempo real  
> 🐳 Contenerizada con Docker  
> ☸️ Orquestada en clúster local de Kubernetes (Docker Desktop en Windows)  

---

## ⚙️ Requisitos Previos

- Windows 10/11 Professional o Enterprise  
- Docker Desktop instalado y en ejecución (con WSL2 habilitado)  
- Kubernetes **habilitado** en Docker Desktop (*Settings → Kubernetes → Enable Kubernetes*)  
- PowerShell (v5 o superior)  
- Conexión a Internet (para consumir la API y construir la imagen)

---


---

## 🚀 Instrucciones de Ejecución

Sigue estos pasos desde **PowerShell**:

### 1. Clonar o copiar el proyecto
```powershell
git clone https://github.com/tu-usuario/php-clima-k8s.git
cd php-clima-k8s


docker build -t php-clima-api:v1 .

kubectl apply -f k8s-deployment.yaml

kubectl get pods
kubectl get service php-clima-service

Abre tu navegador y visita:
➡️ http://localhost:30080

