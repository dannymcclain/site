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

<img {src} {alt} class:loaded bind:this={thisImage} loading="lazy" />

<style>
    img {
      opacity: 0;
      transition: opacity 1000ms ease-out;
      width: 100%;
      height: auto;
    }
    img.loaded {
      opacity: 1;
    }
  </style>