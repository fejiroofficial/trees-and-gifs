<template>
  <div class="nav">
    <div class="burger-menu" type="primary" @click="showDrawer">
      <div class="burger-menu__line"></div>
      <div class="burger-menu__line burger-menu__line_mid"></div>
      <div class="burger-menu__line"></div>
    </div>
    <a-drawer
      placement="right"
      :closable="false"
      :visible="visible"
      @close="onClose"
    >
      <div>
        <router-link to="/">Trees</router-link>
      </div>
      <a-divider type="vertical" />
      <div>
        <router-link to="/gifs">Gifs</router-link>
      </div>
    </a-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false,
    };
  },
  methods: {
    showDrawer() {
      this.visible = true;
    },
    onClose() {
      this.visible = false;
    },
  },
};
</script>

<style lang="scss" scoped>
.burger-menu {
  cursor: pointer;
  width: fit-content;
  position: absolute;
  top: 2%;
  left: 2%;
  &__line {
    width: 30px;
    height: 1px;
    background-color: black;
    margin: 6px 0;
    &_mid {
      width: 23px;
    }
  }
}
</style>
