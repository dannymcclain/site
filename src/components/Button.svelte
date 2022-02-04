<script lang="ts">
    import { fade } from 'svelte/transition'
    export let name:String = '';
    export let label:String = '';
    export let url:string = '';
    export let style:string = '';
//     let hovering = false;
// on:mouseenter={() => {hovering = true}}
// on:mouseleave={() => {hovering = false}}
</script>

<a  

    style={style}
    href={url} 
    class="button">
        <div class="icon-image">
            <svg class="icon line">
                <use href="icons.svg#{name}"></use>
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
        font-weight: 600;
        font-size: 1rem;
        line-height: 1rem;
        letter-spacing: -0.02em;
        text-decoration: none;
        color: var(--accent);
        transition: background-color 125ms linear, border-color 125ms linear, color 125ms linear;
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
        /* margin-right: 0.5rem;  */
        width: 1.5rem;
        height: 1.5rem;
    }

    .filled {
        opacity:0;
        transition: opacity 125ms linear;
        /* transition-delay: 125ms; */
    }
    .line {
        opacity: 1;
        transition: opacity 125ms linear;
    }
    
    .button:hover .filled {
        opacity: 1;
    }

    /* .button:hover .line {
        opacity:0;
    } */
    </style>
    