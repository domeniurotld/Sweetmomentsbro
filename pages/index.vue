<template>
  <div class="home-page">
    <section id="home" class="intro-section">
      <div class="intro-content">
        <div class="image-container">
          <img src="/assets/images/cupcake.png" alt="Cupcake">
        </div>
        <div class="text-content">
          <h1 class="welcome-title">Bun venit la</h1>
          <h2 class="company-name">• SWEET MOMENTS •</h2>
          <p class="simple-text">
            Intră într-un univers al gusturilor rafinate, unde fiecare prăjitură este o operă de artă dulce. La Sweet Moments, te așteaptă o colecție de delicii create pentru a aduce bucurie fiecărui moment special. Explorează produsele noastre și lasă-te cucerit de savoarea autentică a deserturilor deosebite.
          </p>
          <a href="tel:+40747845733">
            <button class="contact-button">Contactează-ne</button>
          </a>
        </div>
      </div>
    </section>

    <section class="mission-section">
      <div class="mission-content">
        <div class="text-content">
          <h1 class="welcome-title">Misiunea noastra</h1>
          <h2 class="company-name">• Momente dulci de neuitat •</h2>
          <p class="simple-text">
            Misiunea noastră este să aducem bucurie prin deserturi realizate cu pasiune și ingrediente de top. La Sweet Moments, fiecare prăjitură este creată pentru a transforma momentele speciale în amintiri dulci și de neuitat.
          </p>
        </div>
        <div class="image-container">
          <img src="/assets/images/minicake.jpg" alt="Mini Cake">
        </div>
      </div>
    </section>

    <section id="products" class="products-section">
      <h2 class="section-title">Produsele noastre</h2>
      <hr class="section-divider">
      <div class="products-grid">
        <div class="product-card">
          <div class="product-image">
            <img src="/assets/images/bdaycake.jpg" alt="Torturi">
          </div>
          <h3 class="product-title">• Torturi</h3>
          <p class="simple-text">
            Torturi create cu atenție la detalii, folosind ingrediente de calitate, pentru a aduce un gust rafinat fiecărei ocazii speciale.
          </p>
        </div>
        <div class="product-card">
          <div class="product-image">
            <img src="/assets/images/minicake2.jpg" alt="Prajituri">
          </div>
          <h3 class="product-title">• Prăjituri</h3>
          <p class="simple-text">
            Prăjituri ce combină arome autentice și texturi fine, oferind momente de răsfăț cu fiecare mușcătură.
          </p>
        </div>
        <div class="product-card">
          <div class="product-image">
            <img src="/assets/images/cupcake2.jpg" alt="Briose">
          </div>
          <h3 class="product-title">• Brioșe</h3>
          <p class="simple-text">
            Răsfățuri mici si delicioase ,cu arome variate și o textură perfectă, ideale pentru orice moment dulce.
          </p>
        </div>
      </div>
    </section>

    <section id="aboutus" class="about-section">
      <h2 class="section-title">Despre noi</h2>
      <hr class="section-divider">
      <p class="simple-text">
        • La Sweet Moments, pasiunea noastră pentru patiserie se reflectă în fiecare desert pe care îl creăm. <br>
        • Suntem dedicați să aducem bucurie și momente dulci în viața fiecărui client prin prăjituri, torturi și brioșe realizate cu dragoste și măiestrie. <br>
        • Începutul nostru a fost simplu, pornind de la dorința de a împărtăși cu alții plăcerea unor deserturi autentice, pregătite cu ingrediente de cea mai bună calitate. Fiecare produs este o combinație perfectă de tradiție și inovație, menită să încânte atât papilele gustative, cât și privirea. <br>
        • Credem că fiecare ocazie merită să fie sărbătorită cu un desert special. De aceea, ne străduim să creăm produse personalizate care să transforme orice moment într-o amintire dulce și de neuitat.
      </p>
    </section>

    <section class="carousel-section">
      <img-carousel/>
    </section>

    <section id="contact" class="contact-section">
      <h2 class="section-title">Contact</h2>
      <hr class="section-divider">
      <p class="simple-text">
        Fiecare prăjitură și tort este creat cu pasiune pentru a aduce bucurie și savoare în viața voastră. <br>
        Vă invităm să descoperiți colecția noastră de delicii și să ne permiteți să facem parte din momentele voastre speciale! <br>
        Contactați-ne și haideți să transformăm împreună aceste momente în amintiri de neuitat. <br>
        <br>
        &nbsp;&nbsp;&nbsp;• Adresa: <b>Str. Poiana Cotargasului, nr. 64, Brosteni, SUCEAVA, ROMANIA</b> <br>
        &nbsp;&nbsp;&nbsp;• Telefon: <b>+40 744 546 027</b> <br>
        &nbsp;&nbsp;&nbsp;• Email: <b>sweetmoments.bro@yahoo.com</b>
      </p>
    </section>
  </div>
</template>

<script>
import ImgCarousel from '~/components/ImgCarousel.vue';
</script>

<style scoped>
.home-page {
  padding: 3rem 1.5rem;
}

/* Apply padding adjustments for larger screens */
@media (min-width: 1300px) {
  .home-page {
    padding-left: 16rem;
    padding-right: 16rem;
  }

  .welcome-title {
    font-size: 3.4rem !important; /* Adjust font size for larger screens */
  }

  .section-title {
    font-size: 3.6rem !important; /* Adjust font size for larger screens */
  }

  .company-name {
    font-size: 2rem !important; /* Adjust font size for larger screens */
  }

  .product-title {
    font-size: 2rem !important; /* Adjust font size for larger screens */
  }

  .simple-text {
    font-size: 1.4rem !important;
  }
}

.intro-section, .mission-section, .products-section, .carousel-section, .contact-section {
  margin-bottom: 4rem;
}

.about-section {
  margin-bottom: 1.5rem;
}

.intro-content, .mission-content {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  align-items: center;
}

.text-content {
  flex: 1;
}

.image-container {
  flex: 1;
  max-width: 500px;
  height: auto;
  overflow: hidden;
}

.image-container img, .product-image img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.welcome-title, .section-title {
  font-size: 3.4rem;
  font-weight: 500;
  margin: 0;
}

.company-name {
  font-size: 1.5rem;
  color: #ef859c;
  margin-top: 0.2em;
  margin-bottom: 0.5em;
}

.simple-text {
  font-size: 1rem;
  color: rgb(54, 54, 54);
  margin-top: 0;
}

.contact-button {
  background-color: #ef859c;
  border: none;
  color: white;
  padding: 0.6rem 1rem;
  border-radius: 6px;
  cursor: pointer;
  font-size: 1rem;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}

.product-title {
  margin-top: 0.6rem;
  margin-bottom: 0.6rem;
  font-size: 1.5rem;
  color: #ef859c;
}

.section-divider {
  border: none;
  height: 1px;
  background-color: black;
  width: 100%;
  margin-bottom: 1rem;
}

@media (max-width: 768px) {
  .intro-content, .mission-content {
    flex-direction: column;
  }
  
  .contact-button {
    width: 100%;
  }

  .welcome-title, .section-title {
    font-size: 2.5rem;
  }
  .intro-section, .mission-section, .products-section, .carousel-section, .contact-section {
    margin-bottom: 2rem;
  }
  .simple-text {
        font-size: 1.2rem;
    }
}

</style>
