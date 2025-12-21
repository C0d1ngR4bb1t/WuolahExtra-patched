# WuolahExtra ~(FIX)~ (Parcheado, NO FUNCIONA)
### Este script YA NO FUNCIONA.
Wuolah ha hecho unos cambios en su sistema de descarga de archivos, inutilizando la mayoría de funciones. La probabilidad de que me ponga a intentar hacer que por lo menos vuelva a funcionar la descarga sin anuncios de PDFs (por el método de Gulag Cleaner) es nula por motivos académicos y personales. Si en un futuro [pablouser1](https://github.com/pablouser1) actualiza y arregla su script original (puesto que él es el creador original), actualizaré este repositorio (aunque con días/semanas de retraso, seguramente) para avisar. 

## Bugfix del Userscript de @pablouser1 para Wuolah. 

Para usar este programa necesitas un gestor de userscripts (por ejemplo, [ViolentMonkey](https://violentmonkey.github.io) o [TamperMonkey](https://tampermonkey.net)) instalado en tu navegador.

## Funciones implementadas
* Quita anuncios de los pdfs
* Client-side PRO
  * Puedes descargar carpetas dando un click (EN DESARROLLO)
* Limpiar partes de la interfaz innecesarias
  * Publicidad en el fondo
  * Vídeos antes de descargar
* ~Forzar modo oscuro~
### Cambios con el bugfix
* Se ha arreglado el Client-side PRO haciendo que siempre se limpie el caché + algunas cookies innecesarias al acceder a Wuolah con el UserScript (y sus opciones) activado. 

## Instalación
Una vez hayas descargado tu gestor de userscripts, descarga el script desde la sección de [Releases](https://github.com/C0d1ngR4bb1t/WuolahExtra-patched/releases), ¡y listo!
Enlace directo de instalación del último release (lanzamiento): [WuolahExtra-patched](https://github.com/C0d1ngR4bb1t/WuolahExtra-patched/releases/latest/download/WuolahExtraPatched.user.js) 

## Configuración
Puedes acceder a la configuración del script desde tu gestor de userscripts en el icono de tu barra de herramientas ([más info](https://wiki.greasespot.net/Greasemonkey_Manual:Monkey_Menu#The_Menu))

### Debug
Muestra información para desarrolladores en la consola

### Métodos de limpieza de PDFs
| Método | Estado | Detalles | Config ID | + info |
| :--: | :--: | :--: | :--: | :--: |
| GulagCleaner | ✅ | **Activado por defecto**, buenos resultados | gulag | [Source](https://github.com/YM162/gulagcleaner) |
| TrolahCleaner | ❌ | **AVISO: CÓDIGO CERRADO**, buenos resultados | trolah | [Web](https://trolah.pp.ua) |
| PDFLib | ❌ | En desarrollo | pdflib | [Source](https://github.com/Hopding/pdf-lib)
| Ninguno | - | Deshabilita todos los sitemas de eliminación de anuncios | none | -

#### TrolahCleaner no funciona
Quizás la web está caída, prueba a acceder directamente para comprobarlo.

### Limpiar UI
Elimina elementos de la interfaz como patrocinios, enlaces sociales...

## Desarrollo (¡NO EMPLEAR!)
### AVISO: Este fork no ha empleado el modo desarrollo para parchear el script de pablouser. Si quieres desarrollar tú mismo el script, usa el [repositorio original](https://github.com/pablouser1/WuolahExtra)
### Instalar dependencias
```bash
yarn install
```

### Modo desarrollo
```bash
yarn dev
```

### Modo producción
```bash
yarn build
```

## TODO
* Para los métodos GULAG / PDFLib
  * Eliminar los anuncios de los pdfs contenidos en los zips
  * Encontrar la forma de sacar el nombre original del archivo
* Eliminar dependencia `GM_config` e implementar la configuración usando exclusivamente `GM.getValue` y `GM.setValue`
* Arreglar e implementar la función de descargar carpetas sin estar suscrito al el plan PRO.
* Hacer que este bugfix (WuolahExtra-Patched) esté presente en el Código del `master` branch para que sea posible su desarrollo y producción más allá de que sólo sea posible obtener el Release del UserScript ya construido/editado.

## Créditos
* [GM_Config](https://github.com/sizzlemctwizzle/GM_config) | [LICENSE](https://github.com/sizzlemctwizzle/GM_config/blob/master/LICENSE)
* [pdflib](https://github.com/Hopding/pdf-lib) | [LICENSE](https://github.com/Hopding/pdf-lib/blob/master/LICENSE.md)
* [gulagcleaner](https://github.com/YM162/gulagcleaner) | [LICENSE](https://github.com/YM162/gulagcleaner/blob/master/LICENSE)
* [pablouser1/WuolahExtra](https://github.com/pablouser1/WuolahExtra)
