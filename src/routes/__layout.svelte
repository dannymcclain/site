<script>
    import Button from '../components/Button.svelte'
    import '../satoshi.css'
</script>

<style>
    :global(:root){
        --accent: #0044ff;
        --accent-4: #F5F8FF;
        --accent-8: #EBF0FF;
        --accent-12: #E0E9FF;
    }

    :global(*),
    :global(*::after),
    :global(*::before) {
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :global(body){
        font-family: 'Satoshi-Variable', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
        font-size: 16px;
        font-weight: 500;
        line-height: 1.75rem;
        text-align: left;
        color: var(--accent);
        background-color: var(--accent-4);
    }
    
    :global(.body-large){
        margin-bottom: 1rem;
        font-style: normal;
        font-weight: 500;
        font-size: 1.25rem;
        line-height: 2rem;
    }

    :global(.body-small){
        font-size: .75rem;
        line-height: 1.25rem;
    }

    :global(a){
        text-decoration: underline;
        color: var(--accent); 
    }

    :global(a:hover) {
        background-color: var(--accent);
        color: #fff;
        text-decoration: none;
    }

    :global(.eyebrow) {
        font-style: normal;
        font-weight: 900;
        font-size: 12px;
        line-height: 12px;
        letter-spacing: 0.04em;
        text-transform: uppercase;
    }

    main {
        padding: 0 1rem;
        max-width: 650px;
        margin: 0 auto;
    }

    nav {
        position: sticky;
        position: -webkit-sticky;
        top: 0;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 1.5rem;
        padding: 1.5rem;
        background-color: #fff;
    }

    footer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 1.5rem 1.5rem 3rem;
    }
    
    footer .eyebrow {
        margin-bottom: .25rem;
    }
</style>

<nav>
    <Button style='nav' name='home' label='Home' url='/'></Button>
    <Button style='nav' name='info' label='Info' url='/info'></Button>
</nav>
<main>
    <slot></slot>
    <footer>
        <p class="eyebrow">Be kind · have fun · Stay safe</p>
        <p class="body-small">© Danny McClain 2022</p>
    </footer>
</main>