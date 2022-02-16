<script>
    import SectionCard from '../components/SectionCard.svelte'
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'

    let iconImages = [
        { src: 'images/icons/sticker-icons.png', alt: 'Sticker Icons'},
        { src: 'images/icons/design-icons.png', alt: 'Design Tools Icons'},
        { src: 'images/icons/location-types.png', alt: 'Location Types Icons'},
        { src: 'images/icons/1px-line-icons.png', alt: '1px Line Icons'},
        { src: 'images/icons/tools-icons.png', alt: 'Tool Icons'},
        { src: 'images/icons/accessibility-icons-grid.png', alt: 'Accessibility Icons'},
        { src: 'images/icons/music-icons.png', alt: 'Music Player Icons'},
        { src: 'images/icons/sharp-icons.png', alt: 'Small Sharp Icons'},
        { src: 'images/icons/dm-icon-set.png', alt: 'Sharp Thin Icons'},
        { src: 'images/icons/dm-icon-set-detail.png', alt: 'Detail of Sharp Thin Icons'},
        { src: 'images/icons/pinterest-style-icons.png', alt: 'Pinterest-style Icons'},
        { src: 'images/icons/playstation-icons.png', alt: 'Playstation Icon Exploration'},
        { src: 'images/icons/presentation-icons.png', alt: 'Personal Presentation Icons'},
        { src: 'images/icons/purple-icons.png', alt: 'Crocs-inspired Icons'}
    ]
</script>

<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >
    <SectionCard title="Icons" icon="image-filled">
        <p class="body-large">
            What can I say, I love a good set of constraints. 
        </p>
        <p style="margin-bottom: 1.5rem;">
            Icon design is a really fun challenge that combines illustration, conceptual thinking, and an “every detail counts” mentality that I really enjoy.
        </p>
        <div class="images">
            {#each iconImages as { src, alt}, i }
                <img class="works" {src} {alt} />
            {/each}
        </div>
        <p><a href="/">Return to homepage</a></p>
    </SectionCard>

</section>

<style>
    .images {
        display: flex;
        flex-direction: column;
        gap: .5rem;
        margin-bottom: 1.5rem;
    }
    img {
        width: 100%;
        display: block;
    }
</style>