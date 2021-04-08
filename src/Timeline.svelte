<script>
	export let student;
	export let baseUrl;
</script>

<main>
	<div class="container">
		<div class="gallery">
            {#each student.anecdotes as anecdote}
			<div class="gallery-item" tabindex="0">
				<img src="{baseUrl}{anecdote.Photo.formats.thumbnail.url}" class="gallery-image" alt="">
				<div class="gallery-item-info">
					<ul>
						<li class="gallery-item-likes"><span class="visually-hidden">Likes:</span><i class="fas fa-heart" aria-hidden="true"></i> 56</li>
						<li class="gallery-item-comments"><span class="visually-hidden">Comments:</span><i class="fas fa-comment" aria-hidden="true"></i> 2</li>
					</ul>
				</div>
			</div>
            {/each}
		<!-- End of gallery -->
        {#if !student.anecdotes}
		<div class="loader"></div>
        {/if}
	</div>
	<!-- End of container -->
</main>