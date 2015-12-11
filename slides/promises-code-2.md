##  Promises Code - II

<pre style="width: 100%;">
	<code data-trim>
{
	path: '/podcast/:podcastId',
	handler: function podcastDetailHandler(context) {
		return new Promise((resolve, reject) => {
			PodcastModel.findById(context.params.namedParams.podcastId)
				.then(function(data) {
					resolve({
						Controller:PodcastPageController, 
						data: {
							podcast: data
						}
					});
				})
				.catch(reject);
		});
	}
}
	</code>
</pre>