<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Sevs Store', icon: 'fa-solid fa-cart-shopping', href:'https://sevsecommerceshop.netlify.app/'},
        {name: 'FIT MOBILE', icon: 'fa-solid fa-list-check', href:'https://fitmobile.netlify.app'},
        {name: 'SPACE APOD', icon: 'fa-solid fa-diagram-project', href:'https://spaceapod.netlify.app/'},
    ];
// need to define our benefits
    let benefits = [
        {name: 'a self taught developer', description: 'Highly effective and extremely resouceful with a great capacity for learning and development, I have used online resources to expand my knowledge in this field and couldn\'t be more happy. All I want to do is learn more and more.'},
        {name: 'a product design & UX fanatic ', description: 'I have always been crazy about design especially when it comes to websites and applications, I have been a skilled painter tradesman most of my life and the job has always required a very keen eye to detail.'},
        {name: 'an excellent communicator', description: 'Also I work extremely well together with a partner or in any group. I can adapt to other minds and come together to solve any problem especially if there is one within the group.'}
    ]


</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">Welcome! I'm <span class="poppins text-red-700"> Sevren</span> Roberge <br/>Full Stack <span class="poppins text-red-700">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-red-600">favorite tech</span> includes Javascript (React.js or SvelteKit), TailwindCSS, Node.js + Express.js, Python (Flask + Django)
            </p>
            <a class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full  text-red-700 cursor-pointer" href='https://www.linkedin.com/in/sevren-roberge-7599361b6/'>
                <div class="absolute top-0 right-full w-full h-full bg-red-400 opacity-20 group-hover:tranred-x-full z-o duration-200"
        />
        <h4 class="relative z-9 group font-semibold">Get in touch <span class="group-hover:text-white group-hover:duration-500">&rarr;</span></h4>

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
                Curious to <span class='poppins text-red-700'>see</span> my work?
            </h3>
          
        </div>
        
        <div class="grid grid-cols-1 lg:grid:cols-3 gap-12 lg:gap-10">
           <!-- pass down a prop named step set equal to steps an array with its index -->
            <Step step={steps[0]}>
                <p><strong class="text-red-700">Sevs Ecommerce</strong> is a merchandising store, currently in the testing phase, created with <strong class="text-red-700">NEXT.JS STRIPE & NODE.JS!</strong></p>
            
            </Step>
            <Step step={steps[1]}>
                <p>Using <strong class="text-red-700">REACT.JS, FIT MOBILE </strong> is a fitness application geared towards generating workout plans and keeping track of exercises that is accessible across all devices</p>
            
            </Step>
            <Step step={steps[2]}>
                <p><strong class="text-red-700">SPACE APOD</strong> is an  Astronomy Picture Of The Day, using <strong class="text-red-700">NASA API</strong> built via REACT.JS and hosted on <strong class="text-red-700">Netlify</strong></p>
            
            </Step>

        </div>

    </section>
    <section id='about' class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-red-800 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-red-800 py-4">

        

            
        
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class='font-semibold text-3xl sm:text-4xl md:text-5xl'>A bit <span class="poppins text-red-700">about</span> me.</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am ...</p>
        <div class="flex flex-col gap-20 w-full mx-auto m-w-[800px]">
            <!-- use the each map over all benefits extract each indiviual benefit as a benefit also take the index close the each-->
            {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-xl sm:text-5xl md:text-6xl text-red-700 font-semibold">
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
        <h5 class={'text-2xl sm:text-3xl font-semibold text-center poppins'}>The <span class="text-red-700 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-auto gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-black rounded text-center">
                <thead class={"border-b border-solid border-slate-400"}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4 text-red-900">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4 text-red-900">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4 text-red-900">Candidate #3</th>
                        <th class="whitespace-nowrap rounded-tr-sm p-2 px-8 bg-red-700 text-white">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-400">
                        <td class="whitespace-nowrap border-solid border-transparent pl-4 py-4 font-semibold text-small">Dedication</td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-xmark text-red-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-400">
                        <td class="whitespace-nowrap border-solid border-white pl-4 py-4 font-semibold text-small">Critical Though</td>
                        <td><i class="fa-solid fa-xmark text-red-600"></i></td>
                        <td><i class="fa-solid fa-xmark text-red-600"></i></td>
                        <td><i class="fa-solid fa-xmark text-red-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                    </tr>
                    <tr >
                        <td class="whitespace-nowrap border-solid border-white pl-4 py-4 font-semibold text-small">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-xmark text-red-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-400">
                        <td class="whitespace-nowrap border-solid border-white pl-4 py-4 font-semibold text-small">Programming Ability</td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
                        <td><i class="fa-solid fa-check text-green-600"></i></td>
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