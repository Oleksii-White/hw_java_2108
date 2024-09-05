# hw_java_2108
public class Main {
    public static void main(String[] args) {
        Dog dog1 = new Dog("Barsik", "Labrador");
        Dog dog2 = new Dog("noName", "Rotveller");
        Dog dog3 = new Dog("Pushok", "Deutch ovcharka");

        dog1.printDogInfo();
        dog2.printDogInfo();
        dog3.printDogInfo();

        System.out.println("Всего собак: " + Dog.getTotalDogs());
    }
}

//------------------------------------------------------------------------------------------------------------------------------------
//Class Dogs
public class Dog {
        private  String name;
        private  String breed;

        private static int totalDogs = 0;

        public Dog (String name, String breed) {
            this.name = name;
            this.breed = breed;
            totalDogs++;
        }

    public void printDogInfo() {
        System.out.println("Кличка: " + name  + ", " + "Порода: " + breed+ "\n");
    }
    public static int getTotalDogs() {
        return totalDogs;
    }
}
