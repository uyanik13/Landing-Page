<template>
  <div class="bg-white flex-row justify-center h-15 w-full bottom-0 z-40 fixed block sm:block md:block lg:hidden" >
      <div class="container mx-auto px-10 flex justify-between items-center ">
            <nav class="w-full">
                <ul class="flex list-none pb-1" >
                  <li v-for="item in Menu" :key="item.id">
                      <div class="grid text-primary hover:text-black text-center" >
                          <font-awesome-icon :icon="['fas', item.icon]" class="mt-3 pb-2 text-7 mx-7"  />
                          <span class="text-xs ">{{item.title}}</span>
                      </div>
                  </li>
                </ul>
            </nav>
      </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  components: {
   
  },
data () {
    return {
        Menu : [
          {
            id: 1,
            title: 'Anasayfa',
            slug: 'home',
            icon: 'home',
          },
          {
            id: 2,
            title: 'Sepet',
            slug: 'my-network',
            icon: 'shopping-cart',
          },
          
          {
            id: 4,
            title: 'Siparişlerim',
            slug: 'post',
            icon: 'shipping-fast',
          },
          {
            id: 5,
            title: 'Hesabım',
            slug: 'notifications',
            icon: 'user',
          },
          // {
          //   id: 6,
          //   title: 'Favorilerim',
          //   slug: 'jobs',
          //   icon: 'heart',
          // },
          
          
        ]
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