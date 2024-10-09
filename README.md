# Predicción de Precios de Alquiler en Madrid

Este proyecto utiliza TensorFlow y Keras para predecir el precio de alquiler mensual de una vivienda en la ciudad de Madrid. El modelo se entrena utilizando un conjunto de datos que incluye diversas características de las propiedades, como la zona, metros cuadrados, número de habitaciones, planta, entre otras variables.

## Descripción

El modelo predice el precio de una vivienda en función de las siguientes características:

1. **Zona/Distrito:**
   - 0 (Carabanchel)
   - 1 (Villa Vallecas)
   - 2 (Usera)
   - 3 (Arganzuela)
   - 4 (Latina)
   - 5 (Ciudad Lineal)
   - 6 (Castellana)
   - 7 (Retiro)
   - 8 (Goya)
2. **Metros cuadrados:** Superficie de la vivienda en m².
3. **Número de habitaciones:** Cantidad de habitaciones en la vivienda.
4. **Planta:** El número de planta en la que se encuentra la vivienda.
5. **Ascensor:**
   - 0 (No)
   - 1 (Sí)
6. **Exterior:**
   - 0 (No)
   - 1 (Sí)
7. **Estado de la vivienda:**
   - 0 (No rehabilitado)
   - 1 (Rehabilitado)
   - 2 (Nuevo)
8. **Vivienda céntrica:**
   - 0 (No)
   - 1 (Sí)

### Salida

El modelo devuelve el **precio mensual estimado del alquiler de la vivienda en euros**, basándose en los valores de entrada proporcionados.

## Tecnologías utilizadas

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- JavaScript (para la parte web)
- HTML/CSS (para la interfaz)

## Instalación

Para ejecutar este programa, asegúrate de tener instalado Python 3.x y las dependencias necesarias. Puedes instalarlas utilizando `pip`:

```bash
pip install tensorflow numpy matplotlib
```

Además, necesitarás un servidor para cargar la interfaz web y el modelo entrenado en formato `model.json`.

## Uso

### Parte 1: Entrenamiento del modelo

1. Ejecuta el archivo Python para entrenar el modelo utilizando los datos proporcionados. El modelo se entrenará durante 1000 épocas y generará una gráfica que muestra la magnitud de pérdida (loss) a lo largo del proceso de entrenamiento.
2. Guarda el modelo entrenado en formato `model.json` para su uso en la interfaz web.

### Parte 2: Interfaz Web

1. Abre el archivo `index.html` en tu navegador web. Esta interfaz permite al usuario ingresar las características de una vivienda y obtener una predicción del precio de alquiler mensual.
2. Introduce los valores solicitados en el formulario web, como metros cuadrados, número de habitaciones, planta, si tiene ascensor, si es exterior, etc.
3. Haz clic en el botón "Calcular precio" para obtener una predicción del precio mensual de alquiler basado en los datos introducidos.
4. Si deseas borrar los valores ingresados y la predicción, puedes hacer clic en el botón "Vaciar".

## Ejemplo de predicción

Si ingresas los siguientes datos en el formulario web:

- Metros cuadrados: 80
- Habitaciones: 3
- Planta: 4
- Zona: Carabanchel
- Ascensor: Sí
- Exterior: Sí
- Estado: Rehabilitado
- Céntrico: No

El modelo te devolverá una predicción de precio, por ejemplo: `Precio: 1081€/mes`.

## Resultados

El modelo generará una gráfica durante el entrenamiento que muestra cómo disminuye la magnitud de pérdida a lo largo de las épocas.

![image](https://github.com/user-attachments/assets/7ad24b57-bceb-423d-9158-6ef162c6c399)

En la interfaz web, la predicción del precio aparecerá en la sección de resultados después de ingresar los datos de la vivienda.

![image](https://github.com/user-attachments/assets/ce7ffe8b-e6ac-4122-9cfa-6557c3bb0d4d)
![image](https://github.com/user-attachments/assets/0399dc37-a5f5-4407-b241-8cb34f13b986)

## Guardar el modelo

Si deseas guardar el modelo entrenado para su uso futuro, puedes descomentar la línea al final del código de entrenamiento en Python:
```bash
modelo.save('appAlquilerCasas.h5')
```
## Consideraciones

Los datos generados por la API son aproximados y pueden no reflejar con precisión la realidad. Para obtener resultados más precisos y confiables, se necesitaría un conjunto de datos más amplio y representativo como entrada. Esto permitirá mejorar la calidad y exactitud de las predicciones.





















