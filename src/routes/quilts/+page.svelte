<script>
    import {slide, fade} from 'svelte/transition'; 
    import {elasticInOut} from 'svelte/easing';		
    import quilt1 from '$lib/images/quilts/IMG_1066.jpg';
    import quilt2 from '$lib/images/quilts/IMG_1351.jpg';
    import quilt3 from '$lib/images/quilts/IMG_6734.jpg';
    import quilt4 from '$lib/images/quilts/IMG_7015.jpg';
    import quilt5 from '$lib/images/quilts/IMG_7017.jpg';
    import quilt6 from '$lib/images/quilts/IMG_9272.jpg';

    const gallery_items = [
        {
            url: quilt1,
            description: "Quilt of wavy squares, with a scrappy pallette.",
        },
        {
            url: quilt2,
            description: "Quilt of squares and trinagles, with a blue, yellow, and red color pallette.",
        },
        {
            url: quilt3,
            description: "Quilt of trinagles, with a brown and red pallette.",
        },
        {
            url: quilt4,
            description: "Quilt of trinagles, with a christmas pallette.",
        },
        {
            url: quilt5,
            description: "Quilt of arrows, with a blue, green, and red color pallette.",
        },
        {
            url: quilt6,
            description: "Quilt of trinagles, with a scrappy pallette.",
        },
    ]    
    let currentSlideItem = 0;
    $: item = gallery_items[currentSlideItem];

    const nextImage = () => {
        currentSlideItem = (currentSlideItem + 1) % gallery_items.length;
    }
    const prevImage = () => {
        if (currentSlideItem != 0) {
        currentSlideItem = (currentSlideItem - 1) % gallery_items.length;
        } else {
            currentSlideItem = gallery_items.length - 1;
        }
    }
</script>

<main class="content">
    <div class="gallery"> 
        <button class="btn" on:click={() => prevImage()}>&lt;</button>
        {#key item}
            <img class="image" in:fade|local={{duration: 400}} src={item.url} alt={item.description}/>
        {/key}                    
        <button class="btn" on:click={() => nextImage()}>&gt;</button>        
    </div>
    <div class="text">
        <p>
            I love doing commissions, and can take on ~3-4 commissions per quarter. 
            For pricing, I charge between $.20 - $.25/sq in depending on complexity of pattern, familiarity of pattern, etc, plus the cost of materials.
        </p>
        <p>
            Some of my favorite quilt patterns are from 
            <a href="https://fancytigercrafts.com/collections/sewing-pattern-sale">Fancy Tiger</a>, 
            <a href="https://suzyquilts.com/">Suzy Quilts</a>, 
            <a href="https://theblanketstatement.ca/">The Blanket Statement</a> and 
            <a href="https://www.missmake.com/">Miss Make</a>, all of which are really bold, modern patterns. 
            I also love to play around with various blocks and several of the quilts pictured above are scrappy or improvised quilts, without following a specific pattern.
        </p>

        <p>
            Some of my favorite fabric shops include <a href="https://www.fatquartershop.com/">Fat Quarter Shop</a> (I love Ruby Star Society fabrics). 
            Also, <a href="https://olliefabrics.com/">Ollie Fabrics</a> & <a href="https://www.cottoneerfabrics.com/">Cottoneer Fabrics</a> both have really great bundles of fabric for quilts, usually in combinations from several fabric designers.
        </p>
        <p>Local to Denver, I love <a href="https://www.treelotta.com/">Trelotta</a> in Englewood. 
            They have such a large selection and it's always fun to go in-person to select fabrics. 
            Right across the street is <a href="https://fancytigercrafts.com/">Fancy Tiger Crafts</a>, another Denver favorite.
        </p>
        <p>
            If you're interested in a quilt commission, <a href="/contact">send me a note and let's chat!</a>
        </p>
    </div>	
</main>

<style>
    .gallery {
        text-align: center;
    }

    .image {
        width: 350px;                
        margin: 1%;
    } 

    .content {        
        font-size: 2rem;        
    }

</style>