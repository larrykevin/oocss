# oocss
Object Oriented CSS


## Ejemplo
Antes de OOCSS

```css
.header-inside {
  width: 980px;
  height: 260px;
  padding: 20px;
  margin: 0 auto;
  position: relative;
  overflow: hidden;
}
```

Algunos de los estilos enumerados aquí son exclusivos del c.header-inside ``` elemento. Pero el resto puede formar un módulo que puedo reutilizar. Entonces puedo abstraer los estilos estructurales en su propia clase reutilizable. Aquí está el resultado:

```css
.globalwidth {
  width: 980px;
  margin: 0 auto;
  position: relative;
  padding-left: 20px;
  padding-right: 20px;
  overflow: hidden;
}

.header-inside {
  padding-top: 20px;
  padding-bottom: 20px;
  height: 260px;
}
```

Los estilos pertenecientes a la clase ```.globalwidth``` cubren lo siguiente:

* Un ancho fijo
* Centrado usando margen: automático
* Posicionamiento relativo para crear un contexto de posicionamiento para elementos secundarios
* Relleno izquierdo y derecho de 20px
* Desbordamiento establecido en "oculto" para borrar


## *Beneficios*

### 1.Sitios web más rápidos: 

Los beneficios de rendimiento de OOCSS deberían ser bastante claros. Si tiene menos estilos que se repiten en su CSS, esto conducirá a tamaños de archivo más pequeños y, por lo tanto, a una descarga más rápida de esos recursos.

Es cierto que el marcado estará más desordenado y, por lo tanto, creará archivos HTML más grandes. Pero en muchos casos, la cantidad de pérdida en el rendimiento del marcado será superada en gran medida por la cantidad de ganancia en el rendimiento de la hoja de estilo.

Otro concepto a tener en cuenta es algo a lo que la wiki de OOCSS se refiere como obsequios de rendimiento . Esto se refiere al hecho de que cada vez que reutiliza algo en su CSS, esencialmente está creando nuevos elementos con estilo sin líneas de código CSS. Para proyectos grandes y de alto tráfico, estos "obsequios" podrían ser una ganancia de rendimiento crucial.

### 2.Mantenimiento de las hojas de estilo

Con OOCSS, en lugar de una hoja de estilo en constante crecimiento llena de guerras de especificidad, tendrá un conjunto de módulos fáciles de mantener donde la cascada natural juega un papel importante.

Al realizar adiciones a un sitio existente, no agregará nuevos estilos al final de su hoja de estilo sin tener en cuenta lo que vino antes. En su lugar, reutilizará los estilos existentes y ampliará sus estilos en función de los conjuntos de reglas existentes.

Con este tipo de previsión, es posible crear páginas completas codificando muy poco CSS. Cualquier módulo CSS existente puede servir como base para todas las páginas nuevas, y cualquier CSS nuevo será mínimo. En algunos casos, es posible que incluso pueda crear una nueva página con estilo completo sin codificar una sola línea de CSS.

Estos beneficios de mantenimiento también se extienden a la solidez de sus hojas de estilo. Debido a que los estilos son modulares, es menos probable que las páginas creadas en OOCSS se rompan cuando un nuevo desarrollador comience a usar la hoja de estilo.

## *DESVENTAJAS*

Para sitios y aplicaciones más pequeños, sin duda podría argumentar que OOCSS sería excesivo. Por lo tanto, no tome este artículo como una defensa de OOCSS en todas las circunstancias; variará según el proyecto.

No obstante, creo que es una buena idea, como mínimo, empezar a pensar en términos de OOCSS en todos sus proyectos. Una vez que lo domine, estoy seguro de que le resultará mucho más fácil hacerlo funcionar en proyectos más grandes donde los beneficios serían más notables y relevantes.


## Algunas Pautas Para La Implementación

Comenzar a trabajar con OOCSS podría llevar tiempo. Todavía estoy trabajando en ello, así que no pretendo tener todas las respuestas y experiencia en esta área.

Pero aquí hay algunas cosas que tal vez quiera comenzar a hacer para ayudarlo a entrar en un modo de pensamiento OOCSS:

* Evite el selector descendente (es decir, no use .sidebar h3)
* Evite las identificaciones como ganchos de estilo
* Evite adjuntar clases a elementos en su hoja de estilo (es decir, no haga div.header / h1.title)
* Excepto en algunos casos raros, evite usar!important
* Use CSS Lint para verificar su CSS (y sepa que tiene opciones y métodos para su locura )
* Usar cuadrículas CSS
* Obviamente, habrá momentos en los que se romperán algunas de estas reglas, pero en general, estos son buenos hábitos para desarrollar y conducirán a hojas de estilo que son más pequeñas y más fáciles de mantener.




