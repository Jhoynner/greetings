# Saludos en Go

Este paquete proporciona una forma simple de obtener saludos personalizados en Go.

## Instalacion
Ejecuta el siguiente comando para instalar el paquete:
```bash
go get -u github.com/Jhoynner/greetings
```

## Uso
Aqui tienes un ejemplo de como utilizar el paquete en tu codigo:

```go
package main

import (
	"fmt"
	"log"

	"github.com/Jhoynner/greetings"
)

func main() {
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{"Alfredo", "Carrillo", "Hernandez"}
	messages, err := greetings.Hellos(names)
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)

	message, err := greetings.Hello("Jhoynner")
	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(message)
}
```
Este ejemplo importa el paquete github.com/Jhoynner/greetings y llama a la funcion Hello o Hellos para generar un saludo personalizado ya sea para una persona o un grupo de personas. Ademas si llega a presentarse un error, se imprime un mensaje de error.