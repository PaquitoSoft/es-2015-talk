##  Enhanced objects code

<pre>
	<code data-trim>
constructor(data) {
	super({
		data,
		template: PodcastPageTemplate,
		partials: {
			podcastSidebar: PodcastSidebarPartialTemplate
		},
		defaultNavigation: false,
		domEvents: {
			'click|.podcast-sidebar a': 'navTo',
			'click|.podcast-episodes a': 'navToEpisode'
		}
	});
}

let obj = {
	name: 'Luke',
	sayHi() {
		return `Greetings from ${this.name}`;
	}
};
	</code>
</pre>