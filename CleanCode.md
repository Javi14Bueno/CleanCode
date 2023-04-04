# <h1>6 TIPS Y EJEMPLOS PARA UN 'CLEAN CODE'♻️


![Código Limpio](/image-blog-social-writing-clean-code_0.png)



# ✔️Claridad:

```javascript
// MAL: Nombre de variable poco descriptivo
int x;

// BIEN: Nombre de variable descriptivo
int edad;
```
```java
// MAL: Código ilegible
if(edad>=18){System.out.println("Eres mayor de edad");}

// BIEN: Código legible
if (edad >= 18) {
    System.out.println("Eres mayor de edad");
}
```


🔹Usa nombres descriptivos para las variables, funciones y métodos.

🔹Separa el código en bloques legibles con espacios en blanco, saltos de línea, etc.
    
🔹Usa comentarios solo cuando sea necesario para explicar algo que no sea obvio en el código.

***

# ✔️Simplicidad:

```java
// MAL: Estructuras de control de flujo complejas
if (x > 0 && x < 10 || x == 20 || (x >= 30 && x <= 40)) {
}

// BIEN: Estructuras de control de flujo simples
boolean esValido = (x > 0 && x < 10) || x == 20 || (x >= 30 && x <= 40);
if (esValido) {
}
```


🔹No uses estructuras de control de flujo complejas si no son necesarias.

🔹Evita anidar demasiado las estructuras de control de flujo (por ejemplo, un if dentro de otro if).

🔹No repitas código innecesariamente; en su lugar, reutiliza funciones y métodos.

***

# ✔️Consistencia:
```java
// MAL: Estilo inconsistente de corchetes
public void metodo1()
{
    // ...
}

public void metodo2() {
    // ...
}

// BIEN: Estilo consistente de corchetes
public void metodo1() {
    // ...
}

public void metodo2() {
    // ...
}
```

🔹Usa una convención de nombres y formato de código consistente en todo el proyecto.

🔹Sigue un estilo de codificación coherente (por ejemplo, el uso de corchetes en la misma línea o en una línea separada).

***

# ✔️ Modularidad:

```java
// MAL: Clase monolítica
public class MiClase {
    public void metodo1() {
        
    }

    public void metodo2() {
        
    }

    public void metodo3() {
        
    }
}

// BIEN: Clase modular
public class MiClase {
    private SubClase1 subClase1;
    private SubClase2 subClase2;

    public MiClase() {
        subClase1 = new SubClase1();
        subClase2 = new SubClase2();
    }

    public void metodo1() {
        subClase1.hacerAlgo();
    }

    public void metodo2() {
        subClase2.hacerAlgo();
    }
}
```

🔹Separa el código en métodos cohesivos y acoplados.

🔹Cada método debe tener una función clara y bien definida.

🔹Los métodos deben interactuar entre sí a través de interfaces bien definidas.

***

# ✔️Comentarios:

```java
// MAL: Comentarios innecesarios
public void metodo1() {
    // Aquí se hace algo importante
    // ...
}

// BIEN: Comentarios útiles
public void metodo1() {
    // Cálculo de la edad a partir de la fecha de nacimiento
    // ...
}
```

🔹Usa comentarios para explicar el propósito y la funcionalidad de los bloques de código importantes.

🔹No uses comentarios para explicar código obvio o para justificar código mal escrito.

🔹Mantén los comentarios actualizados y elimina los comentarios innecesarios.

***

# ✔️Pruebas:

```java
// MAL: Falta de pruebas
public class MiClase {
    public int suma(int a, int b) {
        return a + b;
    }
}

// BIEN: Pruebas automatizadas
public class MiClaseTest {
    @Test
    public void testSuma() {
        MiClase miClase = new MiClase();
        int resultado = miClase.suma(2, 3);
        assertEquals(5, resultado);
    }
}
```

🔹Escribe pruebas automatizadas para cada componente del código.

🔹Verifica que las pruebas cubran todos los casos de uso importantes.

🔹Ejecuta las pruebas de forma regular y corrige los errores encontrados.

***


