<script>

    import Button from '../components/Button.svelte'

    let style= 'line'
    function handleMouseOver(e) {
        style= 'filled'
    }
    function handleMouseOut(e) {
        style= 'line'
    }
</script>

<style>
    @import url('https://rsms.me/inter/inter.css');

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
        font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", sans-serif;
        font-size: 16px;
        color: var(--accent);
    }

    main {
        padding: 40px 20px;
        max-width: 640px;
    }
    nav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    @media screen and (min-width: 768px){
        main {
            padding: 0;
            margin: 40px auto;
        }
    }
</style>

<main>
    
    <nav>
        <Button name='smile' label='Danny McClain' url='/'></Button>
        <Button name='info' label='Info' url='/info'></Button>
    </nav>

    <slot></slot>

</main>