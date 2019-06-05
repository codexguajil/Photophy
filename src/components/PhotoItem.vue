<template>
  <div class="photo-item" >
    <img v-bind:src="photo.urls.small" class="picture"/>
    <p class="desc">{{photo.alt_description}}</p>
    <button class="btn tag">tags</button>
  </div>
</template>

<script>
export default {
  name: "PhotoItem",
  props: ["photo"],
  methods: {
   
  }
}
</script>

<style scoped>
  .desc {
    padding: 10px;
  }

  .photo-item {
    background: rgba(109, 108, 108, 0.692);
    border-radius: 3px;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,.4);
    color: #FFF;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    margin: 15px 15px 35px 0px;
    padding-bottom: 20px;
    z-index: 0;
  }

  .photo-item:hover {
    box-shadow: 1px 1px 5px 1px grey;
    z-index: 1;
  }

  .picture {
    background: rgb(14, 13, 13);
    object-fit: scale-down;
    margin-bottom: 20px;
    width: 100%;
    height: 250px;
    position: relative;
    transition: all .4s ease-in-out;
  }

  .picture:hover {
    transform: scale(1.04);
    transition: transform .4s ease-in-out;
    z-index: 1;
  }

  .tag {
    display: inline-block;
    border: none;
    background: #1CB76F;
    color: #fff;
    margin: 0 5px;
    padding: 7px;
    width: 40px;
    cursor: pointer;
  }

</style>
