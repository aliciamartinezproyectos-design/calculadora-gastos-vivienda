# Casa Clara

Calculadora web estática para estimar la inversión inicial real al comprar una vivienda en España: entrada, impuestos, gastos de compraventa, cuota hipotecaria y mobiliario interactivo.

## Funciones

- Provincia y comunidad autónoma.
- Segunda mano (ITP) u obra nueva (IVA/IGIC + AJD).
- Base de ITP: mayor entre precio y valor de referencia introducido.
- Financiación, TIN, plazo y cuota francesa.
- Comisión de agencia y costes editables.
- Muebles por estancia: activar, quitar, editar precio/cantidad y añadir artículos.
- Guardado local, impresión/PDF, diseño móvil y PWA instalable.
- Sin servidor, dependencias, cookies ni envío de datos.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube el contenido de esta carpeta a la rama `main`.
3. Ve a **Settings > Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**.
5. Selecciona `main` y `/ (root)`, y pulsa **Save**.

También se incluye un workflow en `.github/workflows/pages.yml` para despliegue automático. Si lo usas, selecciona **GitHub Actions** como fuente de Pages.

## Ejecutar en local

Puedes abrir `index.html` directamente. Para probar la instalación PWA y el service worker, sirve la carpeta por HTTP:

```bash
python -m http.server 8000
```

Después abre `http://localhost:8000`.

## Criterios de cálculo

Los tipos precargados son generales y orientativos para 2026. Varias comunidades aplican tramos o beneficios por edad, renta, discapacidad, familia numerosa, vivienda habitual, VPO, municipio o valor. El usuario puede sobrescribir el tipo fiscal en la interfaz.

El escenario inicial utiliza Madrid, vivienda de 300.000 €, entrada del 20 %, financiación del 80 %, TIN del 2,8 %, plazo de 25 años, comisión inmobiliaria del 3 %, notaría del 0,5 % y registro de la propiedad del 0,25 %. La comisión puede configurarse como 3 %, 3 % + IVA, 2,5 % + IVA o porcentaje personalizado.

## Aviso

No es una autoliquidación ni asesoramiento fiscal, legal o bancario. Antes de firmar, deben verificarse la normativa vigente, la base imponible, los beneficios fiscales y los presupuestos reales.
