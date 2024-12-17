// Родительский класс Животное
class Animal {
    // Поля класса
    protected String name;
    protected int age;

    // Конструктор
    public Animal(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Метод для издания звука
    public void makeSound() {
        System.out.println(name + " издает звук.");
    }

    // Метод для отображения информации о животном
    public void displayInfo() {
        System.out.println("Имя: " + name + ", Возраст: " + age + " лет");
    }
}

// Дочерний класс Собака
class Dog extends Animal {
    // Дополнительное поле
    private String breed;

    // Конструктор
    public Dog(String name, int age, String breed) {
        super(name, age);
        this.breed = breed;
    }

    // Переопределенный метод для издания звука
    @id86240433 (@Override)
    public void makeSound() {
        System.out.println(name + " лает: Гав-гав!");
    }

    // Метод, уникальный для класса Собака
    public void fetch() {
        System.out.println(name + " приносит палку.");
    }

    // Метод для отображения информации
    @id86240433 (@Override)
    public void displayInfo() {
        super.displayInfo();
        System.out.println("Порода: " + breed);
    }
}

// Дочерний класс Кошка
class Cat extends Animal {
    // Дополнительное поле
    private String color;

    // Конструктор
    public Cat(String name, int age, String color) {
        super(name, age);
        this.color = color;
    }

    // Переопределенный метод для издания звука
    @id86240433 (@Override)
    public void makeSound() {
        System.out.println(name + " мяукает: Мяу-мяу!");
    }

    // Метод, уникальный для класса Кошка
    public void scratch() {
        System.out.println(name + " точит когти.");
    }

    // Метод для отображения информации
    @id86240433 (@Override)
    public void displayInfo() {
        super.displayInfo();
        System.out.println("Цвет: " + color);
    }
}

// Главный класс для запуска программы
public class Main {
    public static void main(String[] args) {
        // Создаем объект класса Собака
        Dog dog = new Dog("Бобик", 3, "Овчарка");
        dog.displayInfo();
        dog.makeSound();
        dog.fetch();

        System.out.println();

        // Создаем объект класса Кошка
        Cat cat = new Cat("Мурка", 2, "Серый");
        cat.displayInfo();
        cat.makeSound();
        cat.scratch();
    }
}
