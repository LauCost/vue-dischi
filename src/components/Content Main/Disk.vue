 <template>
  <div class="disco">
    <img :src="image" alt="" />
    <p>{{ titolo }}</p>
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