<template>
  <div class="d-flex category py-2 px-3">
    <a class="d-flex"
      ><span class="material-icons icon"> {{ item.img }} </span>
      <span class="pl-2"> {{ item.text }} </span></a
    >
  </div>
</template>

<script>
export default {
  props: {
    item: {
      required: true,
      type: Object,
    },
  },
};
</script>

<style scoped>
.category:hover {
  /* box-shadow: -4px 4px 2px rgba(204, 201, 201, 0.3); */
  box-shadow: -2px 3px 5px rgb(0 0 0 / 10%);
}
a,
a:hover {
  color: inherit;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.3s ease;
}

.icon {
  padding-right: 10px;
}
</style>
