<script>
    export let alt
    export let src
    import IntersectionObserver from './IntersectionObserver.svelte'
    import Image from './Image.svelte'
    import { fade } from 'svelte/transition'
</script>

<IntersectionObserver bottom={100} once={true} let:intersecting={intersecting}>
    {#if intersecting}
        <Image {alt} {src} />
    {/if}
</IntersectionObserver>