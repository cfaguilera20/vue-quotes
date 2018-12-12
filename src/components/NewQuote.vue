<template>
  <div class="row">
    <form class="col-sm-12">
      <div class="row">
        <div class="col-sm-8 offset-sm-2 col-xs-12 col-md-6 offset-md-3 form-group">
          <label for>Quote</label>
          <textarea class="form-control" rows="3" v-model="quote"></textarea>
        </div>
        <div class="col-sm-8 offset-sm-2 col-xs-12 col-md-6 offset-md-3 form-group">
          <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
        </div>
      </div>
    </form>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  }
};
</script>
<style scoped>
</style>
