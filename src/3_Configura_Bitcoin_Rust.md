### Configurar Bitcoin con Rust en macOS

1. **Instalar dependencias necesarias (si las necesitas más adelante):**
   - Si trabajas con `rust-bitcoin`, algunas dependencias como OpenSSL pueden ser útiles. Instálalas con:
     ```bash
     brew install openssl

     ```
2. **Crear un proyecto Rust para Bitcoin:**
   - Crea un proyecto básico:
     ```bash
     cargo new bitcoin_project
     cd bitcoin_project
     ```
   - Añade la biblioteca `rust-bitcoin` al proyecto:
     ```bash
     cargo add bitcoin
     ```
3. **Probar el proyecto:**
   - Edita el archivo `src/main.rs` para incluir esta prueba básica:
     ```rust
     extern crate bitcoin;

     fn main() {
         println!("Hello, Bitcoin with Rust!");
     }

     ```
   - Corre el proyecto:
     ```bash
     cargo run
     ```
