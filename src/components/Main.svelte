<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: 'Fruit Shop',
            link: 'https://mc-fruits.netlify.app/',
            icon: 'fas fa-carrot',
            description: ' is an e-commerce site that allows users to add items to their cart and checkout. The shop is built on <span class="text-blue-400">Next.js</span> using <span class="text-blue-400">Zustand</span> for state management and <span class="text-blue-400">Stripe</span> for handling orders.'
        },
        {
            name: 'Moodi',
            link: 'https://moodiapp.netlify.app/',
            icon: 'text-6xl fas fa-heart-circle-check',
            description: ' is a web app that allows users to track their daily moods and view their trends over time. The app is developed using <span class="text-blue-400">Next.js</span>, styled with <span class="text-blue-400">TailwindCSS</span> for a vibrant design and integrates <span class="text-blue-400">Firebase</span> for secure user authentication.'
        },
        {
            name: 'Zen API',
            link: 'https://zen-api.netlify.app/',
            icon: 'fas fa-seedling',
            description: ' is a functional API marketplace that allows users to purchase a single-use or subscription-based access to an API. The store is built on <span class="text-blue-400">Node.js</span> and <span class="text-blue-400">Express.js</span>, using <span class="text-blue-400">Stripe</span> for payment processing and <span class="text-blue-400">Firebase</span> to store and validate assigned API keys.'
        },
        {
            name: 'NASA Image O.T.D.',
            link: 'https://nasa-daily-image-project.netlify.app/',
            icon: 'fas fa-rocket',
            description: ' is a web application that displays NASA\'s Image of the Day. Built with <span class="text-blue-400">React.js</span>, the app fetches images and descriptions from the <span class="text-blue-400">NASA API</span> and caches the data in a <span class="text-blue-400">NoSQL</span> database for optimized performance.'
        }
    ];

    let benefits = [
        {
            name: 'Self-taught developer',
            description: 'As a self-taught developer, I have proactively combined self-directed learning with formal education to master a diverse range of technologies and skills. This approach has enabled me to gain valuable real-world experience while building upon the technical foundations provided by traditional education.'
        },
        {
            name: 'Passionate and adaptable',
            description: 'By continuously seeking out current industry trends and technologies, I adapt to new challenges and opportunities with ease. My passion for software development drives me to continuously improve my skills and knowledge, ensuring that I can deliver top-tier solutions that meet the needs of my team and projects.'
        },
        {
            name: 'Collaborative and Approachable',
            description: 'I am a team player who thrives in collaborative environments. I am always open to feedback and eager to learn from my peers. My approachable nature and strong communication skills enable me to build strong relationships with colleagues and stakeholders, fostering a positive and inclusive work culture.'
        },
        {
            name: 'Creatively Driven',
            description: 'I aim to leverage my full-stack development skills to build impactful software that enhances user experiences while adhering ethical standards. I excel in dynamic team environments where I can contribute to cutting-edge projects and continuously evolve as a developer.'
            
        }
    ];


</script>

<main class="flex flex-col flex-1 p-4 z-[1]"> 
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-blue-400">McLain</span> Cronin <br/>Full Stack <span class="poppins text-blue-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                <p>
                    My <span class="text-blue-400">favorite technologies</span> include <span class="text-blue-400">JavaScript</span> (React, Next.js, SvelteKit), <span class="text-blue-400">Python</span>, and <span class="text-blue-400">PostgreSQL</span>. I also enjoy working with <span class="text-blue-400">Tailwind CSS</span> and <span class="text-blue-400">Firebase</span> to build dynamic and scalable applications.
            </p>
            <a 
                class="blueShadow mx-auto lg:mx-0 lg:mr-auto lg:lm-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" 
                href="mailto:cronin97@gmail.com" 
                target="_blank"
            >
                <div class="absolute top-0 right-full w-full h-full bg-blue-600 opacity-20 group-hover:translate-x-full duration-200"></div>
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </a>
        </div>
        <div class="relative grid place-items-center">
            <img src={"images/profile-picture.png"} alt="Profile image" class="object-cover z-[2] max-h-[70vh]"/>
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Interested to <span class="poppins text-blue-400">see</span> my work?
            </h3>
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my <span class="text-blue-400">projects</span>:
            </h6>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-10">
            {#each steps as step, i}
                <Step {step}>
                    <p class="text-base md:text-lg">
                        <strong class="text-blue-400">{step.name}</strong>{@html step.description}
                    </p>
                </Step>
            {/each}
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 pt-6 pb-7">
            <h3 class="font-semibold text-3xl smLtext-4xl md:text-5xl">
                A bit <span class="poppins text-blue-400">about</span> me.
            </h3>
        </div>
            <!-- <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">Text that tells alllllll about me</p> -->
            <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
                {#each benefits as benefit, index}
                    <div class="flex gap-6 sm:gap-8">
                        <p class="poppins text-3xl sm:text:5xl md:text-6xl text-slate-500 font-semibold">
                            0{index + 1}
                        </p>
                        <div class="flex flex-col gap-6 sm:gap-8">
                            <h3 class="text-2xl sm:text-3xl md:text-5xl">
                                {benefit.name}
                            </h3>
                            <p>{benefit.description}</p>
                        </div>
                    </div>
                {/each}
            </div>
            <div class="flex flex-col gap-12 text-center relative pt-6">
                <h6 class="text-lg sm:text-x md:text-2xl">Want to know more?</h6>
                <a 
                    href="/path/to/your/resume.pdf" 
                    target="_blank" 
                    class="blueShadow mx-auto text-md md:text-lg poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
                >
                    <div class="absolute top-0 right-full w-full h-full bg-blue-600 opacity-20 group-hover:translate-x-full duration-200"></div>
                    <h4 class="relative z-9">View Résumé &rarr;</h4>
                </a>
            </div>
    </section>
</main>