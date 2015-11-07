##  Promises code - I

<pre>
	<code data-trim>
static findById(podcastId) {
	let cacheKey = PODCAST_CACHE_PREFIX + podcastId,
		podcast = lscache.get(cacheKey);

	if (podcast) {
		return Promise.resolve(podcast);
	} else {
		return new Promise(function(resolve, reject) {
			getPodcastLite(podcastId)
				.then(fetchPodcastFeedUrl)
				.then(fetchPodcastEpisodes)
				.then(function(data) {
					lscache.set(cacheKey, data, PODCAST_DETAIL_CACHE_TTL);
					resolve(data);
				})
				.catch(reject);
		});
	}
}
	</code>
</pre>