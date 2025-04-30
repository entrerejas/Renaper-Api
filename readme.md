# 🔎 API RENAPER

Consulta datos personales mediante **DNI y género** a través de un backend conectado al sistema RENAPER.

📍 **URL Base:** [https://apirnpr.onrender.com](https://apirnpr.onrender.com)

---

## 📌 Descripción

Esta API permite obtener información pública registrada en RENAPER, como:

- Nombre completo  
- Fecha de nacimiento  
- Dirección (calle, ciudad, provincia, código postal)  
- CUIL  
- Información administrativa adicional  

Ideal para proyectos de verificación o automatización documental, siempre respetando las leyes de protección de datos.

---

## 🚀 Cómo usar

### Endpoint

GET 'renaper/{dni}/{genero}'

**Parámetros:**

- `dni`: Número de documento sin puntos (ej: `12345678`)
- `genero`: `"M"` (masculino), `"F"` (femenino) o `"X"` (no binario)

---

## 🧪 Ejemplo

**Request:**
GET https://apirnpr.onrender.com/renaper/44444444/F

**Response:**

```json
{
  "error": false,
  "mensaje": null,
  "respuesta": {
    "apellido": "CORONEL",
    "barrio": "",
    "calle": "ISLAS MALVINAS",
    "ciudad": "SANTIAGO DEL ESTERO",
    "codigoError": 200,
    "codigof": 3,
    "cpostal": "4200",
    "cuil": "24444444440",
    "departamento": "",
    "descripcionError": "DNI/PAS Firmado",
    "ejemplar": null,
    "emision": null,
    "fechaNacimiento": "2002-11-14",
    "fechaf": "",
    "idCiudadano": null,
    "idTramitePrincipal": 0,
    "idTramiteTarjetaReimpresa": 0,
    "mensajef": null,
    "monoblock": "Bª MOSCONI",
    "municipio": "SANTIAGO_DEL_ESTERO_CAPITAL",
    "nombres": "Lucia",
    "nroError": "0",
    "numeroCalle": null,
    "origenf": "RENAPER",
    "paso": null,
    "piso": "",
    "provincia": "SANTIAGO_DEL_ESTERO",
    "vencimiento": null
  }
}
