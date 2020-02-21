# Potential Loop at Runtime Warning

Message : `'<OnRender action>' changes the <Screen | Block>'s data, which triggers the on render event again. To avoid infinite rendering loops, don't change screen or block data in '<OnRender action>'.`

Cause : The OnRender event occurs every time the screen or block data changes. If you change the screen or block data inside the OnRender action, you will trigger the OnRender action again, causing an infinite loop.

Recommendation : Don't change screen or block data in the [OnRender](../../../develop/logic/screen-block-lifecycle-events.md#on-render%3E) action.

Message : `Refreshing '<Aggregate | Data Action>' in '<OnAfterFetch action>' triggers the on after fetch event again. To avoid an infinite loop, remove the refresh of '<Aggregate | Data Action>' from '<OnAfterFetch action>'.`

Cause : The OnAfterFetch action of an Aggregate or Data Action runs right after it finishes fetching data. If you refresh the Aggregate or Data Action inside its own OnAfterFetch action, it will start fetching data again and run the OnAfterFetch action afterwards, causing an infinite loop.

Recommendation : Remove the Aggregate or Data Action refresh from its own [OnAfterFetch](../../../develop/logic/screen-block-lifecycle-events.md#on-after-fetch%3E) action.

