<template>
    <HeroComponent
      sectionTitle='Inicio'
      firstPart="Bienvenidos a"
      secondPart="EnergyXChain"
      firstParagraph="Bienvenidos a EnergyXChain, donde garantizamos la privacidad y seguridad"
      secondParagraph="en tus transacciones de energía con soluciones innovadoras y confiables."
      :showButton="true"
    />
    <div id="ourServices">
        <h1 class="title" v-motion-fade-visible>¿Qué te ofrecemos?</h1>
        <div class="services-container container">
          <div class="service" v-motion-slide-visible-bottom>
            <a href="/servicios" class="enlace-servicios">
              <div class="image-service">
                <img src="../../assets/two-businessmen-shaking-hands-in-front-of-a-large-window-generative-ai-free-photo.jpeg" alt="Servicio 1 - Múltiples proveedores de energía">
                <div class="overlay">
                  Ver más
                </div>
              </div>
            </a>
              <h2 class="sub-title">Múltiples proveedores de energía</h2>
          </div>
          <div class="service" v-motion-slide-visible-bottom>
            <a href="/servicios" class="enlace-servicios">
              <div class="image-service">
                <img src="../../assets/blckchnbsns.jpg" alt="Servicio 2 - Seguridad con Blockchain">
                <div class="overlay">
                  Ver más
                </div>
              </div>
            </a>
              <h2 class="sub-title">Seguridad con Blockchain</h2>
          </div>
          <div class="service" v-motion-slide-visible-bottom>
            <a href="/servicios" class="enlace-servicios">
              <div class="image-service">
                <img src="../../assets/statistics-graph-illustration-e1636972138897.jpg" alt="Servicio 3 - Transparencia y estadísticas en tiempo real">
                <div class="overlay">
                  Ver más
                </div>
              </div>
            </a>
              <h2 class="sub-title">Transparencia y estadísticas en tiempo real</h2>
          </div>
      </div>
    </div>
   
    <div id="aboutUs">
        <h1 class="title" v-motion-fade-visible>Nosotros</h1>
        <div class="aboutUs-container container">
            <div class="left-side">
                <p class="about-us-text">En nuestra empresa. nos enfocamos en garantizar la privacidad y el anonimato en las transacciones, incluso en la compra de energía centralizada. Utilizamos contratos inteligentes para asegurar la transparencia y congruencia de los cargos, permitiendo a los usuarios verificar cada detalle. Nuestro objetivo es proporcionar una solución segura y confiable que brinde tranquilidad en un mundo digitalizado. Nos especializamos en ofrecer una plataforma que proteja la privacidad de los usuarios y promueva la confianza en todas las transacciones.</p>
                <router-link to="/nosotros"><button class="button" v-motion-fade-visible>Conócenos más</button></router-link>
            </div>
            <img class="image-aboutUs" v-motion-fade-visible src="../../assets/dev-team.jpeg" alt="Nosotros">
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
    name: 'InicioView',
    components: {
        FooterComponent,
        HeroComponent,
    },
    data(){
      return {
        msg: 'I will change'
      }
    }
  }
  </script>
  
  <style scoped>



    /* SERVICE */

  #ourServices {
      padding: 3rem;
  }

  .services-container {
      display: flex;
      justify-content: space-evenly;
      gap: 2rem;
      padding: 1rem;
  }
  
  .service {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      color: #024955;
      width: 305px;

  }

  .service .image-service {
      position: relative; /* Asegura que el overlay se superponga a la imagen */
      
  }
  .service .image-service img {
      width: 305px;
      height: 305px;
      object-fit: cover;
      image-orientation: center;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 97%;
    background-color: rgba(36, 160, 218, 0.75); /* Verde con transparencia */
    color: white;
    font-size: 24px;
    text-align: center;
    opacity: 0; /* Inicialmente oculto */
    transition: opacity 0.3s ease;
    display: flex;
    justify-content: center; /* Centrado horizontal */
    align-items: center; /* Centrado vertical */
  }

  /* .enlace-servicios{
    opacity: 0; 
    animation: appearFromBottom 1s ease forwards; 
  } */
  .enlace-servicios:hover .overlay {
    opacity: 1; /* Mostrar overlay al pasar el mouse */
  }

  /* US */

  #aboutUs{
    background-color: #F1F1F1;
    padding: 3rem;
  }

  .aboutUs-container{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
  }

  #aboutUs .left-side{
    width: 50%;
  }

  .image-aboutUs{
    width: 522px;
    height: 388px;
    object-fit: cover;
    image-orientation: center;
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

    .services-container {
      flex-direction: column;
      align-items: center;
      padding: 0;
    }

    .service .image-service img {
      width: 244px;
      height: 244px;
      object-fit: cover;
      image-orientation: center;
  }

  #aboutUs{
    padding: 3rem 0;
  }
    .aboutUs-container{
      flex-direction: column-reverse;
      align-items: center;
      justify-content: center;
    }

    #aboutUs .left-side{
      width: 90%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .image-aboutUs{
    width: 244px;
    height: 244px;
    object-fit: cover;
    image-orientation: center;
  }
 

}
  </style>
  