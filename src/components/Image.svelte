<script>
    export let src = ''
    export let alt = ''

    import { onMount } from 'svelte'

    let loaded = false
    let thisImage

    onMount(() => {
        thisImage.onload = () => {
            loaded = true
            console.log('Loaded image!')
        }
    })
</script>

<div class="img-wrap">
  <img {src} {alt} class:loaded bind:this={thisImage} loading="lazy" />
</div>

<style>
    .img-wrap {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100%;
    }
    img {
      opacity: 0;
      transition: opacity 125ms linear;
      width: 100%;
      height: auto;
    }
    img.loaded {
      opacity: 1;
    }
  </style>