<script>
    import Button from '../components/Button.svelte'
    import SectionCard from '../components/SectionCard.svelte'
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
</script>


<section 
    in:fade="{{ duration: 500, delay: 250, easing: quadInOut}}"
    >
    <SectionCard title="About me" icon="person-heading">
        <figure><img src="portrait.png" alt="A portriat of me by Cymone Wilder" /></figure>
        <p class="body-large">
            I'm Danny McClain, a husband and father of two who enjoys homesteading with my family in Middle Tennessee.
        </p>
        <p>
            I love riding bicycles and goofing around outside. I'm just as likely to be found listening to <a href="https://darkdescentrecords.bandcamp.com/album/hidden-history-of-the-human-race" target="_blank">Blood Incantation</a> as I am <a href="https://acemo.bandcamp.com/album/i-want-to-believe" target="_blank">AceMo</a>.
        </p>
    </SectionCard>
   <SectionCard title="Find me out there" icon="search-heading">
    <ul>
        <li>
            <Button style='grid' name='email' url='mailto:dannymcclainstudio@gmail.com' label='Email'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='figma' url='https://www.figma.com/@dannymcclain' label='Figma'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='instagram' url='http://instagram.com/dannymcclain/' label='Instagram'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='twitter' url='http://twitter.com/dannymcclain/' label='Twitter'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='github' url='http://github.com/dannymcclain/' label='Github'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='dribbble' url='http://dribbble.com/dannymcclain' label='Dribbble'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='linkedin' url='https://www.linkedin.com/in/dannymcclain/' label='Linkedin'></Button>
        </li>
        <li>
            <Button newTab={true} style='grid' name='readcv' url='http://read.cv/danny' label='Read.cv'></Button>
        </li>
    </ul>
   </SectionCard>
   <SectionCard title="Extended reading" icon="book-heading">
       <p class="body-large">
        I've been designing interfaces (websites, apps, diGiTaL eXpEriEnCeS, and more!) for over a decade.
       </p>
       <p>
        I believe design is a craft, and I super care about every little detail. But I'm also experienced enough to know when and where to compromise.
       </p>
       <p>I've always gravitated towards the blurry area where design meets code. That's where I have the most fun, so I'm just as happy mocking something up with HTML, CSS, and JavaScript* as I am perfecting pixels, defining constraints, and creating variants in Figma.</p>
       <aside class="body-small">*I have experience with React and Vue, but lately I've been having tons of fun with Svelte.</aside>
       <p>
        Because of my penchant for neatness, I really fell in love working on design systems. I enjoy and obsess over the finer points of visual design, component architecture, and maintaining high standards throughout.
       </p>
       <p>
        But the thing that I really love about design systems is the impact my work can have for other designers and developers. For me, it's thrilling when my work makes someone else's work easier, faster, or better. And when your teammates are your “customers,” you get the magical gift of seeing your efforts turn to value directly. Getting to hear from someone I see everyday how much better their life is (in whatever small way) because of my work is fulfilling in a way that's more profound to me than shipping a top-tier experience to customers at large. But don't get me wrong, that's great (and imperative) too!
       </p>
   </SectionCard>

   <SectionCard title="Parting thoughts" icon="heart-heading">
       <p class="body-large">
        The web is a wild place, and I strive for my impact to make it a more honest, more accessible, and more enjoyable place to be.
       </p>
       <p>
        If you're looking for a detail-oriented designer to bridge the gap between design and code and keep files, styles, and processes tidy, <a href="mailto:dannymcclainstudio@gmail.com">email me</a>.
       </p>
   </SectionCard>
   <SectionCard title="Colophon" icon="pencil-filled">
       <p>This site is set in <a href="https://www.fontshare.com/fonts/satoshi" target="_blank">Satoshi</a>, or if something's gone wrong, your OS's system font. It was built using <a href="https://kit.svelte.dev" target="_blank">Sveltekit</a> and deployed/hosted with <a href="https://vercel.com/" target="_blank">Vercel</a> and <a href="https://github.com/dannymcclain/site" target="_blank">GitHub</a>.</p>
   </SectionCard> 

</section>

<style>
    p:not(:last-child) {
        margin-bottom: 1rem;
    }
  
    ul {
        list-style: none;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 1rem;
    }

    ul li {
        width: 100%;
    }

    aside {
        padding: .75rem 1rem;
        background-color: var(--accent-8);
        border-radius: 8px;
        margin-bottom: 1rem;
    }
   
    figure {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    img {
        width: 136px;
        height: 136px;
        margin-bottom: 1rem;
    }
</style>