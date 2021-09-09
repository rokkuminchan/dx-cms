<script context='module'>
  export const load = async function ({ page, fetch, session, context }) {
    const data = await import('$lib/data/blogs/{blogId}.json');

    return { props: { data: data.default } };
  };
</script>

<script>
  import BlogDetailPageContent from '$lib/components/blogDetail/blogDetailPageContent.svelte';

  export let data;
</script>

<BlogDetailPageContent {data} />