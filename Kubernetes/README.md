# Comandos Kubernetes

A continuación, se presentan algunos de los comandos básicos más utilizados en Kubernetes junto con ejemplos y explicaciones breves:


### Crear un recurso en Kubernetes
```
kubectl create deployment nginx --image=nginx:latest
```

### Obtener información sobre recursos de Kubernetes
```kubectl get pods```

```kubectl get services```

```kubectl get deployments```   

### Describir un recurso específico
```kubectl describe pod nombre-del-pod```

```kubectl describe service nombre-del-servicio```

### Aplicar cambios en la configuración de un recurso
```kubectl apply -f archivo.yaml```

### Eliminar uno o varios recursos de Kubernetes
```kubectl delete pod nombre-del-pod```

```kubectl delete service nombre-del-servicio```

```kubectl delete deployment nombre-del-deployment```


### Mostrar los logs de un contenedor en un pod
```kubectl logs nombre-del-pod```

### Ejecutar un comando dentro de un contenedor en un pod
```kubectl exec -it nombre-del-pod -- comando-a-ejecutar```

### Reenviar puertos desde el pod hasta la máquina local
```kubectl port-forward nombre-del-pod puerto-local:puerto-remoto```

### Aumentar o disminuir el número de réplicas en un deployment
```kubectl scale deployment nombre-del-deployment --replicas=3```

### Mostrar los eventos ocurridos en el clúster
```kubectl get events```

### Exponer un servicio
```kubectl expose pod nombre-del-pod --type=LoadBalancer --port=8080 --target-port=80```
