<template>
  <div>
    <div class="login-form">
      <div class="g-form">
        <div class="g-form-line" v-for="formLine in formData">
          <span class="g-form-label">{{ formLine.label }}：</span>
          <div class="g-form-input">
            <input type="text"
                   v-model="formLine.model" placeholder="">
          </div>
        </div>
        <div class="g-form-line">
          <div class="g-form-btn">
            <a class="button">注册</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      'isShow': 'boolean'
    },
    data () {
      return {
        formData:[
          {
            label:'用户名',
          },
          {
            label:'密  码',
          }
        ]
      }
    },

    methods: {
      closeMyself () {
        this.$emit('on-close')
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
