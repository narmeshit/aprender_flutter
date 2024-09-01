# Flutter

Es un framework de desarrollo de aplicaciones multiplataforma creado por Google. Con él, puedes crear aplicaciones para Android, iOS, web, y escritorio desde una única base de código utilizando el lenguaje Dart.

## Flutter consta de dos partes importantes

- **SDK (Software Development Kit):** Una colección de herramientas que te ayudarán a desarrollar tus aplicaciones. Esto incluye herramientas para compilar tu código en código de máquina nativo (código para iOS y Android).

- **Framework (biblioteca de interfaz de usuario basada en widgets):** Una colección de elementos de interfaz de usuario reutilizables (botones, entradas de texto, controles deslizantes, etc.) que puedes personalizar según tus propias necesidades.

## Flutter se destaca

- **Hot reload:** Permite ver los cambios en la UI de inmediato sin perder el estado de la aplicación.
- **Widgets:** Todo en Flutter es un widget, lo que facilita la personalización y reutilización de componentes.
- **Rendimiento nativo:** Usa el motor gráfico de Skia, que permite gráficos de alta calidad.

## Instalación y Configuración

### ¿Necesito descargar Dart primero?

- No es necesario instalar Dart por separado, ya que el SDK de Flutter incluye el SDK de Dart completo.

### Descargar Flutter SDK

