# Configurar un parquete en github paso a paso

## 1- Iniciar el proyecto ya sea de react o de node
Debe haber un archivo index que exporte las clases, componentes o funciones.

## 2- Debes configurar el repository en el archivo package.json agengando la siguiente linea:
Debes cambiar username y repository por los valores correspondientes, tambien puedes entrar a la url del repositorio y copiar el link que aparece en el boton de clone.
Lugo debes agregarle .git al final.
```json
"repository": "https://github.com/username/repository.git"
```

## 3- Configurar el publishConfig en el package.json
Debes cambiar username y repository por los valores correspondientes.
```json
"publishConfig": {
    "registry": "https://npm.pkg.github.com/@username"
}
```

## 4- Crear un archivo .npmrc en la raiz del proyecto
Debes cambiar username y token por los valores correspondientes.
```text
v
registry=https://npm.pkg.github.com/@username
```

## 5- Crear un archivo .gitignore en la raiz del proyecto
Debes agregar las siguientes lineas:
```text
node_modules
dist
```

## 6- Hacer login en npm
```bash
npm login --registry=https://npm.pkg.github.com
```