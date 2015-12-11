##  Template strings code - I

<pre>
	<code data-trim>
function fetchPodcastFeedUrl(podcast) {
	return new Promise(function(resolve, reject) {
		ajax.getJsonp(`${PODCAST_ID_DATASOURCE_URL}?id=podcast.id`)
			.then(function(data) {
				if (data.results.length) {
					podcast.feedUrl = data.results[0].feedUrl;
					resolve(podcast);
				} else {
					reject(new Error('No feed Url found for podcast: ' + podcast.id));
				}
			})
			.catch(reject);
	});
}

function foo() { return 42; }
console.log(`The meaning of life is: ${foo()}`);
	</code>
</pre>