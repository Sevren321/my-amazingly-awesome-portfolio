<script>
    export let y;

    let tabs = [
        {name: 'Projects', link: '#projects'},
        {name: 'About me', link: '#about'},
        // {name: 'Blog', '#projects'}
        ];
</script>




<header class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid " +  (
    y > 0 ? ' py-4 bg-slate-950 border-red-950 ' : ' py-6 bg-transparent border-transparent'
)}>
    <h1 class="font-medium upper">
        <b class="font-bold poppins uppercase">Sevren</b> Roberge
    </h1>
    <!-- wrap class in curly parenthesis because it will have some dynamic classes -->
    <div class='sm:flex ml-auto pr-4 items-center gap-4 hidden'>
    <!-- mapping out items using the svelte kit -->
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-red-500">
                <p>{tab.name}</p>
            </a>
        {/each}
    </div> 
    <a href="https://www.linkedin.com/in/sevren-roberge-7599361b6/"
    target="_blank" 
    class="relative overflow-hidden px-4 py-2 group rounded-full bg-slate-100 hover:bg-red-700 hover:duration-1000 ">
        <div class="absolute top-0 right-full w-full h-full z-o "
        />
        <h4 class="relative z-9 font-semibold group-hover:text-white  text-red-700 group-hover:duration-200">Contact</h4>
    </a>
</header>