# Programação orientada a objetos em Java
A programação orientada a objetos (OOP) é um paradigma de programação baseado no
conceito de "classes" e "objetos". Java é uma linguagem de programação
que segue de perto os princípios da OOP. Aqui estão alguns conceitos-chave:

## Princípios

### 1. Classes e objetos
Em Java, tudo é implementado por meio de classes e objetos. Uma **classe** é um
projeto ou modelo a partir do qual são criados **objetos**. Um objeto é uma
instância de uma classe.

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
O encapsulamento em Java é obtido declarando os atributos da classe como 
privados e fornecendo métodos públicos (getters e setters) para acessar e 
modificar esses atributos. Esses atributos

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

### 3. Herança
O Java oferece suporte à herança, o que permite que uma classe herde atributos e
métodos de outra classe. outra classe. A herança é obtida por meio da 
palavra-chave extends.

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
O Java permite o polimorfismo, o que significa que um objeto pode assumir várias
formas. Isso é obtido por meio da sobrecarga de métodos e da implementação de 
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

### 5. Abstração
O Java permite a abstração, que envolve a simplificação e a modelagem de 
conceitos reais em classes e objetos. A abstração é obtida por meio da 
declaração de classes e ‘interfaces’ abstratas

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
Os conceitos de OOP podem ser aprendidos em várias fontes. Aqui estão alguns
links úteis:

- [Javatpoint](https://www.javatpoint.com/java-oops-concepts)
- [Tutorialspoint](https://www.tutorialspoint.com/java/java_object_classes.htm)
- [W3schools](https://www.w3schools.com/java/java_oop.asp)
- [Geeksforgeeks](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)
- [Youtube](https://www.youtube.com/watch?v=tcza2FEz4u4&list=PLQxX2eiEaqbwNP20GMMCjRslRq2lOLWlg&index=2)