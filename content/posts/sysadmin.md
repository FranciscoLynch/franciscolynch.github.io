---
title: "Administrador de sistemas"
date: 2026-08-09
draft: false
tags: ["sysadmin", "devops", "sre", "linux"]
summary: "Introducción a la administración de sistemas de manera sencilla."
---

<u>Mi idea:</u> presentar una introducción para que una persona como mi madre (sin ofenderte mamá) pueda entender qué hace un SysAdmin (administrador de sistemas), esencialmente.

--- 
## Parte 1 - ¿Qué es un administrador de sistemas?

Esta es la pregunta que me hacen cuando me preguntan a qué me dedico: "**¿Y qué es un administrador de sistemas, qué hace?**"

Con 23 años (de edad, no de experiencia) apenas sorteo el momento respondiendo que administro sistemas informáticos, eso implica configurar diversas cosas para asegurarme de que un servicio o programa informático funcione correctamente.

Algo muy vago y generalista.

Para que me entiendan un poco mejor a veces explico que es como administrar una computadora hogareña (la cual es usada talvez por 4 o 5 personas) y que, por ejemplo: 
- En determinados momentos uno quiere usar el navegador para ver los emails y todo se pone muy lento, lo cual es muy molesto. 
- O tal vez en algún momento se tilda y no saben por qué, teniendo que reiniciarla cada ciertas horas. 
- O tal vez llega un momento en el que se quedan sin espacio para guardar fotos y no saben cómo agregar más. 

Bueno, eso es de lo que se encarga un administrador de sistemas en un nivel muy básico, de arreglar ese tipo de problemas.

Yendo a una definición más puntual, una persona con este rol es la encargada de **garantizar que el software de la organización genere valor de negocio de forma continua, segura, predecible y eficiente**.

- Software. 
- Generar valor de negocio.
- De forma continua, segura, predecible y eficiente.

Vamos a detenernos en cada una de estas palabras por un momento para que pueda aclararlas y que sea más fácil la comprensión.

### Software 

¿Qué es? Bueno, el software es la parte "**lógica**" de un dispositivo, es lo que permite que podamos utilizar la parte **física** del dispositivo. 

El dispositivo físico como tal es **una herramienta** en la que podemos almacenar, transformar e intercambiar información de todo tipo. El software es un sistema operativo como **Windows**, que tiene herramientas que también son software, como por ejemplo una calculadora, archivos de texto o navegadores web. 

En resumen, el software es lo que nos permite usar los recursos físicos (memorias, chips, cables, etc) para crear, almacenar, modificar, transformar, eliminar e intercambiar información.

### Generar valor de negocio

Es tan sencillo como que **una empresa no crea software por amor al arte (o tal vez si), sino que lo crea para resolver un problema o hacer la vida más fácil a sus usuarios** (y obviamente poder beneficiarse en el proceso, es ganar de ambos lados).

El "valor de negocio" es el beneficio que ese software genera. Por ejemplo:

- Para un banco, el valor es que puedas transferir dinero desde tu celular en 10 segundos.
- Para un comercio electrónico (e-commerce), es que puedas comprar unas zapatillas sin que la página se caiga.
- Para un hospital, es que el médico pueda ver el historial clínico en pantalla sin esperar 20 minutos a que cargue.

Si el software no funciona, la empresa no puede operar, pierde dinero y/o decepciona a la gente. Generar valor significa que **el programa realmente cumpla su función y sea útil.**

### ¿Qué sería generar valor de forma **continua, segura, predecible y eficiente**?
	
- **De forma continua:** significa que se trabaje para que el servicio no se caiga nunca, o que, si algo falla, en lo posible se recupere tan rápido que nadie logre darse cuenta. Imaginate querer hacer una transferencia en el banco y no poder porque dice: "Cerrado por mantenimiento, vuelva en otro momento".
- **Segura:** significa proteger los datos para que solo quienes tengan permiso puedan acceder a su información y nadie externo pueda robarla. Sería el equivalente a poner rejas, cerraduras y alarmas.
- **Predecible:** significa que el sistema se comporte siempre de forma estable y esperada constantemente de ser posible, porque si tarda 1 segundo cuando hay 10 usuarios, pero tarda 10 segundos o más cuando hay 10.000, perjudica la experiencia de los usuarios y por ende, la del servicio y la empresa.
- **Eficiente:** significa lograr que todo funcione rápido y seguro **sin gastar recursos de más**. Si para que funcione mejor tenes que utilizar mayor poder de computo (es decir, más CPUs y/o memoria RAM), quiere decir que el sistema no es tan eficiente como podría y para solucionar las faltas del mismo hay que agregar hardware.

### En conclusión

Básicamente el administrador de sistemas es la persona detrás de escena asegurándose de que la infraestructura que sostiene los servicios de la empresa funcione correctamente.

