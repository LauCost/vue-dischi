 <template>
  <div class="disco">
    <div class="cover">
      <img :src="image" alt="" />
    </div>
    <h2>{{ titolo }}</h2>
  </div>
</template>


<script>
export default {
  props: {
    image: String,
    titolo: String,
  },
};
</script> 


<style lang="scss">
.disco {
  width: 15%;
  background-color: #2e3a46;
  margin: 15px;

  h2 {
    color: #fff;
    text-align: center;
    width: 60%;
    margin: auto;
  }
}

.cover {
  width: 80%;
  margin: 20px auto;
  img {
    width: 100%;
  }
}
</style>