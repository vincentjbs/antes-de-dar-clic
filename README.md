# Antes de dar clic

Página de concientización ciudadana sobre fraudes digitales: phishing, smishing, vishing, robo de WhatsApp, suplantación de identidad, duplicado de SIM, ransomware y otros.

Es un solo archivo `index.html` sin dependencias ni build. Todo el JavaScript y el CSS van dentro. Las únicas peticiones externas son las tipografías de Google Fonts.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo, por ejemplo `antes-de-dar-clic`.
2. Sube `index.html` a la raíz del repositorio.
3. Entra a **Settings → Pages**.
4. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`. Guarda.
5. A los dos o tres minutos queda en `https://<usuario>.github.io/antes-de-dar-clic/`.

Desde la terminal:

```bash
git init
git add index.html README.md
git commit -m "Guía de prevención de fraudes digitales"
git branch -M main
git remote add origin https://github.com/<usuario>/antes-de-dar-clic.git
git push -u origin main
```

## Qué contiene

- **Portada animada**: reproduce un intento de smishing bancario y va marcando las cuatro señales que lo delatan. Se puede repetir con el botón.
- **Doce tipos de fraude** agrupados por vía de entrada, con la frase típica y la reacción correcta. Cada ficha se abre al dar clic.
- **Ponte a prueba**: seis mensajes reales, dos de ellos legítimos, con retroalimentación.
- **Listas de verificación** para teléfono, computadora y cuentas, marcables desde el navegador.
- **Qué hacer si ya caíste**, en orden de prioridad.
- **Canales de reporte y denuncia**: Guardia Nacional CERT-MX (088), CONDUSEF, 911 y Fiscalía General del Estado de Morelos, con acceso al portal de Denuncia Digital.

Los iconos de las tarjetas de contacto son SVG genéricos dibujados en el propio archivo, no logotipos oficiales. Si la institución autoriza el uso de los emblemas de CONDUSEF o de la Fiscalía, sustituye el `<svg>` dentro de cada `<span class="ico">` por un `<img>` con el archivo oficial.

## Antes de distribuirla

- Verifica los números de atención en los portales oficiales; cambian de vez en cuando.
- Si la vas a publicar a nombre de una institución, agrega el escudo y el pie de página que corresponda.
- Las listas de verificación no guardan el progreso al recargar, por diseño: no se almacena nada del usuario.

## Personalizar

Los colores y tipografías están en el bloque `:root` al inicio del archivo. Las preguntas del cuestionario están en el arreglo `quiz` dentro del `<script>`, al final.
