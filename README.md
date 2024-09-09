## Custom Hooks
1. useCounter:
    --
    El hook `useCounter` es un hook personalizado que permite manejar de forma sencilla y eficiente un contador en componentes de React. Este hook proporciona funcionalidad para incrementar, decrementar y restablecer el valor del contador, con la capacidad de personalizar el valor inicial y ajustar los pasos de incremento/decremento.

    Instalacion:
    --

    Este hook esta diseñado para ser utilizado en cualquier proyecto de React, por lo que no requiere instalacion adicional de dependencias.

    Parametros:
    --
    - `initialValue (opcional)`: El valor inicial del contador. Por defecto es 10.

    Retorno:
    --
    El hook devuelve un objeto con los siguientes valores:

    El hook retorna un objeto que contiene:

    - `counter`: El valor actual del contador.

    - `increment`: La funcion para incrementar el contador.

    - `decrement`: La funcion para decrementar el contador.

    - `reset`: La funcion para reiniciar el contador al valor inicial.

2. useFetch:
    --
    
    El hook `useFetch` es un hook personalizado que facilita la obtención de datos desde una API de manera eficiente y con manejo de estado integrado. Tambien implementa un sistema de **cache local** para optimizar las solicitudes repetidas a la misma URL.

    Instalacion:
    --
    No se requiere instalación adicional. Este hook está diseñado para ser utilizado directamente en cualquier proyecto de React.

    Parametros:
    --
    - `url`: La URL desde la cual se obtendran los datos.

    Retorno:
    --
    El hook devuelve un objeto con los siguientes valores:

    - `data`: Los datos obtenidos de la API. Inicialmente es `null` hasta que los datos sean recibidos.
    - `isLoading`: Un booleano que indica si los datos están siendo cargados. Por defecto, es `true` hasta que se completa la solicitud.
    - `hasError`: Un booleano que indica si ocurrió un error al realizar la solicitud.

3. useForm:
    --

    El hook `useForm` es un hook personalizado que simplifica el manejo del estado de formularios en aplicaciones React. Proporciona una forma sencilla de gestionar los valores de los inputs, actualizarlos y restablecer el formulario.

    Instalacion:
    --
    No se requiere instalacion adicional. Este hook esta listo para ser utilizado en cualquier proyecto de React.

    Parametros:
    --
    - `initialForm`: Un objeto que representa el estado inicial del formulario. Cada propiedad debe corresponder con un campo del formulario.

    Retorno:
    --

    El hook devuelve un objeto con los siguientes valores y funciones:

    - `formState`: Un objeto que contiene el estado actual de todos los campos del formulario.
    - `...formState`: El estado de cada campo del formulario como propiedades individuales. Esto permite acceder a cada campo de manera directa.
    - `onInputChange`: Una funcion que maneja el cambio de valor de los inputs, actualizando el estado del formulario de manera automatica.
    - `onResetForm`: Una función que restablece el formulario a su estado inicial.
  
4. useTodos:
    --
    
    El hook `useTodos` es un hook personalizado que permite gestionar una lista de tareas (todos) con las operaciones comunes de agregar, eliminar y marcar como completada. También utiliza `localStorage` para persistir las tareas en el navegador, de modo que la lista se mantenga incluso tras recargar la página.

    Instalacion:
    --

    Este hook no requiere ninguna instalacian adicional, ya que está diseñado para ser utilizado directamente en cualquier proyecto de React.

    Parametros:
    --

    No requiere parámetros directos, ya que gestiona el estado de las tareas (todos) de forma interna.

    Retorno:
    --

    El hook devuelve un objeto con las siguientes propiedades y funciones:

    - **`todos`**: La lista actual de tareas.
    - **`handleNewTodo`**: Funcion para agregar una nueva tarea. Toma un objeto `todo` como argumento.
    - **`handleDeleteTodo`**: Funcion para eliminar una tarea por su `id`.
    - **`handleToggleTodo`**: Funcion para alternar el estado de completado de una tarea (completa/incompleta) por su `id`.
    - **`todosCount`**: El numero total de tareas en la lista.
    - **`pendingTodosCount`**: El numero de tareas pendientes (no completadas).