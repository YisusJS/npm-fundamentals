# Dependencias con NPM

## Comandos básicos

### Ver configuración por defecto

```javascript
npm config ls -l // Esto muestra la configuración general
npm config set init.author.email // Definir valores
npm config get init.author.email // Obtener valores
```

### Iniciar un proyecto

```
npm init
```

### Iniciar un proyecto rapidamente con una configuración por defecto

```
npm init -y
```

### Definir información por defecto

```
npm config set init.author.email "edwinjpr11@gmail.com"
npm config set init.author.name "Edwin J. Páez"
npm config set init.author.url "https://edwin-p.com"
npm config set init.license "MIT"
```


## Dependencias

Si no asigamos una bandera, su defecto será
--save-prod o -P

### Instalar todas las dependencias del package

```
npm install
npm i
```

### Instalación en producción

```
npm install --save-prod node-fetch
npm i -P node-fetch
```

### Instalación en desarrollo

```
npm install --save-dev node-fetch
npm i -D node-fetch
```

### Instalación global

```
npm install --global node-fetch
npm i -G node-fetch
```

### Instalaciones opcionales

```
npm install --optional node-fetch
npm i -O node-fetch
```

### Simulación de instalación de dependencias

```
npm install react --dry-run
```

### Forzar instalación

NPM buscará hasta el último recurso disponible y lo instalará

```
npm install --force node-fetch
npm i -f node-fetch
```

### Instalar una versión específica

Después del nombre del paquete, se coloca la versión después del @

```
npm install -D json-server@0.15.0
```
