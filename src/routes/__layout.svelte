<script>
    import Button from '../components/Button.svelte'
    import '../satoshi.css'
</script>

<style>
    /* @import url('../satoshi.css'); */

    :global(:root){
        --accent: #0044ff;
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
        text-align: center;
        color: var(--accent);
    }

    main {
        padding: 1.25rem;
        max-width: 1200px;
    }
    nav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 2.5rem;
        padding: 1.25rem;
        border-bottom: 2px solid rgba(0, 68, 255, 0.12);
    }

    @media screen and (min-width: 481px){
        main {
            padding: 0;
            margin: 2.5rem;
        }
    }
    @media screen and (min-width: 769px){
        main {
            padding: 0;
            margin: 4rem;
        }
    }
    @media screen and (min-width: 1025px){
        main {
            padding: 0;
            margin: 5rem auto;
        }
    }
</style>

<nav>
    <Button style='nav' name='home' label='Home' url='/'></Button>
    <Button style='nav' name='info' label='Info' url='/info'></Button>
</nav>
<main>
    <slot></slot>
</main>