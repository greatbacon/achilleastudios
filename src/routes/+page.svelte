<script>	
	import bandana from '$lib/images/dog_bandanas.jpg'
	import quilt from '$lib/images/quilt.jpg'
	import clothes from '$lib/images/upcycled_clothes.jpg'
</script>

<!-- TODO add images & spin up new email-->
<div class="offerings">	
	<a class="tile" href="/quilts">
		<img class="image" src={quilt} alt="a quilt drapped over a fence" />
		<div>
			QUILTS
		</div>
	</a>
	<a class="tile" href="/bandanas">
		<img class="image" src={bandana} alt="a quilt drapped over a fence" />
		<div>
			DOG BANDANAS
		</div>
	</a>
	<a class="tile" href="/upcycled">
		<img class="image" src={clothes} alt="a quilt drapped over a fence" />
		<div>
			UPCYCLED CLOTHES
		</div>
	</a>
</div>

<style>
	.offerings {
		font-size: 3rem;
		display: flex;
		justify-content: center;		
		height: 50%;
		flex-wrap: wrap;
	}

	.tile {
		padding-top: 1rem;
		margin: 0.25em;
		text-align: center;
		height: 18rem;
		width: 15rem;
		border : 5px solid black;
		border-radius: 25px;
	}

	.image {
		width: 10rem;
	}
</style>