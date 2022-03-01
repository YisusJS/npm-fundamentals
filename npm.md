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

## Actualizar paquetes

### Ver los paquetes instalados

```javascript
npm list
npm list -g --depth 0 // Ver paquetes instalados globalmente
```

### Revisar paquetes que disponen de nuevas versiones

Podemos usar la bandera --dd para obtener un output detallado

```
npm outdate
```

### Actualizar todos los paquetes

```
npm update
```

### Actualizar paquetes específicos

Puede usar @latest para la última versión o @semver para definir una versión

```
npm update json-server
```

## Eliminar paquetes

### Eliminar un paquete de node_modules y package

```
npm uninstall json-server
```

### Eliminar un paquete de node_modules pero no de package

```
npm uninstall json-server --no-save
```

### Eliminar paquetes que no se están usando

```
npm prune
```

## Seguridad

### Verificar vulnerabilidades

```javascript
npm audit
npm audit --json // Genera un json con la información
```

Si se encuentran vulnerabilidades debemos actualizar el paquete de esta manera

### Solucionar vulnerabilidades

```
npm audit fix
```

Si no se soluciona, debemos hacerlo con cada una de las vulnerabilidades

```javascript
npm update eslint-utils --depth 2 // Con esto le decimos que actualice eslint y sus dependencias
```

## Crear paquetes en NPM

Para subir un paquete en NPM debemos añadir en el package

```javascript
"bin": {"random-msg": "./bin/index.js/"}, // En este archivo se debe iniciar la app
"preferGlobal": true
```

Hacer pruebas del paquete antes de subirlas

```javascript
sudo npm link // Con esto instalamos el paquete de manera global, para iniciarlo usamos el nombre del archivo dentro de bin
```

### Subir los paquetes a NPM

Primero tenemos que iniciar sesión con nuestra cuenta de NPM

```javascript
npm adduser
npm publish --access=public // En el root del package
```

### Eliminar paquetes de NPM (3 días)

```javascript
npm unpublish <package_name> --force // Si su paquete no depende de otro
npm unpublish <package_name>@<version> // Anular una versión
```

### Actualizar la versión usando SEMVER

```
npm version patch/minor/major
```
