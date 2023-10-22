<script lang="ts">
    export let background:string;
    export let size: "small" | "large" = "large";

    $: height = size === "small" ? "65vh" : "30vh";
</script>

<div
    class="relative overflow-hidden flex justify-center items-center"
    style:min-height={height}
>
    <img
        src={background}
        class="absolute left-0 top-0 w-full h-full object-cover object-center"
        alt="backgorund"
    />

    <div class="content max-w-xl relative z-100">
        <slot />
    </div>
</div>