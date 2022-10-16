<template>
  <div id="content">
    <div class="container">
      <h2>Картины эпохи Возрождения</h2>
      <div class="cards__inner">
        <bs-card
            v-for="card in cards"
            :card="card"
            :key="card.id"
        ></bs-card>
      </div>
    </div>
  </div>
</template>

<script>
import BsCard from "@/Components/BsCard";

export default {
  name: "bsBody",
  components: {BsCard},
  props: {
    cards: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>
#content {
  flex: 1 0 auto;
}

.cards__inner {
  margin: 0 -15px;
  display: flex;
}

h2 {
  margin-top: 25px;
}
</style>