<script lang="ts">
    export let name:String = '';
    export let label:String = '';
    export let url:string = '';

    let hovering;

	function enter() {
		hovering = true;
	}

	function leave() {
		hovering = false;
	}
</script>

<a on:mouseenter={enter} on:mouseleave={leave}
href={url} 
class="button">
    <div class="icon-image">
        <div class="svg-wrap">
            <svg class="icon">
                <use href="icons.svg#{name}-line"></use>
            </svg>
            <svg class="icon">
                <use href="icons.svg#{name}-filled"></use>
            </svg>
        </div>
    </div>
    {label}
</a>

<style>
    .icon-image {
        height:24px;
        width:24px;
        position: relative;
        display:inline-block;
        overflow: hidden;
        margin-right: .5em
    }
    .svg-wrap {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        position:absolute;
        top:0;
        left:0;
        /* transition: top 300ms cubic-bezier(0.175, 0.885, 0.32, 1); */
    }
    .button:hover .svg-wrap {
        top:-24px;
    }
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
        /* transition: background-color 150ms ease-in-out, border-color 150ms ease-in-out, color 150ms ease-in-out; */
    }
    .button:hover {
        background: var(--accent);
        border-color: var(--accent);
        color: #fff;
    }
    .icon {
        width: 1.5rem;
        height: 1.5rem;
        margin-right: 0.5rem; 
    }
    </style>
    