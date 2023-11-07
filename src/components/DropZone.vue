<template>
    <div
        @dragenter.prevent="toggleActive"
        @dragleave.prevent="toggleActive"
        @dragover.prevent
        @drop.prevent="toggleActive"
        :class="{ 'active-dropzone': active }"
        class="dropzone"
    >
        <span>Drag or Drop File</span>
        <span>OR</span>
        <label for="dropzoneFile">Select File</label>
        <input type="file" id="dropzoneFile" />
    </div>
</template>

<script>
import { ref } from "vue";

export default {
    name: "HelloWorld",

    setup() {
        const active = ref(false);

        const toggleActive = () => {
            active.value = !active.value;
        };

        return { active, toggleActive };
    },
};
</script>

<style scopedhnm>
.dropzone {
    width: 400px;
    height: 200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    row-gap: 16px;
    border: 2px dashed #41b883;
    background-color: #fff;
    transition: 0.3s ease all;
}

label {
    padding: 8px 12px;
    color: #fff;
    background-color: #41b883;
    transform: 0.3s ease all;
}

input {
    display: none;
}
</style>
