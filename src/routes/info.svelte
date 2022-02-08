<script>
    import Button from '../components/Button.svelte'
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
</script>


<div 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >

    <section>
        <h2>
            <div class="svg-wrap">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <use href="icons.svg#person-heading"></use>
                </svg>
            </div>
            About me
        </h2>
        
        <p class="body-large">
            I'm Danny McClain, a husband and father of two who enjoys homesteading with my family in Middle Tennessee.
        </p>
        <p>
            I love riding bicycles and goofing around outside. I'm just as likely to be found listening to <a href="https://darkdescentrecords.bandcamp.com/album/hidden-history-of-the-human-race" target="_blank">Blood Incantation</a> as I am <a href="https://acemo.bandcamp.com/album/i-want-to-believe" target="_blank">AceMo</a>.
        </p>
    </section>

    <section>
        <h2>
            <div class="svg-wrap">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <use href="icons.svg#search-heading"></use>
                </svg>
            </div>
            Find me out there
        </h2>
        <ul>
            <li><Button style='grid' name='email' url='mailto:dannymcclainstudio@gmail.com' label='Email'></Button></li>
            <li><Button style='grid' name='figma' url='https://www.figma.com/@dannymcclain' label='Figma'></Button></li>
            <li><Button style='grid' name='instagram' url='http://instagram.com/dannymcclain/' label='Instagram'></Button></li>
            <li><Button style='grid' name='twitter' url='http://twitter.com/dannymcclain/' label='Twitter'></Button></li>
            <li><Button style='grid' name='github' url='http://github.com/dannymcclain/' label='Github'></Button></li>
            <li><Button style='grid' name='dribbble' url='http://dribbble.com/dannymcclain' label='Dribbble'></Button></li>
            <li><Button style='grid' name='linkedin' url='https://www.linkedin.com/in/dannymcclain/' label='Linkedin'></Button></li>
            <li><Button style='grid' name='readcv' url='http://read.cv/danny' label='Read.cv'></Button></li>
        </ul>
    </section>

    <section class="extended-reading">
        <h2>
            <div class="svg-wrap">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <use href="icons.svg#book-heading"></use>
                </svg>
            </div>
            Extended reading
        </h2>
    
        <p>
            I've been designing interfaces (websites, apps, diGiTaL eXpEriEnCeS, etc.) for over a decade. I believe design is a craft, and I super care about every little detail (but I'm also experienced enough to know when to compromise). I've always gravitated towards, and had the most fun in, the blurry area where design meets code—so I'm just as happy mocking something up with HTML/CSS/JS as I am defining constraints and creating variants in Figma.
        </p>

        <p>
            Because of my penchant for neatness, I really fell in love working on design systems. While I enjoy—and obsess over—the finer points of visual design, component architecture and organization, and maintaining high standards throughout, the thing that I really love about design systems is the impact my work can have for other designers and developers. For me, it's thrilling when <em>my</em> work makes <em>someone else's</em> work easier, faster, or better. And when your teammates are your “customers,” you get this magical gift of seeing your efforts turn to value <strong>directly</strong>. Hearing from someone you see everyday how much better their life is (in whatever small way) because of your work definitely hits me in the feels differently than delivering a top-tier experience to customers at large—that's still great too though!
        </p>
    </section>

    <section>
        <h2>
            <div class="svg-wrap">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <use href="icons.svg#heart-heading"></use>
                </svg>
            </div>
            Parting thoughts
        </h2>
    
        <p class="body-large">
            The web is a wild place, and I strive for my impact to make it a more honest, more accessible, and more enjoyable place to be.
        </p>

        <p>
            Have fun and stay safe!
        </p>
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <use href="icons.svg#smile"></use>
        </svg>
    </section>
</div>

<style>
    section {
        margin-bottom: 4rem;
    }
    h2 {
        font-style: normal;
        font-weight: 900;
        font-size: 1.5rem;
        line-height: 2rem;
        
        margin-bottom: 1.75rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

    }
    h2 .svg-wrap {
        padding: .5rem;
        background: rgba(0, 68, 255, 0.08);
        border-radius: .5rem;
        margin-bottom: .5rem;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .body-large {
        font-style: normal;
        font-weight: 500;
        font-size: 1.25rem;
        line-height: 2rem;
        margin-bottom: 1rem;
    }
    p a {
        font-weight: 600;
        text-decoration: none;
        border-bottom: 2px solid rgba(0, 68, 255, 0.12);
        padding: 2px 6px;
        color: var(--accent);
        transition: border-color 125ms linear, background-color 125ms linear, color 125ms linear;
    }
    p a:hover {
        border-radius: 8px;
        border-color: var(--accent);
        background-color: var(--accent);
        color: white;
    }
    p:not(:last-child) {
        margin-bottom: 1rem;
    }
    .extended-reading p {
        text-align: left;
    }
    ul {
        list-style: none;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 1.25rem;
    }
    ul li {
        width: 100%;
    }
    em {
        font-style: italic;
    }
    strong {
        font-weight: 900;
    }
</style>