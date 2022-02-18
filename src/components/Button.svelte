<script lang="ts">
    import { fade } from 'svelte/transition'
    export let name:String = '';
    export let label:String = '';
    export let url:string = '';
    export let style:string = '';
    export let newTab:boolean = false;
    let target;

    if (newTab === true){
        target = 'target="_blank"'
    } else {
        
    }
//     let hovering = false;
// on:mouseenter={() => {hovering = true}}
// on:mouseleave={() => {hovering = false}}
</script>

<a  
    
    href={url} 
    class="button {style}"
    {target}
    >
        <div class="icon-image">
            <svg class="icon line">
                <use href="icons.svg#{name}"></use>
            </svg>
            <svg class="icon filled">
                <use href="icons.svg#{name}-filled"></use>
            </svg>
        </div>
    {label}<slot></slot>
</a>

<style>   
/* BASE STYLES */
    .button {
        font-style: normal;
        font-weight: 700;
        font-size: 1rem;
        line-height: 1rem;
        text-decoration: none;
        color: var(--accent);
        display: inline-flex;
    }

/* NORMAL VARIANT */
    .normal {
        flex-direction: row;
        align-items: center;
        flex-basis: auto;
        padding: .75rem 1rem;
        background: transparent;
        border: 2px solid rgba(0, 68, 255, 0.12);
        border-radius: 8px;
        transition: background-color 125ms linear, border-color 125ms linear, color 125ms linear;
    }
    
    .normal:hover, .grid:hover {
        background: var(--accent);
        border-color: var(--accent);
        color: #fff;
    }
    
    /* NAV VARIANT */
    .nav {
        flex-direction: row;
        align-items: center;
        flex-basis: auto;
        background: transparent;
    }
    
    /* GRID VARIANT */
    .grid {
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 1rem 1.25rem;
        border: 2px solid rgba(0, 68, 255, 0.12);
        border-radius: 8px;
        width: 100%;
        transition: background-color 125ms linear, border-color 125ms linear, color 125ms linear;
    }
    .grid .icon-image {
        margin-right: 0;
        margin-bottom: .5rem;
    }

/* ICON SWAPPING     */
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
    }

    .filled {
        opacity:0;
        transition: opacity 125ms linear;
    }
    .line {
        opacity: 1;
        transition: opacity 125ms linear;
    }
    
    .button:hover .filled {
        opacity: 1;
    }
    .button:hover .line {
        opacity: 0;
    }
    </style>
    