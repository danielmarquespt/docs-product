---
tags: runtime-traditionalweb;
summary: Learn how to embed a native video player in your app.
---

# Video

Embeds a native video player.

Use Video as a powerful tool to engage users. However, remember to always show all essential information as text in the application.

 Note: if you want to stream videos from YouTube, Vimeo, or others, see the \[How to Add Video to Your Applications\]\(https://success.outsystems.com/Documentation/Development\_FAQs/How\_to\_Add\_Video\_to\_Your\_Applications\) article.

**How to use**

In the Interface tab of Service Studio, drag the Video block from the Toolbox into your application's screen. At the Properties tab define the source video file to embed. All other parameters such as controls or size are optional.

1. Drag the Video pattern from the toolbox into the preview.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-2.png%3E)

2. Set the SourceFile value:
   * If using an external source file, insert the file URL.

     ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-3.png%3E)

   * If using a local file, include the video in a module as a resource and use the runtime path:
     1. In the **Data** tab, right-click the **Resources** folder and select **Import Resource**.

        ![](../../../../../../.gitbook/assets/video-image-add-resource.png)

     2. Browse the video file and click **Open**.
     3. Go to the **Interface** tab and select the screen where you inserted the Video pattern.
     4. Select the Video pattern.
     5. In the **Properties** tab, click at the **SourceFile** field and type the runtime path `"Resources.video-file-name"`. See an example below:

        ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-runtime-path.png%3E)

## Input Parameters

The following table describes all the available input parameters:

| **Input Name** | **Description** | **Type** | **Mandatory** | **Default Value** |
| :--- | :--- | :--- | :--- | :--- |
| SourceFile | Insert the video file URL or the runtime path of the resource video file. | Text | True | none |
| Width | Width \(in pixel or percentage\) is added for the video, otherwise the original video Width is detected. | Text | False | "100%" |
| Height | Height \(in pixel or percentage\) is added for the video, otherwise the original video Height is detected. | Text | False | "100%" |
| Autoplay | If True, specifies that the video will start playing as soon as it is ready. | Boolean | False | False |
| Loop | If True, specifies that the video will restart playing as soon as it ends. | Boolean | False | False |
| Muted | If True, specifies that the audio of the video will be disabled. | Boolean | False | False |
| Controls | If False, disabled video controls. In case of mobile, the controls will always be enable. | Boolean | False | True |
| ExtendedClass | Add custom style classes to this Block. | Text | False | none |

## Layout and Classes

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-1.png%3E)

## Advanced Use Case

### Use custom Play and Pause buttons

1. Set a name to the Video pattern.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-4.png%3E)

2. Create Play and Pause actions on the screen.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-5.png%3E)

3. In the Logic tab, click on the OutSystems UI Web to go to the Video Folder.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-6.png%3E)

4. Drag the PlayVideo and PauseVideo actions inside the Play and Pause actions you created.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-7.png%3E)

5. For each server action, set the WidgetId parameter to the name of the Video pattern.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-image-8.png%3E)

6. Create the elements you want to act as buttons. You can also wrap icons around containers and set the OnClick to the Play and Pause actions.
7. Publish and test.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/ui/patterns/web/controls/images/video-gif-1.gif%3E)

## Notes

Autoplay parameter only works if Muted is set to True.

## Device Compatibility

In case of mobile, the controls will always be enabled.

