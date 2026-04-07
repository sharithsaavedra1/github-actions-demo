# 🚀 GitHub Actions - Exposición



## 🧠 ¿Qué es GitHub Actions?

GitHub Actions es una herramienta que permite automatizar tareas dentro de un repositorio. Funciona ejecutando procesos automáticamente cuando ocurre un evento, como subir código o crear un pull request.

En otras palabras, es un sistema que actúa como un “robot” que trabaja por nosotros para revisar, ejecutar o validar nuestro código sin intervención manual.

---

## 🎯 ¿Para qué sirve?

GitHub Actions se utiliza para:

* Automatizar procesos repetitivos
* Ejecutar pruebas automáticamente
* Validar código
* Compilar proyectos
* Desplegar aplicaciones
* Mejorar la calidad del software

---

## ⚙️ ¿Cómo funciona?

El funcionamiento se basa en una serie de componentes:

### 🔔 Eventos (Events)

Son los que activan el flujo de trabajo.

Ejemplos:

* push (cuando se sube código)
* pull_request (cuando se crea una solicitud de cambios)
* schedule (ejecución por tiempo)

---

### 📄 Workflow

Es un archivo en formato `.yml` donde se define qué acciones se van a ejecutar.

---

### 🧩 Jobs

Son los trabajos que se ejecutan dentro del workflow.

---

### 🔨 Steps

Son los pasos específicos dentro de cada job.

---

### 🤖 Runner

Es la máquina virtual donde se ejecutan los procesos.

---

## 🔄 Flujo de funcionamiento

Evento → Workflow → Job → Steps → Resultado

---

## 🔀 ¿Qué es un Pull Request?

Un Pull Request es una solicitud para integrar cambios de una rama a otra. Permite revisar el código antes de unirlo al proyecto principal.

Sirve para:

* Trabajar en equipo
* Revisar cambios
* Evitar errores

---

## 🧪 Ejercicios prácticos

### 🟢 Ejercicio 1: Saludo automático

```yaml
name: Ejercicio 1 - Saludo

on: push

jobs:
  saludo:
    runs-on: ubuntu-latest
    steps:
      - name: Mostrar mensaje
        run: echo "Hola, este es mi primer workflow 🚀"
```

📌 Descripción:
Este workflow se ejecuta cuando se realiza un push y muestra un mensaje automático.

---

### 🟢 Ejercicio 2: Contar archivos

```yaml
name: Ejercicio 2 - Contar archivos

on: push

jobs:
  contar:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Contar archivos
        run: ls | wc -l
```

📌 Descripción:
Cuenta automáticamente la cantidad de archivos en el repositorio.

---

### 🟢 Ejercicio 3: Mostrar información del repositorio

```yaml
name: Ejercicio 3 - Info repo

on: push

jobs:
  info:
    runs-on: ubuntu-latest
    steps:
      - name: Mostrar repo
        run: echo $GITHUB_REPOSITORY
```

📌 Descripción:
Muestra el nombre del repositorio utilizando variables de entorno.

---

### 🟣 Ejercicio 4: Ejecutar solo en rama main

```yaml
name: Solo main

on:
  push:
    branches: [ main ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - run: echo "Solo funciona en main"
```

---

### 🟣 Ejercicio 5: Crear archivo automático

```yaml
name: Crear archivo

on: push

jobs:
  crear:
    runs-on: ubuntu-latest
    steps:
      - name: Crear archivo
        run: echo "Hola mundo" > archivo.txt
```

---

### 🟣 Ejercicio 6: Detectar cambios en README

```yaml
name: Detectar cambios en README

on:
  push:
    paths:
      - 'README.md'

jobs:
  detectar:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Mensaje
        run: echo "Se modificó el README"
```

---

## 🤝 Trabajo colaborativo

Este repositorio fue desarrollado de manera colaborativa, permitiendo que múltiples usuarios trabajen simultáneamente mediante control de versiones.

---

## 🚀 Conclusión

GitHub Actions es una herramienta fundamental en el desarrollo moderno, ya que permite automatizar procesos, reducir errores y optimizar el tiempo de trabajo, siendo ampliamente utilizada en entornos profesionales.

---

## 🎤 Nota final

Durante la exposición se demostrará en tiempo real cómo un workflow se ejecuta automáticamente al realizar cambios en el repositorio.
