<template>
  <div class="container dischi-cont" >
       <div class="disco-cont" v-for="(elm, index) in dischi" :key="index">
            <Album :info="elm" />
      </div>
  </div>
</template>

<script>
import Disco from "./Disco.vue";
import axios from "axios";
export default {
    name: "Dischi",
    components: {
        Disco
  },
  data(){
      return {
          dischi : []
      }
  },
  created(){
      axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) =>{
            this.dischi = res.data.response;
        }
        );
  }
}
</script>

<style lang="scss" scoped>
.dischi-cont{
    display: flex;
    flex-wrap: wrap;
    gap: .9375rem 1.5625rem;
    .disco-cont{
        width: calc(100% / 5 - 1.5625rem);
    }
}
</style>