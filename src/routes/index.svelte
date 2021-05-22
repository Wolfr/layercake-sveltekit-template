<script>
  import { LayerCake, Svg, Html, Canvas } from 'layercake';

  import AxisX from '$lib/components/AxisX.svelte';
  import AxisY from '$lib/components/AxisY.svelte';
  import Line from '$lib/components/Line.svelte';

  const data = [{ x: 0, y: 1 }, { x: 1, y: 2 }];
</script>

<style>
  /* Set dimensions on the parent.
     The <LayerCake> component will expand to fill it.
   */
  .chart-container {
    width: 100%;
    height: 500px;
    font-family: sans-serif;
  }
</style>

<div class="chart-container">
  <LayerCake
    x='x'
    y='y'
    {data}
  >
  <AxisX />
    <Svg>
      <AxisX/>
      <AxisY/>
      <Line color='#f0c'/>
    </Svg>
  </LayerCake>
</div>
