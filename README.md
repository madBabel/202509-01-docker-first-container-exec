# 🐳 Ejercicio: Tu primer servidor web con Docker

El objetivo de este ejercicio es familiarizarte con el uso básico de **Docker**, desde la búsqueda de imágenes oficiales en **Docker Hub** hasta la ejecución y gestión de contenedores.

---

## 📌 Pasos a realizar

### 1. Explora Docker Hub
1. Ingresa a [https://hub.docker.com](https://hub.docker.com)  
2. Busca la imagen oficial de **nginx** y revisa su documentación.  

---

### 2. Descarga la imagen
Ejecuta en tu terminal:  
```bash
docker pull nginx
```

---

### 3. Crea y ejecuta un contenedor
Lanza un contenedor con **nginx** utilizando las siguientes opciones:  
- `-d` → para ejecutarlo en segundo plano  
- `-p 8080:80` → para mapear el puerto 8080 de tu máquina al puerto 80 del contenedor  
- `--name servidor-web` → para asignarle un nombre al contenedor  

```bash
docker run -d -p 8080:80 --name servidor-web nginx
```

---

### 4. Verifica el contenedor en ejecución
Lista los contenedores activos:  
```bash
docker ps
```

---

### 5. Prueba el servidor web
- Abre un navegador y visita: [http://localhost:8080](http://localhost:8080)  
- Alternativamente, usa `curl`:  
```bash
curl http://localhost:8080
```

---

### 6. Detén el contenedor
Cuando hayas terminado, detén el contenedor de forma elegante:  
```bash
docker stop servidor-web
```

---

## ✅ Resultado esperado
Un contenedor en ejecución que sirva la página por defecto de **nginx**, accesible en [http://localhost:8080](http://localhost:8080).
