# Java Interface Private Method

* In Java 9, we can create private methods inside an interface.
* Interface allows us to declare private methods that help to share common code between non-abstract methods.

### Private Method

        public class Main {
            public static void main(String[] args) {
                Printable printer = new Printer();
                printer.print();
            }
        }

        public class Printer implements Printable {

        }

        public interface Printable {

            default void print() {
                printSomething();
            }

            private void printSomething() {
                System.out.println("it is interface private method!");
            }
        }

### Private Static Method

        public class Main {
            public static void main(String[] args) {
                Printable.print();
            }
        }

        public interface Printable {

            static void print() {
                printSomething();
            }

            private static void printSomething() {
                System.out.println("it is interface private method!");
            }
        }

### Ref
* https://www.javatpoint.com/java-9-interface-private-methods
