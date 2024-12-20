## **Construir un nodo Bitcoin básico:**
  
   - Implementar un nodo que conecte a la red P2P de Bitcoin.
   - Escuchar mensajes básicos como `version` y `ping`.
  
   - **_Guía_**
       ### 1. **Conceptos Previos**
       **Red P2P de Bitcoin:**
       - Los nodos se comunican usando mensajes como `version`, `ping`, y `pong`.
  
       ***
  
       ### 2. **Objetivo del Ejercicio**
       Crear un nodo que pueda conectarse a otros nodos y manejar mensajes básicos.
  
       ***
  
       ### 3. **Pasos Detallados**
       **Paso 1: Crear una conexión TCP**
       - Usa una librería como `tokio` para manejar la red.
       **Paso 2: Enviar y recibir mensajes**
       - Implementa mensajes básicos como `version`.
  
       ***
  
       ### 4. **Código Base**
       ```rust
       extern crate tokio;

       use tokio::net::TcpStream;

       #[tokio::main]
       async fn main() {
           let stream = TcpStream::connect("peer.bitcoin.network:8333").await.unwrap();
           println!("Conectado a un nodo Bitcoin.");
       }

       ```
       
       ***
       
       ### 5. **Tareas para Resolver**
       1. Envía un mensaje `version` a un nodo.
       2. Escucha y responde a mensajes como `ping`.
       
       ***
       
       ### 6. **Validación**
       - Conéctate a nodos reales y verifica las respuestas.
       
       ***
       
       ### 7. **Reflexión Final**
       Este ejercicio combina redes y Bitcoin, acercándote al desarrollo de nodos completos.
