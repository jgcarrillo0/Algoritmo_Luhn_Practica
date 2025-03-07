# Aplicación del Algoritmo de Luhn

<p align="center">
    <img src="Imagenes_readme/Tarjetas.jpg" />
</p>

## 📌Objetivo de la práctica
El objetivo de la práctica es implementar el algoritmo de Luhn mediante funciones que permitan generar números de tarjetas bancarias aleatorios o validar un número existente. Esto se logrará aplicando la lógica del algoritmo para calcular el dígito de control y verificar la autenticidad de los números ingresados, garantizando su conformidad con el estándar utilizado en sistemas de identificación bancaria.

## Conceptos básicos
### 💡¿Qué es el Algoritmo de Luhn?
El algoritmo de Luhn, o Algoritmo de módulo 10, es un método de verificación diseñado por Hans Peter Luhn en 1954 y patentado en 1960, utilizado para validar números de identificación como tarjetas de crédito y números IMEI. Su propósito es detectar errores accidentales en la digitación o transmisión de datos, más que proporcionar seguridad criptográfica. De dominio público y especificado en la norma ISO/IEC 7812-1, es ampliamente utilizado para distinguir números válidos de combinaciones aleatorias en sistemas de identificación, siendo una herramienta fundamental en la validación de datos numéricos [^1].

Pasos del algoritmo:

1. Quita el dígito de control del número (si ya está presente). Esto deja la carga útil
2. Comience con los dígitos de la carga útil. Moviéndote de derecha a izquierda, duplica cada segundo dígito, empezando por el último dígito. Si duplicar un dígito da como resultado un valor > 9, reste 9 (o sume sus dígitos)
3. Suma todos los dígitos resultantes (incluidos los que no se duplicaron)
4. El dígito de control se calcula de la siguiente manera: $(10 - (s mod 10))mod 10$, donde s es la suma del paso 3. Este es el número más pequeño (posiblemente cero) al que se debe sumar $s$
para hacer un múltiplo de 10

[^1]: [Algoritmo de Luhn](https://en.wikipedia.org/wiki/Luhn_algorithm)

### 💡¿Qué es el código BIN (Bank Identification Number)?
El BIN (Bank Identification Number) es el conjunto de los primeros 6 a 8 dígitos de una tarjeta bancaria, que identifica la entidad emisora, el tipo de tarjeta y la red de pago (Visa, Mastercard, etc.). Se utiliza para procesar transacciones y detectar fraudes.

## 📦 Descripción de los ficheros
El repositorio cuenta con los siguientes archivos:
- **Algoritmo_Luhn.ipynb:** Cuaderno con la práctica
- **Folder data:** Contiene el dataset con los dantos de los códigos BIN
- **Folder imagenes:** Contiene las imágenes usadas dentro del cuaderno

## 🛠️Dependecias para poder realizar la práctica
Para una correcta ejecución de la práctica debe instalar en su entorno las siguinetes librerías:
- pandas

## 🏆 Visualice la práctica
> [!TIP]
> Visualice el cuaderno en nbviewer aquí: [Práctica: Algoritmo de Luhn](https://nbviewer.org/github/jgcarrillo0/Algoritmo_Luhn_Practica/blob/main/Cuaderno/Algoritmo_Luhn.ipynb)
