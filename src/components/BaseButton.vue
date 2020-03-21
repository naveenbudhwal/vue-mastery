<template>
  <div>
    <button v-on="$listeners" class="button" :class="buttonClass" v-bind="$attrs">
      <slot/>
    </button>
  </div>
</template>

<script>
  export default {
    inheritAttrs: false,
    props: {
      buttonClass: {
        type: String
      }
    }
  }
</script>

<style scoped>
.button {
  display: inline-flex;
  align-items: center;
  justify-content: space-between;
  height: 52px;
  padding: 0 40px;
  background: transparent;
  border: none;
  border-radius: 6px;
  text-align: center;
  font-weight: 600;
  white-space: nowrap;
  transition: all 0.2s linear;
  cursor: pointer;
}

.button:hover {
  -webkit-transform: scale(1.02);
  transform: scale(1.02);
  box-shadow: 0 7px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.button.-fill-gradient {
  background: linear-gradient(to right, #16c0b0, #84cf6a);
  color: #fff;
}
</style>