<script>
    // import ImageLoader from '../components/ImageLoader.svelte';
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
    import SectionCard from '../components/SectionCard.svelte'
    // import { src_url_equal } from 'svelte/internal';

    let iconImages = [
        { src: 'images/icons/site-icons-fill.png', alt: 'The filled version of my website icons'},
        { src: 'images/icons/site-icons-line.png', alt: 'The line version of my website icons'},
        { src: 'images/icons/site-icons-detail.png', alt: 'A detail view of one of the icons for my website'},
    ]
    let sdcImages = [
        { src: 'images/smiledirectclub/foundations.png', alt: 'Foundations Figma Library'},
        { src: 'images/smiledirectclub/web-components.png', alt: 'Web Components Figma Library'},
        { src: 'images/smiledirectclub/website-screens.png', alt: 'Website Screens Figma File'},
    ]
</script>

<section 
    in:fade="{{ duration: 500, delay: 250, easing: quadInOut}}"
    >
    
    <section class="intro">
        <h1>I'm Danny McClain, a multi-disciplinary designer currently focusing on design systems.</h1>
        <p class="body-large">I like to design methodically and put an emphasis on tidiness.</p>
        <p><a href="/info">Learn more about me</a></p>
    </section>

    <SectionCard title='Recent work' icon='clock-filled'>
        <p class="body-large">
            Modernizing the way SmileDirectClub designs and develops user interfaces.
        </p>
        <p style="margin-bottom: 1.5rem;">
            I led the design of SmileDirectClub's design system and website replatform—a massive, cross-organization effort to increase efficiency, bring harmony to a varied web presence, and delight customers while improving the designer and developer experience.
        </p>
        
        <div class="tab-panels-container">
            {#each sdcImages as { src, alt}, i }
            <div class="tab-panel">
                <div class="tab-panel-content">
                    <img class="works" {src} {alt} />
                </div>    
            </div>
            {/each}
        </div>
        <p>
            <a href="/smiledirectclub">View the case study</a>
        </p>
    </SectionCard>

    <SectionCard title="Icons" icon="image-filled">
        <p class="body-large">
            Outside of my product design work, I like to design icons and icon sets.
        </p>
        <p style="margin-bottom: 1.5rem;">
            My most recent icon set is the one for this very website—here they are all together, plus one or two extras.
        </p>
        <div class="tab-panels-container">
            {#each iconImages as { src, alt}, i }
            <div class="tab-panel">
                <div class="tab-panel-content">
                    <img class="works" {src} {alt} />
                </div>    
            </div>
            {/each}
        </div>
        <p>
            <a href="/icondesign">View more icon design</a>
        </p>
    </SectionCard>
 
    <SectionCard title="Utilities" icon="pencil-filled">
        <p class="body-large">
            I like to explore the technologies that bring design to life on the web. 
        </p>
        <p style="margin-bottom: 1.5rem;">
            Here are a few small projects I've built to satisfy my own curiosity and speed up my workflow.
        </p>
        <a class="utility-card" href="https://www.figma.com/community/plugin/917796239623005893/Fitter" target="_blank">
            Fitter
            <span class="body-small">
                A tiny Figma plugin that resizes an item to fit its parent's width, height, or both.
            </span>
        </a>
        <a class="utility-card" href="https://ratio.dannymccla.in" target="_blank">
            Ratio
            <span class="body-small">
                A quick, dead-simple proportion calculator made with Svelte.
            </span>
        </a>
        <a class="utility-card" href="https://gridfinder.dannymccla.in" target="_blank">
            Grid Finder
            <span class="body-small">
                A tool to help you calculate perfect grids with whole values. (Plugin version in development.)
            </span>
        </a>
    </SectionCard>
</section>

<style>

    .intro {
            padding: 1.25rem;
            margin-bottom: 1rem;
    }

    @media screen and (min-width: 769px) {
        .intro {
            padding: 2rem;
            margin-bottom: 1.25rem;
        }
    }

    h1 {
        font-style: normal;
        font-weight: 900;
        font-size: 2rem;
        line-height: 2.5rem;
        letter-spacing: -0.02em;
        margin-bottom: 1rem;
    }

    p:not(:last-child) {
        margin-bottom: 1rem;
    }

    .tab-panels-container {
		scroll-snap-type: x mandatory;
		-webkit-overflow-scrolling: touch;
		overflow-x: scroll;
		display: flex;
        gap: .5rem;
        margin-bottom: 1rem;
	}
	
	.tab-panel {
        scroll-snap-align: start;
        scroll-snap-stop: always;
		width: 90%;
		flex: 1 0 auto;
		height: auto;
		display: flex;
    }

    .tab-panel-content {
        display: flex;
    }

    .works {
        width: 100%;
        height: auto; 
        /* border-radius: 8px; */
        margin: 0;
        padding: 0;
    }

    .utility-card {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        padding: 1rem;
        border: 2px solid var(--accent-12);
        border-radius: 8px;
        margin-top: 1rem;
        text-decoration: none;
        font-weight: 700;
        transition: background-color 125ms linear, border-color 125ms linear, color 125ms linear;
    }

    .utility-card span {
        font-weight: 500;
    }

    .utility-card:hover {
        background-color: var(--accent);
        border-color: var(--accent);
    }
    
    .utility-card:not(:last-child) {
        margin-bottom: 1rem;
    }
</style>