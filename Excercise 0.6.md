```mermaid
sequenceDiagram
    participant User as Usuario
    participant Browser as Navegador
    participant Server as Servidor

    User ->> Browser: Selecciona "Crear nueva nota"
    Browser -->> User: Muestra formulario de creación
    User ->> Browser: Ingresa detalles de la nota
    User ->> Browser: Envía el formulario
    Browser -->> Server: POST https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server -->> Browser: Confirmación de creación de nota
    deactivate Server
    Browser -->> Browser: Actualiza estado local con la nueva nota
    Browser -->> User: Muestra nueva nota en la lista

    Note over Browser: La SPA actualiza la vista dinámicamente sin recargar la página
