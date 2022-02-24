<script>
    import SectionCard from '../components/SectionCard.svelte'
    import Button from '../components/Button.svelte'
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'

    let sdcImages = [
        { src: 'images/smiledirectclub/foundations.png', alt: 'A snippet from our foundations Figma library that defines universal styles and guidelines across platforms and applications'},
        { src: 'images/smiledirectclub/storybook.png', alt: 'A screenshot of our UI component library in Storybook'},
        { src: 'images/smiledirectclub/web-components.png', alt: 'A small piece of our web components Figma library, which utilizes our foundations to create robust, web-specific patterns and components'},
        { src: 'images/smiledirectclub/website-screens.png', alt: 'A screen from the website Figma file that assembles customized web components and sections into page layouts to accomplish business and user goals'},
        { src: 'images/smiledirectclub/other-projects.png', alt: 'A few of the other projects I worked on: navigation, getting started, and booking a visit'},
        { src: 'images/smiledirectclub/partner-portal.png', alt: "A small selection of screens I designed for SmileDirectClub's partner network"},
    ]

    let quotes = [
        "“I LOVE the components, it makes everything so much easier”",
        "“I really can't thank you enough for setting all of these up! It has been SO NICE to work with these!!”",
        "“The design system is DOPE!!!!!”",
        "“Team member shoutout today goes to Danny McClain once again for making our lives easier”"

    ]
</script>

<section 
    in:fade="{{ duration: 500, delay: 250, easing: quadInOut}}"
    >
    <SectionCard title="SmileDirectClub" icon="smile-filled">
        <p class="body-large">Creating a design system from the ground up during a major replatform was no easy task, but it was one that I was happy to lead.</p>
          
        <aside class="body-small">
            I'll gladly walk through my work upon request. <a href='mailto:dannymcclainstudio@gmail.com'>Email me</a> to schedule a chat.
        </aside>
        <p>
            SmileDirectClub's website architecture was outdated and a huge hinderance to designers, developers, and project owners across the company. Due to a variety of limitations, the divide between design handoff and implementation left something to be desired.
        </p>

        <p>
            We needed to modernize our approach to design and create cross-team alignment on how design and development should happen at SmileDirectClub. Under the leadership of the Director of Product Design, I spearheaded the design of a comprehensive design system. 
        </p>

        <p style="margin-bottom: 1.5rem">
            I honed the visual design, defined interaction patterns, created organization-wide Figma libraries for foundational styles and complex components, and created best practices, usage guidelines, and how-to videos to give other designers the awesome power of designing systematically.
        </p>

        <figure>
            <img src={sdcImages[0].src} alt={sdcImages[0].alt} />
            <figcaption class="body-small">
                {sdcImages[0].alt}
            </figcaption>
        </figure>

        <p style="margin-bottom: 1.5rem">
            I worked closely with my developer counterpart throughout the process, and together we made sure that styles and components represented in Figma were also represented in our front end UI library.
        </p>

        <figure>
            <img src={sdcImages[1].src} alt={sdcImages[1].alt} />
            <figcaption class="body-small">
                {sdcImages[1].alt}
            </figcaption>
        </figure>

        <p style="margin-bottom: 1.5rem">
            While this work is in the process of being implemented, our efforts have already increased design and development efficiency, created a consistent visual language for SmileDirectClub's web presence, greatly improved the user experience of their website, and enabled fast, consistent scaling of design as SmileDirectClub grows.
        </p>

        <figure>
            <img src={sdcImages[2].src} alt={sdcImages[2].alt} />
            <figcaption class="body-small">
                {sdcImages[2].alt}
            </figcaption>
        </figure>

        <figure>
            <img src={sdcImages[3].src} alt={sdcImages[3].alt} />
            <figcaption class="body-small">
                {sdcImages[3].alt}
            </figcaption>
        </figure>
        
        <figure>
            <img src={sdcImages[4].src} alt={sdcImages[4].alt} />
            <figcaption class="body-small">
                {sdcImages[4].alt}
            </figcaption>
        </figure>

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

       <aside class="body-small">
            *As I transitioned into a more DesignOps/design systems-focused role for SDC's replatform, <a href="https://www.linkedin.com/in/chelseaguerrera/">Chelsea Guerrera</a> took over leading design for the iOS app and did a fantastic job seeing the project through to launch and beyond.
        </aside>

        <figure>
            <img src={sdcImages[5].src} alt={sdcImages[5].alt} />
            <figcaption class="body-small">
                {sdcImages[5].alt}
            </figcaption>
        </figure>

       <p style="margin-bottom: 1.5rem">
            While it's impossible to articulate my every contribution, as the second member of our team (under the fabulously talented <a href="https://www.linkedin.com/in/bryan-kemp-a1472224/">Bryan Kemp</a>) I played a key role in shaping the growth and culture of the team and had a huge impact on setting quality standards for UX design at SmileDirectClub.
       </p>
       
       <figure class="quote-gallery">
        <div class="tab-panels-container" style="margin-bottom: 0">
            {#each quotes as quote}
                <div class="tab-panel">
                    <div class="tab-panel-content">
                        <div class="quote">
                            <h4>{quote}</h4>
                        </div>
                    </div>
                </div>
            {/each}        
        </div>
        <figcaption class="body-small">
            Actual quotes from my teammates regarding my design systems work
        </figcaption>
    </figure>

       <p>
        <a href="mailto:dannymcclainstudio@gmail.com">Email me</a> if you're looking for a detail-oriented designer to bridge the gap between design and code and keep files, styles, and processes tidy.
       </p>
    </SectionCard>
</section>

<style>
    p:not(:last-child) {
        margin-bottom: 1rem;
    }

    figure {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        margin-bottom: 1.5rem;
    }

    figure img {
        width: 100%;
        height: auto;
    }

    aside {
        padding: .75rem 1rem;
        background-color: var(--accent-8);
        border-radius: 8px;
        margin-bottom: 1.5rem;
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
        width: 100%;
    }

    .quote {
        background: var(--accent);
        padding: 1.25rem;
        width: 100%;
    }

    @media screen and (min-width: 769px){
        .quote {
            padding: 2rem;
        }
    }

    h4 {
        font-weight: 900;
        font-size: 1.25rem;
        line-height: 1.75rem;
        color: #FFFFFF;
    }
</style>