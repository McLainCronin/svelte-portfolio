<script>
    export let y;

    let tabs = [
        {name: 'Projects', link: '#projects'},
        {name: 'About Me', link: '#about'},
        // {name: 'Contact', '#contact'}
    ];
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid ' + (y > 0 ? ' py-4 bg-slate-950 border-blue-950' : ' py-6 bg-transparent border-transparent')}>
    <h1 class="font-medium">
        <b class="" >McLain</b> Cronin
    </h1>
    <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a href={tab.link} class="px-3 duration-200 hover:text-blue-400">
                <p>{tab.name}</p>
            </a>
        {/each}
    
        <a href="#https://www.linkedin.com/in/mclain-cronin-963781117/" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950">
            <div class="absolute top-0 right-full w-full h-full bg-blue-600 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
            <h4 class="relative z-9">Get in touch</h4>
        </a>
    </div>
</header>