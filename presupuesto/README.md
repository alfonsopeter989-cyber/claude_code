# Presupuesto Familiar · Panel móvil

Dashboard de gastos familiares que se ve en el iPhone (y en cualquier navegador) desde una URL fija,
**sin subir tus datos a internet**.

## Cómo funciona (la idea clave)

La página que se publica en la web es solo el **cascarón** del dashboard: código y una vista de
demostración con datos ficticios. **No contiene ninguna cifra tuya.**

Tus datos reales entran así:

1. Abrís la URL en Safari o Chrome (teléfono o PC).
2. Tocás **▲ Cargar .xlsx** y elegís tu `Presupuesto_Familiar_2026-2027.xlsx`
   (desde iCloud Drive / Archivos en el iPhone, o desde tu carpeta en la PC).
3. El Excel se procesa **dentro del navegador de tu dispositivo**. Nada viaja a la red.
4. Queda guardado **solo en ese dispositivo** (IndexedDB del navegador): al reabrir la URL,
   tus cifras ya aparecen sin volver a cargar el archivo.

El botón **✕ Borrar** elimina los datos guardados de ese dispositivo y vuelve a la demo.
Tu archivo Excel original nunca se toca.

## Privacidad

- La web (GitHub Pages) sirve únicamente el cascarón + datos de demostración.
- Tus cifras nunca se suben: se leen y se guardan en el navegador de cada dispositivo, aislados.
- En un equipo **compartido**, usá **✕ Borrar** al terminar (o cargá el archivo en una ventana
  de incógnito, que no deja rastro al cerrarla).

## Requisitos

- **iPhone/iPad:** Safari con **iOS 16.4 o superior** (el lector de Excel usa `DecompressionStream`).
- **PC/Mac:** cualquier navegador moderno (Chrome, Edge, Safari, Firefox).

## Actualizar tus datos

No hay que "re-publicar" nada: la URL no cambia nunca. Cada mes actualizás tu Excel donde lo tengas
(iCloud, Drive, etc.), abrís la URL y volvés a tocar **▲ Cargar .xlsx** con la versión nueva.

## Publicar / cambiar el dashboard

El único caso en que hay que tocar la web es si querés modificar el **diseño o los gráficos**.
Ahí editás `presupuesto/index.html`, hacés commit y push, y GitHub Pages lo publica solo.
