# 🌐 Fundamentos de la programación orientada a objetos (POO)

## 📘 Resumen del Curso
Este curso de **1 hora** introduce a estudiantes de secundaria (de 12 a 17 años) en los **Fundamentos de la programación orientada a objetos**, utilizando **Java** de manera práctica y visual.  
El aprendizaje se basa en ejercicios interactivos en línea y explicaciones simples, sin necesidad de instalar software.

**Duración total:** ~60 minutos  
**Público objetivo:** Estudiantes de 12 a 17 años sin experiencia en programación  
**Prerrequisitos:** Ninguno  
**Herramientas necesarias:** Solo un navegador web (Chrome, Firefox, Safari o Edge)

**📂 Repositorio de código fuente:**  
[Github](https://github.com/upc-pre-202520-1asi0729-7357-CodeCadetz/Course-Plan/tree/main)

---

## 🎬 Secuencia de lecciones

### Lección 1: Primeros Pasos en Java (Integrante 1) — 10–12 minutos

- **Descripción:** En esta lección introductoria se da a enseñar qué es la programación y por qué Java es un lenguaje ideal para principiantes. Conocerás el concepto de variables (cajas para guardar datos) y los tipos de datos básicos: `int` (para números) y `String` (para texto).
- **Enlace:** [Ver la lección 1](https://youtu.be/-FUS9sfPINw)
- **Conclusiones clave:**
    - Programar es dar instrucciones claras a la computadora.
    - Java se usa para crear aplicaciones, juegos y sistemas, y es excelente para empezar.
    - Una variable es una caja etiquetada para guardar un valor.
    - Los tipos de datos básicos son `int` (números enteros) y `String` (texto).
    - Toda instrucción en Java termina con un punto y coma (`;`).

### Lección 2: Lógica y Matemáticas con Java (Integrante 2) — 10–12 minutos

- **Descripción**:  
  Introduce los **operadores y expresiones** en Java (sumas, restas, comparaciones) y cómo usarlos para tomar decisiones y repetir acciones simples. Se trabaja con los tipos de dato `int` y `boolean`, y se muestran ejemplos con `if`, `while` y `for`.

- **Enlace**:  
  [Ver la lección 2](https://www.youtube.com/watch?v=GU94k8-TygQ)

- **Conclusiones clave**:
  - Un `int` sirve para guardar **números enteros**; un `boolean` guarda `true` o `false`.
  - Operadores aritméticos: `+`, `-`, `*`, `/`, `%`.
  - Operadores relacionales: `>`, `<`, `>=`, `<=`, `==`, `!=`.
  - Operadores lógicos: `&&` (y), `||` (o), `!` (no).
  - El `if` permite ejecutar código **solo si** se cumple una condición.
  - Los bucles `while` y `for` permiten **repetir** una acción varias veces.

- **Código final Explicado**
Este es el programa completo que mostramos durante la lección, donde utilizamos:

- Variables `int`
- Operadores aritméticos
- Operadores lógicos y relacionales
- Valores booleanos
- Condiciones con operadores lógicos
- Ciclo `while`

```java
public class Main {
    public static void main(String[] args){

        // --- VARIABLES ENTERAS ---
        int a = 10;
        int b = 3;

        // --- OPERADORES ARITMÉTICOS ---
        int suma = a + b;        // 13
        int resta = a - b;       // 7
        int producto = a * b;    // 30
        int division = a / b;    // 3
        int resto = a % b;       // 1

        // --- MOSTRAR RESULTADOS ---
        System.out.println("Suma: " + suma);
        System.out.println("Resta: " + resta);
        System.out.println("Producto: " + producto);
        System.out.println("División: " + division);
        System.out.println("Resto: " + resto);

        // --- OPERADORES RELACIONALES ---
        boolean esMayor = a > b;        // true
        boolean sonIguales = a == b;    // false

        System.out.println("¿a es mayor que b?: " + esMayor);
        System.out.println("¿a es igual a b?: " + sonIguales);

        // --- OPERADORES LÓGICOS ---
        int edad = 14;
        boolean tieneDNI = true;

        boolean puedeEntrar = edad >= 14 && tieneDNI;
        System.out.println("¿Puede entrar?: " + puedeEntrar);

        // --- CICLO WHILE ---
        int contador = 1;

        while (contador <= 5) {
            System.out.println("Vuelta " + contador);
            contador = contador + 1;
        }
    }
}
```
- **Práctica:** [Click para practicar](https://www.jdoodle.com/ga/ceCcGkGN9P3NPiAk436BUg%3D%3D)

### Lección 3: Reutilizando Código

- **Descripción:**
  En esta lección se introduce el uso de métodos en Java como herramienta para reutilizar código y organizar mejor los programas.
  Se explica cómo crear métodos simples, métodos con parámetros, métodos que devuelven valores y cómo integrar esto con entrada de datos usando Scanner.
  También se muestra un ejemplo práctico para evaluar condiciones con métodos.
- **Enlace:** [Ver la lección](https://www.youtube.com/watch?v=gGJ6L_j6ezY)
- **Consejos clave:**
    - Un método es un bloque de código que podemos llamar cuando lo necesitemos.
    - Un método void no devuelve valores; un método con tipo (int, boolean, String…) sí devuelve.
    - Los parámetros permiten enviar información al método.
    - La palabra clave return permite regresar un resultado.
    - Scanner sirve para leer datos escritos por el usuario.
    - Los métodos hacen que el programa sea más ordenado, reutilizable y fácil de mantener.

- **Código final explicado:** 
Este es el programa usado en la lección. En él aplicamos:
    - Métodos sin parámetros
    - Métodos con parámetros
    - Métodos que retornan valores
    - Entrada de datos con Scanner
    - Uso de return
    - Condiciones utilizando métodos booleanos

```java
import java.util.Scanner;

public class Leccion3Metodos {

    public static void main(String[] args) {
        saludar();
        
        //saludo
        saludarPersona("Marco");
        saludarPersona("Ana");
        
        //entrada del usuario
        Scanner sc = new Scanner(System.in);
        
        System.out.print("Ingresa un número: ");
        int n1 = sc.nextInt();

        System.out.print("Ingresa otro número: ");
        int n2 = sc.nextInt();
        
        //uso del metodo sumar
        int suma = sumar(n1,n2);
        System.out.println("El resultado de la suma es" + suma);
        
        sc.close();
        
        // uso del metodo espar
        
        if(esPar(n1))
        {
            System.out.println("El primer numero es par.");
        }
        else{
            System.out.println("El primer numero es impar.");
        }
        
        sc.close();
        
    }
    
    public static void saludar() {
        System.out.println("Hola, bienvenido a la lección de métodos.");
    }
    
    public static void saludarPersona(String nombre) {
        System.out.println("Hola " + nombre + ", ¡bienvenido!");
    }
    
    public static int sumar(int a, int b) {
        int resultado = a + b;
        return resultado;
    }
    
    public static boolean esPar(int numero) {
        return numero % 2 == 0;
    } 
}

```

- **Práctica:** [Click para practicar](https://www.jdoodle.com/ga/Wd5Njxe4QjWoTeJsJU1zBg%3D%3D)

### Lección 4: Introducción a POO

- **Descripción:** Aprende las bases de la Programación Orientada a Objetos en Java: qué son las **clases**, **objetos**, **atributos**, **métodos** y **constructores**, y cómo usarlos para crear tus propias estructuras y modelos en tus programas.

- **Enlace:** [Ver la lección](https://www.youtube.com/watch?v=Zo160ZtZN4E&list=PLfTXn7hHkOOXuwp1E9n_959lazKXyTrsI)
- **Conclusiones clave:**
  - Una **clase** es una plantilla.  
  - Un **objeto** es un ejemplo real creado a partir de esa plantilla.  
  - Los **atributos** almacenan información del objeto.  
  - Los **métodos** definen acciones.  
  - Los **constructores** permiten iniciar objetos con datos.
    
- **Práctica:** [Click para practicar](https://www.jdoodle.com/ga/NLbUp2gspHHe8pd0bKVBHA%3D%3D) 👈 **¡Inicio rápido!**

- **Código final Explicado**
  
  - POO sin constructor:

```java
// Definición de clase
class Persona {
    String nombre; //atributo
    int edad; //atributo
    
    //método
    void saludar() {
        System.out.println("Hola, soy " + nombre + " y tengo " + edad + " años ");
    } 
}

// Creación de objeto
public class Main {
    public static void main(String[] args) {
        Persona p1 = new Persona();
        p1.nombre = "Ana";
        p1.edad = 16;
        p1.saludar(); 
    }
}
```

 - POO con constructor:

```java
class Persona {
    String nombre;
    int edad;
    int peso;

    // Constructor
    Persona(String n, int e, int p) {
        nombre = n;
        edad = e;
        peso=p;
    }

    void saludar() {
        System.out.println("Hola, soy " + nombre + "  ,tengo " + edad + " años y peso " + peso + "kg.");
    }
}

public class Main {
    public static void main(String[] args) {
        Persona p1 = new Persona("Ana", 16, 45);
        Persona p2 = new Persona("Luis", 17, 57);
        Persona p3 = new Persona("Jorge", 15, 60);
        p1.saludar();
        p2.saludar();
        p3.saludar();
    }
}
```

### Lección 5: Fundamentos Avanzados de POO

- **Descripción:** 
- **Enlace:** [Ver la lección](https://www.youtube.com/watch?v=8IqthtFUUSs)
- **Consejos clave:**
- **Práctica:**
 

### Lección 6: Proyecto Final y Consejos

- **Descripción:** 
- **Enlace:** [Ver la lección]()
- **Consejos clave:**
- **Práctica:**
 

## 📁 Recursos adicionales

- **Código fuente completo:**


## 👥 Elaboración

**Universidad Peruana de Ciencias Aplicadas (UPC)**  

**Carrera:** Ingeniería de Software  

**Curso:** 1ASI0729 – Desarrollo de Aplicaciones Open Source

**Ciclo académico:** 202520  

**NRC:** 7357 

**Nombre del equipo:** SenseEat

**Líder del equipo:** Vega Coronado Fabricio Samir
**Integrantes del equipo:**
- Villanueva Andrade Ysaac Ligorio
- Tumi Oliden Manuel Ignacio
- Valverde Portuguez Natalia Ximena
- Romina Alejandra Tuesta Marin 

  **Fecha de entrega:** Domingo 16 de noviembre de 2025
