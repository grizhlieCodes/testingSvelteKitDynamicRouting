<script>
    import blogContent from './blogContent'
</script>


<div class="flex flex-col mt-8">

    {#each blogContent as {slug}}
        <a class="ml-4 hover:underline" sveltekit:prefetch href="/blog/{slug}">{slug}</a>
    {/each}

</div>