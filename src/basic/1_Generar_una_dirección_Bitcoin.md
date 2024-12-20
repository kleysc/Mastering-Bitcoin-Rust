## **Generar una dirección Bitcoin:**

   - Generar una clave privada aleatoria.
   - Derivar la clave pública asociada.
   - Codificar la dirección en formato Base58Check.

   - **_Guía_**

   ### 1. **Conceptos Previos**

   **Dirección Bitcoin**:

   - Una dirección Bitcoin es un identificador público que puedes compartir para recibir bitcoins.
   - Se deriva de una clave privada, que es un número secreto generado aleatoriamente.
   - Las direcciones están codificadas en un formato especial llamado **Base58Check** para mejorar su usabilidad y seguridad.

   **Proceso para generar una dirección Bitcoin:**

   1. Generar una **clave privada** aleatoria.
   2. Calcular la **clave pública** correspondiente usando la curva elíptica secp256k1.
   3. Aplicar el **hash doble (SHA-256 + RIPEMD-160)** a la clave pública.
   4. Codificar el resultado en formato **Base58Check**.

   ***

   ### 2. **Objetivo del Ejercicio**

   Generar una dirección Bitcoin a partir de una clave privada aleatoria utilizando Rust y la biblioteca `rust-bitcoin`.

   ***

   ### 3. **Pasos Detallados**

   **Paso 1: Configurar el entorno**

   - Asegúrate de tener Rust configurado correctamente.
   - Crea un nuevo proyecto:
     ```bash
     bash
     Copy code
     cargo new generate_bitcoin_address
     cd generate_bitcoin_address

     ```
   - Añade la biblioteca `rust-bitcoin` al proyecto:
     ```bash
     bash
     Copy code
     cargo add bitcoin

     ```

   **Paso 2: Generar la clave privada**

   - Usa la función `secp256k1::SecretKey` para generar una clave privada aleatoria.

   **Paso 3: Derivar la clave pública**

   - Usa la función `PublicKey::from_secret_key` para calcular la clave pública.

   **Paso 4: Crear la dirección Bitcoin**

   - Aplica el hash doble SHA-256 y RIPEMD-160 a la clave pública.
   - Codifica el resultado en Base58Check.

   ***

   ### 4. **Código Base**

   Aquí tienes un esqueleto de código para empezar:

   ```rust
   rust
   Copy code
   extern crate bitcoin;

   use bitcoin::secp256k1::{Secp256k1, SecretKey};
   use bitcoin::util::address::Address;
   use bitcoin::Network;

   fn main() {
       // 1. Crear el contexto para manejar la curva elíptica
       let secp = Secp256k1::new();

       // 2. Generar clave privada (completar)
       // let secret_key = ...;

       // 3. Derivar clave pública (completar)
       // let public_key = ...;

       // 4. Crear la dirección Bitcoin (completar)
       // let address = ...;

       println!("¡Dirección Bitcoin generada!");
   }

   ```

   ***

   ### 5. **Tareas para Resolver**

   1. Genera una clave privada utilizando `Secp256k1`.
   2. Deriva la clave pública correspondiente.
   3. Calcula la dirección Bitcoin para la red principal (`mainnet`).

   ***

   ### 6. **Validación**

   - Compara la dirección generada con herramientas en línea como Blockchain Explorer.
   - Asegúrate de que la dirección comienza con `1` (para direcciones estándar en mainnet).

   ***

   ### 7. **Reflexión Final**

   Este ejercicio te ayuda a entender cómo se generan las direcciones Bitcoin y cómo Rust maneja las operaciones criptográficas necesarias.
