<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Sevs Store', icon: 'fa-solid fa-cart-shopping'},
        {name: 'Ultimate Todos', icon: 'fa-solid fa-list-check'},
        {name: 'Tablet', icon: 'fa-solid fa-diagram-project'},
    ];
// need to define our benefits
    let benefits = [
        {name: 'a self taught developer', description: 'taught myself.....'},
        {name: 'a product design & UX fanatic ', description: 'crazy about....'},
        {name: 'an excellent communicator', description: 'when we work together.....'}
    ]


</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">Welcome! I'm <span class="poppins text-violet-400"> Sevren</span> Roberge <br/>Full Stack <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes Javascript (React.js or SvelteKit), TailwindCSS, Node.js + Express.js
            </p>
            <a class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" href='https://www.linkedin.com/in/sevren-roberge-7599361b6/'>
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-o duration-200"
        />
        <h4 class="relative z-9 font-semibold">Get in touch &rarr;</h4>

            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/1.png"} alt="Profile" class="object-cover z-[2] "/>
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavours.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class='poppins text-violet-400'>see</span> my work?
            </h3>
          
        </div>
        <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200 ">
            <i class="fa-regular fa-circle-play"></i>
            <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid:cols-3 gap-12 lg:gap-10">
           <!-- pass down a prop named step set equal to steps an array with its index -->
            <Step step={steps[0]}>
                <p>Sevs Store is a merchandising store created with <strong class="text-violet-400">Next.js Commerce.js Stripe & Node.js + Express.js!</strong> Commerce.js is a product CMS and Stripe is used for all transaction handling</p>
            
            </Step>
            <Step step={steps[1]}>
                <p>Ultimate Todos is a Full Stack <strong class="text-violet-400">Next.js, Node.js + Express.js & FIrebase</strong> CRUD application that allows a user to login manage a tidy and efficacious todo list, and persist this information across all devices</p>
            
            </Step>
            <Step step={steps[2]}>
                <p>The Tablet is a <strong class="text-violet-400">SvelteKit & TailwindCSS </strong> web application hosted on <strong class="text-violet-400">Netlify</strong> that stores all of the information of this <strong class="text-violet-400">Universe</strong></p>
            
            </Step>

        </div>

    </section>
    <section id='about' class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">

        

            
        
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class='font-semibold text-3xl sm:text-4xl md:text-5xl'>A bit <span class="poppins text-violet-400">about</span> me.</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am ...</p>
        <div class="flex flex-col gap-20 w-full mx-auto m-w-[800px]">
            <!-- use the each map over all benefits extract each indiviual benefit as a benefit also take the index close the each-->
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                    <!-- use curly braces to render out js value 01 02 03-->
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl smtext-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>{benefit.description}</p>
                </div>
            </div>
            {/each}
        </div>
        <h5 class={'text-2xl sm:text-3xl font-semibold text-center poppins'}>The <span class="text-violet-400 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200"}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap p-2 px-8 bg-violet-700 text-white">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="whitespace-nowrap border-r border-solid border-white pl-4 py-4 font-semibold text-small">Dedication</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="whitespace-nowrap border-r border-solid border-white pl-4 py-4 font-semibold text-small">Critical Though</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr >
                        <td class="whitespace-nowrap border-r border-solid border-white pl-4 py-4 font-semibold text-small">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td class="whitespace-nowrap border-r border-solid border-white pl-4 py-4 font-semibold text-small">Programming Ability</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
    </section>
</main>