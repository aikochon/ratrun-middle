<template>
  <div>
    <button @click="clickAccordion">{{ title }}</button>
    <div v-if="isAccordion">
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: { type: String, default: "ボタン" },
    description: { type: String, default: "詳細" },
  },
  setup() {
    const isAccordion = ref(false);
    const clickAccordion = () => {
      isAccordion.value = !isAccordion.value;
      //   if (isAccordion.value === true) {
      //     isAccordion.value = false;
      //   } else {
      //     isAccordion.value = true;
      //   }
    };
    return {
      isAccordion,
      clickAccordion,
    };
  },
};
</script>