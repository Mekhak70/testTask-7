<template>
  <div class="Button" :style="styleObject">
    <span>{{ text }}</span>
  </div>
</template>
    
<script>
export default {
  
    props: {
    text: String,
    verticalPadding: {
      type: String,
      default: '16px', 
    },
    horizontalPadding: {
      type: String,
      default: '90px', 
    },
    fontSize: {
      type: String,
      default: '19px', 
    },
  },
    computed: {
    styleObject() {
      return {
        '--vertical-padding': this.verticalPadding,
        '--horizontal-padding': this.horizontalPadding,
        '--font-size': this.fontSize,
      };
    },
  },
}
</script>
    
<style scoped>
.Button {
  cursor: pointer;
  display: flex;
  width: max-content;
  justify-content: center;
  align-items: center;
  padding: var(--vertical-padding) var(--horizontal-padding);
  border-radius: 12px;
  background: linear-gradient(96deg, rgba(251, 21, 96, 0.80) 0%, #4A1690 87%);
  box-shadow: 0px 0px 35px 0px rgba(0, 0, 0, 0.20);
}

.Button span {
  color: #FFF;
  text-align: center;
  font-feature-settings: 'clig' off, 'liga' off;
  font-family: 'Golos', sans-serif;
  font-size: var(--font-size);
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
</style>