# Programación Orientada a Objetos en Java
La programación orientada a objetos (OOP) es un paradigma de programación que se
basa en el concepto de "clases" y "objetos". Java es un lenguaje de programación
que sigue de cerca los principios de la OOP. Aquí hay algunos conceptos clave:

## Requisitos
> Para poder seguir los siguientes ejemplos es necesario seguir esta 
[guía](https://github.com/laboratoria/java-setup) y tener todo listo para
comenzar a programar con Java 🫡

Antes de comenazar con la POO se debe repasar y entener los conceptós básicos
de java. Crea la primera clase del proyecto que contenga el método main. 
Puedes agregar un comando que muestre "¡Hola mundo!", en la consola.
Así podrás verificar si tus configuraciones son correctas.
Además, puedes estudiar conceptos del lenguaje como:

- ¿Qué son las clases y cómo construirlas?
- ¿Qué son los métodos y cómo utilizarlos?
- ¿Qué tipos de datos existen en el lenguaje? (Recuerda los que más usaste en
  JavaScript y trata de buscar tipos similares).
- ¿Cómo crear un array usando Java?
- ¿Qué son los modificadores de acceso como: `public`, `private`, `protected`?
- ¿Qué son los métodos constructores? ¿Cómo hacerlos?
- ¿Qué es el encapsulamiento? ¿Cómo hacerlo?
- ¿Qué es la herencia? ¿Cómo crearla en Java?

Recuerda también utilizar contenidos prácticos para comprender estos conceptos.
¡No pases mucho tiempo solo leyendo o viendo videos!
¡Crea códigos! Inténtalo, equivócate, inténtalo de nuevo, etc.

#### Contenidos que pueden ayudarte en los primeros pasos con Java

- [Learn the Basics of Java Programming](https://www.freecodecamp.org/news/learn-the-basics-of-java-programming/)
- [Programación Orientada a Objetos com Java](https://www.freecodecamp.org/news/object-oriented-programming-concepts-java/)
- [Java Basic Syntax](https://www.geeksforgeeks.org/java-basic-syntax/)
- [Java Data Types And Variables – Explained for Beginners](https://www.freecodecamp.org/news/java-data-types-and-variables/)
- [Learn Java](https://www.w3schools.com/java/default.asp)
- [Java Classes and Objects](https://www.w3schools.com/java/java_classes.asp)
- [Java Methods](https://www.w3schools.com/java/java_methods.asp)

## Principios

### 1. Clases y Objetos
En Java, todo se implementa a través de clases y objetos. Una **clase** es un 
plano o modelo a partir del cual se crean **objetos**. Un objeto es una 
instancia de una clase.

```java
public class Person {
    public String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return this.getName;
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
    }
}
```

### 2. Encapsulamiento
El encapsulamiento en Java se logra declarando atributos de clase como privados
y proporcionando métodos públicos (getters y setters) para acceder y modificar 
esos atributos.

```java
public class Person {
    private String name;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return this.getName;
    }
}
```

### 3. Herencia
Java admite la herencia, que permite que una clase herede atributos y métodos de
otra clase. La herencia se logra mediante la palabra clave extends.

```java
public class Animal {
    private String name;

    public Animal(String name) {
        this.name = name;
    }

    // Método getter y setter
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public void makeSound() {
        System.out.println("🎶🎶🎶🎶🎶🎶🎶");
    }
}

public class Dog extends Animal {
    public Dog(String name) {
        super(name);
    }
    
    @Override
    public void makeSound() {
        System.out.println(getNombre() + " 🐶🐶🐶🐶 ¡Guau Guau!");
    }
}

public class Cat extends Animal {
    public Cat(String name) {
        super(name);
    }

    @Override
    public void makeSound() {
        System.out.println(getNombre() + " 🐱🐱🐱🐱 ¡Miau Miau!");
    }
}
```

### 4. Polimorfismo
Java permite el polimorfismo, lo que significa que un objeto puede tomar muchas 
formas. Esto se logra mediante la sobrecarga de métodos y la implementación de 
interfaces.
```java
public interface MusicalInstrument {
    void play();
}

public class Guitar implements MusicalInstrument {
    @Override
    public void play() {
        System.out.println("🎸🎸🎸🎸🎸🎸");
    }
}
public class Piano implements MusicalInstrument {
    @Override
    public void play() {
        System.out.println("🎹🎹🎹🎹🎹🎹");
    }
}

public class Main {
    public static void main(String[] args) {
        MusicalInstrument guitar = new Guitar();
        MusicalInstrument piano = new Piano();
        
        guitar.play();
        piano.play();
    }
}
```

### 5. Abstracción
Java permite la abstracción, que implica simplificar y modelar conceptos del 
mundo real en clases y objetos. La abstracción se logra mediante la declaración 
de clases abstractas e interfaces.

```java
public abstract class Shape {
    public abstract double calculateArea();

    public void display() {
        System.out.println("This is a shape.");
    }
}

public class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }

    public void displayInfo() {
        System.out.println("This is a circle with radius " + radius);
    }
}

public class Rectangle extends Shape {
    private double length;
    private double width;

    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    @Override
    public double calculateArea() {
        return length * width;
    }

    public void displayInfo() {
        System.out.println("This is a rectangle with length " + length + " and width " + width);
    }
}

public class Main {
    public static void main(String[] args) {
        Circle myCircle = new Circle(5.0);
        Rectangle myRectangle = new Rectangle(4.0, 6.0);

        myCircle.displayInfo();
        System.out.println("Area of the circle: " + myCircle.calculateArea());

        myRectangle.displayInfo();
        System.out.println("Area of the rectangle: " + myRectangle.calculateArea());
    }
}
```

## Referencias
Los conceptos de OOP se pueden aprender de varias fuentes. Aquí hay algunos 
enlaces útiles:

- [Javatpoint](https://www.javatpoint.com/java-oops-concepts)
- [Tutorialspoint](https://www.tutorialspoint.com/java/java_object_classes.htm)
- [W3schools](https://www.w3schools.com/java/java_oop.asp)
- [Geeksforgeeks](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)
- [Youtube](https://www.youtube.com/watch?v=tcza2FEz4u4&list=PLQxX2eiEaqbwNP20GMMCjRslRq2lOLWlg&index=2)