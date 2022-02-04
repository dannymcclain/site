<script>
    import Button from '../components/Button.svelte'
    import { fly } from 'svelte/transition'
    import { backInOut } from 'svelte/easing'
</script>

<section 
    in:fly="{{y: 40, delay: 400, duration: 400, easing: backInOut}}"
    out:fly="{{y: 20, duration: 200, easing: backInOut}}"
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
        letter-spacing: -0.04em;
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