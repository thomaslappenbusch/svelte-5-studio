<div class="w-full max-w-[900px] px-8 flex flex-col items-center justify-center z-0 sm:pb-[10vh] relative space-y-5 mt-4">
    <div class="text-lg w-full py-3 font-medium border-b border-t border-y-zinc-200">Recent Posts</div>
    {#each Array(3) as _, i}
        <div class="flex items-center justify-center border border-zinc-300 rounded-md overflow-hidden">
            <img src="favicon.png" class="rounded-md rounded-r-none bg-zinc-400 h-full object-fill"/>
            <div class="w-full flex flex-col overflow-hidden pl-3">
                <div class="flex items-center justify-between">
                    <div class="text-2xl">
                        Title
                        <div class="text-sm">
                            Subtitle
                        </div>
                    </div>
                </div>
                <div class="text-lg line-clamp-2">
                    Description Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut aliquet dui sit amet dolor tristique molestie. Phasellus pulvinar nibh ipsum. Suspendisse scelerisque suscipit sapien, gravida hendrerit tortor sodales eget. Aenean varius ligula gravida felis luctus, sit amet ornare erat sagittis.
                </div>
            </div>
        </div>
    {/each}
</div>