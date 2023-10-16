8th November 2021, Monday

Today I while I was completing the task for uploading support request, I had to use `fileReader`, the API is provided in the browser and was fairly easy to use, just wasted some time figuring it out.

As I mentioned earlier using `fileReader` is fairly simple and even more easy in react where you don't need a form and you can handle validation using . For using `fileReader` first we need to make an object using the `fileReader`  constructor, after that you read the file with the preferred methods e.g: `.readAsText` .

After all that setup, you're provided with the `eventListeeners` like `onLoad` that triggers when the file is uploaded.