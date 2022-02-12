<script>
    import ImageLoader from '../components/ImageLoader.svelte';
    import { fade } from 'svelte/transition'
    import { quadInOut } from 'svelte/easing'
    import SectionCard from '../components/SectionCard.svelte'
    import { src_url_equal } from 'svelte/internal';

    let iconWorks = [
        { src: 'images/works/icons/sticker-icons.png', alt: 'Sticker Icons'},
        { src: 'images/works/icons/design-icons.png', alt: 'Design Tools Icons'},
        { src: 'images/works/icons/location-types.png', alt: 'Location Types Icons'},
        { src: 'images/works/icons/1px-line-icons.png', alt: '1px Line Icons'},
        { src: 'images/works/icons/building-icons.png', alt: 'Building and Tools Icons'},
        { src: 'images/works/icons/tools-icons.png', alt: 'Tool Icons'},
        { src: 'images/works/icons/accessibility-icons-grid.png', alt: 'Accessibility Icons'},
        { src: 'images/works/icons/music-icons.png', alt: 'Music Player Icons'},
        { src: 'images/works/icons/colorful-icons.png', alt: 'Colorful Icons'},
        { src: 'images/works/icons/sharp-icons.png', alt: 'Small Sharp Icons'},
        { src: 'images/works/icons/dm-icon-set.png', alt: 'Sharp Thin Icons'},
        { src: 'images/works/icons/happy-avatar-icon.png', alt: 'Happy Avatar Icon'},
        { src: 'images/works/icons/pinterest-style-icons.png', alt: 'Pinterest-style Icons'},
        { src: 'images/works/icons/playstation-icons.png', alt: 'Playstation Icon Exploration'},
        { src: 'images/works/icons/presentation-icons.png', alt: 'Personal Presentation Icons'},
        { src: 'images/works/icons/purple-icons.png', alt: 'Crocs-inspired Icons'}
    ]
</script>

