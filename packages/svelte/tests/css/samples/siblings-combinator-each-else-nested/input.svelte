<script>
	let array = [];
</script>

<style>
	.a + .e { color: green; }
	.a + .f { color: green; }
	.a + .g { color: green; }
	.b + .c { color: green; }
	.b + .d { color: green; }
	.c + .e { color: green; }
	.c + .f { color: green; }
	.c + .g { color: green; }
	.c + .k { color: green; }
	.d + .e { color: green; }
	.d + .f { color: green; }
	.e + .e { color: green; }
	.i + .j { color: green; }
	.g + .h + .j { color: green; }
	.g + .i + .j { color: green; }
	.g + .j { color: green; }
	.m + .m { color: green; }
	.m + .l { color: green; }
	.l + .m { color: green; }

	/* no match */
	.a + .c { color: red; }
	.b + .e { color: red; }
	.d + .d { color: red; }
	.e + .f { color: red; }
	.f + .f { color: red; }
	.g + .h + .i + .j { color: red; }
</style>

<div class="a"></div>

{#each array as a}
	<div class="b"></div>
	{#each array as b}
		<div class="c"></div>
	{:else}
		<div class="d"></div>
	{/each}
{/each}

{#each array as c}
	{#each array as d}
		<div class="e"></div>
	{/each}
{:else}
	<div class="f"></div>
{/each}

{#each array as item}
	<div class="g"></div>
	{#each array as item}
		{#each array as item}
			<div class="h"></div>
		{/each}
	{:else}
		<div class="i"></div>
	{/each}
	<div class="j"></div>
{/each}

<div class="k"></div>

{#each array as item}
	{#each array as item}
		<div class="l"></div>
	{:else}
		<div class="m"></div>
	{/each}
{/each}
