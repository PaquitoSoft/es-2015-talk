##  Variables const

<pre>
	<code data-trim>		
const PODCASTS_DATASOURCE_URL = 'https://itunes.apple.com/us/rss/toppodcasts/limit=100/genre=1310/json';
const PODCAST_CACHE_PREFIX = 'podcast-data_';
const PODCASTS_LIST_CACHE_TTL = 1440; // minutes (one day)

const CONFIG = { defaultTTl: 1440 };
console.log(CONFIG); // --> { defaultTTl: 1440 }
CONFIG.defaultTtl = 10;
console.log(CONFIG); // --> { defaultTTl: 10 }

const CONFIG = Object.freeze({ defaultTtl: 1440 });
console.log(CONFIG); // --> { defaultTTl: 1440 }
CONFIG.defaultTtl = 10;
console.log(CONFIG); // --> { defaultTTl: 1440 }
	</code>
</pre>

<aside class="notes">
	If you use _freeze_ you don't need _const_, it's useless
	Arrays can be _freezed_ so you cannot assign new values. Adding, removing throws error
</aside>