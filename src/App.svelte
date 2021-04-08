<script>
	import Timeline from "./Timeline.svelte";
	import Profile from "./Profile.svelte";

	import { onMount } from "svelte";
    let student = {anecdotes : [], events : [], Avatar : {formats : {thumbnail:{}}}};
    let baseUrl = "http://localhost:1337";
    onMount(async () => {
        const res = await fetch("http://localhost:1337/students/1");
        student = await res.json();
    });
</script>

<main>
	<Profile {student} {baseUrl}  />
	<Timeline {student} {baseUrl} />
</main>
