# unity-coding-conventions
Quiero que mis propios proyectos sigan las mismas convenciones de codificación. Escribí esta nota para no tener que volver a buscar siempre en Google cómo se suponía que algo debía escribirse. Quzás esto también te inspire : )<br>

Estas son en parte, las mejores prácticas de Unity, las convenciones de C # de Microsoft y como me gusta hacerlo yo mismo.<br>

## Pautas de nombres

## Editos de Unity

### Carpetas/Folders
Todas las carpetas raíz (en Archivos) que se crean deben comenzar con un guión bajo (_). De esta manera, al descargar paquetes/assets a Unity, las carpetas no se mezclarán. Ejemplo:<br>

<b>_Scenes</b><br>

Las carpetas dentro de las carpetas raíz se nombrarán usando PascalCase. Ejemplo:<br>

<b>SideQuestScript</b><br>

### Nombres de archivos
Los nombres de archivo en C# son los mismos que el nombre de la clase. Estos nombres estarán escritos en PascalCase. Ejemplo:<br>

<b>GameManager</b><br>

Los archivos de escena están escritos en PascalCase. Ejemplo:<br>

<b>MainMenu</b><br>

#### Jerarquía de GameObject
Tolos los GameObjects usan PascalCase, Mantenga la palabra más descriptivvva a la izquierda, Ejemplo: <br>

<b>FireZombie</b> en lugar de <b> ZombieFire</b>.<br>

El nombre debe de terminar con el tipo de GameObject, por lo que es más fácil ver qué GameObject es. Ejemplo:<br>

<b>PauseButton</b> ó <b>HighScoreBackgroundPanel</b><br>

## Código

### Clases
Las clases están nnescritas en PascalCase. Ejemplo:<br>

<b>GameManager</b><br>

Dicho nombre de clase deberá de ser un sustantivo.

<span style="color:blue">## Interfaces
Las interfaces están escritas en PascalCase. Los nombres de las interfaces deberán empezar por "I". Ejemplo:<br>

<b>IAnimal</b><br>

<span style="color:blue">### Métodos
Todos los métodos están escritos en PascalCase. Ejemplo:<br>

<b>DoThis()</b><br>

Dicho nombre deberá de ser un verbo.

Los parámetros del método están escritos en camelCase. Ejemplo:<br>

<b>DoThis(float num)</b><br>

### Variables y campos
Los campos privados(private) comienzan con un guión bajo (_). Ejemplo:<br>

<b>private int _speedOfCar</b><br>

Los campos públicos se escriben en PascalCase. Ejemplo:<br>

<b>public string NameOfCharacter</b><br>

Las variables locales se escriben en camelCase. Ejemplo:<br>

<b>string myLocalVariable</b><br>

Los valores constantes se escriben en SCREAMING_SNAKE_CASE. Ejemplo:<br>

<b>const string MY_CONST_STRING</b><br>

### Enums
Enums debe estar escrito en PascalCase. El nombre deberá de ser en singular. Ejemplo:<br>

<b>public enum Status {Idle,NotSet}</b><br>

### Atributos
Cuadno se usan atributos con propiedades, se marca en la misma línea y no por separado. Ejemplo:<br>

<b>[SerializeField] private float _speed</b><br>
En lugar de:<br>
<b>[SerializeField]</b><br>
<b>private flaot _speed</b>

## Namespaces
Los Namespaces están escritos en PascalCase y los componentes del Namespace deben separarse con períodos. Ejemplo:<br>

<b>namesspace MyAwesomeGame.Enemy</b><br>

### Eventos
los eventos están escritos en PascalCase y termina en "EventHandler". Intenta ser los más descriptivo-específico posible. Ejemplo:
<br>
<b>private void OnPlayerDied() {<br>
&emsp;EndGame();<br>
&emsp;UpdatePlayerScore();<br>
}</b><br>
