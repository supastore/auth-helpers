<script lang="ts">
	import type { PageData } from './$types';

	export let data: PageData;
	$: ({ user } = data);
</script>

<p>
	[<a href="/">Home</a>] | [<a href="/protected-page">supabaseServerClient</a>]
</p>

<div>Hello {user.email}</div>
<pre>{JSON.stringify(user, null, 2)}</pre>
