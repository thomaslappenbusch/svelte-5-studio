<script>

	import { ExternalLink } from "lucide-svelte";

</script>
<div class="w-full max-w-[1000px] px-8 flex flex-col items-center justify-center z-0 sm:pb-[10vh] relative space-y-12 mt-4">
    {#each Array(3) as _, i}
        <div class="w-full rounded-md flex flex-col p-5">
            <div class="flex items-center justify-between">
            <div class="text-2xl mb-5">
                Logo Placeholder
            </div>
            <div class="text-sm mb-5">
                Detail Placeholder
            </div>
            </div>
            <div class="aspect-video bg-zinc-300 w-full rounded-md">
            </div>
            <div class="text-lg mt-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut aliquet dui sit amet dolor tristique molestie. Phasellus pulvinar nibh ipsum. Suspendisse scelerisque suscipit sapien, gravida hendrerit tortor sodales eget. Aenean varius ligula gravida felis luctus, sit amet ornare erat sagittis.
            </div>
            <div class="flex items-center space-x-3 ml-auto mt-5">
            <button class="bg-zinc-600 p-2 rounded-md text-white">Github</button>
            <button class="bg-zinc-600 p-2 rounded-md text-white flex items-center">Go to website
                <ExternalLink/>
            </button>
            </div>
        </div>
        <div class="w-full h-[1px] bg-zinc-200"></div>
    {/each}
</div>