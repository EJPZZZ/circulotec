<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Footer from '@/Components/Footer.vue';
import Login from '@/Pages/Auth/Login.vue';
import Register from '@/Pages/Auth/Register.vue';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});

</script>


<template v-else>
    <div>
  
      <!-- Header Section -->
      <div class="flex flex-col md:flex-row items-center p-4 #b9d6f2">
        <!-- Logo on the left -->
        <div style="display: flex; align-items: flex-start;">
  <img src="/storage/images/TECNO.png" alt="ITSS Logo" width="200" height="240" />
</div>
        
        <div class="space-x-4 ml-auto">
          <Link :href="route('login')">
            <button @click="iniciarSesion" class="custom-button">
             Iniciar Sesión
           </button>
          </Link>
          <Link :href="route('register')">
           <button @click="registrarse" class="custom-button">
             Registrarse
           </button>
          </Link>
        </div>
      </div>
  
      <!-- Main Content Section -->
    <!-- Main Content Section -->
    <div class="container mx-auto mt-[-20px] flex flex-col md:flex-row items-center">
  <div class="w-full md:w-1/2 md:pr-4 order-2 md:order-1">
    <h1 class="text-4xl md:text-8xl font-extrabold mb-5 pl-15">Bienvenido al Foro de Lectura ITSS</h1>
  </div>
  <div class="w-full md:w-1/2 mt-[-20px] md:mt-0 md:order-2">
    <img src="/storage/images/tecblue2.jpg" alt="" class="w-full md:w-4/4 h-auto">
  </div>
</div>
  
      <div class="mt-8"></div>
  
      <div class="bg-custom-blue text-white py-2">
        <div class="container mx-auto">
          <p class="text-2xl md:text-7xl text-center font-extrabold">
            ¡Te damos la bienvenida a nuestro espacio dedicado a la exploración y el disfrute de la literatura!
          </p>
        </div>
      </div>
  
      <div class="bg-custom-blue-light text-white py-8 flex flex-col md:flex-row items-center">
        <div class="container mx-auto md:w-1/2 pr-4 pt-8 md:pt-36">
          <p class="text-3xl md:text-5xl text-white font-extrabold pl-4 md:pl-36">
            Acceso Equitativo y Flexibilidad
          </p>
          <div class="mt-4 md:mt-8"></div>
          <p class="text-lg md:text-3xl text-white font-normal pl-4 md:pl-36 pb-2 md:pb-36">
            La plataforma digital permite a los estudiantes participar en círculos de lectura desde cualquier lugar, eliminando barreras geográficas y de movilidad.
          </p>
        </div>
        <div class="container mx-auto md:w-1/2 mt-4 md:mt-0">
          <img src="https://blogs.iadb.org/gestion-fiscal/wp-content/uploads/sites/6/2023/05/GettyImages-1331574296.jpg" alt="" class="w-full h-auto md:pr-36 pt-2">
        </div>
      </div>
      
      <div class="bg-custom-blue-light text-white py-8 flex flex-col md:flex-row items-center">
    <div class="container mx-auto w-full md:w-1/2 md:order-1">
        <img src="https://img.interempresas.net/fotos/P1376599.jpg" alt="" class="w-full h-auto md:pr-12 pt-2 pl-0 md:pl-36">
    </div>
    <div class="container mx-auto w-full md:w-1/2 pr-4 pt-8 md:pt-36 md:order-2">
        <p class="text-3xl md:text-5xl text-white font-extrabold pl-8 md:pl-20">
            Reducción del Uso de Recursos Naturales
        </p>
        <div class="mt-4 md:mt-8"></div>
        <p class="text-lg md:text-3xl text-white font-normal pl-8 md:pl-20 pb-2 md:pb-36">
            La eliminación del uso de papel y otros recursos asociados a la impresión reducirá la demanda de madera, agua y energía.
        </p>
    </div>
</div>

    <div class="bg-custom-blue-light text-white py-8 flex flex-col md:flex-row items-center">
        <div class="container mx-auto md:w-1/2 pr-4 pt-8 md:pt-36">
          <p class="text-3xl md:text-5xl text-white font-extrabold pl-4 md:pl-36">
            Mejora en el Seguimiento Académico
          </p>
          <div class="mt-4 md:mt-8"></div>
          <p class="text-lg md:text-3xl text-white font-normal pl-4 md:pl-36 pb-2 md:pb-36">
            La plataforma permite un seguimiento más preciso de la participación y el progreso académico de los estudiantes en los círculos de lectura.
          </p>
        </div>
        <div class="container mx-auto md:w-1/2 mt-4 md:mt-0">
          <img src="https://i.ibb.co/rm44hDd/Alumno.png" alt="" class="w-full h-auto md:pr-32 pt-2">
        </div>
      </div>
      
      <div class="bg-eaf4fe py-8 flex flex-col md:flex-row items-center">
        <div class="container mx-auto md:w-1/2 pr-4 pt-8 md:pt-36">
          <p class="text-3xl md:text-2xl text-white font-extrabold pl-4 md:pl-56">
            "Leer es más importante que escribir, porque la lectura es el camino que conduce a la escritura."
          </p>
          <div class="mt-4 md:mt-8"></div>
          <p class="text-lg md:text-2xl text-white font-normal pl-4 md:pl-56 pb-2 md:pb-36 md:text-right">
            Mario Benedetti
          </p>
        </div>
        <div class="container mx-auto md:w-1/2 mt-4 md:mt-0 ">
          <img src="https://s2.abcstatics.com/media/cultura/2020/09/14/Mario-Benedetti-kHfG-U401206819722nVG-620x649@abc.jpg" class=" rounded-3xl w-full md:w-2/3 lg:w-2/3 h-auto md:pt-2 pl-36">
        </div>
      </div>

      <Footer />
    </div>
  </template>
  
  <style scoped>
    h1 {
      color: #f8fafc;
    }
  
    button {
      cursor: pointer;
      border-radius: 1rem;
    }
  
    button.border-blue-500 {
      font-size: 1rem;
      line-height: 1.5rem;
      font-weight: 800;
      border: 2px solid #3490dc;
    }
  
    button.border-green-500 {
      font-size: 1rem;
      line-height: 1.5rem;
      font-weight: 800;
      border: 2px solid #38a169;
    }
  
    button:hover {
      transform: scale(1.05);
    }
  
    .custom-button {
      color: #f8fafc;
      background-color: transparent;
      border-radius: 16px;
      padding: 15px 30px;
      font-size: 18px;
      font-weight: 800;
      transition: background-color 0.3s, color 0.3s;
    }
  
    .custom-button:hover {
      background-color: #AEB7D4;
      color: white;
    }
  
    .bg-custom-blue {
      background-color: #1e378a;
    }
  
    .bg-custom-blue-light {
      background-color: #192B67;
    }
  </style>




