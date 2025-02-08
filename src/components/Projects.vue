<template lang="">
    <div class="flex flex-col px-10">
        <div v-if="showProjects"
            class="flex section font-Josefin min-h-[500px] min-w-[1000px] mt-10 rounded-xl p-4 bg-[#1679AB] w-full text-white "
            data-aos="fade-right">
            <div class="flex flex-row items-center w-full">
                <video src="../assets/Cvbuilder.mp4" autoplay loop
                    class="rounded-2xl max-w-[800px] max-h-[800px] flex-shrink-0">
                </video>
                <div class="flex flex-col min-w-[350px] h-full px-52 items-center mt-8">
                    <h1 class="p-2 text-2xl">CV-Builder:</h1>
                    <p class="mb-10"><i>React</i>, <i>Flask</i>, <i>MySQL</i></p>
                    <p>Intuitive interface built with React.js allows the user to enter all of their resume information
                        to 1
                        of the selected
                        popular resume templates. Using Python's Flask library, CV-Builder pulls sections of LaTeX code
                        from
                        a MySQL database
                        via REST API to insert into a text document where the appropriate sections are replaced by the
                        user's information.
                    </p>
                    <a class="text-white flex justify-center min-w-[100px] text-center h-10 items-center hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-xl focus:outline-none bg-[#36Ba98] focus:text-white active"
                        href="https://github.com/Morningstar515/CV-Builder">
                        Code
                    </a>
                </div>
            </div>
        </div>
        <div v-if="showProjects" 
            class="flex section font-Josefin min-h-[500px] min-w-[1000px] mt-10 rounded-xl p-4 bg-[#1679AB] w-full text-white"
            data-aos="fade-left" data-aos-offset="200">
            <div class="flex flex-row items-center w-full">
                <video src="../assets/Cvbuilder.mp4" autoplay loop class="rounded-2xl max-w-[800px] max-h-[800px]">
                </video>
                <div class="flex flex-col min-w-[350px] h-full px-52 items-center mt-8">
                    <h1 class="p-2 text-2xl">Warcraft Raid Bingo</h1>
                    <p class="mb-10"><i>Vue</i>, <i>Spring-Boot</i>, <i>MySQL</i></p>
                    <p> Developed an online multiplayer bingo game inspired by Blizzard's game World of Warcraft. Built with a dynamic Vue.js user interface
                        and Spring-Boot backend, this game facilitates game rooms supporting 40 players each while providing real time updates to player boards
                        using websockets.
                    </p>
                    <a class="text-white flex justify-center min-w-[100px] text-center h-10 items-center hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-xl focus:outline-none bg-[#36Ba98] focus:text-white active"
                        href="https://github.com/t.mains515/CV-Builder">
                        Code
                    </a>
                </div>
            </div>
        </div>
        <div v-if="showProjects" 
            class="flex section font-Josefin min-h-[500px] min-w-[1000px] mt-10 rounded-xl p-4 bg-[#1679AB] w-full text-white"
            data-aos="fade-right">
            <div class="flex flex-row items-center w-full">
                <video src="../assets/Cvbuilder.mp4" autoplay loop class="rounded-2xl max-w-[800px] max-h-[800px]">
                </video>
                <div class="flex flex-col min-w-[350px] h-full px-52 items-center mt-8">
                    <h1 class="p-2 text-2xl">CV-Builder:</h1>
                    <p class="mb-10"><i>React</i>, <i>Flask</i>, <i>MySQL</i></p>
                    <p>Intuitive interface built with React.js allows the user to enter all of their resume information
                        to 1
                        of the selected
                        popular resume templates. Using Python's Flask library, CV-Builder pulls sections of LaTeX code
                        from
                        a MySQL database
                        via REST API to insert into a text document where the appropriate sections are replaced by the
                        user's information.
                    </p>
                    <a class="text-white flex justify-center min-w-[100px] text-center h-10 items-center hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-xl focus:outline-none bg-[#36Ba98] focus:text-white active"
                        href="https://github.com/Morningstar515/CV-Builder">
                        Code
                    </a>
                </div>
            </div>
        </div>


    </div>


</template>
<script>
            import AOS from 'aos';
            import 'aos/dist/aos.css';
            export default {
                data() {
                    return {
                        showProjects: false
                    }
                },

                mounted() {
                    this.showProjects = true
                    AOS.init({
                        duration: 1000,
                        easing: 'ease-in-out',
                        once: true,
                    });

                    const sections = document.querySelectorAll("section");

                    const observerOptions = {
                        threshold: 0.4, // Trigger when 10% of the element is visible
                    };

                    const observerCallback = (entries, observer) => {
                        entries.forEach((entry) => {
                            if (entry.isIntersecting) {
                                entry.target.classList.add("visible");
                                entry.target.classList.remove("hidden");
                                observer.unobserve(entry.target); // Stop observing once it's visible
                            }
                        });
                    };

                    const observer = new IntersectionObserver(observerCallback, observerOptions);

                    sections.forEach((section) => {
                        observer.observe(section);
                    });




                },
                unmounted() {
                    this.showProjects = false
                }
            }
        </script>
        <style lang="">
        
        </style>