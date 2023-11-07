<template>
    <div id="app">
        <h1>DropZone</h1>
        <DropZone />
        <span class="file-info">File: {{ dropzoneFile.name }}</span>
    </div>
</template>

<script>
import DropZone from "./components/DropZone.vue";

export default {
    name: "App",
    components: {
        DropZone,
    },
};
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>
