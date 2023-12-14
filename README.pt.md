# Programação orientada a objetos em Java
A programação orientada a objetos (OOP) é um paradigma de programação baseado no
conceito de "classes" e "objetos". Java é uma linguagem de programação
que segue de perto os princípios da OOP. Aqui estão alguns conceitos-chave:

## Requisitos
> Para poder seguir os exemplos a seguir, é necessário seguir o seguinte
[guia](https://github.com/Laboratoria/java-setup/blob/main/README.pt.md) 
e ter tudo pronto para começar a programar com Java 🫡

Antes de começar a usar a OOP, você deve revisar e entender os conceitos básicos de Java.
Crie a primeira classe do projeto que contenha o método main.
Você pode adicionar um comando que exiba "Olá mundo!" no console. Assim vc
poderá checar se as suas configurações estão corretas.
Além disso, você pode estudar conceitos da linguagem como:

- O que são classes e como construí-las?
- O que são métodos e como utilizá-los?
- Quais o tipos de dados existentes na linguagem?
(Lembre-se dos que você mais utilizou em JavaScript e tente buscar por tipos similares)
- Como criar um array usando Java?
- O que são modificadores de acesso como: `public`, `private`, `protected`?
- O que são métodos construtores? Como fazê-lo?
- O que é encapsulamento? Como fazê-lo?
- O que é herança? Como criar no Java?

Lembre-se de também utilizar conteúdos práticos para compreender esses
conceitos. Não passe muito tempo somente lendo ou assistindo vídeos!
Crie códigos! Tente, erre, tente de novo, etc.

#### Conteúdos que podem te apoiar nos primeiros passos com Java

- [Learn the Basics of Java Programming](https://www.freecodecamp.org/news/learn-the-basics-of-java-programming/)
- [Programação Orientada a Objetos com Java - Kamila Code](https://www.youtube.com/watch?v=zHPx0vyFMOI&list=PL_pqVN-1MnwNhaNktj8ukfX9yfjWFf7S-)
- [Java Basic Syntax](https://www.geeksforgeeks.org/java-basic-syntax/)
- [Java Data Types And Variables – Explained for Beginners](https://www.freecodecamp.org/news/java-data-types-and-variables/)
- [Learn Java](https://my-learning.w3schools.com/tutorial/java)
- [Java Classes and Objects](https://www.w3schools.com/java/java_classes.asp)
- [Java Methods](https://www.w3schools.com/java/java_methods.asp)

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