<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>GameTime - Artículos Deportivos</title>
<style>
    body {
        font-family: 'Arial', sans-serif;
        background-color: #f8f8f8;
        margin: 0;
        padding: 0;
    }
    header {
        background-color: #2e8b57;
        color: white;
        padding: 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    header img {
        height: 50px;
    }
    .carrito {
        background-color: white;
        color: #2e8b57;
        padding: 10px 15px;
        border-radius: 50px;
        font-weight: bold;
        cursor: pointer;
        position: relative;
    }
    .carrito span {
        position: absolute;
        top: -8px;
        right: -8px;
        background-color: red;
        color: white;
        border-radius: 50%;
        padding: 3px 7px;
        font-size: 12px;
    }
    .contenedor {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 30px;
        gap: 20px;
    }
    .articulo {
        background-color: white;
        border-radius: 15px;
        width: 270px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        padding: 15px;
        text-align: center;
        transition: transform 0.2s;
    }
    .articulo:hover { transform: translateY(-5px); }
    .articulo img { width: 100%; border-radius: 10px; }
    .articulo h2 { color: #2e8b57; margin: 10px 0 5px 0; }
    .articulo p { color: #555; font-size: 14px; line-height: 1.4; }
    .precio { font-weight: bold; margin: 5px 0; color: #ff6600; }
    select {
        padding: 5px;
        margin: 5px 0;
        border-radius: 5px;
        border: 1px solid #ccc;
    }
    .boton-comprar {
        background-color: #ff6600;
        color: white;
        padding: 10px 15px;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        font-size: 14px;
        margin-top: 10px;
        transition: background-color 0.2s;
    }
    .boton-comprar:hover { background-color: #ff8533; }
</style>
</head>
<body>

<header>
    <img src="logo_GT_minimalista.png" alt="Logo GameTime">
    <div class="carrito">Carrito <span id="contador">0</span></div>
</header>

<div class="contenedor">

    <!-- Zapatillas de Baloncesto -->
    <div class="articulo">
        <img src="baloncesto.jpg" alt="Zapatillas NBA">
        <h2>Zapatillas NBA</h2>
        <p>Modelos: Curry, LeBron, KD, Kyrie, LaMelo Ball, Ja Morant.</p>
        <p class="precio">RD$ 3,500 - RD$ 12,000</p>
        <label>Talla:</label>
        <select id="size-zapatillas">
            <option>38</option>
            <option>39</option>
            <option>40</option>
            <option>41</option>
            <option>42</option>
            <option>43</option>
        </select>
        <button class="boton-comprar" onclick="agregarCarrito('Zapatillas NBA')">Agregar al carrito</button>
    </div>

    <!-- Camisetas NBA -->
    <div class="articulo">
        <img src="camiseta.jpg" alt="Camiseta NBA">
        <h2>Camisetas NBA</h2>
        <p>Camisetas oficiales de tus jugadores favoritos.</p>
        <p class="precio">RD$ 2,000 - RD$ 4,000</p>
        <label>Talla:</label>
        <select id="size-camiseta">
            <option>S</option>
            <option>M</option>
            <option>L</option>
            <option>XL</option>
            <option>XXL</option>
        </select>
        <button class="boton-comprar" onclick="agregarCarrito('Camiseta NBA')">Agregar al carrito</button>
    </div>

    <!-- Béisbol -->
    <div class="articulo">
        <img src="beisbol.jpg" alt="Bate y guante de béisbol">
        <h2>Béisbol</h2>
        <p>Bate Rawlings, Guante Wilson, Pelotas oficiales.</p>
        <p class="precio">RD$ 1,800 - RD$ 8,000</p>
        <button class="boton-comprar" onclick="agregarCarrito('Béisbol')">Agregar al carrito</button>
    </div>

    <!-- Licras tobilleras -->
    <div class="articulo">
        <img src="licras.jpg" alt="Licras Tobilleras">
        <h2>Licras Tobilleras</h2>
        <p>Licras deportivas para mayor comodidad y soporte.</p>
        <p class="precio">RD$ 500 - RD$ 1,200</p>
        <label>Talla:</label>
        <select id="size-licras">
            <option>S</option>
            <option>M</option>
            <option>L</option>
            <option>XL</option>
        </select>
        <button class="boton-comprar" onclick="agregarCarrito('Licras Tobilleras')">Agregar al carrito</button>
    </div>

</div>

<script>
    let contador = 0;
    let carritoProductos = [];

    function agregarCarrito(producto) {
        contador++;
        carritoProductos.push(producto);
        document.getElementById('contador').innerText = contador;
        alert(producto + ' agregado al carrito!');
        console.log('Productos en carrito:', carritoProductos);
    }
</script>

</body>
</html>
