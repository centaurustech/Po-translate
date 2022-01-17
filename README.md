# .Po Translator con PHP

Usando la teoría funcional del trabajo realizado por Julio Sánchez en HelpTranslator (LINUX)
https://jsbsan.blogspot.com/2015/02/helptranslator-herramienta-para-ayudar.html,

_Nace este script traductor semi-automático para archivos .PO capaz de ayudar en el proceso de traducción de estos archivos, con PHP._


## BETA 🚀

A futuro, pienso agregarle una interfaz para que cualquier usuario pueda utilizarla sin tener que tocar lineas de codigo, pero, por ahora, es necesario ensuciarse los dedos.

En principio cuenta con dos scripts. El primero **[extraer.php]**, encargado de extraer las frases a ser traducidas del archivo .po a un archivo de texto linea por linea [file_name]_detached.txt, dicho archivo deberá ser traducido con Google, a la par, genera un archivo [file_name]_opt.po (una versión optimizada para poder extraer frases multilineas). El resultado de la traducción de Google deberá ser grabado en otro archivo con nombre [file_name]_traducido.txt para luego ser procesado y combinado con el script **[combinar.php]**. En el proceso combinatorio se utiliza el archivo [file_name]_opt.po y el [file_name]_traducido.txt generando el archivo [file_name]_combinado.po, dicho archivo deberá ser abierto y guardado con PoEdit para la generación del archivo ([file_name].mo).

P.D.: Previa edición del archivo .po con PoEdit, es necesario reemplazar "\\" por "\". Por falta de tiempo aún no llegué a corregir ese detalle.

_(Archivo .po original)_

**[file_name].po**
```
..
msgid "Hello World"
msgstr ""

msgid "Good Morning"
msgstr ""
..
```
_(archivo generado por el script con lineas extraidas del archivo [file\_name].po para ser traducidas en Google Translate® u otro traductor)_

**[file_name]_detached.txt**
```
Hello World
Good Morning
```

_(lineas copiadas desde Google Translate® u otro traductor)_

**[file_name]_traducido.txt**
```
Hola Mundo
Buenos dias
```

_(Archivo resultante de la combinacion de [file\_name].po y [file_name]\_traducido.txt listo para ser verificado con PoEdit®)_

**[file_name]_combinado.po**


### Pre-requisitos 📋

```
- Tener algún servidor web con PHP >=5 corriendo
- Un archivo .po en la misma carpeta del script
```
## Construido con 🛠️

* [PHP] >= 5

## Autores ✒️

* **Ronald Caetano** - *Adaptación a PHP* - [centaurustech](https://github.com/centaurustech)

## Licencia 📄

Oimene nde roga lao ojeipuru la licencia che kavaju. (Libre como el viento)

## Expresiones de Gratitud 🎁

* Comenta a otros sobre este proyecto 📢
* Invita una cerveza 🍺 o un café ☕ a alguien del equipo. 
* Da las gracias públicamente 🤓. (Gracias público)

---
Con ❤️ por [Ronald Caetano](https://github.com/centaurustech) 😊
