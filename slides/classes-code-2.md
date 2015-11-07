##  Classes code - II

<pre>
	<code data-trim>
class EpisodeController extends BaseController {

	constructor(data) {
		super({
			data,
			template: EpisodePageTemplate,
			partials: {
				podcastSidebar: PodcastSidebarPartialTemplate
			}
		});
	}

}
	</code>
</pre>

<aside class="notes">
	Don't forget to mention 'static' functions (promises code-1)
</aside>