

  <script>






/*================open & close===================*/
   let displayElement = false;
    
    function toggleElement() {
      displayElement = !displayElement;
    }




    import { onMount } from 'svelte';

let message = '';
let typedMessage = '';

const typeSpeed = 200; // in milliseconds
const originalMessage = 'Faruq Elediko';

onMount(() => {
  typeMessage(originalMessage);
});

function typeMessage(msg) {
  if (!msg) return;

  message = msg;
  typedMessage = '';

  let i = 0;
  const intervalId = setInterval(() => {
    typedMessage += message[i];
    i++;

    if (i >= message.length) {
      clearInterval(intervalId);
      setTimeout(() => {
        typeMessage(msg); // retype after 5 seconds
      }, 3000);
    }
  }, typeSpeed);
}





    
    
  </script>
  
  
  
   
  
  
  
  
<html lang="en">
<head>

    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>

</head>
<body class=" scroll-smooth">




        <nav class=" shadow-md bg-white flex justify-between items-center h-[5rem] px-[1rem] fixed w-full md:px-[2rem] lg:px-[6rem] z-50">

            <a href="#slow">
                <div class="logo">
                    <h4 class=" rounded-[50%] font-bold p-2 h-10 w-10  text-white bg-gradient-to-r from-cyan-500 to-teal-500 lg:font-bold lg:w-12 lg:h-12 lg:p-3">F.E</h4>
                </div>
            </a>
    
           
           
            
           <div>
                <ul id="element" class:show={displayElement} class:return={!displayElement}  class="flex flex-col text-center  font-medium h-full gap-[2rem] pt-[4rem] bg-teal-500 fixed top-[5rem] w-0 right-0  text-slate-700  lg:text-slate-700 lg:flex-row  lg:relative lg:pt-0 lg:top-0 lg:gap-[3rem] lg:items-center lg:bg-transparent lg:h-full ">
                    <li class="after:bg-white lg:after:bg-cyan-500 after:w-0 after:left-0 after:h-[.1rem] after:flex after:hover:w-full transition-all after:delay-400 after:duration-300 after:hover:left-full"><a href="#slow">Home</a></li>
                    <li class="after:bg-white  lg:after:bg-cyan-500 after:w-0 after:left-0 after:h-[.15rem] after:flex after:hover:w-full transition-all after:delay-400 after:duration-300 after:hover:left-full"><a href="#about">About</a></li>
                    <li class="after:bg-white  lg:after:bg-cyan-500 after:w-0 after:left-0 after:h-[.15rem] after:flex after:hover:w-full transition-all after:delay-400 after:duration-300 after:hover:left-full"><a href="#experience">Experiecnce</a></li>
                    <li class="after:bg-white  lg:after:bg-cyan-500 after:w-0 after:left-0 after:h-[.1rem] after:flex after:hover:w-full transition-all after:delay-400 after:duration-300 after:hover:left-full"><a href="#contact">Contact</a></li>
                    <li><a class=" border-[.01rem]  border-white text-white lg:bg-gradient-to-r from-cyan-500 to-teal-500 px-[1rem] py-[0.5rem] rounded-md -all hover:translate-y-[-.5rem] duration-400 delay-300 hover:from-teal-500 hover:to-cyan-500 lg:ml-[8rem]" download href="">Resume</a></li>
                </ul>
           </div>
    
    
          
    
           
    
    
            <div class="cursor-pointer lg:hidden border-none outline-none">
                <button on:click={toggleElement}>
                    {#if !displayElement}
                    <i class='bx bx-menu open-bar rounded-[30%] p-2 text-white bg-gradient-to-r from-cyan-500 to-teal-500'></i>
                    {:else}
                    <i class=' bx bx-x close-bar h rounded-[30%] p-2 text-white bg-gradient-to-r from-cyan-500 to-teal-500'></i>
                    {/if}
                </button>
            </div>
    
        </nav>
    
    
        <div class="social-media">
            <ul class="fixed bottom-1 left-[2rem] right-[2rem] lg:left-[4rem] lg:right-[4rem] rounded-full text-[1.2rem] py-[0.7rem] flex justify-center items-center gap-[2rem] lg:gap-[4rem] lg:text-2xl text-white bg-gradient-to-r from-cyan-500 to-teal-500 z-40">
                <li class="transition:all hover:scale-125 delay-450"><a href="https://twitter.com/EledikoDcoder"target="_blank" rel="noopener noreferrer"><i class='bx bxl-twitter' ></i></a></li>
                <li class="transition:all hover:scale-125 delay-450"><a href="https://www.instagram.com/eledikofaruq/"target="_blank" rel="noopener noreferrer"><i class='bx bxl-instagram' ></i></a></li>
                <li class="transition:all hover:scale-125 delay-450"><a href="https://www.linkedin.com/in/Faruq Elediko/" target="_blank" rel="noopener noreferrer"><i class='bx bxl-linkedin'></i></a></li>
                <li class="transition:all hover:scale-125 delay-450"><a href="https://github.com/EledikoDcoder" target="_blank" rel="noopener noreferrer"><i class='bx bxl-github'></i></a></li>
            </ul>
        </div>
    
    
    
        <header id="slow" class="pt-[9rem] lg:pt-[6rem] pb-[7rem] text-center px-[2rem] md:px-[2.5rem] md:flex md:justify-center md:items-center lg:px-[6rem] lg:w-full">
    
            <div class="header-top md:pt-[6rem] lg:text-left lg:w-[50%]">
                <span class="text-slate-700 text-lg font-serif">Hello, my name is</span>
                <h1 class=" font-serif text-teal-500 font-extrabold text-[2rem] lg:text-5xl">{typedMessage}</h1>
                <p class="pt-[1rem] text-slate-700  font-serif lg:w-[90%]">
                    I am a skilled and motivated front-end developer who is committed to delivering top-quality
                    results, and am excited to contribute my skills and experience to new projects and teams.
                </p>
    
    
                <div class="btn-1 pt-[2rem] flex justify-center items-center gap-5 lg:justify-start">
                    <a class=" text-white bg-gradient-to-r from-cyan-500 to-teal-500 px-[1rem] py-[0.5rem] rounded-md -all hover:translate-y-[-.5rem] duration-400 delay-300 hover:from-teal-500 hover:to-cyan-500" href="">My Resume</a>
                    <a class=" text-slate-700 px-[1rem] py-[0.5rem] border-[.1rem]  border-teal-500 rounded-md transition-all hover:translate-y-[-.5rem] duration-400 delay-300 " href="#contact">Let's talk</a>
                </div>
            </div>
    
           
    
            
   
            <div class="header-bottom lg:pt-[7rem] pt-[5rem] md:w-[100%] lg:w-[50%]">
                <img src="/prog-r.png" alt="">
            </div>
           
    
        </header>



    <section id="about" class="px-[1rem] md:px-[2rem] lg:px-[6rem] pt-[2rem]">
        <h2 class="font-extrabold text-lg text-center text-slate-700 pb-[2rem]">About Me</h2>
        <h3  class=" text-teal-600 font-bold text-[1rem] pb-[1rem]">Frontend Developer</h3>
        <p class="leading-7  font-serif pb-[2rem] text-slate-700">I am a versatile and experienced Frontend Developer, with a wealth of kwnoledge in
           Codeside Academy. My portfolio is as sample of my work, demonstrating my skills and
           my ability to deliver results. I am always looking for new opportunities to learn,
           grow and to push the boundaries of what is possible.  I also build a responsive website
           for your business growth make the it more & more interactive with web animations.A responsive
           design makes your website accessible to all users, regardless of their devices.
        </p>
        <a class=" text-white bg-gradient-to-r from-cyan-500 to-teal-500 px-[1rem] py-[0.5rem] hover:text-slate-700 rounded-md transition-all hover:bg-none duration-400 delay-300 border-[.1rem] border-cyan-500" href="#contact">Let's talk</a>
    </section>



    <section id="experience" class=" px-[1rem] py-[7rem] md:px-[2rem] lg:px-[6rem]">
        <h3 class=" font-extrabold text-lg text-center text-slate-700 pb-[2rem]">Skills</h3>
        <div class="flex gap-[2rem] flex-col  font-serif px-[4rem] text-slate-800 md:flex-row md:px-[0] md:grid-2 md:grid md:grid-cols-2 lg:grid-cols-3">
            <div class=" shadow-xl flex flex-col items-center justify-center ] p-[1.5rem] rounded-lg gap-[.5rem]">
                <img class="w-[25%]" src="html-removebg-preview.png" alt="">
                <span class=" text-3xl">HTML</span>
                <p class=" text-teal-500 text-xl font-medium">Proficient</p>
            </div>
            <div class="  shadow-xl flex flex-col items-center justify-center   p-[2rem] rounded-lg gap-[.5rem]">
                <img class="w-[25%]" src="css-removebg-preview.png" alt="">
                <span class=" text-3xl">CSS</span>
                <p class=" text-teal-500 text-xl font-medium">Expert</p>
            </div>
            <div class="  shadow-xl flex flex-col items-center justify-center  p-[1.5rem] rounded-lg gap-[.5rem]">
                <img class="w-[25%]" src="svelte-removebg-preview.png" alt="">
                <span class=" text-3xl">SvelteKit</span>
                <p class=" text-teal-500 text-xl font-medium">Expert</p>
            </div>
            <div class="  shadow-xl flex flex-col items-center justify-cente p-[1.5rem] rounded-lg gap-[.5rem]">
                <img class="w-[60%]" src="tailwindcss-removebg-preview.png" alt="">
                <span class=" text-3xl">TailwindCSS</span>
                <p class=" text-teal-500 text-xl font-medium">Proficient</p>
            </div>
            <div class="  shadow-xl flex flex-col items-center justify-center  p-[1.5rem] rounded-lg gap-[.5rem]">
                <img class="w-[25%]" src="git-removebg-preview.png" alt="">
                <span class=" text-3xl">GitHub</span>
                <p class=" text-teal-500 text-xl font-medium">Experience</p>
            </div>
        </div>

        <h2 class="font-extrabold text-lg text-center text-slate-700 pb-[2rem] pt-[3rem]">Experience</h2>
        <h3 class=" text-teal-600 font-bold text-[1rem] pb-[1rem]">@ Codeside Academy >>>></h3>
        <ul class=" list-disc px-[1rem] text-slate-700">
            <li>Collaborated with senior developers to create and maintain web applications using HTML, CSS, and JavaScript</li>
            <li>Assisted with the design and implementation of user-friendly and responsive interfaces, utilizing popular front-end frameworks such as SvelteKit and TailwindCSS</li>
            <li>Conducted careful testing to ensure cross-browser compatibility and optimal performance</li>
            <li>Contributed to team code reviews and actively sought out feedback to improve technical skills</li>
            <li>Actively participated in daily stand-up meetings and sprint planning sessions</li>
        </ul>
       
        
    </section>


    <section id="contact" class=" px-[1rem] py-[5rem] text-slate-800">
        <h2 class="font-extrabold text-lg text-center pb-[2rem]">Contact Me</h2>

        <div class="flex flex-col items-center justify-center gap-[1rem] pb-[2rem] md:flex-row md:gap-[3rem]">
            <div class="flex items-center gap-[.5rem]">
                <span class="text-green-500 text-2xl"><i class='bx bxl-whatsapp'></i></span>
                <p class=" cursor-pointer flex items-center justify-center">
                    <a href="https://wa.me/2348068254048"  target="_blank">2348068254048</a>
                    <a class=" text-white bg-gradient-to-r from-cyan-500 to-teal-500 px-[1rem] py-[0.5rem] hover:text-slate-700 rounded-md transition-all hover:bg-none duration-300 delay-300 border-[.1rem] ml-4 border-cyan-600" href="https://wa.me/2348068254048"  target="_blank">let's chat</a>
                    
                </p>
            </div>
            <div class="flex items-center gap-[.5rem]">
                <span class="text-blue-500 text-2xl"><i class='bx bx-envelope'></i></span>
                <p class=" cursor-pointer"> 
                    eledikofaruq@gmail.com
                </p>
            </div>
        </div>


        <div class=" md:flex md:px-[2rem] md:justify-center md:items-center md:gap-[4rem] lg:px-[6rem] lg:gap-[6rem]">
            <div class="flex flex-col items-center justify-center gap-[1rem] lg:w-[50%]">

                <img src="contact-img.png" alt="">
                <p class=" font-serif">If you have questions or just want to get in touch,use the form below. I look forward to hear from you</p>
             </div>
             <div class="flex flex-col bg-gradient-to-r from-cyan-500 to-teal-500 rounded-xl p-[2rem] gap-[1rem] mt-[2rem] md:p-[2rem] lg:w-[50%] lg:p-[3rem]">
                <h3 class=" text-center text-lg font-semibold pb-[1rem]">Get in touch</h3>
                <input type="text" placeholder="First name" required class=" py-[.4rem]  px-[.9rem] placeholder:font-mono font-mono rounded-xl border-none outline-none text-slate-600">
                <input type="text" placeholder="Surname" required class=" py-[.4rem]  px-[.9rem] rounded-lg border-none outline-none font-mono placeholder:font-mono  text-slate-600">
                <input type="email" placeholder="Your email" required class=" py-[.4rem]  px-[.9rem] rounded-lg border-none outline-none placeholder:font-mono font-mono  text-slate-600">
                <textarea cols="20" rows="5" placeholder="Your questions..." required class=" py-[.4rem]  px-[.9rem] rounded-lg border-none outline-none placeholder:font-mono font-mono  text-slate-600"></textarea>
                <button class="text-lg px-[1rem] py-[.3rem] border-[.1rem] mx-[4rem]  rounded-md mt-[1rem] coutline-none transition-all hover:text-white delay-400 hover:-translate-y-2" type="submit"> Submit</button>
             </div>
        </div>
    </section>






    <section>
            <div class=" px-[1rem] font-serif flex items-center justify-center py-[.5rem] text-lg text-cyan-900 border-t-cyan-900 border-b-teal-900 border-[.1rem] mb-[3.5rem] lg:mb-[4rem] ">
                <small>Let's connect and create something great together.<i class="bx bxs-heart bx-tada"></i></small>
            </div>
    </section>
</body>
</html>


<style>
    *{
        outline: none;
        box-sizing: border-box;
    }
    body{
        font-family: sans-serif;
    }

   

   


 

    #element {
      animation-duration: 0.4s;
      animation-timing-function: ease;
      animation-fill-mode: forwards;
    }
    
    .show {
      animation-name: show-element;
    }
    
    .return {
      animation-name: return-element;
    }
    
    @keyframes show-element {
        0%{
                width: 0;
            }
            100%{
                width: 60%;
            }
        }
    
    @keyframes return-element {
        0%{
                width: 60%;
            }
            100%{
                width: 0;
            }
        }





 

       
       







        #slow{
        animation: slow 5s;
        animation-timing-function: ease;
        animation-duration: 5s;
    }
        
        @keyframes slow{
            0%{
                transform: translatey(-100%);
            }
            100%{
                transform: translatey(0%);
            }
        }

</style>