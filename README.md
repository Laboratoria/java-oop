# Programación Orientada a Objetos en Java
La programación orientada a objetos (OOP) es un paradigma de programación que se
basa en el concepto de "clases" y "objetos". Java es un lenguaje de programación
que sigue de cerca los principios de la OOP. Aquí hay algunos conceptos clave:

## Clases y Objetos
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
    
## Encapsulamiento
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

## Herencia
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

## Polimorfismo
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

## Abstracción
Java permite la abstracción, que implica simplificar y modelar conceptos del mundo real en clases y objetos. La abstracción se logra mediante la declaración de clases abstractas e interfaces.
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

