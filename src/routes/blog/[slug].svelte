<script context="module">
    import blogContent from './blogContent.js'
    export async function load(ctx){
        let slug = ctx.page.params.slug
        let content = {...blogContent.find(post => post.slug === slug)}.content
        console.log(content)
        return { props: {slug, content} }
    }
</script>

<script>
    export let slug
    export let content

    console.log(content)

</script>

<h1>
    {slug}
</h1>

<div>
    {@html content}
</div>

