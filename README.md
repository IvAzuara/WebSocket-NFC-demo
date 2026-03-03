# 📡 NFC Terminal

Demo interactivo de lectura de tags NFC con envío en tiempo real vía WebSocket. Construido con Web NFC API, Node.js y Express.

> ⚠️ La Web NFC API solo funciona en **Google Chrome para Android** (versión 89+).

---

## 📁 Estructura del proyecto

```
WebSocket-NFC-demo/
├── server.js
├── package.json
└── public/
    ├── index.html
    ├── css/
    │   └── style.css
    └── js/
        └── app.js
```

---

## 🚀 Instalación

Requiere **Node.js v18+** — [nodejs.org](https://nodejs.org)

```bash
git clone https://github.com/IvAzuara/WebSocket-NFC-demo.git
cd WebSocket-NFC-demo
npm install
npm start
```

El servidor estará disponible en `http://localhost:3000`

---

## 📱 Uso

1. Inicia el servidor con `npm start`
2. Abre **Chrome en tu Android** y navega a `http://<IP-de-tu-máquina>:3000`
3. Presiona **Iniciar escaneo** y acerca una tarjeta NFC

---

## 🔒 Exponer el servidor con ngrok (HTTPS)

La Web NFC API requiere HTTPS fuera de `localhost`. Usa [ngrok](https://ngrok.com) para obtener una URL pública:

**1.** Crea una cuenta gratuita en [ngrok.com](https://ngrok.com) e instálalo desde [ngrok.com/download](https://ngrok.com/download)

**2.** Inicia sesión y configura tu token siguiendo las instrucciones oficiales:
👉 [dashboard.ngrok.com/get-started/your-authtoken](https://dashboard.ngrok.com/get-started/your-authtoken)

**3.** Con el servidor corriendo, en otra terminal ejecuta:

```bash
ngrok http 3000
```

Usa la URL `https://` que te genera ngrok en Chrome de Android.

> ⚠️ La URL cambia en cada reinicio en el plan gratuito.

---

## 📦 Dependencias

| Paquete | Versión |
|---------|---------|
| `express` | ^4.18.2 |
| `ws` | ^8.16.0 |
