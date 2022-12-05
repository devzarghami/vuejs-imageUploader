# vuejs-imageUploader
single &amp; multiple image uploader with drag and drop mode

![before upload](https://github.com/devzarghami/vuejs-imageUploader/blob/main/beforeUpload.PNG)

![uploading](https://github.com/devzarghami/vuejs-imageUploader/blob/main/uploading.PNG)


```html

<file-upload
    ref="fileUploader"
    :upload-url="fileUploader.url"
    :upload-key="fileUploader.key"
    :method="fileUploader.post"
    :files.sync="fileUploader.images"
    :max-file-size="fileUploader.fileSize"
    :label="fileUploader.label"
    :remove-on-fail="fileUploader.removeOnFail"
    :custom-class="fileUploader.customClass"
    :acceptFormats="fileUploader.acceptFormats"
    :file-type="fileUploader.fileType"
    :params="fileUploader.params"
    :auto-upload="fileUploader.autoUpload"
    :single-mode="false">
</file-upload>


```

```js
data: () => ({
    fileUploader: {
      url: "https://example.com/api/upload-file-api",
      key: 'file',
      label: 'Please select your file',
      fileSize: 20,
      removeOnFail:true,
      fileType: 'image',
      acceptFormats: ['.jpeg', '.jpg', '.png'],
      responseField: 'data',
      responseFieldID: 'data',
      customClass: 'uidUploadBox',
      method: 'post',
      autoUpload: false,
      params: {
        type: 'nationalCard',
        hash: null
      },
      images: [],
    },
  }),

```
### manual upload
If you have disabled the automatic upload mode, you should run the upload command using the following command

```js
await this.$refs.fileUploader.uploadFile();
```
