# Reto Bíblico — proyecto Capacitor

Este proyecto contiene la miniapp HTML del concurso bíblico de Zoe, preparada para compilarse como APK Android **sin instalar Android Studio ni Node.js en tu laptop**.

## Opción recomendada: compilar gratis con GitHub Actions

### 1. Crear una cuenta en GitHub
Si ya tienes una cuenta, omite este paso.

### 2. Crear un repositorio nuevo
- En GitHub pulsa **New repository**.
- Nombre sugerido: `RetoBiblico`.
- Puede ser **Private**.
- Pulsa **Create repository**.

### 3. Subir el contenido de este ZIP
- Descomprime el ZIP.
- En el repositorio de GitHub entra a **Add file > Upload files**.
- Sube **todo el contenido de la carpeta**, incluyendo la carpeta oculta `.github`.
- Pulsa **Commit changes**.

### 4. Esperar la compilación
Al subir los archivos, GitHub Actions debería iniciar automáticamente la compilación.

Ve a:
**Actions > Compilar APK Android**

Abre la ejecución más reciente y espera a que todos los pasos estén en verde.

### 5. Descargar el APK
Al final de la ejecución, en la sección **Artifacts**, descarga:

`RetoBiblico-APK`

GitHub descargará un ZIP. Dentro estará:

`app-debug.apk`

Ese APK se puede copiar al celular Android e instalar.

## Si GitHub no ejecuta la compilación automáticamente
En el repositorio:
- Ve a **Actions**.
- Elige **Compilar APK Android**.
- Pulsa **Run workflow**.

## Seguridad de Android
Como el APK no viene de Google Play, Android puede mostrar:
“Instalar apps desconocidas”.

Debes autorizar temporalmente la instalación desde Chrome, Archivos o la app que estés usando para abrir el APK.

## Sobre iPhone / iOS
Este mismo HTML también puede usarse para iOS con Capacitor, pero Apple exige compilación y firma específica para iPhone. Para distribuir una app iOS instalada como app nativa normalmente se necesita:
- Xcode en macOS, o un servicio de compilación iOS en la nube.
- Certificado/perfil de firma de Apple.
- Para distribución sencilla, una cuenta Apple Developer.

Por eso este ZIP automatiza Android, que es el camino más directo para obtener un instalable.

## Archivos principales
- `www/index.html` — la miniapp que ya funciona en Chrome/Safari.
- `capacitor.config.ts` — configuración de Capacitor.
- `package.json` — dependencias.
- `.github/workflows/build-android.yml` — automatiza la generación del APK.
