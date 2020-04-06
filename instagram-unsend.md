# Instagram Bulk Unsend Delete Messages

1. Open Chrome Browser
2. Open [Instagram.com](https://instagram.com)
3. Press `F12`
4. Press `Ctrl + Shift + M` (Change the browser mode to phone mode (icon between the Elements Tab and Arrow))
5. Press Reload (`Ctrl + R`)
6. Open any chat and then see the link should be such as (https://www.instagram.com/direct/t/xxxx)
7. Now Copy the `InstagramHelper.js` file contents and paste it in `Console` tab
8. Run the followin code

```javascript

var igHelper  = new InstagramHelper();
igHelper.METHOD_NAME();

```

9. First of all we need to get the messages which we want to unsend.

```javascript

/**
     * Fetch the messages and its itemIds for fetching from currentPageIndex to maxPageIndex
     * @param {number} currentPageIndex starting page index to start fetching (default 0)
     * @param {number} maxPageIndex last page till which all the messages will be fetched (default 5)
     * @param {boolean} isAllMessages (default false) if true ignores currentPageIndex and maxPageIndex
     */
    getMessagesItemsArray(currentPageIndex, maxPageIndex, isAllMessages)

```
10. Call `ig.getMessagesItemsArray(0, 5, false);` to get 5 scroll pages messages.
> If you want to delete all the messages since the chat begin then call `ig.getMessagesItemsArray(0, 5, true);`

12. Now call `ig.deleteAllMessages(0);` to start deleting.

> [Video Demo](./assets/instagram_delete_unsend_messages.gif)

> Note: Instagram has a limit of unsending messages per day, so try daily.
