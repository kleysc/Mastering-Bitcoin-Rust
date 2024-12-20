**Explorar claves y direcciones:**

- Convertir entre diferentes formatos de claves privadas (WIF y hexadecimal).
- Generar direcciones Bitcoin para diferentes redes (mainnet, testnet).
  - **_Guía_**
    ### 1. **Conceptos Previos**
    **Formatos de Claves:**
    - Las claves privadas pueden representarse en hexadecimal o en formato WIF.
    - Las direcciones pueden ser para mainnet o testnet.
    ***
    ### 2. **Objetivo del Ejercicio**
    Explorar diferentes representaciones de claves privadas y generar direcciones para diferentes redes.
    ***
    ### 3. **Pasos Detallados**
    **Paso 1: Crear una clave privada**
    - Usa `Secp256k1` para generar una clave privada.
    **Paso 2: Convertir al formato WIF**
    - Usa `rust-bitcoin` para convertir la clave a formato WIF.
    **Paso 3: Generar direcciones**
    - Usa la clave privada para generar direcciones para mainnet y testnet.
    ***
    ### 4. **Código Base**
    ```rust
    rust
    Copy code
    extern crate bitcoin;

    use bitcoin::secp256k1::Secp256k1;
    use bitcoin::util::key::PrivateKey;
    use bitcoin::Network;

    fn main() {
        let secp = Secp256k1::new();
        let private_key = PrivateKey::new(&secp, Network::Bitcoin);

        // 1. Mostrar la clave en WIF
        println!("Clave privada WIF: {}", private_key.to_wif());

        // 2. Generar una dirección para mainnet (completar)
        // println!("Dirección mainnet: {}", ...);

        // 3. Generar una dirección para testnet (completar)
        // println!("Dirección testnet: {}", ...);
    }

    ```
    ***
    ### 5. **Tareas para Resolver**
    1. Genera y muestra una clave privada en WIF.
    2. Crea direcciones para mainnet y testnet.
    ***
    ### 6. **Validación**
    - Asegúrate de que las direcciones generadas sean válidas.
    ***
    ### 7. **Reflexión Final**
    Entender los formatos de claves y direcciones es fundamental para trabajar con wallets y transacciones.
