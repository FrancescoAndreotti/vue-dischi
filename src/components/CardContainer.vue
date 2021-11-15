<template>
  <div class="row row-cols-5 g-4">
    <div class="col" v-for="(item, i) in discsList" :key="i">
      <div class="card my-card">
        <img :src="item.poster" class="card-img-top" alt="..." />
        <div class="card-body">
          <h5 class="card-title text-center text-white">{{ item.title }}</h5>
          <p class="card-text text-center text-secondary my-0">
            {{ item.author }}
          </p>
          <p class="card-text text-center text-secondary my-0">
            {{ item.year }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from "axios";
export default {
  name: "CardContainer",
  data() {
    return {
      discsList: [],
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => (this.discsList = [...response.data.response]));
  },
};
</script>
