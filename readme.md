compilar sass
1. sassmeister
2. Node sass
3. codepen
4. Prepros
5. Webpack

npm i -g node-sass
node-sass -w styles.scss styles.css
node-sass --watch styles.scss styles.css

### indico carpeta de entrada y salida
node-sass -w scss --output css
node-sass -w scss -o css

node-sass -w scss -o css --output-style=expanded | compressed | nested

## agrega la linea de scss que lo origino cada estilo
node-sass -w scss -o css --output-style=compact --source-comments


Mixins 
codigo reutilizable que pueden tener selectores, reglas css y logica interna.

podemos tener mixins para tipografias, botones, media queries, etc

## Funciones
es un codigo cuyo objetivo es devolver un valor final

## Paleta de colores HSL
https://color.adobe.com


## Wheel hsl

https://www.google.com/search?q=wheel+hsl&sxsrf=ALeKk03706H_PKgbCn0ynNco-gJgv5b2yA:1607896496669&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjszJOc-cvtAhX6ILkGHbk2B_4Q_AUoAXoECA8QAw&biw=1195&bih=745#imgrc=AALvJSsYnQtYNM


## estructura de proyecto
SMACSS
  base (etiquetas HTML) normalize va en esta carpeta.
  modulos (componentes reusables)
  layout (geometria y posicion) es como se divide la pantalla
  theme (tipografia y color, identidad visual de la marca)
  estado (elementos q cambian)

https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/

ITCSS
  settings (variables)
  tools (mixins)
  generic (igual que base en SMACSS) reset and/or normalize styles
  elements (igual que base en SMACSS)
  objects (igual que modulos en SMACSS)
  components
  utilities

7in1

sass/
|
|– base/
|   |– _reset.scss       # Reset/normalize
|   |– _typography.scss  # Typography rules
|   ...                  # Etc…
|
|– components/
|   |– _buttons.scss     # Buttons
|   |– _carousel.scss    # Carousel
|   |– _cover.scss       # Cover
|   |– _dropdown.scss    # Dropdown
|   ...                  # Etc…
|
|– layout/
|   |– _navigation.scss  # Navigation
|   |– _grid.scss        # Grid system
|   |– _header.scss      # Header
|   |– _footer.scss      # Footer
|   |– _sidebar.scss     # Sidebar
|   |– _forms.scss       # Forms
|   ...                  # Etc…
|
|– pages/
|   |– _home.scss        # Home specific styles
|   |– _contact.scss     # Contact specific styles
|   ...                  # Etc…
|
|– themes/
|   |– _theme.scss       # Default theme
|   |– _admin.scss       # Admin theme
|   ...                  # Etc…
|
|– utils/
|   |– _variables.scss   # Sass Variables
|   |– _functions.scss   # Sass Functions
|   |– _mixins.scss      # Sass Mixins
|   |– _helpers.scss     # Class & placeholders helpers
|
|– vendors/
|   |– _bootstrap.scss   # Bootstrap
|   |– _jquery-ui.scss   # jQuery UI
|   ...                  # Etc…
|
|
`– main.scss             # Main Sass file