--- 

## Parte 2 - Detrás de escena -- ¿Cómo se logra y cuál es la complejidad real?

Habiendo explicado qué es un SysAdmin, ahora me gustaría ahondar en lo interesante: **¿cómo lo hace?, ¿qué es lo que necesita para garantizar que el software genere valor?, ¿cuál es la complejidad detrás de este rol?**

Primero y principal creo que hay que entender algo fundamental: **¿qué necesita el software para "vivir"?**. Después de todo, es lo que uno en este rol debe alojar y cuidar, no?

Bueno, un programa o una aplicación es una secuencia de instrucciones digitales que necesita un lugar físico para poder existir y ejecutarse. Así como un pez necesita agua, o un auto necesita una calle, combustible y un motor para andar, el software necesita **condiciones básicas para funcionar**:

1. **Poder de cómputo:** Son la CPU y la Memoria RAM, que procesan las órdenes del programa instante a instante (sería como el cerebro que se encarga de procesar y almacenar temporalmente las tareas).
2. **Espacio para guardar cosas:** nos referimos al espacio de almacenamiento en discos. Sería la estantería digital donde el programa guarda su información (bases de datos, archivos, imágenes).
3. **Caminos para comunicarse:** Son las redes informáticas que permiten la conectividad (los cables, puertos y rutas virtuales), la cual permite que la información viaje desde el celular del usuario hasta el servidor de la empresa y vuelva.
4. **Un piso firme:** El sistema operativo. Esta es la capa base (generalmente Linux, aunque también está Windows) que organiza y gestiona todo lo anterior.

Si falta alguno de estos cuatro elementos, o si uno solo está mal configurado, el software se traba o directamente deja de existir para los usuarios.

Teniendo esto en cuenta, me gustaría profundizar en **Los Sistemas Operativos** ya que es la base fundamental de un administrador de sistemas y con lo que generalmente se comienza. 

Independientemente de si es Linux, Windows u otro, me pregunto **¿qué es lo que hay que saber para lograr administrar un sistema correctamente?**

A nivel abstracto, todo sistema operativo cumple el mismo rol (administrar el hardware y ofrecer un entorno a los programas). Por ende, en cualquier SO tenés que dominar **seis pilares**:

1. **Gestión de Recursos:** Cómo se mide, se asigna y limita la CPU (Unidad de Procesamiento Central), Memoria RAM, E/S de disco y de red, y qué hace el sistema cuando estos se agotan.
2. **Ciclo de Vida de Procesos y Servicios:** Qué es un proceso, cómo se inicia, cómo corre en segundo plano (_daemon/service_), cómo se configura su reinicio automático y cómo se detiene.
3. **Seguridad y Permisos:** Quién puede ejecutar qué (_autenticación_), a qué archivos o recursos puede acceder (_autorización_) y cómo se aíslan los usuarios/procesos.
4. **Almacenamiento y Archivos:** Cómo persiste la información en disco, cómo se estructuran las particiones/volúmenes y cómo se gestionan las lecturas/escrituras.
5. **Red e Interfaces:** Cómo el sistema expone puertos, maneja la tabla de enrutamiento y aplica reglas de filtrado/firewall para recibir o enviar tráfico.
6. **Registros y Estado (Logging):** Dónde escribe el sistema cuando algo falla y cómo consultar la salud interna mediante logs e inspección de estados.

Después de esto mi mamá ya debe haber dejado de leer de lo mareada que quedo, espero estar subestimandote mamá :)

Para concluir, esos son los pilares que uno debe buscar entender y dominar si quiere lograr administrar sistemas operativos de la mejor manera posible.

Ahora, para seguir comprendiendo la complejidad a la que enfrenta un SysAdmin en general, hay que entender que no todo el software se aloja de la misma manera. La forma de gestionarlo va a variar según:

- **La arquitectura de la aplicación:** ¿Es un monolito clásico todo-en-uno, o son microservicios independientes que se comunican por API?
- **La demanda y tolerancia al escalado:** ¿Maneja un tráfico constante y predecible, o sufre picos masivos donde necesita multiplicar sus instancias en segundos?
- **El nivel de aislamiento y regulaciones:** ¿Requiere correr en hardware físico dedicado por normas de seguridad (_Bare Metal_), o puede compartir infraestructura virtualizada en la nube?
- **La complejidad operativa y costos:** ¿Tenés capacidad para mantener tus propios servidores (IaaS), preferís empaquetar todo en contenedores usando herramientas modernas como Kubernetes (CaaS), o directamente delegar toda la infraestructura para despreocuparte de los servidores (PaaS / Serverless)? (Nombres raros en inglés que dejaremos para otro post).


### En desarollo...