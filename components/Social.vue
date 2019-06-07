<template>
  <div class="social">
    <a href class="social__link">
      <ok-icon/>
    </a>
    <a href class="social__link">
      <vk-icon/>
    </a>
    <a href class="social__link">
      <fb-icon/>
    </a>
  </div>
</template>

<script>
import FbIcon from './icons/FbIcon'
import VkIcon from './icons/VkIcon'
import OkIcon from './icons/OkIcon'
export default {
    name: 'Social',
    components: {
        FbIcon,
        VkIcon,
        OkIcon
    }
}
</script>

<style lang="scss">
.social {
  // padding-left: 20px;
  // padding-right: 20px;

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  // align-items: center;
  height: 80px;
}
</style>
