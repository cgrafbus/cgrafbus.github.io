<script setup>
let props = defineProps({
  header: {
    type:String,
    required: true
  },
  iconsource: {
    type: String,
    required: true,
  },
  content:{
    type:String,
    required: true
  },
  fromdate: {
    type:String,
  },
  untildate: {
    type:String
  }
});
const resolvedIcon = new URL(`../assets/icons/${props.iconsource}.png`, import.meta.url).href;
</script>

<template>
  <div class="expitem">
    <div class="exp">
        <img :src="resolvedIcon" class="expicon"/>
        <div class="expdate">{{ fromdate }} - {{ untildate }}</div>
    </div>
    <div class="expheader">{{ header }}</div>
    <p>
     {{ content }}
    </p>
</div>
</template>

<style scoped>
.exp {
    display: flex;
    flex-direction: row;
}

.exp {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: start;
  width: 100%;
}

.expdate{
    font-weight: bold;
    text-align: right;
}

.expitem {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.expicon {
  width: 180px;
  -webkit-filter: invert(80%);
  filter: invert(80%);
}

.expheader {
  text-align: left;
  color: var(--text-primary);
  font-weight: bolder;
  font-size: larger;
}
</style>
