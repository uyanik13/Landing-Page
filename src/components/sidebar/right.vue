<template>
  <div>
     <div class="mr-6 w-full  flex-shrink-0 flex flex-col">
        <div class="bg-white my-2 pb-6 w-full justify-center items-center overflow-hidden md:max-w-sm rounded-lg shadow-sm mx-auto">
          <div class="flex mt-0 px-2  items-center justify-between">
            <p class="text-l text-secondary text-center px-2 py-2">
              Add to your feed
            </p>
              <font-awesome-icon :icon="['fas', 'info-circle']" class="text-3"  />
          </div>
          <div class="flex flex-col">
              <a :href="feed.slug" class="flex p-4 items-start justify-between  " v-for="(feed, index) in feeds" :key="index">
                  <div>
                      <img class="rounded-full w-12"  :src="feed.avatar" alt="">
                  </div>
                  <div class="text-left  ">
                      <p class="mx-2 text-sm font-bold  flex items-start  ">{{feed.name}}</p>
                      <p class="mx-2 text-sm font-light text-gray-600 flex items-center ">{{feed.title}}</p>
                  </div>
                  <div class="flex text-blue-500  items-center  pr-2 rounded-full border-1 border-blue-500 hover:bg-theme1">
                      <font-awesome-icon :icon="['fas', 'plus']" class="mx-2"  /> Follow
                  </div>
              </a>
              

          </div>
          <a href="" class="my-2 text-l mx-4 px-4 py-1 rounded-lg text-blue-500 font-bold hover:bg-theme1">
              View all recommendations
            </a>
        </div>
     </div>
    <div class="mr-6 w-full  flex-shrink-0 flex flex-col">
      <div class="bg-white my-2 pb-6 w-full justify-center items-center overflow-hidden md:max-w-sm rounded-lg shadow-sm mx-auto">
        <div class="flex mt-0 px-2  items-center justify-between">
          <p class="text-l text-secondary text-center px-2 py-2 sm:text-white ">
            Today’s most viewed courses
          </p>
            <font-awesome-icon :icon="['fas', 'info-circle']" class="text-3"  />
        </div>
          <div class="text-3 hover:bg-theme1 mt-0 px-4 py-1">
            <a class="" href="#">
                <p class="text-gray-800 font-bold text-4  px-0">1. The Six Morning Habits of High Performe...</p>
                <p class="text-gray-500 font-bold text-3  px-0">Pete Mockaitis | How to Be Awesome at Your Job...</p>
            </a>
         </div>
          <div class="text-3 hover:bg-theme1 mt-0 px-4 py-1">
            <a class="" href="#">
                <p class="text-gray-800 font-bold text-4  px-0">2. Unconscious Bias</p>
                <p class="text-gray-500 font-bold text-3  px-0">Stacey Gordon</p>
            </a>
         </div>
          <div class="text-3 hover:bg-theme1 mt-0 px-4 py-1">
            <a class="" href="#">
                <p class="text-gray-800 font-bold text-4  px-0">3. Critical Thinking for Better Judgment and Decision-Making...</p>
                <p class="text-gray-500 font-bold text-3  px-0">Becki Saltzman</p>
            </a>
         </div>


        <a href="" class="my-2 text-l mx-4 px-4 py-1 rounded-lg text-blue-500 font-bold hover:bg-theme1">
            Show more on LinkedIn Learning
          </a>
      </div>
      
    </div>
  </div>

</template>

<script>
export default {
  name: "right-sidebar",
  components: {
   
  },

data () {
    return {
        
          feeds: [
            {
              name:'Cassie Kozyrkov',
              avatar:'https://media-exp1.licdn.com/dms/image/C4E03AQGFpxJsCianIg/profile-displayphoto-shrink_100_100/0/1517757130020?e=1614211200&v=beta&t=cuam354cLFrAn9dlnwdChYoqVO3vFvOOz6_wiXgKHB0',
              title:'Chief Decision Scientist at Google, Inc.',
              slug:'cassie-kozyrkov',
            },
            {
              name:'Ruya Aslantepe',
              avatar:'https://media-exp1.licdn.com/dms/image/C4D03AQFeIkZwQM1JIQ/profile-displayphoto-shrink_100_100/0/1556306342696?e=1614211200&v=beta&t=JZ8U_4SY2raKrB_5NBOvkb_HDB1UE8niVVcEDIzklmQ',
              title:'Web Developer at Linkedin ',
              slug:'ruya-aslantepe',
            },
            {
              name:'Simon Sinek',
              avatar:'https://media-exp1.licdn.com/dms/image/C4D03AQE8tuDC7QL-Nw/profile-displayphoto-shrink_100_100/0/1555526594402?e=1614211200&v=beta&t=vKeOBQtcmW-h8Qx0Ccfn4Jq_QLAHJmb_SzBY6tHEDaM',
              title:'Optimist and Author at Simon Sinek Inc',
              slug:'simon-sinek',
            },
          ]
    
     }
  },
  computed: {
  

  },
  watch : {

     
  },
  methods : {
     

  },
 
  mounted () {
  

  },
  created () {
    

  }

}
</script>