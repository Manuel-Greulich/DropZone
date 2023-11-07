<template>
    <div class="dropzone">
        <span>Drag or Drop File</span>
        <span>OR</span>
        <label for="dropzoneFile">Select File</label>
        <input type="file" id="dropzoneFile" />
    </div>
</template>

<script>
export default {
    name: "HelloWorld",
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
