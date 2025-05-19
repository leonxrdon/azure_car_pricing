# Predicción de Precio de Coches con Flask y Azure ML

Este proyecto es una aplicación web desarrollada con **Flask** que se conecta a un **endpoint de Azure Machine Learning** para predecir el precio de un coche en función de sus características.

## 🚀 ¿Cómo funciona?

1. Al abrir la aplicación en [http://127.0.0.1:5000](http://127.0.0.1:5000), se mostrará un formulario.
2. El formulario se rellena por defecto con los datos de un coche de ejemplo.
3. Puedes editar los valores para introducir tus propios datos.
4. Al enviar el formulario, se realiza una petición al endpoint de Azure ML que devuelve el precio estimado del coche.
5. El resultado se muestra con formato monetario (`$`).

## 🧾 Ejemplo de predicción

Formulario por defecto:
```json
{
  "marca": "Audi",
  "modelo": "A1",
  "version": "A1 1.0 TFSI Adrenalin",
  "startYear": 2015,
  "endYear": 2018,
  "cilindrada": 999,
  "cv": 95,
  "id_carroceria": "Ber",
  "pf": 0,
  "puertas": 3,
  "id_combustible": "G",
  "matriculacion": 2015,
  "periodoDescripcion": "4º trimestre",
  "Anno": 2017
}
```

Resultado (ejemplo):
```
$8,518.85
```

## 🛠️ Requisitos

- Python 3.8+
- Flask
- Requests
- python-dotenv

Instalación de dependencias:

```bash
pip install -r requirements.txt
```

## 📁 Estructura del proyecto

```
project/
│
├── app.py
├── .env
├── requirements.txt
├── templates/
│   └── index.html
├── venv/
└── .gitignore
```

## ⚙️ Variables de entorno

Crea un archivo `.env` con tus credenciales de Azure:

```env
API_KEY=tu_api_key_aqui
ENDPOINT=https://tu-endpoint.azurewebsites.net/score
```

## ▶️ Cómo ejecutar

En terminal:

```bash
flask run
```

La aplicación estará disponible en: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---