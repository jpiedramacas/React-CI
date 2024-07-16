
Aquí están los pasos para instalar Node.js y npm en Windows:

1. **Descargar e instalar Node.js**:
   - Ve al sitio web oficial de Node.js: [nodejs.org](https://nodejs.org/).
   - Descarga el instalador de la versión LTS (Long Term Support), ya que es la más estable.
   - Ejecuta el instalador y sigue las instrucciones para completar la instalación.

2. **Verificar la instalación**:
   - Abre una terminal (puedes usar Git Bash, PowerShell, o la terminal de Windows).
   - Ejecuta los siguientes comandos para asegurarte de que Node.js y npm se hayan instalado correctamente:
     ```bash
     node -v
     npm -v
     ```
   - Ambos comandos deberían devolver la versión instalada de Node.js y npm, respectivamente.

3. **Usar npx**:
   - Una vez que npm esté instalado, npx debería estar disponible automáticamente.
   - Puedes verificarlo ejecutando:
     ```bash
     npx -v
     ```

4. **Crear una nueva aplicación React**:
   - Ahora puedes usar npx para crear una nueva aplicación React ejecutando:
     ```bash
     npx create-react-app my-app
     ```
   - Este comando descargará e instalará las dependencias necesarias y creará un nuevo proyecto React en la carpeta `my-app`.

## GitHub Actions

```yaml
name: CI Pipeline

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Set up Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'

    - name: Install dependencies
      run: npm install

    - name: Run tests
      run: npm test

    - name: Build
      run: npm run build
```

### Explicación de cada parte:
1. **`name: CI Pipeline`**: Define el nombre de la pipeline.
2. **`on: [push, pull_request]`**: Especifica que la pipeline se ejecutará en eventos de `push` y `pull_request`.
3. **`jobs`**: Define los trabajos que se ejecut
