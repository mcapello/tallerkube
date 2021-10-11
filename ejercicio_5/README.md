Healthcheck
Comando que sirve para que una app que corre dentro de un container pueda decir si esta saludable o no. Docker en si mismo puede decir que el status es UP pero la app segun lo que haga, puede contener errores de distintos tipos. Este chequeo puede ser una url que exponga la misma app que de por ejemplo devolver un cod 200 se toma como saludable y con un 400 como no saludable. Esto se puede definir en el mismo dockerfile o en el docker run.

ONBUILD 
Comando que agrega un trigger (puede ser cualquier instruccion) a la imagen para ser ejecutado luego cuando por ejemplo esta imagen se usa como base de otra. En el momento del build de la imagen "hija" se ejecutaran estas instrucciones que lo haran en el contexto de esta nueva imagen. Por ejemplo el seteo de alguna variable de ambiente o correr alguna compilacion o descargar el fuente de algun git.

VOLUME 
Comando que monta por ejemplo un directorio del host a uno dentro del container (tambien se puede hacer referencia a un volumen externo previamente definido) para poder o compartir informacion o tener persistencia ya que cuando se elimina el container se pierde todo lo que esta dentro de el.
