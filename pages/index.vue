<!-- pages/index.vue -->
<template>
  <div>
    <div class="main-content">
      <section class="hero">
        <h1 class="title">Selamat datang, Guys!</h1>
        <p class="subtitle">Temukan keuntungan belanja dengan kami</p>
      </section>

      <section class="features">
        <div class="feature">
          <h2 class="feature-title">Belanja Cepat</h2>
          <p class="feature-description">
            Temukan produk dengan cepat dan santai.
          </p>
        </div>

        <div class="feature">
          <h2 class="feature-title">Harga Terjangkau</h2>
          <p class="feature-description">
            Kualitas tinggi dengan harga yang ramah di kantong.
          </p>
        </div>

        <div class="feature">
          <h2 class="feature-title">Produk Lengkap</h2>
          <p class="feature-description">
            Pilih dari berbagai produk lengkap berkualitas.
          </p>
        </div>
      </section>
    </div>
  </div>
</template>

<style scoped>
.main-content {
  background-color: #f9f9f9;
  width: 100%;
  margin: 0 auto;
  padding: 80px 15px;
}

.hero {
  text-align: center;
  margin-bottom: 40px;
}

.title {
  font-size: 3rem;
  color: #333;
  margin-bottom: 10px;
}

.subtitle {
  font-size: 1.2rem;
  color: #555;
}

.features {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.feature {
  flex: 1;
  text-align: center;
  padding: 20px;
  border: 2px solid #ddd;
  border-radius: 8px;
  margin: 0 10px 20px;
  background-color: white;
  transition: transform 0.3s;
}

.feature:hover {
  transform: scale(1.05);
}

.feature-title {
  font-size: 1.8rem;
  color: #333;
  margin-bottom: 10px;
}

.feature-description {
  font-size: 1.2rem;
  color: #666;
}
</style>
