<script lang="ts">
  import { onDestroy, onMount } from 'svelte'
  import { App } from './boundingCircle_app'
  let app: App
  onMount(() => {
    app = new App()
  })
  function stopAnimation() {
    cancelAnimationFrame(app.animationId)
  }
  function startAnimation() {
    app.animationId = requestAnimationFrame(app.animate.bind(app))
  }

  onDestroy(() => {
    stopAnimation()
  })
</script>

<div class="flex flex-col justify-center p-10">
  <div class="flex justify-center text-3xl p-2">Bounding Circle</div>
  <div id="container" class="w-full h-[60vh] bg-slate-800 rounded-sm" />
  <div class="flex justify-center p-2 gap-2">
    <button class="btn btn-outline btn-sm" on:click={stopAnimation}>stop animation</button>
    <button class="btn btn-outline btn-sm" on:click={startAnimation}>start animation</button>
  </div>
</div>
