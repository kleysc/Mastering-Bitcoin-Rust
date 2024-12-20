# Mastering Bitcoin in Rust

Este repositorio contiene una serie de ejercicios diseñados para aprender Rust mientras se exploran los fundamentos técnicos de Bitcoin. Los ejercicios cubren conceptos básicos como generación de direcciones Bitcoin, hasta temas avanzados como la creación de nodos y la interacción con Lightning Network.

---

## **Plan de Aprendizaje**

### **Semana 1-2: Nivel Básico**
- **Objetivo:** Familiarizarte con Rust y los fundamentos de Bitcoin.
- **Ejercicios:**
  1. Generar una dirección Bitcoin.
  2. Firmar y verificar mensajes.
  3. Crear una transacción Bitcoin simple.
- **Resultados esperados:**
  - Generar y entender claves privadas, públicas y direcciones.
  - Usar firmas digitales para mensajes.
  - Construir una transacción básica.

### **Semana 3-4: Nivel Intermedio**
- **Objetivo:** Comprender transacciones avanzadas y scripts.
- **Ejercicios:**
  4. Decodificar una transacción Bitcoin.
  5. Explorar claves y direcciones en formatos avanzados.
  6. Trabajar con transacciones multifirma.
  7. Explorar UTXOs y crear transacciones que los gasten.
- **Resultados esperados:**
  - Leer y analizar transacciones existentes.
  - Implementar multifirmas y scripts personalizados.
  - Consultar y usar UTXOs en nuevas transacciones.

### **Semana 5-6: Nivel Avanzado**
- **Objetivo:** Adquirir habilidades avanzadas en bloques, nodos y Lightning Network.
- **Ejercicios:**
  8. Transacciones bloqueadas por tiempo.
  9. Firmar transacciones completas.
  10. Explorar bloques de Bitcoin.
  11. Construir un nodo básico.
- **Resultados esperados:**
  - Crear transacciones más complejas, como timelocks.
  - Decodificar bloques y entender su estructura.
  - Conectar un nodo a la red Bitcoin.

### **Semana 7-8: Lightning Network (Opcional)**
- **Ejercicio Opcional:** Interacción con Lightning Network.
- **Resultados esperados:**
  - Conectar a un nodo Lightning.
  - Crear un canal y realizar pagos básicos.

---

## **Estructura del Repositorio**

```plaintext
mastering-bitcoin-rust/
├── src/
│   ├── basic/
│   │   ├── exercise1_generate_address.rs
│   │   ├── exercise2_sign_verify.rs
│   │   ├── exercise3_create_transaction.rs
│   ├── intermediate/
│   │   ├── exercise4_decode_transaction.rs
│   │   ├── exercise5_explore_keys.rs
│   │   ├── exercise6_multisig.rs
│   │   ├── exercise7_utxos.rs
│   ├── advanced/
│   │   ├── exercise8_timelock.rs
│   │   ├── exercise9_sign_transactions.rs
│   │   ├── exercise10_explore_blocks.rs
│   │   ├── exercise11_basic_node.rs
│   ├── lightning/
│       ├── exercise12_lightning.rs
├── README.md
├── Cargo.toml
├── Cargo.lock
└── LICENSE
```

---

## **Requisitos**

Antes de comenzar, asegúrate de tener instalados los siguientes programas:

- **Rust y Cargo**: Puedes instalarlo ejecutando:
  ```bash
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  ```

---

## **Recomendaciones:**

- Se recomienda usar **Visual Studio Code** con la extensión **rust-analyzer** para una mejor experiencia de desarrollo.
- **Git**: Para clonar este repositorio.

- **Clona el repositorio:**
  ```bash
  git clone https://github.com/tu-usuario/mastering-bitcoin-rust.git
  cd mastering-bitcoin-rust
  ```

- **Instala las dependencias necesarias (opcional):**
  ```bash
  brew install openssl
  cargo build
  ```