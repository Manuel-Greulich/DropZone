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
        <input type="file" id="dropzoneFile" class="dropzoneFile" />
    </div>
</template>

<script>
export default {
    name: "HelloWorld",
    data() {
        return {
            active: false,
        };
    },
    methods: {
        toggleActive() {
            this.active = !this.active;
        },
    },
};
</script>

<style scoped>
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

.active-dropzone {
    color: #fff;
    border-color: #fff;
    background-color: #41b883;
}

.active-dropzone label {
    background-color: #fff;
    color: #41b883;
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
