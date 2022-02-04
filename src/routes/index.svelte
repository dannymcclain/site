<script>
    import Button from '../components/Button.svelte'
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
</script>

<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >
    
    <h1>I'm a multidisciplinary designer currently focusing on design systems & icon sets.</h1>
    
    <p>I like to design systematically and put an emphasis on tidiness.</p>
    
    <Button name='about' url='/info' label='Learn more about me'></Button>
</section>

<style>
    h1 {
        font-style: normal;
        font-weight: 800;
        font-size: 2rem;
        line-height: 3rem;
        letter-spacing: -0.02em;
        margin-bottom: 1.25rem;
    }

    p {
        font-style: normal;
        font-weight: normal;
        font-size: 1.25rem;
        line-height: 2rem;
        letter-spacing: -0.02em;
        margin-bottom: 2.5rem;
    }
</style>