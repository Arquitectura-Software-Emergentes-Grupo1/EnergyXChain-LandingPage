<template>
    <HeroComponent
      sectionTitle='Servicios'
      firstPart="Nuestros"
      secondPart="servicios"
      paragraph=""
      :showButton="false"
    />

    <div id="ourService1">
        <h2 class="title" v-motion-fade-visible>Múltiples proveedores de energía</h2>
        <div class="ourServices-container container">
            <div class="left-side">
                <p class="ourServices-text">Ofrecemos una plataforma que agiliza el acceso a una amplia gama de opciones, permitiendo a los usuarios elegir entre ser proveedores o consumidores con base en sus preferencias y necesidades individuales. Esto garantiza una mayor flexibilidad y competitividad en el mercado de la energía, brindando a nuestros usuarios la capacidad de encontrar las mejores ofertas y optimizar sus costos.</p>
            </div>
            <img class="image-ourServices" v-motion-fade-visible src="../../assets/two-businessmen-shaking-hands-in-front-of-a-large-window-generative-ai-free-photo.jpeg" alt="Servicio 1 - Múltiples proveedores de energía">
        </div>
    </div>
    <div id="ourService2">
        <h2 class="title" v-motion-fade-visible>Seguridad con Blockchain</h2>
        <div class="ourServices-container container">
            <div class="left-side">
                <p class="ourServices-text">En cuanto a la seguridad con Blockchain, implementamos tecnología de vanguardia para proteger cada transacción. Mediante el uso de blockchain, aseguramos la integridad y la inmutabilidad de los datos, previniendo así fraudes y garantizando la confianza en cada interacción. Nuestros usuarios pueden realizar transacciones con total tranquilidad, sabiendo que sus datos están protegidos de manera segura y transparente.</p>
            </div>
            <img class="image-ourServices" v-motion-fade-visible src="../../assets/blckchnbsns.jpg" alt="Servicio 2 - Seguridad con Blockchain">
        </div>
    </div>
    <div id="ourService3">
        <h2 class="title" v-motion-fade-visible>Transparencia y estadísticas en tiempo real</h2>
        <div class="ourServices-container container">
            <div class="left-side">
                <p class="ourServices-text">Ofrecemos transparencia y estadísticas en tiempo real para empoderar a nuestros usuarios con información detallada sobre sus transacciones. Con acceso instantáneo a estadísticas actualizadas, nuestros usuarios pueden monitorear sus gastos, analizar patrones de consumo y tomar decisiones informadas para optimizar su experiencia financiera. Esto promueve una mayor confianza y control en sus operaciones económicas en un entorno cada vez más digitalizado.</p>
            </div>
            <img class="image-ourServices" v-motion-fade-visible src="../../assets/statistics-graph-illustration-e1636972138897.jpg" alt="Servicio 3 - Transparencia y estadísticas en tiempo real">
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
    name: 'ServiciosView',
    components: {
        FooterComponent,
        HeroComponent
    }
}
</script>
<style scoped>
      /* OUR SERVICES */

    #ourService1, #ourService3{
        padding: 3rem;
    }
    #ourService2{
        background-color: #F1F1F1;
        padding: 3rem;
    }

  .ourServices-container{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
  }

  .ourServices .left-side{
    width: 50%;
  }

  .image-ourServices{
    width: 522px;
    height: 388px;
    object-fit: cover;
    image-orientation: center;
    margin-top: 2rem;
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

    #ourService1, #ourService2, #ourService3{
      padding: 2rem 0;
    }
    .ourServices-container {
      flex-direction: column-reverse;
      align-items: center;
      padding: 0;
    }
    .ourServices-container .left-side{
      width: 90%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .image-ourServices{
        width: 242px;
        height: 242px;
        object-fit: cover;
        image-orientation: center;
        margin: 0;
    }
    .ourServices-text{
      margin: 0;
    }
}
</style>