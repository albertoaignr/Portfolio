<script>
    import Step from './Step.svelte';

    let steps = [
        {name: 'Alberto Store', icon: 'fa-solid fa-shopping-cart'},
        {name: 'Ultimate todos', icon: 'fa-solid fa-list-check'},
        {name: 'Pokedex', icon: 'fa-solid fa-diagram-project'},

    ]
    let benefits = [
        {name: 'name for list', description: 'description for list'},
        {name: 'name for list', description: 'description for list'},
        {name: 'name for list', description: 'description for list'}
    ];

</script>

<main class='flex flex-col flex-1 p-4'>
    <section id='introPage' 
        class='grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14'>
        <div 
          class='flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10'
        >

            <h2 class='font-semibold text-4xl sm:text-5xl md:text-6xl'>
                Hi! I'm <span class='text-blue-400'>Alberto</span> Aigner <br/> Full Stack
                <span class='poppins text-blue-400'>Developer</span> 
            </h2>
            <p class='text-base sm:text-lg md:text-xl'>
                My <span class='text-blue-400'>favorite tech</span> includes JavaScript (NEXT.js or SvelteKit), React, TailwindCSS, Node.js + Express.js & PostgreSQL and of course Python! 
            </p>
            <a  class='blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative  overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer z-[11]' href='https://www.linkedin.com/in/albertoaigner/' target= '_blank' >
                <div class='absolute top-0 right-full w-full h-full bg-blue-400 opacity-20 group-hover:translate-x-full z-0 duration-200'/>
                <h4 class='relative z-9'>Get in touch &rarr;</h4>
            </a>
        </div>
        <div class='relative shadow-2xl grid place-items-center'>
            <img src={"images/profile.png"} alt='Profile image' class='rounded-full object-cover z-[2] max-h-[30hv]'/>
        </div>
    </section>
    
    <section id='projects' class='py-20 lg:py-32 flex flex-col gap-24'>

        <div class='flex flex-col gap-2 text-center'>
            <h6 class='text-lg sm:text-xl md:text-2xl'>
                A few of my creative stuff
            </h6>
            <h3>
                Curious to <span class='poppins text-blue-400'>see</span> my work? 
            </h3>
            
        </div>
        <a href='#' target='_blank' class='mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-blue-700 duration-200 cursor-pointer z-[11]'>
            <i class='fa-regular fa-circle-play'></i>
            <p>Watch the video</p>

        </a>
        <div class='grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10'>

            <Step step={steps[0]}> 
                <p>Text for the store <strong class='text-blue-400'>Texto Fuerte</strong></p>
            </Step>
            <Step step={steps[1]}> 
                <p>Text for the project <strong class='text-blue-400'>Texto Fuerte</strong></p>
            </Step>
            <Step step={steps[2]}> 
                <p>Text for the project <strong class='text-blue-400'>Texto Fuerte</strong></p>
            </Step>

        </div>

    </section>
    <section id='about' class='py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative'> 
        <div class='flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 py-4'>
        <h6 class='text-lg sm:text-xl md:text-2xl'>Want to know more?</h6>
        <h3 class='font-semibold text-3xl sm:text-4xl md:text-5xl'>A bit <span class='poppins text-blue-400'>about</span> me</h3>
        </div>
        <p class='mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl'>I am . . .</p>
        <div class='flex flex-col gap-20 w-full mx-auto max-w-[800px]'>
            {#each benefits as benefit, index}
            <div class='flex gap-6 sm:gap-8'>
                <p class='poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold'>
                    0{index+1}
                </p>
                <div class='flex flex-col gap-6 sm:gap-8'>
                    <h3 class='text-2xl sm:text-3xl md:text-5xl'>
                        {benefit.name}
                    </h3> 
                    <p>{benefit.description}</p>

                </div>
            </div>
            {/each}
        </div>

    </section>
</main>