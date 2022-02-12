<script lang="ts">
    export let title:string = ''
    export let icon:string = ''
    export let style:string=''
</script>

<section class="card">
    <div class="title">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <use href="icons.svg#{icon}"></use>
        </svg>

        <h2 class="eyebrow">{title}</h2>
    </div>

    <div class="content" {style}>
        <slot></slot>
    </div>
        
</section>

<style>
    section {
        background: #fff;
        border-radius: 1rem;
        margin-bottom: 1.5rem;
    }
    .title {
        padding: 1.5rem;
        border-bottom: 2px solid var(--accent-4);
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
    }

    .title svg {
        margin-right: .5rem;
    }

    /* h2 {
        font-style: normal;
        font-weight: 900;
        font-size: 12px;
        line-height: 12px;
        letter-spacing: 0.04em;
        text-transform: uppercase;
    } */
    .content {
        padding: 1.5rem;
    }
</style>