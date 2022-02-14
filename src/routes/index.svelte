<script>
    import ImageLoader from '../components/ImageLoader.svelte';
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
    import SectionCard from '../components/SectionCard.svelte'
    import { src_url_equal } from 'svelte/internal';

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
    let designSystemImages = [
        { src: 'images/design-systems/structure.png', alt: 'Design System Structure'},
        { src: 'images/design-systems/foundations.png', alt: 'Foundations Figma Library'},
        { src: 'images/design-systems/web-components.png', alt: 'Web Components Figma Library'},
        { src: 'images/design-systems/website-screens.png', alt: 'Website Screens Figma File'},
    ]
</script>

<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >
    
    <section class="intro">
        <h1>I'm Danny McClain, a multidisciplinary designer currently focusing on design systems.</h1>
        <p class="body-large">I like to design methodically and put an emphasis on tidiness.</p>
        <p><a href="/info">Learn more about me</a></p>
    </section>

    <SectionCard title='Recent work' icon='clock-filled'>
        <p class="body-large">
            Most recently I led the design of SmileDirectClub's design system and website replatform.
        </p>
        <p>
            I honed the visual design, defined interaction patterns, created organization-wide Figma libraries for foundational styles and complex components, and created best practices, usage guidelines, and how-to videos to give other designers the awesome power of designing systematically.
        </p>
        <p>
            I worked closely with my developer counterpart throughout the process, and together we made sure that styles and components represented in Figma were also represented in our front end UI library.
        </p>
        <p style="margin-bottom: 1.5rem;">
            While this work is in the process of being implemented, our efforts have already increased design and development efficiency, created a consistent visual language for SmileDirectClub's web presence, greatly improved the user experience of their website, and enabled fast, consistent scaling of design as SmileDirectClub grows.
        </p>
        <div class="tab-panels-container" style="margin-bottom: 1.5rem;">
            {#each designSystemImages as { src, alt}, i }
            <div class="tab-panel">
                <div class="tab-panel-content">
                    <img class="works" {src} {alt} />
                </div>    
            </div>
            {/each}
        </div>
        <p>
            I'm happy to walkthrough my work upon request. <a href="mailto:dannymcclainstudio@gmail.com">Email me</a> to schedule a chat.
        </p>
        <p>
            SmileDirectClub's design system was my most recent focus, but during my tenure at SDC, I was also the design and UX lead for many high-impact, customer-facing initiatives. A few notable projects I worked on:
        </p>
        <ul class="projects">
            <li>
                The first iteration of the SmileDirectClub iOS app* (including research, user flows, testing, and visual design)
            </li>
            <li>
                The web interface for SmileDirectClub's partner network, which allows dentists and orthodontist to prescribe SDC's clear aligner treatment to their patients
            </li>
            <li>
                A complete overhaul of user flows and visual design for getting started with SmileDirectClub (finding a location and booking a visit or ordering an at-home kit)
            </li>
        </ul>
        <p>
            While it's impossible to articulate my every contribution, as the second member of the UX team (under the fabulously talented <a href="https://www.linkedin.com/in/bryan-kemp-a1472224/">Bryan Kemp</a>) I played a key role in shaping the growth and culture of the team and had a huge impact on setting quality standards for UX design at SmileDirectClub. 
        </p>
        <aside class="body-small">
            *As I transitioned into a more DesignOps/design systems-focused role for SDC's replatform, <a href="https://www.linkedin.com/in/chelseaguerrera/">Chelsea Guerrera</a> took over leading design for the iOS app and did a fantastic job seeing the project through to launch and beyond.
        </aside>
    </SectionCard>

    <SectionCard title="Icons" icon="image-filled">
        <p style="margin-bottom: 1.5rem;">
            Outside of my product design work, I like to design icons and icon sets. What can I say, I love a good set of constraints. Icon design is a really fun challenge that combines illustration, conceptual thinking, and an “every detail counts” mentality that I really enjoy.
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
    </SectionCard>
 
    <SectionCard title="Utilities" icon="pencil-filled">
        <p style="margin-bottom: 1.5rem;">
            As someone primarily designing for the web, I like to explore the technologies that bring my designs to life. Here are a few small projects I've built to satisfy my own curiosity and speed up my workflow. Always more in the works.
        </p>
        <a class="utility-card" href="https://www.figma.com/community/plugin/917796239623005893/Fitter" target="_blank">
            Fitter
            <span class="body-small">
                A tiny Figma plugin that resizes an item to fit its parent's width, height, or both.
            </span>
        </a>
        <a class="utility-card" href="https://ratio.dannymcclain.com/" target="_blank">
            Ratio
            <span class="body-small">
                A quick, dead-simple proportion calculator made with Svelte.
            </span>
        </a>
        <a class="utility-card" href="https://gridfinder.dannymcclain.com/" target="_blank">
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
        margin-right: 0.5rem;
    }

    .works {
        width: 100%;
        height: auto; 
        border-radius: 8px;
        margin: 0;
        padding: 0;
    }

    aside {
        padding: .75rem 1rem;
        background-color: var(--accent-8);
        border-radius: 8px;
        /* margin-bottom: 1rem; */
    }

    .projects {
        list-style: none;
    }

    .projects li {
        margin: 0 0 .5rem 1rem;
    }

    .projects li:last-child {
        margin-bottom: 1.5rem;
    }

    .projects li:before {
        content: "\2022";
        color: var(--accent-12);
        /* font-weight: bold; */
        display: inline-block;
        width: 1rem;
        margin-left: -1rem;
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