<script lang="ts">
    import image1 from '$lib/images/bandanas/IMG_0417.jpg';
    import image2 from '$lib/images/bandanas/IMG_7182.jpg';
    import image3 from '$lib/images/bandanas/IMG_5570.jpg';
    import image4 from '$lib/images/bandanas/IMG_9875.jpg';
    import image5 from '$lib/images/bandanas/IMG_1003.jpg';
    import image6 from '$lib/images/bandanas/IMG_9003.jpg';
	import ImageGallery from '$lib/ImageGallery.svelte';
    import type {Image} from '$lib/imageGallery';
 
    const gallery_items = [
        {
            url: image1,
            description: "A yellow lab named Yarrow, looking at the camera upside down, wearing a green and blue bandana.",
        },
        {
            url: image2,
            description: "A pointy eared mutt named Sweet Pea, wearing a yellow bandana.",
        },
        {
            url: image3,
            description: "A mop of a dog, Orzo, wearing a blue and white bandana",
        },
        {
            url: image4,
            description: "A sleepy golden retriever wearing a blue and white bandana.",
        },
        {
            url: image5,
            description: "A sweet looking bully wearing an orange bandana.",
        },
        {
            url: image6,
            description: "A svelte, black dog giving the camera the side-eye while wearing a yellow bandana.",
        },
    ] as Image[]

</script>

<main class="content">
    <ImageGallery {gallery_items} />
    <div class="text">
        <p>
            Dog bandanas are where Achillea Studios got started! 
            The dog bandanas are one-size-fits-most (works for most dogs, probably not best for XS dogs or cats). 
            I primarily sell these pieces at in-person events and spaces in Denver, but feel free to <a href="/contact">reach out</a> to see what inventory I have on hand.
        </p>
    </div>	
</main>

<style>
    .content {        
        font-size: 2rem;        
    }

</style>