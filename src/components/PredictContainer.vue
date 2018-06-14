<script>
  export default {
    props: ['value'],
    render() {
      return this.$scopedSlots.default({
        items: this.value
      })
    },
    mounted() {}
  }
</script>
