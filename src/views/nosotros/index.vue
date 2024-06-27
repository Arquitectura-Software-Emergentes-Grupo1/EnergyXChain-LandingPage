<template>
    <HeroComponent
      sectionTitle='Nosotros'
      firstPart="Nosotros"
      secondPart=""
      paragraph=""
      :showButton="false"
    />

    <div id="ourGoal">
        <h1 class="title" v-motion-fade-visible>Nuestro Objetivo</h1>
        <div class="ourGoal-container container">
            <div class="left-side">
                <p class="about-us-text">Nuestro objetivo es claro: promover la privacidad y la seguridad en las transacciones, especialmente en criptomonedas y compra de energía centralizada. Nos esforzamos por ser líderes en el sector, ofreciendo soluciones innovadoras basadas en tecnología blockchain y contratos inteligentes.<br><br>En resumen, nuestra meta es asegurar que cada transacción sea segura, transparente y congruente, contribuyendo así a un mundo digital más confiable y protegido.</p>
            </div>
            <img class="image-ourGoal" v-motion-fade-visible src="../../assets/smiling-business-people-having-discussion-in-meeting-while-sitting-at-office-JSRF01362.jpg" alt="Nosotros">
        </div>
    </div>
    <div id="misionVision">
        <div class="misionVision-container container">
            <div class="left-side">
                <h1 class="title" v-motion-fade-visible>Misión</h1>
                <p class="misionVision-text">Proporcionar una solución innovadora y confiable que garantice la congruencia y transparencia en cada compra, utilizando tecnología avanzada como contratos inteligentes y blockchain para promover la confianza y la integridad en un mundo digitalizado.</p>
            </div>
            <div class="middle">
                <div class="vertical-line"></div>
            </div>
            <div class="right-side">
                <h1 class="title" v-motion-fade-visible>Visión</h1>
                <p class="misionVision-text">Ser la principal plataforma global que garantice la privacidad, la seguridad y la transparencia en todas las transacciones, revolucionando la forma en que las personas realizan compras, especialmente en el ámbito de las criptomonedas y la adquisición de energía centralizada. Nos esforzamos por crear un mundo digital donde cada usuario pueda realizar transacciones con total confianza y tranquilidad.</p>
            </div>
        </div>
    </div>
    <div id="about">
        <div class="misionVision-container container">
            <div class="left-side">
                <h1 class="title" v-motion-fade-visible>About the Product</h1>
                <iframe width="560" height="315" src="https://www.youtube.com/embed/t-ES2-IY9U0?si=L8G1bHqgIGgO7T3T" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
            <div class="middle">
                <div class="vertical-line"></div>
            </div>
            <div class="right-side">
                <h1 class="title" v-motion-fade-visible>About the Team</h1>
                <iframe width="560" height="315" src="https://www.youtube.com/embed/fU1Tb4UVDBk?si=wesHuimW7ZuVT9WY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <div id="contactUs">
        <h1 class="title" v-motion-fade-visible>Comunícate con nosotros</h1>
        <div class="contactUs-container container">
          <router-link to="/contacto"><button class="button-big" v-motion-fade-visible>CONTÁCTANOS</button></router-link>
        </div>
    </div>

    <FooterComponent/>

</template>

<script>
import FooterComponent from "../../components/Footer.vue";
import HeroComponent from "../../components/Hero.vue";
export default {
    name: 'NosotrosView',
    components: {
        FooterComponent,
        HeroComponent
    }
}
</script>
<style scoped>
    /* OUR GOAL */

    #ourGoal{
    padding: 3rem;
  }

  .ourGoal-container{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
  }

  #ourGoal .left-side{
    width: 50%;
  }

  .image-ourGoal{
    width: 522px;
    height: 388px;
    object-fit: cover;
    image-orientation: center;
    margin-top: 2rem;
  }

    /* MISION VISION */

    #misionVision{
        background-color: #F1F1F1;
        padding: 3rem;
    }
    #about{
        padding: 3rem;
    }

    .misionVision-container{
        display: grid;
        grid-template-columns: 1fr 0 1fr;
        gap: 2rem;
    }
    .left-side, .right-side{
      display: flex;
      flex-direction: column;
    }
    .misionVision-text{
        text-align: justify;
    }
    .vertical-line{
        border-left: 5px solid #024955;
        height: 100%;
    }
    /* CONTACT */

  #contactUs{
    padding: 3rem;
  }

  .contactUs-container{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
  }

  /* RESPONSIVE */
@media only screen and (max-width: 1000px) {
    /* Estilos específicos para pantallas con ancho máximo de 1000px */

    #ourGoal{
        padding: 3rem 0;
    }
    .ourGoal-container {
        flex-direction: column-reverse;
        align-items: center;
        padding: 0;
    }
    #ourGoal .left-side{
      width: 90%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .image-ourGoal{
        width: 323px;
        height: 242px;
        object-fit: cover;
        image-orientation: center;
    }

    #misionVision{
        padding: 3rem 0;
    }
    .misionVision-container{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 0;
      gap: 0;
    }
    .vertical-line{
        display: none;
    }
    #misionVision .left-side, #misionVision .right-side{
      width: 90%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

}
</style>