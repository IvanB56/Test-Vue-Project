<template>
  <div class="bs__card" :class="card.sailed? 'disabled': ''">
    <div class="card__body">
      <div class="img-inner">
        <img :src="card.img" alt="Photo">
      </div>
      <div class="info-inner">
        <div class="title">
          <p>{{ card.name }}</p>
          <p>{{ card.author }}</p>
        </div>
        <div v-if="!card.sailed" class="info">
          <div class="cost">
            <span class="cost__old" v-if="!!card.old_cost">{{ card.old_cost }}</span>
            <span>{{ card.cost }}</span>
          </div>
          <my-button v-if="!card.isBasket" @click="$emit('addBasket', card)" :data-key="card.id">Купить</my-button>
          <my-button v-else><i class="fa fa-check" aria-hidden="true"></i> В корзине</my-button>
        </div>
        <div v-else class="sailed">
          <span>Продана на аукционе</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyCard",
  props: {
    card: {
      type: Object,
      required: true,
    }
  },
}
</script>

<style scoped>
.bs__card {
  max-width: 25%;
  width: 25%;
  padding: 15px;
  align-self: stretch;
}

.disabled {
  opacity: 0.5;
}

.card__body {
  border: 1px solid #E1E1E1;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.info-inner {
  padding: 0 15px 15px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  flex: 1 0 auto;
}

.info {
  display: flex;
  flex: 0 0 auto;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.cost {
  display: flex;
  flex-direction: column;
  flex: 0 0 auto;
  font-size: 16px;
}

.cost__old {
  text-decoration: line-through;
  font-size: 14px;
  color: #A0A0A0;
}

.title {
  flex: 0 0 auto;
  margin-bottom: 5px;
}

.sailed {
  margin: auto 0;
  flex: 0 0 auto;
}

img {
  width: 100%;
  height: auto;
}

p {
  margin-bottom: 5px;
  font-size: 18px;
}
</style>