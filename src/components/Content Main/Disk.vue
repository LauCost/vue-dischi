 <template>
  <div class="disco">
    <div class="cover">
      <img :src="image" alt="" />
    </div>
    <h2>{{ titolo }}</h2>
    <p>
      {{ autore }} <br />
      {{ anno }}
    </p>
  </div>
</template>


<script>
export default {
  props: {
    image: String,
    titolo: String,
    autore: String,
    anno: String,
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

  p {
    width: 80%;
    margin: 25px auto;
    color: #808080;
    text-align: center;
    font-size: 25px;
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