<script>
    import Button from '../components/Button.svelte'
    import ImageLoader from '../components/ImageLoader.svelte';
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
import { src_url_equal } from 'svelte/internal';

    let images = [
        { src: 'images/1px-line-icons.png', alt: '1px Line Icons'},
        { src: 'images/building-icons.png', alt: 'Building and Tools Icons'},
        { src: 'images/accessibility-icons-grid.png', alt: 'Accessibility Icons'},
        { src: 'images/colorful-icons.png', alt: 'Colorful Icons'},
        { src: 'images/design-icons.png', alt: 'Design Tools Icons'},
        { src: 'images/dm-icon-set.png', alt: 'Sharp Thin Icons'},
        { src: 'images/grid-finder.png', alt: 'Grid Finder UI'},
        { src: 'images/happy-avatar-icon.png', alt: 'Happy Avatar Icon'},
        { src: 'images/inbox-replacement-icon.png', alt: 'Inbox Replacement Icon'},
        { src: 'images/little-figma-icon.png', alt: 'Little Figma Fanart Icon'},
        { src: 'images/music-icons.png', alt: 'Music Player Icons'},
        { src: 'images/pinterest-style-icons.png', alt: 'Pinterest-style Icons'},
        { src: 'images/playstation-icons.png', alt: 'Playstation Icon Exploration'},
        { src: 'images/presentation-icons.png', alt: 'Personal Presentation Icons'},
        { src: 'images/purple-icons.png', alt: 'Crocs-inspired Icons'},
        { src: 'images/ratio-app.png', alt: 'Ratio App UI'},
        { src: 'images/sharp-icons.png', alt: 'Small Sharp Icons'},
        { src: 'images/ratio.png', alt: 'Ratio Web UI'},
        { src: 'images/sticker-icons.png', alt: 'Sticker Icons'},
        { src: 'images/tools-icons.png', alt: 'Tool Icons'},
        { src: 'images/typora-replacement-icon.png', alt: 'Typora Replacement Icon'}
    ]
</script>

<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >
    
    <section class="intro">
        <img src="portrait.png" alt="A portriat of me by Cymone Wilder" />
        <h1>I'm a multidisciplinary designer currently focusing on design systems and icon sets.</h1>
        
        <p>I like to design systematically and put an emphasis on tidiness.</p>
        
        <Button style='normal' name='about' url='/info' label='Learn more about me'></Button>
    </section>

    <section class="grid">
        <!-- <ImageLoader src='images/design-icons.png' alt='Design Icons'/>
        <ImageLoader src='images/colorful-icons.png' alt='Colorful Icons'/>
        <ImageLoader src='images/dm-icon-set.png' alt='Personal Icon Set'/> -->
        {#each images as { src, alt}, i }
            <ImageLoader {src} {alt} />
        {/each}
    </section>


</section>

<style>
    img {
        width: 136px;
        height: 136px;
        margin-bottom: 2rem;
    }
    h1 {
        font-style: normal;
        font-weight: 900;
        font-size: 2rem;
        line-height: 2.5rem;
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

    @media screen and (min-width:769px) {
        .grid {
            grid-template-columns: 1fr 1fr;
        }
    }
    @media screen and (min-width: 1025px){
        .grid {
            grid-template-columns: 1fr 1fr 1fr;
        }    
    }
</style>