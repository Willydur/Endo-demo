<script>
  import Graph from "../components/graph.svelte";
  import SliderCat from "../components/sliderCat.svelte";
  import Qui from "../components/qui.svelte";
</script>

<div class="mother">
  <section>
    <Qui />
  </section>
  <section>
    <Graph />
  </section>
  <section>
    <SliderCat />
  </section>
</div>

<style>
  .mother {
    display: flex;
    flex-wrap: nowrap;
    flex-direction: column;
  }
</style>
