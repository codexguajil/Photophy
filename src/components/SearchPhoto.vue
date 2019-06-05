<template>
  <div class="submit-form">
    <form @submit="searchPhoto">
      <input type="text" v-model="title" name="title" placeholder="Type a search category...">
      <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
export default {
  name: "searchPhoto",
  data() {
    return {
      title: ''
    }
  },
  methods: {
    searchPhoto(e) {
      e.preventDefault()
      const newPhoto = {
        title: this.title
      }
      
      this.$emit('search-photo', newPhoto);

      this.title = '';
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
  }

  input[type="text"] {
    background: hsla(0,0%,100%);
    border: 1px solid transparent;
    border-radius: 3px;
    padding: 8px 35px 8px 10px;
    outline: 0 none;
    font-size: 16px;
    font-weight: 700;
    letter-spacing: .4px;
    -webkit-text-fill-color: inherit;
  }

  input[type="submit"] {
    flex: 2;
  }

  input[type="submit"]:hover {
    opacity: .9;
  }

  .submit-form {
    margin-top: 8px;
    padding: 20px;
  }
</style>
