##  Modules code - II

<pre>
	<code data-trim>
// models/podcast.js
class Podcast {
	...
}

export default Podcast;

// config/routes.js
import PodcastModel from '../models/podcast';

{
	path: '/',
	handler: function homePageController() {
		return new Promise((resolve, reject) => {
			PodcastModel.findAll()
				.then(function(data) {
					...
				})
				.catch(reject);
		});
	}
}
	</code>
</pre>