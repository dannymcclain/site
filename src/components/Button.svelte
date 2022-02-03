<script lang="ts">
    import { goto } from '$app/navigation';
    export let name:String = '';
    export let label:String = '';
    export let url:string = '';

    function handleClick() {
        goto(url)
    }
</script>

<a on:click={handleClick}
    href={url} 
    class="button">
        <div class="icon-image">
            <svg class="icon line">
                <use href="icons.svg#{name}-line"></use>
            </svg>
            <svg class="icon filled">
                <use href="icons.svg#{name}-filled"></use>
            </svg>
        </div>
    {label}
</a>

<style>   
    .button {
        display: inline-flex;
        flex-direction: row;
        align-items: center;
        flex-basis: auto;
        padding: 12px 16px;
        background: transparent;
        border: 2px solid rgba(0, 68, 255, 0.12);
        border-radius: 200px;
        font-style: normal;
        font-weight: 500;
        font-size: 1rem;
        line-height: 1rem;
        letter-spacing: -0.02em;
        text-decoration: none;
        color: var(--accent);
        transition: background-color 100ms linear, border-color 100ms linear, color 100ms linear;
    }
    
    .button:hover {
        background: var(--accent);
        border-color: var(--accent);
        color: #fff;
    }
    
    .icon-image {
        position: relative;
        height: 1.5rem;
        width: 1.5rem;
        margin-right: .5rem;
    }

    .icon {
        position: absolute;
        top:0;
        left:0;
        width: 1.5rem;
        height: 1.5rem;
        margin-right: 0.5rem; 
    }

    .filled {
        opacity:0;
        transform: scale(.2);
        transition: transform 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275), opacity 200ms linear;
    }
    .line {
        opacity: 1;
        transform: scale(1);
        transition: transform 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275), opacity 200ms linear;
    }
    
    .button:hover .filled {
        opacity: 1;
        transform: scale(1);
    }

    .button:hover .line {
        opacity:0;
        transform: scale(.2);
    }
    </style>
    