- Visita [flutter.dev](https://flutter.dev) y descarga el SDK

### Configurar el entorno

- Descomprimir el SDK y añade Flutter en tu variable de entorno `PATH`.

### Herramientas de desarrollo

- [Git](https://git-scm.com/downloads) para Windows 2.27 o posterior para administrar el código fuente.
- [Android Studio](https://developer.android.com/studio) 2023.3.1 (Jellyfish) o posterior para depurar y compilar código Java o Kotlin para Android. Flutter requiere la versión completa de Android Studio.
- [Visual Studio Code](https://code.visualstudio.com/download) 1.77 o posterior con la [extensión Flutter para VS Code](https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter).

### Comprueba tu configuración de desarrollo

- **Ejecuta Flutter Doctor:** Comando valida todos los componentes de un entorno de desarrollo Flutter completo para Windows.

```bash
flutter doctor
```

- **Solucionar problemas de Flutter**
Cuando el flutter doctor devuelve un error, podría deberse a Flutter, VS Code, Android Studio, el dispositivo conectado o los recursos de red. Para saber más específico use el siguiente comando.

```bash
flutter doctor -v
```

Verifique la salida para ver si hay otro software que pueda necesitar instalar o si hay otras tareas que realizar.

Si cambia la configuración de su SDK de Flutter o sus componentes relacionados, ejecútelo flutter doctor nuevamente para verificar la instalación.

### Felicitaciones

Una vez que haya instalado todos los requisitos previos y el SDK de Flutter, podrá comenzar a desarrollar aplicaciones de Flutter para Android en Windows.

## Documentación

Puedes aprender mucho de la documentación de Flutter, y todo está muy detallado con ejemplos sencillos para casos de uso básicos. [docs.flutter.dev](https://docs.flutter.dev/)

## Comandos Básicos

### Crear un nuevo proyecto

Este comando crea un nuevo proyecto de Flutter con el nombre especificado.

```bash
flutter create my_first_app
```

### Listar dispositivos conectados o emuladores disponibles

Este comando muestra una lista de dispositivos físicos o emuladores conectados disponibles para ejecutar la aplicación.

```bash
flutter devices
```

### Ejecutar el proyecto

Este comando compila y ejecuta tu aplicación en el emulador o dispositivo conectado.

```bash
flutter run
```

### Depurar la aplicación en modo observador

Esto te permitirá ejecutar la aplicación en modo de depuración y hacer cambios en tiempo real usando Hot Reload y Hot Restart.

```bash
flutter run --debug
```

### Entender la estructura

El código de la app inicial está en `lib/main.dart`. Aquí encontrarás el punto de entrada de la app (`void main()`), y el uso de widgets como `MaterialApp`, `Scaffold`, y `Text`.

### Actualizar dependencias

Este comando actualiza las dependencias del proyecto definidas en el archivo `pubspec.yaml`.

```bash
flutter pub get
```

### Añadir dependencias

Este comando añade una dependencia específica al proyecto en el archivo `pubspec.yaml`.

```bash
flutter pub add nombre_paquete
```

### Limpiar el proyecto

Este comando elimina los archivos generados automáticamente y los archivos temporales del proyecto, lo que puede ayudar a resolver problemas de compilación.

```bash
flutter clean
```

### Mostrar el registro de la aplicación

Este comando muestra el log de la aplicación que se está ejecutando en el dispositivo/emulador.

```bash
flutter logs
```

### Compilar la aplicación

Este comando compila tu aplicación en un archivo ejecutable para la plataforma nombrado.

```bash
flutter build nombre_plataforma
```

### Obtener ayuda sobre los comandos

Muestra la lista de todos los comandos disponibles y opciones de uso.

```bash
flutter help
```

## Conceptos Básicos

### Widget

Los widgets son la base de Flutter. Todo en Flutter es un widget, desde un simple botón hasta un diseño completo de una pantalla. Hay dos tipos principales de widgets:

- **Stateful Widgets:** Son widgets que pueden cambiar de estado durante su vida útil. Se usan cuando la interfaz de usuario depende de datos dinámicos o eventos (como clics o actualizaciones de datos).
- **Stateless Widgets:** Son widgets que no cambian de estado después de ser construidos. Se usan para elementos que no requieren actualizaciones dinámicas (como un título o una imagen fija).

### Árbol de Widgets

Flutter organiza los widgets en un árbol jerárquico. Cada widget puede tener uno o más widgets secundarios, y juntos forman un árbol de widgets. Este árbol define la estructura y apariencia de la interfaz de usuario.

### MaterialApp

Es el widget de nivel superior en una aplicación Flutter que proporciona el diseño y estilo Material Design. Configura el tema de la aplicación, las rutas de navegación y más.

### Scaffold

Es un widget que proporciona la estructura básica para la interfaz de una pantalla, como un AppBar (barra de aplicaciones) y un cuerpo de contenido.

### State

En Flutter, el estado se refiere a cualquier información que pueda cambiar durante la ejecución de la aplicación. El estado de un widget puede actualizarse usando setState(), lo que provoca la reconstrucción del widget para reflejar los nuevos datos.

### Layouts

En Flutter, los layouts o diseños son fundamentales para estructurar la interfaz de usuario. Los widgets que se usan para construir layouts se encargan de organizar y alinear otros widgets en la pantalla.

#### Principales widgets de layout

- **Container:** Un widget versátil que puede tener márgenes, padding, bordes, un tamaño específico y más. Es uno de los bloques de construcción básicos.
- **Column:** Organiza sus hijos en una columna vertical.
- **Row:** Organiza sus hijos en una fila horizontal.
- **Stack:** Permite superponer widgets unos sobre otros.
- **Expanded:** Se utiliza dentro de Row, Column o Flex para que los widgets hijos ocupen el espacio disponible proporcionalmente.
- **Padding:** Añade espacio alrededor de un widget.
- **Align:** Alinea a un widget hijo dentro de su contenedor de acuerdo a una alineación especificada.

### Material Design

Flutter tiene una integración completa con Material Design, el sistema de diseño visual desarrollado por Google. MaterialApp es el widget que habilita Material Design en tu aplicación.

#### Principales componentes

- **AppBar:** Es la barra de aplicaciones que generalmente incluye el título y opciones de acción.
- **Scaffold:** Proporciona una estructura básica con soporte para AppBar, Drawer, SnackBars, y más.
- **FloatingActionButton (FAB):** Un botón flotante que generalmente representa la acción principal de la pantalla.
- **Cards:** Contenedores con bordes redondeados y sombra, usados para agrupar información relacionada.
- **ListTile:** Un widget útil para listas, que contiene un título, subtítulo, ícono y más.

## Navegación y Rutas

Son conceptos esenciales para manejar la navegación entre pantallas o páginas también conocidas como `routes`. Flutter ofrece diferentes formas de gestionar la navegación, desde una navegación sencilla hasta navegaciones más complejas que involucran pilas de rutas y parámetros.

- Ejemplo básico de navegación en Flutter

```dart
//Navigator.push(): Navega a una nueva pantalla empujándola a la pila de navegación.
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondScreen()),
);
//Navigator.pop(): Regresa a la pantalla anterior eliminando la ruta de la pila.
Navigator.pop(context);
```

- Para una navegación más avanzada, puedes usar `Navigator 2.0` o paquetes como `go_router`.

## Gestión del Estado

Es uno de los aspectos más cruciales y, a menudo, desafiantes en el desarrollo de aplicaciones en Flutter. La gestión del estado se refiere a cómo se manejan los datos que cambian con el tiempo en una aplicación y cómo estos datos impactan la interfaz de usuario. Existen diferentes enfoques y patrones para gestionar el estado en Flutter, dependiendo de la complejidad de la aplicación.

### Conceptos Básicos de la Gestión del Estado

#### Estado Local (Local State)

Se refiere al estado que es necesario únicamente dentro de un widget. Este tipo de estado se puede manejar fácilmente utilizando widgets con estado (`StatefulWidget`).

#### Estado Global (Global State)

Es el estado que necesita ser compartido entre múltiples widgets o que debe persistir a través de diferentes pantallas o rutas. Este tipo de estado requiere un enfoque más avanzado para la gestión.

#### StatefulWidget

Es un widget que puede tener un estado mutable. Este tipo de widget se utiliza cuando parte de la interfaz de usuario necesita actualizarse dinámicamente según los cambios en el estado.

#### StatelessWidget

Es un widget que no cambia. No gestiona el estado; simplemente muestra datos estáticos.

#### setState()

Es un método que se usa dentro de un StatefulWidget para notificar al framework que el estado ha cambiado y que la interfaz de usuario debe volver a renderizarse.

### Enfoques para la Gestión del Estado

- **setState():** Este es el enfoque más básico y adecuado para gestionar el estado local en un widget individual. Sin embargo, no es ideal para aplicaciones más complejas o para compartir el estado entre múltiples widgets.

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Contador(),
    );
  }
}

class Contador extends StatefulWidget {
  @override
  _ContadorState createState() => _ContadorState();
}

class _ContadorState extends State<Contador> {
  int _contador = 0;

  void _incrementarContador() {
    setState(() {
      _contador++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Gestión del Estado con setState()'),
      ),
      body: Center(
        child: Text(
          'El contador es: $_contador',
          style: TextStyle(fontSize: 24),
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementarContador,
        child: Icon(Icons.add),
      ),
    );
  }
}

```

- **Provider:** Es un paquete popular para la gestión del estado en Flutter. Proporciona una manera sencilla de compartir el estado entre widgets y es recomendado por el equipo de Flutter.

Primero, agrega la dependencia de `provider` en el archivo `pubspec.yaml`

```dart
import 'package:flutter/material.dart';
import 'package:provider/provider.dart';

void main() {
  runApp(
    ChangeNotifierProvider(
      create: (context) => ContadorModel(),
      child: MyApp(),
    ),
  );
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: ContadorScreen(),
    );
  }
}

class ContadorModel extends ChangeNotifier {
  int _contador = 0;

  int get contador => _contador;

  void incrementar() {
    _contador++;
    notifyListeners();  // Notifica a los widgets que escuchan que el estado ha cambiado.
  }
}

class ContadorScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final contadorModel = Provider.of<ContadorModel>(context);

    return Scaffold(
      appBar: AppBar(
        title: Text('Gestión del Estado con Provider'),
      ),
      body: Center(
        child: Text(
          'El contador es: ${contadorModel.contador}',
          style: TextStyle(fontSize: 24),
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: contadorModel.incrementar,
        child: Icon(Icons.add),
      ),
    );
  }
}
```

- **Riverpod:** Es una evolución de `Provider` que soluciona algunos de sus inconvenientes y simplifica aún más la gestión del estado, especialmente en aplicaciones más grandes.
- **Bloc (Business Logic Component):** Es un patrón de arquitectura y una biblioteca que ayuda a separar la lógica empresarial de la UI. Usa Streams y es ideal para aplicaciones más complejas que requieren una gestión avanzada del estado.
