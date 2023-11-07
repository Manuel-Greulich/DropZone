<template>
    <div id="app">
        <h1>DropZone</h1>
        <DropZone />
        <span class="file-info">File: {{ dropzoneFile.name }}</span>
    </div>
</template>

<script>
import DropZone from "./components/DropZone.vue";
import { ref } from "vue";

export default {
    name: "App",
    components: {
        DropZone,
    },

    setup() {
        let dropzoneFile = ref("");

        return { dropzoneFile };
    },
};
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#app {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #f1f1f1;
}

h1 {
    font-size: 40px;
    margin-bottom: 32px;
}

.file-info {
    margin-top: 32px;
}
</style>
