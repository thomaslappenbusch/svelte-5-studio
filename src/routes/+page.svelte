<script lang="ts">

	import { ArrowRight, ChartColumnIncreasing, Check, Code, DollarSign, Ellipsis, ExternalLink, Folder, Handshake, Package, Paintbrush, Pen, Search, Triangle, User } from "lucide-svelte";
    import { fade } from "svelte/transition";

    let isModalOpen:any = $state(false)
    let modalState:any = $state();

    function modifyModal(modalState:any) {

    }
</script>

<!-- svelte-ignore a11y_no_static_element_interactions -->
{#if isModalOpen}
    <!-- svelte-ignore a11y_click_events_have_key_events -->
    <div onclick={() => isModalOpen == false} transition:fade={{duration:300}} class="fixed h-screen w-screen bg-black/20 backdrop-blur-[2px] z-10">

    </div>
    <div class="flex items-center justify-center h-screen w-screen bg-transparent fixed z-20">
        <div class="w-[400px] h-[300px] bg-zinc-200 rounded-md border border-zinc-300 flex flex-col p-4">
            <div class="flex justify-between">
                <div>Let's call today</div>
            </div>
        </div>
    </div>
{/if}

<div class="sm:h-[calc(100vh-80px)] w-full max-w-[1600px] px-8 flex items-center justify-center z-0 sm:pb-[10vh] relative">
    <!-- <div class="absolute bottom-2 flex items-center justify-center">
        <div class="flex items-center mt-6 mb-2 space-x-24">
            <img src="clutchMaps.svg" class="h-5 opacity-50 hover:opacity-100 grayscale hover:grayscale-0 transition cursor-pointer"/>
            <img src="blue_coderprep.svg" class="h-5 opacity-50 hover:opacity-100 grayscale hover:grayscale-0 transition cursor-pointer"/>
            <img src="virlo.svg" class="h-5 opacity-50 hover:opacity-100 grayscale hover:grayscale-0 transition cursor-pointer"/>
            <img src="creatorcontact.png" class="h-10 opacity-50 hover:opacity-100 grayscale hover:grayscale-0 transition cursor-pointer"/>
        </div>
    </div> -->
    <div class="flex flex-col justify-between items-center w-full">
        <!-- Left side with text content -->
        <div class="flex flex-col items-start justify-start w-full sm:pr-32 mt-[10vh] sm:-mt-[3vh]">
            <!-- <div class="rounded-full border border-green-400 text-green-800 mr-auto py-[2px] px-2 text-xs flex items-center bg-gradient-to-b from-green-100 to-green-200">
                <div class="h-1.5 w-1.5 bg-green-400 animate-pulse rounded-full mr-1.5"></div>
                Open for new projects
            </div> -->
            <div class="uppercase text-xs font-semibold text-zinc-400 mb-1">
                OPEN TO WORK
            </div>
            <div class="tracking-tighter text-5xl sm:text-7xl font-medium antialiased">We Develop Svelte Web Apps</div>
            <div class="mt-6 gap-y-5 text-sm sm:text-xl text-zinc-900 leading-7 max-w-[700px]">
                Built with 
                <span class="inline-flex items-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" class="mr-1.5 text-[rgb(62,207,142)]">
                    <path fill="currentColor" d="M3.084 15.25c-1.664 0-2.6-1.912-1.58-3.226L10.21.806C10.794.054 12 .466 12 1.42v7.33h8.916c1.663 0 2.6 1.912 1.58 3.226L13.79 23.194c-.584.752-1.79.34-1.79-.613V15.25z" />
                </svg>
                <span class="text-[rgb(62,207,142)] mr-[1px] font-medium">Supabase</span>
                </span> 
                and 
                <span class="inline-flex items-center align-middle">
                <svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" class="mr-[3px] text-[rgb(14,165,233)]">
                    <path fill="currentColor" d="M12 6c-2.67 0-4.33 1.33-5 4c1-1.33 2.17-1.83 3.5-1.5c.76.19 1.31.74 1.91 1.35c.98 1 2.09 2.15 4.59 2.15c2.67 0 4.33-1.33 5-4c-1 1.33-2.17 1.83-3.5 1.5c-.76-.19-1.3-.74-1.91-1.35C15.61 7.15 14.5 6 12 6m-5 6c-2.67 0-4.33 1.33-5 4c1-1.33 2.17-1.83 3.5-1.5c.76.19 1.3.74 1.91 1.35C8.39 16.85 9.5 18 12 18c2.67 0 4.33-1.33 5-4c-1 1.33-2.17 1.83-3.5 1.5c-.76-.19-1.3-.74-1.91-1.35C10.61 13.15 9.5 12 7 12" />
                </svg>
                <span class="text-[rgb(14,165,233)] font-medium">Tailwind v4</span>
                </span>. Let's chat today and see what we can do for you, no project is too large or too small.
            </div>
            
            <div class="flex items-center mt-6 space-x-2">
               <button class="bg-[#272729] text-white rounded-full px-5 py-2.5">Book a free call</button>
               <button class="bg-white text-black border border-zinc-300 px-5 py-2.5 flex items-center rounded-full">
                    View development options
                    <ExternalLink class="ml-1 h-4" strokeWidth={1.5}/>
                </button>
            </div>
        </div>
        
        <div class="sm:flex sm:flex-row flex-col space-y-12 items-start gap-3 w-full sm:h-[20vh] sm:min-h-[230px] mt-16">
            <div class="rounded-sm sm:w-1/3 h-[300px] sm:h-full hover:from-yellow-300 cursor-pointer  bg-gradient-to-bl from-zinc-200 to-zinc-300 group transition  duration-500 flex flex-col relative overflow-hidden">
                <div class="grow m-4 flex flex-col mx-auto justify-center space-y-3 l mt-4 mb-4 relative">
                    <img src="virlo.svg" class=" w-48 opacity-90"/>
                </div>
                <div class="flex flex-col justify-between items-end mt-auto p-4 pt-0 text-black">
                    <div class="flex justify-between items-end mt-auto pt-0 text-black">
                        <div class="tracking-tight flex flex-col">
                            SAAS Projects
                            <div class="text-sm -pb-[6px] pr-3 pt-[2px] text-zinc-700 font-medium sm:h-0 sm:opacity-0 group-hover:h-10 group-hover:opacity-100 transition-all duration-300">
                                We are not an agency, you will have the direct contact information of each person.
                            </div>
                        </div>
                        <ArrowRight strokeWidth={2} class="p-[3px]  group-hover:-rotate-45 group-hover:bg-zinc-300 transition duration-500  shrink-0 rounded-full border bg-zinc-100/20 border-black/30"/>
                    </div>
                </div>
            </div>
            <div class="rounded-sm sm:w-1/3 h-[300px] sm:h-full cursor-pointer group bg-gradient-to-br hover:from-blue-300  from-zinc-200 to-zinc-300 transition duration-500 flex flex-col relative overflow-hidden group">
                <div class="grow m-4 flex items-center justify-center mt-8 mb-4 px-3">
                    <img src="mapbox.png" class=" w-48 opacity-90"/>
                </div>
                <div class="flex flex-col justify-between items-end mt-auto p-4 pt-0 text-black">
                    <div class="h-4 w-full">
                    </div>
                    <div class="flex justify-between items-end mt-auto pt-0 text-black">
                        <div class="tracking-tight flex flex-col">
                            Mapping Projects
                            <div class="text-sm -pb-[3px] pr-3 pt-[2px] text-zinc-700 font-medium sm:h-0 sm:opacity-0 group-hover:h-10 group-hover:opacity-100 transition-all duration-300">
                                We are profficent at Mapbox, and can help create incredible mapping projects with ease.
                            </div>
                        </div>
                        <ArrowRight strokeWidth={2} class="p-[3px] group-hover:bg-zinc-300 transition duration-500  shrink-0 rounded-full border bg-zinc-100/20 border-black/30 group-hover:-rotate-45"/>
                    </div>
                </div>
            </div>
            <div class="rounded-sm sm:w-1/3 h-[300px] sm:h-full hover:from-purple-300 cursor-pointer  bg-gradient-to-tr from-zinc-200 to-zinc-300 group transition  duration-500 flex flex-col relative overflow-hidden">
                <div class="grow m-4 flex flex-col mx-auto justify-center space-y-3 l mt-8 mb-4 relative">
                    <img src="blue_coderprep.svg" class=" w-48 opacity-90"/>
                </div>
                <div class="flex flex-col justify-between items-end mt-auto p-4 pt-0 text-black">
                    <div class="flex justify-between items-end mt-auto pt-0 text-black">
                        <div class="tracking-tight flex flex-col">
                            Educational Tech Projects
                            <div class="text-sm -pb-[6px] pr-3 pt-[2px] text-zinc-700 font-medium sm:h-0 sm:opacity-0 group-hover:h-10 group-hover:opacity-100 transition-all duration-300">
                                We are not an agency, you will have the direct contact information of each person.
                            </div>
                        </div>
                        <ArrowRight strokeWidth={2} class="p-[3px]  group-hover:-rotate-45 group-hover:bg-zinc-300 transition duration-500  shrink-0 rounded-full border bg-zinc-100/20 border-black/30"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>