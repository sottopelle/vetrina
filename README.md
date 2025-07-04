<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Sottopelle Brand</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
<style>
body {
  margin: 0;
  background-color: #111;
  color: #f3f3f3;
  font-family: 'Montserrat', sans-serif;
}
  header {
    background-color: #000;
    padding: 60px 20px 40px;
    text-align: center;
    position: relative;
  }
  .header-bar {
    position: absolute;
    top: 15px;
    left: 20px;
  }
 .welcome-link {
  color: #ccc;
  text-decoration: none;
  font-size: 1.2rem;        /* più grande */
  font-weight: bold;        /* grassetto */
  letter-spacing: 0.5px;
  transition: color 0.3s ease;
}
.subtitle-small {
  margin: 4px 0 0;
  font-size: 0.75rem;
  color: #aaa;
  font-weight: 400;
}

  .welcome-link:hover {
    color: #fff;
    text-decoration: underline;
  }
  header img {
    max-width: 180px;
    margin-bottom: 15px;
  }
  p.subtitle {
    margin: 0;
    font-size: 1rem;
    color: #aaa;
  }
  main {
    max-width: 1000px;
    margin: 40px auto;
    padding: 0 20px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
  }
  .product {
    background-color: #1c1c1c;
    border-radius: 12px;
    overflow: hidden;
    text-align: center;
    padding-bottom: 20px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.4);
    position: relative;
    cursor: pointer;
  }
  .product .image-container {
    position: relative;
    width: 100%;
    overflow: hidden;
  }
  .product img {
    width: 100%;
    height: auto;
    display: block;
    transition: opacity 0.5s ease;
  }
  .product img.front {
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    pointer-events: none;
  }
  .product:hover img.retro {
    opacity: 0;
  }
  .product:hover img.front {
    opacity: 1;
  }
  .product h3 {
    margin: 15px 0 5px;
    font-size: 1.2rem;
  }
  .product p {
    color: #aaa;
    font-size: 0.9rem;
    padding: 0 10px;
  }
  footer {
    text-align: center;
    padding: 40px 20px;
    font-size: 0.9rem;
    color: #777;
  }
  a {
    color: #f3f3f3;
    text-decoration: underline;
  }
  /* Lightbox */
  #lightbox {
    display: none;
    position: fixed;
    top:0; left:0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.8);
    z-index: 1000;
    justify-content: center;
    align-items: center;
  }
  #lightbox .content {
    display: flex;
    gap: 40px;
    max-width: 90vw;
    max-height: 80vh;
  }
  #lightbox img {
    max-width: 40vw;
    max-height: 80vh;
    border-radius: 10px;
    object-fit: contain;
  }
  #lightbox .close-btn {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 2rem;
    color: #fff;
    cursor: pointer;
  }
  .size-guide {
  max-width: 900px;
  margin: 60px auto;
  padding: 0 20px;
  color: #eee;
  text-align: center;
}

.size-guide h2 {
  font-size: 1.5rem;
  margin-bottom: 20px;
}

.size-guide table {
  width: 100%;
  border-collapse: collapse;
  border: 2px solid #777;
  background-color: #1a1a1a;
  border-radius: 8px;
  overflow: hidden;
}

.size-guide th,
.size-guide td {
  padding: 12px;
  border: 1px solid #777;
  font-weight: 500;
}

.size-guide th {
  background-color: #2c2c2c;
  color: #f3f3f3;
}

.size-guide td {
  color: #ddd;
}

</style>
</head>
<body>

<header>
  <div class="header-bar">
    <a href="index.html" class="welcome-link">Benvenuti in Sottopelle</a>
    <p class="subtitle-small">Scrivici per preordinare le tue magliette</p>
  </div>
  <img src="logo.png" alt="Logo Sottopelle Brand" />
</header>

<main>

  <div class="product" onclick="openLightbox('tshirt1-front.png','tshirt1.png')">
    <div class="image-container">
      <img src="tshirt1.png" alt="T-shirt retro" class="retro" />
      <img src="tshirt1-front.png" alt="T-shirt fronte" class="front" />
    </div>
    <h3>T-shirt Unisex Nera</h3>
    <p>Passa sopra col mouse per vedere il fronte. Clicca per ingrandire.</p>
  </div>

  <div class="product" onclick="openLightbox('tshirt2-front.png','tshirt2.png')">
    <div class="image-container">
      <img src="tshirt2.png" alt="T-shirt retro" class="retro" />
      <img src="tshirt2-front.png" alt="T-shirt fronte" class="front" />
    </div>
    <h3>T-shirt Unisex Bianca</h3>
    <p>Passa sopra col mouse per vedere il fronte. Clicca per ingrandire.</p>
  </div>

  <div class="product" onclick="openLightbox('tshirt3-front.png','tshirt3.png')">
    <div class="image-container">
      <img src="tshirt3.png" alt="T-shirt retro" class="retro" />
      <img src="tshirt3-front.png" alt="T-shirt fronte" class="front" />
    </div>
    <h3>T-shirt Unisex Nera</h3>
    <p>Passa sopra col mouse per vedere il fronte. Clicca per ingrandire.</p>
  </div>

  <div class="product" onclick="openLightbox('tshirt4-front.png','tshirt4.png')">
    <div class="image-container">
      <img src="tshirt4.png" alt="T-shirt retro" class="retro" />
      <img src="tshirt4-front.png" alt="T-shirt fronte" class="front" />
    </div>
    <h3>T-shirt Unisex Bianca</h3>
    <p>Passa sopra col mouse per vedere il fronte. Clicca per ingrandire.</p>
  </div>

</main>
<section class="size-guide">
  <h2>Guida alle taglie</h2>
  <table>
    <thead>
      <tr>
        <th>Taglia</th>
        <th>XS</th>
        <th>S</th>
        <th>M</th>
        <th>L</th>
        <th>XL</th>
        <th>XXL</th>
        <th>3XL</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Altezza</td>
        <td>0</td>
        <td>70</td>
        <td>72</td>
        <td>74</td>
        <td>76</td>
        <td>78</td>
        <td>0</td>
      </tr>
      <tr>
        <td>Larghezza</td>
        <td>0</td>
        <td>47</td>
        <td>50</td>
        <td>53</td>
        <td>56</td>
        <td>59</td>
        <td>0</td>
      </tr>
    </tbody>
  </table>
</section>

<footer>
  Seguici su <a href="https://instagram.com/sottopelle.brand" target="_blank">Instagram</a> — oppure scrivici a <a href="mailto:sottopelle.brand@gmail.com">sottopelle.brand@gmail.com</a>
</footer>

<!-- Lightbox -->
<div id="lightbox" onclick="closeLightbox()">
  <span class="close-btn" onclick="closeLightbox(event)">&times;</span>
  <div class="content">
    <img id="lightbox-front" src="" alt="Fronte" />
    <img id="lightbox-retro" src="" alt="Retro" />
  </div>
</div>

<script>
  function openLightbox(frontImg, retroImg) {
    event.stopPropagation();
    const lightbox = document.getElementById('lightbox');
    document.getElementById('lightbox-front').src = frontImg;
    document.getElementById('lightbox-retro').src = retroImg;
    lightbox.style.display = 'flex';
  }

  function closeLightbox(e) {
    if(e) e.stopPropagation();
    document.getElementById('lightbox').style.display = 'none';
  }
</script>/Users/debora/Desktop/SottopelleSite/vetrina/logo.png

</body>
</html>
