<script>
    import Button from '../components/Button.svelte'
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
</script>


<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >

    <h2>
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0_1543_5427)">
            <path d="M12 0C8.68629 0 6 2.68629 6 6C6 9.31371 8.68629 12 12 12C15.3137 12 18 9.31371 18 6C18 2.68629 15.3137 0 12 0Z" fill="#0044FF"/>
            <path d="M7 14C4.23858 14 2 16.2386 2 19C2 21.7614 4.23858 24 7 24H17C19.7614 24 22 21.7614 22 19C22 16.2386 19.7614 14 17 14H7Z" fill="#0044FF"/>
            </g>
            <defs>
            <clipPath id="clip0_1543_5427">
            <rect width="24" height="24" fill="white"/>
            </clipPath>
            </defs>
        </svg>                     
        About me
    </h2>

    <p class="intro">
        I'm a husband and father of two who enjoys homesteading with my family outside <a href="/">Nashville, TN</a>. I love riding bicycles and am just as likely to be found listening to <a href="/">Blood Incantation</a> as I am <a href="/">AceMo</a>.
    </p>
</section>

<style>
    h2 {
        font-weight: 800;
        font-size: 1rem;
        line-height: 1rem;
        letter-spacing: -0.01em;
        margin-bottom: 1.25rem;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
    }
    h2 svg {
        margin-right: .5rem;
    }

    .intro {
        font-weight: normal;
        font-size: 1.25rem;
        line-height: 2.25rem;
        letter-spacing: -0.02em;
    }
    p a {
        text-decoration: none;
        border-bottom: 2px solid rgba(0, 68, 255, 0.12);
        /* background: rgba(0, 68, 255, 0.12); */
        padding: 2px 6px;
        color: var(--accent);
        transition: border-color 125ms linear, background-color 125ms linear, color 125ms linear;
    }
    p a:hover {
        border-radius: 4px;
        border-color: var(--accent);
        background-color: var(--accent);
        color: white;
    }
    /* p a {
        text-decoration: none;
        border-bottom: 2px solid rgba(0, 68, 255, 0.12);
        padding: 2px;
        color: var(--accent);
        transition: border-color 125ms linear, background-color 125ms linear, color 125ms linear;
    }
    p a:hover {
        border-color: var(--accent);
        background-color: var(--accent);
        color: white;
    } */
    
</style>