<template>
    <div style="border: solid 2px red;">
        <h3>File Uploader</h3>
        <input v-show="showNative" type="file" :name="name" @change="onFileChanged" :multiple="multiple" :accept="accept" />
    </div>
</template>

<script>
    export default {
        name: "ImageUploader",
        props: {
            name: { type: String, required: true },
            show: { type: Boolean, Default: false },
            multiple: { type: Boolean, default: false },
            accept: { type: String, default: "" },
            showNative: { type: Boolean, default: false }
        },
        watch: {
            show(value) {
                if (value) {
                    // Resets the file to let <onChange> event to work.
                    this.$el.value = "";

                    // Opens select file system dialog.
                    this.$el.click();

                    // Resets the show property (sync technique), in order to let the user to reopen the dialog.
                    this.$emit('update:show', false);
                }
            }
        },
        methods: {
            onFileChanged(event) {
                var files = event.target.files || event.dataTransfer.files;
                if (!files.length) {
                    return;
                }

                var formData = new FormData();

                // Maps the provided name to files.
                formData.append(this.name, this.multiple ? files : files[0]);

                console.log(formData);
                console.log(files);

                // Returns formData (which can be sent to the backend) and optional, the selected files (parent component may need some information about files).
                this.$emit("files", formData, files);
            }
        }
    }

</script>