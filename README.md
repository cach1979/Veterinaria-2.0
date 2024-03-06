package co.edu.uniquindio.poo;

import java.util.ArrayList;
import java.util.Comparator;
import java.util.HashSet;
import java.util.List;
import java.util.Scanner;
import java.util.Set;
import java.util.stream.Collectors;

public record Veterinaria2 (String ID, String nombre, String especie, String raza, String genero, String color, int edad, int peso) {
    
    // Enum con las propiedades

            public class EnumsAnimal {

            public enum especie {

                PERRO, GATO, TORTUGA, PEZ ;
            }
        
            public enum raza {

                PERSA, SIAMES, SIBERIANO, BULLDOG, PASTOR, LABRADOR, GOLFINA, CAGUAMA, CAREY, BETTA, GUPPY, TETRANEON ;
            }
        
            public enum genero {

                MASCULINO, FEMENINO ;
            }
        
            public enum color {
                
                AZUL, VERDE, CAFE, NEGRO, GRIS, BLANCO, MANCHADO, DORADO ;
            }
        
        }

        public static List<Veterinaria2> generateListOfAnimals() {
            List<Veterinaria2> listaVeterinaria2 = new ArrayList<>();
    
           return listaVeterinaria2;
        }
    
        public static List<Veterinaria2> filterAnimalsByAge(List<Veterinaria2> animals, int age) {
            return animals.stream()
                    .filter(animal -> animal.edad() > age)
                    .collect(Collectors.toList());
        }
        
    // Constructor
    public Veterinaria2 {
        assert ID != null && !ID.isBlank() : "El ID debe de ser diferente y unico";
        assert nombre != null && !nombre.isBlank() : "El nombre debe ser diferente";
        assert especie != null && !especie.isBlank() : "La especie debe ser diferente";
        assert raza != null && !raza.isBlank() : "La raza debe ser diferente";
        assert genero != null && !genero.isBlank() : "El género debe ser diferente";
        assert color != null && !color.isBlank() : "El color debe ser diferente";
        assert edad > 0 : "La edad debe ser mayor a cero";
        assert peso > 0 : "El peso debe ser mayor a cero";      
    }

    public void agregarAnimal(List<Veterinaria2> listaVeterinaria2, Set<String> ids) {
        // Lógica para agregar un animal a la lista y verificar los IDs aquí
    }

    public String getID() {
        return ID;
    }

