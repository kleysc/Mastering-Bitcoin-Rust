## **Firmar y verificar mensajes:**

- Usar la clave privada para firmar un mensaje.
- Verificar la firma con la clave pública correspondiente.

  - **_Guía_**
    ### 1. **Conceptos Previos**
    **Firmas Digitales:**
    - Una firma digital permite autenticar un mensaje, garantizando que proviene de un remitente específico (clave privada).
    - Utiliza criptografía de clave pública (secp256k1 en Bitcoin).
    **Proceso de Firma y Verificación:**
    1. Generar una clave privada y calcular la clave pública.
    2. Crear una firma digital utilizando un mensaje y la clave privada.
    3. Verificar la firma utilizando el mensaje, la clave pública y la firma.
    ***
    ### 2. **Objetivo del Ejercicio**
    Firmar un mensaje con una clave privada y verificar la firma utilizando la clave pública correspondiente.
    ***
    ### 3. **Pasos Detallados**
    **Paso 1: Configurar el entorno**
    - Asegúrate de que tu entorno de Rust esté configurado (como en el ejercicio 1).
    - Añade `rust-bitcoin` a tu proyecto:
      ```bash
      bash
      Copy code
      cargo add bitcoin

      ```
    **Paso 2: Generar claves**
    - Usa `Secp256k1` para generar una clave privada.
    - Deriva la clave pública correspondiente.
    **Paso 3: Firmar un mensaje**
    - Usa el método `sign` para crear la firma del mensaje.
    **Paso 4: Verificar la firma**
    - Utiliza `verify` con la clave pública, el mensaje y la firma.
    ***
    ### 4. **Código Base**
    ```rust
    rust
    Copy code
    extern crate bitcoin;

    use bitcoin::secp256k1::{Secp256k1, SecretKey, PublicKey, Message, Signature};

    fn main() {
        // 1. Crear el contexto para manejar la curva elíptica
        let secp = Secp256k1::new();

        // 2. Generar clave privada (completar)
        // let secret_key = ...;

        // 3. Derivar clave pública (completar)
        // let public_key = ...;

        // 4. Crear el mensaje a firmar
        let message = Message::from_slice(&[0xab; 32]).expect("Mensaje inválido");

        // 5. Firmar el mensaje (completar)
        // let signature = ...;

        // 6. Verificar la firma (completar)
        // let is_valid = ...;

        println!("¿La firma es válida? {}", is_valid);
    }

    ```
    ***
    ### 5. **Tareas para Resolver**
    1. Genera una clave privada y su clave pública.
    2. Firma el mensaje `0xab...` (32 bytes).
    3. Verifica la firma creada.
    ***
    ### 6. **Validación**
    - Verifica que la firma sea válida para el mensaje dado.
    - Cambia el mensaje y asegúrate de que la firma no sea válida.
    ***
    ### 7. **Reflexión Final**
    Este ejercicio refuerza conceptos sobre criptografía de clave pública, esenciales para entender cómo funcionan las transacciones en Bitcoin.
