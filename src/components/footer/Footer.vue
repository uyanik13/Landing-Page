<template>
  <footer class="bg-themeBG " >
    <div class="text-white text-center w-full py-20 hidden md:block lg:block xl:block  "
          style="background-image: url(assets/img/footer-bg-1.png) ; background-size: cover; background-attachment:scroll">
        <span class="font-commissioner text-8">What's Happening in Brisbane</span>
        <div class="flex flex-row px-24 mt-6">
             <div class="flex-1">
               <span class="text-10 font-sans">2,154</span>
               <p class="text-grey-400 text-sm uppercase font-sans ">PROPERTIES AVAIBLE</p>
            </div>
             <div class="flex-1">
               <span class="text-10 font-sans">$20M</span>
                <p class="text-grey-400 text-sm uppercase font-sans">DEALS MADE ON PROPTO</p>
            </div>
             <div class="flex-1">
               <span class="text-10 font-sans">132</span>
                <p class="text-grey-400 text-sm uppercase font-sans">LOCAL AGENTS REGISTERED</p>
            </div>
             <div class="flex-1">
               <span class="text-10 font-sans">312</span>
                <p class="text-grey-400 text-sm uppercase font-sans">CURRENT DEAL NEGOTIATIONS</p>
            </div>
            
        </div>
    </div>

    <div class="bg-themeBG flex flex-row lg:py-20 lg:px-24 text-left text-grey-400 font-noto-sans z-0">
        <div class="text-left ml-8  md:w-1/5 lg:w-1/5 sm:w-1/2  block lg:mx-auto md:mx-auto">
           <span class="my-4 text-xl sm:text-light  block">See how Propto can turn your ideal commercial property into reality</span>
           <input type="text" class="bg-transparent rounded-lg h-8 w-8/12 border border-grey-100 focus:border-blue-500 text-white px-4" placeholder="Enter your email address">
            <button @click="tryFreeNow" class="bg-transparent mt-4 text-sm text-white text-left block rounded-none border-none mb-6">
              <a class="mt-4 text-sm block">try free now</a>
               <img src="/assets/img/button_line.png" alt="">
            </button>
        </div>

        <div class="md:w-1/5 lg:w-1/5 sm:w-1/2  block ">
           
        </div>

        <div class="md:w-1/5 lg:w-1/5 sm:w-1/2 block">
           
           <ul class="text-left list-none  ">
             <span class="text-xs text-grey-500  uppercase block">PROPTO</span>
             
            <li class="mt-2 inline-block flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">why propto</a>
            </li>
            <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">our mission</a>
            </li>
               <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">pricing structure</a>
            </li>
              <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">agent login</a>
            </li>
           
          </ul>
           
        </div>

        <div class="md:w-1/5 lg:w-1/5 sm:w-1/2 block " >
           
           <ul class="text-left">
             <span class="text-xs text-grey-500 uppercase">LEARN</span>
               <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">knowledge base</a>
            </li>
               <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">how it works</a>
            </li>
             <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">market info</a>
            </li>
               <li class="mt-2 inline-block  flex md:mr-0">
              <a href="#" class="font-light no-underline hover:underline text-grey-300 hover:text-grey-600">contact us</a>
            </li>
           
          </ul>
           
        </div>
        

        <div class="md:w-1/5 lg:w-1/5 block ">
           
           <ul class="text-left">
             <span class="text-xs text-grey-500 uppercase">CONNECT WITH US</span>
           <div class="flex flex-row">
                  <font-awesome-icon @click="tryFreeNow" :icon="['fab', 'facebook-square']" class="px-2 mt-3 text-grey-600 hover:text-white" size="2x"   />
                  <font-awesome-icon :icon="['fab', 'twitter']" class="px-2 mt-3 text-grey-600 hover:text-white" size="2x"   />
                  <font-awesome-icon :icon="['fab', 'youtube']" class="px-2 mt-3 text-grey-600 hover:text-white" size="2x"  />
           </div>
            
          </ul>
           
        </div>
          
    </div>

        <div class="divide-y-2 grey-400"></div>
            <div class="bg-grey-700" style="padding-bottom:1px"></div>
          <ul class="text-left">
             <li class="mt-2 inline-block ">
              <a href="#" class="font-light text-sm  mr-2 no-underline hover:underline text-grey-600 hover:text-grey-800">© Propto 2020</a>
            </li>

               <li class="mt-2 inline-block  md:mr-0">
              <a href="#" class="font-light text-sm  mr-2 no-underline hover:underline text-grey-600  hover:text-grey-600">Disclaimer</a>
            </li>

             <li class="mt-2 inline-block  md:mr-0">
              <a href="#" class="font-light text-sm  mr-2 no-underline hover:underline text-grey-600 hover:text-grey-600"> Terms & Conditions </a>
            </li>
           
            <li class="mt-2 inline-block  md:mr-0">
              <a href="#" class="font-light text-sm  mr-2 no-underline hover:underline text-grey-600 hover:text-grey-600">Privacy Policy</a>
            </li>

            <li class="mt-2 inline-block  md:mr-0">
              <a href="#" class="font-light text-sm  mr-2 no-underline hover:underline text-grey-600 hover:text-grey-600">Sitemap</a>
            </li>

            <li class="mt-2 inline-block  md:mr-0">
              <a href="#" class="font-light text-sm no-underline hover:underline text-grey-600 hover:text-grey-600">Agent Dashboard</a>
            </li>
           
          </ul>

  </footer>
</template>

<script>
export default {
  name: "Footer",
  components: {
   
  },
data () {
    return {
     
     }
  },
  computed: {
  

  },
  watch : {

     
  },
  methods : {
      tryFreeNow(){
        console.log('clicked')
      }

  },
 
  mounted () {
  

  },
  created () {
    

  }

}
</script>

<style scoped>

</style>