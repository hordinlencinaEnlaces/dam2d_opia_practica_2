# Práctica 2: Despliegue de Modelo de IA (California Housing)

**Autores:** Alejandro Felices, Hector Ordín  
**Repositorio GitHub:** [dam2d_opia_practica_2](https://github.com/hordinlencinaEnlaces/dam2d_opia_practica_2)  
**URL del Servicio Desplegado:** `https://dam2d-california-housing.onrender.com` *(Sustituye por tu URL exacta de Render)*

## Pasos del Despliegue

1. **Configuración del Repositorio:** Subida de los ficheros `app.py`, `requirements.txt` y el modelo serializado `modelo_california.pkl` a la rama `main` de GitHub.
2. **Creación del Servicio en Render:** Creación de cuenta en la plataforma Render, selección de **New > Web Service** y vinculación con el repositorio público de GitHub.
3. **Parámetros de Despliegue:**
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `uvicorn app:app --host 0.0.0.0 --port $PORT`
4. **Verificación:** Comprobación del health-check (`GET /`) y del endpoint de inferencia (`POST /predict`). *Nota: Debido al plan gratuito de Render, la primera petición puede tardar unos segundos en responder por el arranque en frío.*