<script>
  export default {
    data: () => ({ bar: 1 }),
    computed: {
      foo: function () {
        this.$set(this, 'bar', 1);
        this.$nextTick(() => this.$set(this, 'bar', 2));
        return 1;
      }
    }
  };
</script>
