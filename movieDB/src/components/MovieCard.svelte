<script>
    export let movie;
</script>
<div class="movie-card">
    <a sveltekit:noscroll sveltekit:prefetch href={'/movie/' + movie.id}>
        <img src={'https://image.tmdb.org/t/p/w500' + movie.poster_path} alt={movie.title} />
    </a>
    <!--<img src={'https://image.tmdb.org/t/p/w500' + movie.backdrop_path} alt=""/> -->
    <div class="description">
        <h2>{movie.title}</h2>
        <p>{movie.release_date}</p>
    </div>
    <div>{movie.vote_average} - Based on {movie.vote_count} votes.</div>
</div>



<style>
    img {
        width: 100%;
        height: 40vh;
        object-fit: cover;
        border-radius: 1rem;
        margin-bottom: 1rem;
    }

    h2 {
        font-size: 0.9rem;
    }
    .description {
        height: 5vh;
    }
    p {
        font-size: 0.7rem;
    }
</style>

