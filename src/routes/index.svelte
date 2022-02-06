<script>
    import Button from '../components/Button.svelte'
    import ImageLoader from '../components/ImageLoader.svelte';
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
</script>

<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >
    
    <section class="intro">
        <h1>I'm a multidisciplinary designer currently focusing on design systems & icon sets.</h1>
        
        <p>I like to design systematically and put an emphasis on tidiness.</p>
        
        <Button style='normal' name='about' url='/info' label='Learn more about me'></Button>
    </section>

    <section class="grid">
        <ImageLoader src='images/colorful-icons.png' alt='Colorful Icons'/>
        <ImageLoader src='images/design-icons.png' alt='Design Icons'/>
        <ImageLoader src='images/dm-icon-set.png' alt='Personal Icon Set'/>
    </section>


</section>

<style>
    h1 {
        font-style: normal;
        font-weight: 900;
        font-size: 2rem;
        line-height: 2.5rem;
        text-align: center;
        letter-spacing: -0.02em;
        margin-bottom: 1rem;
    }

    p {
        margin-bottom: 2rem;
        font-style: normal;
        font-weight: 500;
        font-size: 1.25rem;
        line-height: 2rem;
    }

    .intro {
        margin-bottom: 4rem;
    }

    .grid {
        display: grid;
        grid-template-columns: 1fr;
        grid-gap: 1.25rem;
    }

    @media screen and (min-width:768px) {
        .grid {
            grid-template-columns: 1fr 1fr;
        }
    }
</style>