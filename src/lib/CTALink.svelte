<script>
	import { ChevronsRight } from "lucide-svelte";

    export let text = "";
</script>

<div class="flex flex-row items-start justify-start w-full gap-1 text-orange-600 hover:cursor-pointer hover:underline">
    <p class="font-semibold text-orange-600 text-md">{text}</p>
    <ChevronsRight color="#EA580C" size={24} />
</div>