# unity-coding-conventions
Quiero que mis propios proyectos sigan las mismas convenciones de codificación. Escribí esta nota para no tener que volver a buscar siempre en Google cómo se suponía que algo debía escribirse. Quzás esto también te inspire : )<br>

Estas son en parte, las mejores prácticas de Unity, las convenciones de C # de Microsoft y como me gusta hacerlo yo mismo.<br>

## Convenciones de Nombramientos

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

### Clases
Las clases están nnescritas en PascalCase. Ejemplo:<br>

<b>GameManager</b><br>

Dicho nombre de clase deberá de ser un sustantivo.

### Métodos
Todos los métodos están escritos en PascalCase. Ejemplo:<br>

<b>DoThis()</b><br>

Dicho nombre deberá de ser un verbo.

Los parámetros del método están escritos en camelCase. Ejemplo:<br>

<b>DoThis(float num)</b><br>

### Static Field
Todos los static fields se escribirán en PascalCase. Ejemplo:<br>

<b> public static int SomeStaticValue = 10;</b><br>

### Propiedades
Todas las propiedades usarán PascalCase. Ejemplo:<br>
<b>private string name;<br>
private string Name<br>
{<br>
&emsp;get<br>
&emsp;{<br>
&emsp;&emsp;return name;<br>
&emsp;}<br>
&emsp;set<br>
&emsp;{<br> 
&emsp;&emsp;name = value;<br>
&emsp;}<br>
}<br>

### Parámetros
Deberán estar escritos en camelCase. Ejemplo:<br>

<b>public void SomeMethod(bool someCondition)</b><br>

### Añadir Sufijo "Callback" al delegates
Ejemplo:<br>
//Declara un tipo delegado para procesarun usuario:<br>
<b>public delegatevoid ProcessUserCallback(User u);</b><br>

### Añadir Prefijo "On" a los eventos y acciones
Ejemplo:<br>
<b>public UnityAction OnDeath;</b><br>

### Interfaces
Las interfaces están escritas en PascalCase. Los nombres de las interfaces deberán empezar por "I". Ejemplo:<br>

<b>IAnimal</b><br>

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

### Añadir Sufijo Callback al delegates
//Declara un tipo delegado para procesarun usuario:<br>
<b>public delegatevoid ProcessUserCallback(User u);</b><br>

### Eventos
los eventos están escritos en PascalCase y termina en "EventHandler". Intenta ser los más descriptivo-específico posible. Ejemplo:
<br>
<b>private void OnPlayerDied() {<br>
&emsp;EndGame();<br>
&emsp;UpdatePlayerScore();<br>
}</b><br>

## Prácticas Recomendadas Básicas

### Declaraciones
Se recomienda siempre la utilización de modificadores de nivel de acceso. 

<b>private int Variable;</b><br>

Utilizar una sola declaración por línea. Ayudará a mantener el código más claro y limpio. Ejemplo:<br>

<b>private int firstVariable;<br>
private int secondVariable;</b><br>

### Espaciado
Mantener todo el espaciado correctamente no solo aumentará la velocidad a la que está leyendo el código, sino que también aumentará la legibilidad y ayudará a comprender claramente la lógica del código. Cuando hablamos de espaciado.<br>

#### Llaves {}
Cada llave deberá de ir en su propia línea. Ejemplo:<br>

<b>public void CreateSomething()<br>
{<br>
&emsp;//code<br>
}</b><br>

En el caso de los "case" deberán estar indentados desde el "switch". Ejemplo:<br>

<b>switch (someExpression) <br>
{<br>
&emsp;case 0:<br>
&emsp;&emsp;{<br>
&emsp;&emsp;&emsp;DoSomething();br
&emsp;&emsp;}<br>
&emsp;&emsp;break;<br>
&emsp;case 1:<br>
&emsp;&emsp;{<br>
&emsp;&emsp;&emsp;DoSomethingElse();br
&emsp;&emsp;}<br>
&emsp;&emsp;break;<br>
}<br>
