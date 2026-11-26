class Student {
    String name;
    Student(String n) { name = n; }
    void display() { System.out.println(name); }
}
class Main {
    public static void main(String[] args) {
        Student s = new Student("Rahul");
        s.display();
    }
}
Dockerfile
FROM eclipse-temurin:17
WORKDIR /app
COPY Main.java .
RUN javac Main.java
CMD ["java", "Main"]
Commands
docker build -t constructor .
docker run --rm constructor

