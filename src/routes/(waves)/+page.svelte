<script lang="ts">
    import About from '$lib/components/organisms/About.svelte';
    import RecentPosts from '$lib/components/organisms/RecentPosts.svelte';
    import type { Feature, BlogPost } from '$lib/utils/types';

    export let data: {
        features: Feature[];
        posts: BlogPost[];
    };

    let { posts } = data;
</script>

<!-- Landing Page Container -->
<div class="landing-container">
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="cta-buttons">
                <img src="/images/gpt.png" height="70" width="70"  class="circle-image" />
                <h1 class="hero-title">جی پی تی پلاس</h1>
                
             
            </div>

            <!-- <p class="hero-subtitle">هر کاری داری به هوش مصنوعی بگو</p> -->
            
            <p class="hero-subtitle"></p>
            <div class="cta-buttons">
                <a href="https://cafebazaar.ir/app/com.gpt.gpt_plus">
                    <img src="/images/bazar.svg" alt="Get it on Google Play" class="download-image" />
                </a>
                <a href="https://sibapp.com/applications/GPTPlus?from=collection">
                    <img src="/images/sibapp.svg" alt="Download on the App Store" class="download-image" />
                </a>
            </div>
        </div>
    </section>

    <!-- Blog Posts Section -->
    <section class="blog-posts">
        <h2 class="section-title">Latest Posts</h2>
        {#if posts && posts.length > 0}
            <RecentPosts {posts} />
        {/if}
    </section>
</div>

<!-- Style Section -->
<style>
    :global(body) {
        margin: 0;
        font-family: 'Roboto', sans-serif;
        background-color: #f9f9f9;
    }

    .landing-container {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }

    /* Hero Section Styling */
    .hero {
        background-color: #1b1e23;
        color: white;
        padding: 100px 20px;
        width: 100%;
    }

    .hero-content {
        max-width: 900px;
        margin: 0 auto;
    }

    .hero-title {
        font-size: 2.5rem;
        font-weight: 700;
        margin-bottom: 20px;
    }

    .hero-subtitle {
        font-size: 1.2rem;
        margin-bottom: 40px;
    }

    .cta-buttons {
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    .download-button {
        padding: 15px 30px;
        border-radius: 25px;
        font-size: 1rem;
        color: white;
        text-decoration: none;
        background-color: #ff6f61;
        transition: background-color 0.3s ease;
    }

    .download-button:hover {
        background-color: #ff4f41;
    }

    .google-play {
        background-color: #4CAF50;
    }

    .app-store {
        background-color: #007bff;
    }

    /* Features Section */
    .features {
        padding: 60px 20px;
        background-color: #ffffff;
        width: 100%;
    }

    .section-title {
        font-size: 2rem;
        margin-bottom: 20px;
        color: #333;
    }

    .features-content {
        max-width: 800px;
        margin: 0 auto;
    }

    /* Blog Posts Section */
    .blog-posts {
        padding: 60px 20px;
        background-color: #f3f3f3;
        width: 100%;
    }

    .blog-posts .section-title {
        margin-bottom: 30px;
    }
    .circle-image {
          border-radius: 30%;
        }
    /* General Styles */
    @media (max-width: 768px) {
        .hero-title {
            font-size: 2rem;
        }

        .hero-subtitle {
            font-size: 1rem;
        }

        .download-button {
            font-size: 0.9rem;
        }

        .cta-buttons {
            flex-direction: column;
        }
    
    }
</style>