    public static void main(String[] args) {
        
        // Crear una lista de Veterinaria2 utilizando ArrayList
        List<Veterinaria2> listaVeterinaria2 = new ArrayList<>();
        Set<String> ids = new HashSet<>();
        ids.add("001");

        // Crear 60 instancias de Veterinaria2 y agregarlas a la lista

        listaVeterinaria2.add(new Veterinaria2("001","Sasha", "Perro", "Labrador", "Femenino", "Azul", 3, 25));

        listaVeterinaria2.add(new Veterinaria2("002","Simba", "Gato", "Guppy", "Masculino", "Verde", 2, 10));

        listaVeterinaria2.add(new Veterinaria2("003","Puffy", "Tortuga", "Siberiano", "Masculino", "Cafe", 5, 15));

        listaVeterinaria2.add(new Veterinaria2("004","Luna", "Pez", "Persa", "Femenino", "Gris", 4, 12));

        listaVeterinaria2.add(new Veterinaria2("005","Rocky", "Perro", "Bulldog", "Masculino", "Negro", 7, 30));

        listaVeterinaria2.add(new Veterinaria2("006","Bella", "Gato", "Siames", "Femenino", "Verde", 1, 8));

        listaVeterinaria2.add(new Veterinaria2("007","Max", "Tortuga", "Pastor", "Masculino", "Blanco", 15, 28));

        listaVeterinaria2.add(new Veterinaria2("008","Nina", "Pez", "Golfina", "Femenino", "Azul", 3, 18));

        listaVeterinaria2.add(new Veterinaria2("009","Lucky", "Perro", "Labrador", "Masculino", "Verde", 6, 22));

        listaVeterinaria2.add(new Veterinaria2("010","Daisy", "Gato", "Persa", "Femenino", "Verde", 2, 10));

        listaVeterinaria2.add(new Veterinaria2("011","Charlie", "Tortuga", "Caguama", "Masculino", "Cafe", 5, 5));

        listaVeterinaria2.add(new Veterinaria2("012","Milo", "Pez", "Guppy", "Masculino", "Dorado", 3, 14));

        listaVeterinaria2.add(new Veterinaria2("013","Coco", "Perro", "Siberiano", "Masculino", "Verde", 8, 18));

        listaVeterinaria2.add(new Veterinaria2("014","Lola", "Gato", "Carey", "Femenino", "Manchado", 4, 20));

        listaVeterinaria2.add(new Veterinaria2("015","Toby", "Tortuga", "Bulldog", "Masculino", "Negro", 14, 25));

        listaVeterinaria2.add(new Veterinaria2("016","Chloe", "Pez", "Siames", "Femenino", "Verde", 2, 8));

        listaVeterinaria2.add(new Veterinaria2("017","Teddy", "Perro", "Betta", "Masculino", "Azul", 6, 16));

        listaVeterinaria2.add(new Veterinaria2("018","Lucy", "Gato", "Golfina", "Femenino", "Gris", 12, 22));

        listaVeterinaria2.add(new Veterinaria2("019","Buddy", "Perro", "Labrador", "Masculino", "Dorado", 7, 30));

        listaVeterinaria2.add(new Veterinaria2("020","Zoe", "Gato", "Persa", "Femenino", "Verde", 1, 7));

        listaVeterinaria2.add(new Veterinaria2("021","Jack", "Perro", "Pastor", "Masculino", "Azul", 4, 26));

        listaVeterinaria2.add(new Veterinaria2("022","Mia", "Tortuga", "Golfina", "Femenino", "Verde", 3, 15));

        listaVeterinaria2.add(new Veterinaria2("023","Rocky", "Pez", "Caguama", "Masculino", "Cafe", 5, 6));

        listaVeterinaria2.add(new Veterinaria2("024","Luna", "Pez", "Carey", "Femenino", "Manchado", 2, 10));

        listaVeterinaria2.add(new Veterinaria2("025","Max", "Tortuga", "Siberiano", "Masculino", "Verde", 8, 20));

        listaVeterinaria2.add(new Veterinaria2("026","Daisy", "Tortuga", "Guppy", "Femenino", "Gris", 4, 12));

        listaVeterinaria2.add(new Veterinaria2("027","Charlie", "Gato", "Bulldog", "Masculino", "Negro", 5, 28));

        listaVeterinaria2.add(new Veterinaria2("028","Milo", "Gato", "Siames", "Masculino", "Verde", 3, 16));

        listaVeterinaria2.add(new Veterinaria2("029","Charlie", "Perro", "Bulldog", "Masculino", "Negro", 5, 28));

        listaVeterinaria2.add(new Veterinaria2("030","Milo", "Perro", "Siames", "Masculino", "Verde", 3, 16));

        listaVeterinaria2.add(new Veterinaria2("031","Sasha", "Tortuga", "Labrador", "Femenino", "Azul", 3, 25));

        listaVeterinaria2.add(new Veterinaria2("032","Simba", "Pez", "Guppy", "Masculino", "Verde", 2, 10));

        listaVeterinaria2.add(new Veterinaria2("033","Puffy", "Perro", "Siberiano", "Masculino", "Cafe", 5, 15));

        listaVeterinaria2.add(new Veterinaria2("034","Luna", "Gato", "Persa", "Femenino", "Gris", 11, 12));

        listaVeterinaria2.add(new Veterinaria2("035","Rocky", "Tortuga", "Bulldog", "Masculino", "Negro", 7, 30));

        listaVeterinaria2.add(new Veterinaria2("036","Bella", "Pez", "TetraNeon", "Femenino", "Verde", 1, 8));

        listaVeterinaria2.add(new Veterinaria2("037","Max", "Perro", "Pastor", "Masculino", "Blanco", 4, 28));

        listaVeterinaria2.add(new Veterinaria2("038","Nina", "Gato", "Golfina", "Femenino", "Azul", 3, 18));

        listaVeterinaria2.add(new Veterinaria2("039","Lucky", "Perro", "Labrador", "Masculino", "Verde", 6, 22));

        listaVeterinaria2.add(new Veterinaria2("040","Daisy", "Gato", "Persa", "Femenino", "Verde", 2, 10));

        listaVeterinaria2.add(new Veterinaria2("041","Charlie", "Tortuga", "Caguama", "Masculino", "Cafe", 5, 5));

        listaVeterinaria2.add(new Veterinaria2("042","Milo", "Pez", "Guppy", "Masculino", "Gris", 3, 14));

        listaVeterinaria2.add(new Veterinaria2("043","Coco", "Tortuga", "Siberiano", "Masculino", "Verde", 8, 18));

        listaVeterinaria2.add(new Veterinaria2("044","Lola", "Pez", "Carey", "Femenino", "Manchado", 4, 20));

        listaVeterinaria2.add(new Veterinaria2("045","Toby", "Perro", "Bulldog", "Masculino", "Negro", 5, 25));

        listaVeterinaria2.add(new Veterinaria2("046","Chloe", "Tortuga", "Siames", "Femenino", "Verde", 2, 8));

        listaVeterinaria2.add(new Veterinaria2("047","Teddy", "Perro", "Betta", "Masculino", "Azul", 6, 16));

        listaVeterinaria2.add(new Veterinaria2("048","Lucy", "Gato", "Golfina", "Femenino", "Gris", 5, 22));

        listaVeterinaria2.add(new Veterinaria2("049","Buddy", "Tortuga", "TetraNeon", "Masculino", "Blanco", 7, 30));

        listaVeterinaria2.add(new Veterinaria2("050","Zoe", "Gato", "Persa", "Femenino", "Verde", 1, 7));

        listaVeterinaria2.add(new Veterinaria2("051","Jack", "Perro", "Pastor", "Masculino", "Azul", 4, 26));

        listaVeterinaria2.add(new Veterinaria2("052","Mia", "Pez", "Golfina", "Femenino", "Verde", 3, 15));

        listaVeterinaria2.add(new Veterinaria2("053","Rocky", "Perro", "Caguama", "Masculino", "Cafe", 12, 6));

        listaVeterinaria2.add(new Veterinaria2("054","Luna", "Pez", "Carey", "Femenino", "Manchado", 2, 10));

        listaVeterinaria2.add(new Veterinaria2("055","Max", "Perro", "Siberiano", "Masculino", "Verde", 8, 20));

        listaVeterinaria2.add(new Veterinaria2("056","Daisy", "Gato", "Guppy", "Femenino", "Gris", 4, 12));

        listaVeterinaria2.add(new Veterinaria2("057","Charlie", "Perro", "Bulldog", "Masculino", "Negro", 5, 28));

        listaVeterinaria2.add(new Veterinaria2("058","Milo", "Tortuga", "Siames", "Masculino", "Verde", 3, 16));

        listaVeterinaria2.add(new Veterinaria2("059","Charlie", "Perro", "TetraNeon", "Masculino", "Negro", 5, 28));

        listaVeterinaria2.add(new Veterinaria2("060","Milo", "Pez", "Siames", "Masculino", "Verde", 3, 16));

        Set<Integer> idsSet = new HashSet<>();
        boolean repetido = false;

        for (Veterinaria2 mascotas : listaVeterinaria2) {
            if (!idsSet.add(Integer.parseInt(mascotas.getID()))){
                repetido = true;
                break;
            }
        }

        if (repetido) {
            System.out.println("Se verifico la lista de ID está mal y se necesita reestablecer algunos valores.");
        } else {
            System.out.println("Todos los ID están perfectos.");
        }
 
         // Contadores para cada especie
         int contadorPerros = 0;
         int contadorGatos = 0;
         int contadorTortugas = 0;
         int contadorPeces = 0;
 
         // Contadores para cada raza
         int contadorPersas = 0;
         int contadorSiameses = 0;
         int contadorSiberianos = 0;
         int contadorBulldogs = 0;
         int contadorPastores = 0;
         int contadorLabradores = 0;
         int contadorGolfinas = 0;
         int contadorCaguamas = 0;
         int contadorCareys = 0;
         int contadorBettas = 0;
         int contadorGuppys = 0;
         int contadorTetraNeones = 0;
 
         // Contadores para cada genero
         int contadorMasculinos = 0;
         int contadorFemeninos = 0;
 
         // Contadores para cada color
         int contadorAzules = 0;
         int contadorVerdes = 0;
         int contadorCafes = 0;
         int contadorNegros = 0;
         int contadorGrises = 0;
         int contadorBlancos = 0;
         int contadorManchados = 0;
         int contadorDorados = 0;
 
         // Recorre la lista y cuenta cuantas especies hay
         for (Veterinaria2 animal : listaVeterinaria2) {

             if (animal.especie().equals("Perro")) {
                 contadorPerros++;
 
             } else if (animal.especie().equals("Gato")) {
                 contadorGatos++;
 
             } else if (animal.especie().equals("Tortuga")) {
                 contadorTortugas++;
 
             } else if (animal.especie().equals("Pez")) {
                 contadorPeces++;
 
             }
         }
 
         // Recorre la lista y cuenta cuantas razas hay
         for (Veterinaria2 animal : listaVeterinaria2) {

             if (animal.raza().equals("Persa")) {
                 contadorPersas++;
 
             } else if (animal.raza().equals("Siames")) {
                 contadorSiameses++;
 
             } else if (animal.raza().equals("Siberiano")) {
                 contadorSiberianos++;
 
             } else if (animal.raza().equals("Bulldog")) {
                 contadorBulldogs++;
 
             } else if (animal.raza().equals("Pastor")) {
                 contadorPastores++;
 
             } else if (animal.raza().equals("Labrador")) {
                 contadorLabradores++;
 
             } else if (animal.raza().equals("Golfina")) {
                 contadorGolfinas++;
 
             } else if (animal.raza().equals("Caguama")) {
                 contadorCaguamas++;
 
             } else if (animal.raza().equals("Carey")) {
                 contadorCareys++;
 
             } else if (animal.raza().equals("Betta")) {
                 contadorBettas++;
 
             } else if (animal.raza().equals("Guppy")) {
                 contadorGuppys++;
 
             } else if (animal.raza().equals("TetraNeon")) {
                 contadorTetraNeones++;
 
             }
         }
 
         // Recorre la lista y cuenta cuantos generos hay
         for (Veterinaria2 animal : listaVeterinaria2) {
 
             if (animal.genero().equals("Masculino")) {
                 contadorMasculinos++;
 
             } else if (animal.genero().equals("Femenino")) {
                 contadorFemeninos++;
 
             }
         }
 
         // Recorre la lista y cuenta cuantos colores hay
 
         for (Veterinaria2 animal : listaVeterinaria2) {

             if (animal.color().equals("Azul")) {
                 contadorAzules++;
 
             } else if (animal.color().equals("Verde")) {
                 contadorVerdes++;
 
             } else if (animal.color().equals("Cafe")) {
                 contadorCafes++;
 
             } else if (animal.color().equals("Negro")) {
                 contadorNegros++;
 
             } else if (animal.color().equals("Gris")) {
                 contadorGrises++;
 
             } else if (animal.color().equals("Blanco")) {
                 contadorBlancos++;
 
             } else if (animal.color().equals("Manchado")) {
                 contadorManchados++;
 
             } else if (animal.color().equals("Dorado")) {
                 contadorDorados++;
 
             }
         }

        
         for (Veterinaria2 veterinaria2 : listaVeterinaria2) {

            System.out.println("---------------------------------------------------------------------------------------");
            System.out.println("- Nombre: " + veterinaria2.nombre());
            System.out.println("- Especie: " + veterinaria2.especie());
            System.out.println("- Raza: " + veterinaria2.raza());
            System.out.println("- Género: " + veterinaria2.genero());
            System.out.println("- Color: " + veterinaria2.color());
            System.out.println("- Edad: " + veterinaria2.edad());
            System.out.println("- Peso: " + veterinaria2.peso());
            System.out.println("----------------------------------------------------------------------------------------");
            System.out.println();

            
        }

        Scanner scanner = new Scanner(System.in);
        
        // Crear un objeto Scanner para recibir la entrada del usuario

        while (true) {
           
            System.out.println("Ingrese los datos del nuevo animal:");
            System.out.print("ID: ");
            String id = scanner.nextLine();
            System.out.print("Nombre: ");
            String nombre = scanner.nextLine();
            System.out.print("Especie: ");
            String especie = scanner.nextLine();
            System.out.print("Raza: ");
            String raza = scanner.nextLine();
            System.out.print("Género: ");
            String genero = scanner.nextLine();
            System.out.print("Color: ");
            String color = scanner.nextLine();
            System.out.print("Edad: ");
            int edad = Integer.parseInt(scanner.nextLine());
            System.out.print("Peso: ");
            int peso = Integer.parseInt(scanner.nextLine());
        
        
            // Verificar si el ID ya existe en la lista
            if (ids.contains(id)) {
                System.out.println("El ID ingresado ya existe, por favor ingrese uno nuevo.");

                continue;
            }

            // Agregar el nuevo animal a la lista y actualizar el conjunto de IDs
            listaVeterinaria2.add(new Veterinaria2(
                    id.trim(), nombre.trim(), especie.trim(), raza.trim(),
                    genero.trim(), color.trim(), (edad), (peso)
            ));

            ids.add(id.trim());

            System.out.println("Animal agregado correctamente.");

            // Preguntar al usuario si desea agregar otro animal
            System.out.println("¿Desea agregar otro animal? (s/n)");
            String respuesta = scanner.nextLine();
            if (!respuesta.equalsIgnoreCase("s")) {

                break;
                
            }
        }
        scanner.close();
    

        // Mostrar la lista actualizada de animales
        System.out.println("Lista de animales actualizada:");
        for (Veterinaria2 animal : listaVeterinaria2) {
            System.out.println(animal);
        }

            // Filtrar y mostrar solo mascotas mayores de 10 años
            System.out.println("Mascotas mayores de 10 años:");
            System.out.println("----------------------------------------------------------------------------------------");
        
            List<Veterinaria2> mascotasMayores = listaVeterinaria2.stream()
                    .filter(m -> m.edad() > 10)
                    .collect(Collectors.toList());
            for (Veterinaria2 mascota : mascotasMayores) {
                System.out.println(mascota);
                System.out.println("----------------------------------------------------------------------------------------");
            }
        
            // Organizar y mostrar nombres alfabéticamente
            System.out.println("Nombres de mascotas ordenados alfabéticamente:");
            System.out.println("----------------------------------------------------------------------------------------");
        
             List<Veterinaria2> listaVeterinariaOrdenada = listaVeterinaria2.stream().sorted(Comparator.comparing(Veterinaria2::nombre)).collect(Collectors.toCollection(ArrayList::new));
            // List<Veterinaria2> listaVeterinariaOrdenada = listaVeterinaria2.sort(Comparator.comparing(Veterinaria2::nombre));
            for (Veterinaria2 mascota : listaVeterinariaOrdenada) {
                System.out.println(mascota.nombre());
                System.out.println("----------------------------------------------------------------------------------------");
            }
        
            // Organizar y mostrar edades de mayor a menor
            System.out.println("Edades de mascotas ordenadas de mayor a menor:");
            System.out.println("----------------------------------------------------------------------------------------");
        
            listaVeterinaria2.sort(Comparator.comparingInt(Veterinaria2::edad).reversed());
            for (Veterinaria2 mascota : listaVeterinaria2) {
                System.out.println(mascota.edad());
                System.out.println("----------------------------------------------------------------------------------------");
            }
        
        // Imprimir la información de cada contador de especie
        System.out.println("----------------------------------------------------------------------------------------");
        System.out.println("Contador de especies:");
        System.out.println("Número de Perros: " + contadorPerros);
        System.out.println("Número de Gatos: " + contadorGatos);
        System.out.println("Número de Tortugas: " + contadorTortugas);
        System.out.println("Número de Peces: " + contadorPeces);
        System.out.println("----------------------------------------------------------------------------------------");
        
        // Imprimir la información de cada contador de raza
        System.out.println("----------------------------------------------------------------------------------------");
        System.out.println("Contador de razas:");
        System.out.println("Persas: " + contadorPersas);
        System.out.println("Siameses: " + contadorSiameses);
        System.out.println("Siberianos: " + contadorSiberianos);
        System.out.println("Bulldogs: " + contadorBulldogs);
        System.out.println("Pastores: " + contadorPastores);
        System.out.println("Labradores: " + contadorLabradores);
        System.out.println("Golfinas: " + contadorGolfinas);
        System.out.println("Caguamas: " + contadorCaguamas);
        System.out.println("Careys: " + contadorCareys);
        System.out.println("Bettas: " + contadorBettas);
        System.out.println("Guppys: " + contadorGuppys);
        System.out.println("TetraNeones: " + contadorTetraNeones);
        System.out.println("----------------------------------------------------------------------------------------");
        
        // Imprimir la información de cada contador de genero
        System.out.println("----------------------------------------------------------------------------------------");
        System.out.println("\nContador de géneros:");
        System.out.println("Masculinos: " + contadorMasculinos);
        System.out.println("Femeninos: " + contadorFemeninos);
        System.out.println("----------------------------------------------------------------------------------------");
        
        // Imprimir la información de cada contador de colores
        System.out.println("----------------------------------------------------------------------------------------");
        System.out.println("\nContador de colores:");
        System.out.println("Azules: " + contadorAzules);
        System.out.println("Verdes: " + contadorVerdes);
        System.out.println("Cafes: " + contadorCafes);
        System.out.println("Negros: " + contadorNegros);
        System.out.println("Gris: " + contadorGrises);
        System.out.println("Blancos: " + contadorBlancos);
        System.out.println("Manchados: " + contadorManchados);
        System.out.println("Dorados: " + contadorDorados);
        System.out.println("----------------------------------------------------------------------------------------");

    }
}
