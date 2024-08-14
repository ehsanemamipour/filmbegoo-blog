<script lang="ts">
import About from '$lib/components/organisms/About.svelte';
import RecentPosts from '$lib/components/organisms/RecentPosts.svelte';
import type {
    Feature,
    BlogPost
} from '$lib/utils/types';

export let data: {
    features: Feature[];
    posts: BlogPost[];
};

let {
    posts
} = data;
</script>

<div class="container">
    <About />
    {#if posts && posts.length > 0}
    <RecentPosts {posts} />
    {/if}
</div>