<section 
    in:fade="{{ delay: 300, duration: 300, easing: quadInOut}}"
    out:fade="{{ duration: 150, easing: quadInOut}}"
    >
    
    <section class="intro">
        <h1>I'm Danny McClain, a multidisciplinary designer currently focusing on design systems & icon sets.</h1>
        <p class="body-large">I like to design systematically & put an emphasis on tidiness.</p>
        <p><a href="/info">Learn more about me.</a></p>
    </section>

    <SectionCard title='Recent work' icon='clock-filled'>
        <svg width="295" height="221" viewBox="0 0 295 221" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0_128_5908)">
            <rect width="295" height="221" rx="8" fill="#E0E9FF"/>
            <path d="M32 64V227C32 229.209 33.7909 231 36 231H304C306.209 231 308 229.209 308 227V64M32 64V36C32 33.7909 33.7909 32 36 32H304C306.209 32 308 33.7909 308 36V64M32 64H308" stroke="#0044FF" stroke-opacity="0.12" stroke-width="2"/>
            <circle cx="48" cy="48" r="4" fill="#0044FF" fill-opacity="0.12"/>
            <circle cx="60" cy="48" r="4" fill="#0044FF" fill-opacity="0.12"/>
            <circle cx="72" cy="48" r="4" fill="#0044FF" fill-opacity="0.12"/>
            <path d="M85 46V53H88.5V49H91.5V53H95V46L90 42L85 46Z" fill="#0044FF" fill-opacity="0.12"/>
            <path d="M79.528 119.288C83.968 119.288 87.28 116.672 87.904 112.712H83.872C83.392 114.464 81.784 115.544 79.6 115.544C76.744 115.544 74.968 113.456 74.968 110.12C74.968 106.736 76.72 104.696 79.6 104.696C81.736 104.696 83.248 105.704 83.776 107.48H87.88C87.328 103.496 84.136 100.952 79.696 100.952C74.392 100.952 70.864 104.6 70.864 110.144C70.864 115.76 74.2 119.288 79.528 119.288ZM89.4003 112.976C89.4003 116.768 92.1842 119.288 96.0243 119.288C99.8403 119.288 102.624 116.768 102.624 112.976C102.624 109.184 99.8403 106.64 96.0243 106.64C92.1842 106.64 89.4003 109.184 89.4003 112.976ZM93.1203 112.952C93.1203 111.152 94.2963 109.952 96.0243 109.952C97.7283 109.952 98.9043 111.152 98.9043 112.952C98.9043 114.776 97.7283 115.976 96.0243 115.976C94.2963 115.976 93.1203 114.776 93.1203 112.952ZM108.463 119V112.568C108.463 110.552 109.543 109.976 110.599 109.976C111.775 109.976 112.543 110.696 112.543 112.184V119H116.239V112.568C116.239 110.528 117.295 109.952 118.351 109.952C119.527 109.952 120.319 110.672 120.319 112.184V119H124.015V111.152C124.015 108.416 122.479 106.616 119.383 106.616C117.655 106.616 116.239 107.456 115.615 108.728C114.919 107.456 113.767 106.616 111.967 106.616C110.239 106.616 109.063 107.408 108.463 108.248L108.223 107H104.767V119H108.463ZM128.482 105.128C129.634 105.128 130.57 104.192 130.57 103.016C130.57 101.84 129.634 100.928 128.482 100.928C127.306 100.928 126.37 101.84 126.37 103.016C126.37 104.192 127.306 105.128 128.482 105.128ZM126.658 119H130.354V107H126.658V119ZM136.822 119V112.424C136.822 110.936 137.758 109.976 139.222 109.976C140.494 109.976 141.334 110.96 141.334 112.472V119H145.03V111.584C145.03 108.44 143.374 106.616 140.518 106.616C138.958 106.616 137.59 107.216 136.846 108.248L136.606 107H133.126V119H136.822ZM147.081 112.784C147.081 116.384 149.409 118.856 152.769 118.856C154.329 118.856 155.673 118.304 156.393 117.44V119C156.393 120.704 155.265 121.76 153.489 121.76C151.857 121.76 150.849 120.968 150.777 119.624H147.033C147.369 123.032 149.841 125.12 153.513 125.12C157.617 125.12 160.089 122.528 160.089 118.232V107H156.609L156.417 108.2C155.769 107.216 154.473 106.592 152.841 106.592C149.457 106.592 147.081 109.136 147.081 112.784ZM150.801 112.688C150.801 110.984 151.929 109.808 153.561 109.808C155.265 109.808 156.393 110.936 156.393 112.688C156.393 114.464 155.265 115.64 153.585 115.64C151.953 115.64 150.801 114.416 150.801 112.688ZM168.356 115.208C168.356 117.632 170.348 119.312 173.516 119.312C176.636 119.312 178.82 117.752 178.82 115.184C178.82 113.264 177.74 112.352 175.772 111.92L173.54 111.44C172.7 111.248 172.244 110.936 172.244 110.384C172.244 109.736 172.772 109.304 173.612 109.304C174.5 109.304 175.004 109.856 175.004 110.672H178.508C178.508 108.248 176.564 106.616 173.78 106.616C170.9 106.616 168.764 108.056 168.764 110.552C168.764 112.664 169.844 113.624 172.052 114.104L174.26 114.584C175.148 114.776 175.34 115.16 175.34 115.52C175.34 116.144 174.812 116.552 173.66 116.552C172.532 116.552 171.908 116.048 171.86 115.208H168.356ZM180.103 112.976C180.103 116.768 182.887 119.288 186.727 119.288C190.543 119.288 193.327 116.768 193.327 112.976C193.327 109.184 190.543 106.64 186.727 106.64C182.887 106.64 180.103 109.184 180.103 112.976ZM183.823 112.952C183.823 111.152 184.999 109.952 186.727 109.952C188.431 109.952 189.607 111.152 189.607 112.952C189.607 114.776 188.431 115.976 186.727 115.976C184.999 115.976 183.823 114.776 183.823 112.952ZM194.822 112.976C194.822 116.768 197.606 119.288 201.446 119.288C205.262 119.288 208.046 116.768 208.046 112.976C208.046 109.184 205.262 106.64 201.446 106.64C197.606 106.64 194.822 109.184 194.822 112.976ZM198.542 112.952C198.542 111.152 199.718 109.952 201.446 109.952C203.15 109.952 204.326 111.152 204.326 112.952C204.326 114.776 203.15 115.976 201.446 115.976C199.718 115.976 198.542 114.776 198.542 112.952ZM213.885 119V112.424C213.885 110.936 214.821 109.976 216.285 109.976C217.557 109.976 218.397 110.96 218.397 112.472V119H222.093V111.584C222.093 108.44 220.437 106.616 217.581 106.616C216.021 106.616 214.653 107.216 213.909 108.248L213.669 107H210.189V119H213.885Z" fill="#0044FF" fill-opacity="0.48"/>
            </g>
            <defs>
            <clipPath id="clip0_128_5908">
            <rect width="295" height="221" rx="8" fill="white"/>
            </clipPath>
            </defs>
            </svg>
    </SectionCard>

    <SectionCard title="Icons" icon="image-filled">
        <div class="tab-panels-container">
            {#each iconWorks as { src, alt}, i }
            <div class="tab-panel">
                <div class="tab-panel-content">
                    <ImageLoader {src} {alt} />
                </div>    
            </div>
            {/each}
        </div>
    </SectionCard>
 
    <SectionCard title="Utilities" icon="pencil-filled">
        <p class="utilities-content">
            As someone primarily designing for the web, I like to explore the technologies that bring my designs to life. Here are a few small projects I've built to satisfy my own curiosity and speed up my workflow. Always more in the works.
        </p>
        <a class="utility-card" href="/" target="_blank">
            Fitter
            <span class="body-small">
                A tiny Figma plugin that resizes an item to fit its parent's width, height, or both.
            </span>
        </a>
        <a class="utility-card" href="/" target="_blank">
            Ratio
            <span class="body-small">
                A quick, dead-simple proportion calculator made with Svelte.
            </span>
        </a>
        <a class="utility-card" href="/" target="_blank">
            Grid Finder
            <span class="body-small">
                A tool to help you calculate perfect grids with whole values. (Plugin version in development.)
            </span>
        </a>
    </SectionCard>

    


</section>

<style>
    .tab-panels-container {
		scroll-snap-type: x mandatory;
		-webkit-overflow-scrolling: touch;
		overflow-x: scroll;
		display: flex;
	}
	
	/* .tab-panel-content {
		margin: auto;
	} */

	.tab-panel {
        scroll-snap-align: start;
        scroll-snap-stop: always;
		width: 90%;
		flex: 1 0 auto;
		height: auto;
		display: flex;
        margin-right: 1rem;
    }

    .intro {
        padding: 1.25rem;
        margin-bottom: 1rem;
    }
    h1 {
        font-style: normal;
        font-weight: 900;
        font-size: 2rem;
        line-height: 2.5rem;
        letter-spacing: -0.02em;
        margin-bottom: 1rem;
    }
    
    .utilities-content {
        margin-bottom: 1.5rem;
    }
    .utility-card {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        padding: 1rem;
        border: 2px solid var(--accent-12);
        border-radius: 8px;
        margin-top: 1rem;
        text-decoration: none;
        font-weight: 700;
        transition: background-color 125ms linear, border-color 125ms linear, color 125ms linear;
    }
    .utility-card span {
        font-weight: 500;
    }
    .utility-card:hover {
        background-color: var(--accent);
        border-color: var(--accent);
    }
    .utility-card:not(:last-child) {
        margin-bottom: 1rem;
    }
</style>