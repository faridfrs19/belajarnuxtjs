<template>
  <div>
    <div class="main-content">
      <section class="hero">
        <div class="hero-background"></div>
        <div class="hero-content">
          <h1 class="title">SELAMAT DATANG DI KOPERASI SEKOLAH</h1>
          <p class="subtitle">Melayani Kebutuhan Anda dengan Layanan Terbaik</p>
          <div class="shop-container">
            <img class="shop" src="../public/images/shop.png" alt="">
          </div>
          <NuxtLink to="/product" class="buton text-base bg-blue-600 px-4 py-2 text-white rounded-lg hover:bg-blue-600/80">Selengkapnya</NuxtLink>
        </div>
      </section>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

.title,
.subtitle {
  font-family: 'Poppins', sans-serif;
  margin: 10px;
}

.buton{
  margin-top: 20px; /* Sesuaikan dengan tinggi margin yang diinginkan */
  display: inline-block;
  text-decoration: none;
  color: white;
  background-color: #3490dc;
  padding: 8px 16px;
  border-radius: 8px;
}

.buton:hover{
  background-color: blue;
}

.shop-container {
  width: 100%;
  text-align: center;
}

.shop {
  width: 35%;
  display: inline-block;
  margin-top: 20px; /* Sesuaikan dengan tinggi margin yang diinginkan */
}

/* Responsivitas Tablet (ukuran lebar antara 600px dan 1023px) */
@media (min-width: 600px) and (max-width: 1023px) {
  .shop {
    width: 50%; /* Sesuaikan lebar gambar shop untuk tablet */
  }
}

/* Responsivitas Mobile (ukuran lebar kurang dari 600px) */
@media (max-width: 599px) {
  .shop {
    width: 100%; /* Sesuaikan lebar gambar shop untuk perangkat mobile */
  }
}

.main-content {
  background-image: url(../public/images/sknc.jpg);
  background-size: cover;
  margin: 0 auto;
  padding: 50px 50px;
  position: relative;
}

.hero {
  position: relative;
  text-align: center;
  margin-bottom: 20px;
  overflow: hidden;
  border-radius: 8px;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  opacity: 0.8;
}

.hero-content {
  color: white;
  padding: 20px;
}

.title {
  font-size: 2rem;
  font-weight: bold;
  font-family: 'Poppins', sans-serif;
  margin-bottom: 10px;
  animation: fadeInUp 1s ease;
}

.subtitle {
  font-size: 1rem;
  font-weight: bold;
  font-family: 'Poppins', sans-serif;
  color: white;
  animation: fadeInUp 1.5s ease;
}

/* Animasi CSS */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
