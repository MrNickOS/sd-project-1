# Proyecto Sistemas Distribuidos
### Autor: Nicolás Machado Sáenz
### Tema: Aprovisionamiento de Infraestructura con Docker Compose y Kubernetes

En este ejercicio final se aprovisionará una infraestructura de contenedores, para desplegar una
aplicación sencilla en Python de manera local con Docker Compose y luego escalarla a la plataforma
Kubernetes.

Esta plataforma se encarga de gestionar equipos high-availability en un cluster de trabajo, sin
necesidad de relacionar las aplicaciones del cluster a una máquina independiente. Esto permite la
distribución eficiente de los contenedores asociados a cada aplicación en el cluster.

Un cluster consta de dos componentes.
  * Maestro: responsable de la gestión global del cluster, realiza programación, monitoreo, escalamiento
  y actualización de las aplicaciones que allí residen. El despliegue de una aplicación en Kubernetes
  hace responsable al maestro de iniciar los nodos que tiene asociados.
  * Nodos: Es un equipo físico o virtual que hace parte de un cluster de Kubernetes. Para comunicarse
  con el maestro, cada nodo debe contar con un controlador o agente Kubectl, así como herramientas
  para gestionar contenedores (ejemplo, Docker). En general, cada nodo se comunica con el Maestro
  mediante el API Kubernetes.
  
Para desplegar Kubernetes, se hizo uso de los siguientes recursos.
  * Equipo cliente Ubuntu 16.04
  * Minikube para Linux
  * Docker-Compose
  * Cuenta en Docker Cloud
  
Primeramente, se debe instalar MiniKube para distribuciones Linux, utilizando el siguiente comando:

``` curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.24.1/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/ ```
