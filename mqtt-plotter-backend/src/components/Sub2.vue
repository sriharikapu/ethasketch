<template>
  <div class="sub" v-html="buff">
  </div>
</template>

<script>
export default {
  data () {
    return {
      buff: 'Sub1:<br>'
    }
  },
  mqtt: {
    /** 'VueMqtt/publish2' or '+/publish2' */
    '/move' (data) {
      this.buff = this.buff + data + '<br>'
    }
  }
}
</script>
