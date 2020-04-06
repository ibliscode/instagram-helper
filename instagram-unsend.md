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


<hr>
<hr>
<hr>
<hr>

### ~~Android App Instagram Unsender Bot~~

- ~~If you wish older version of app automation bot then follow the below instructions~~
> ~~Note: This following code for android bot is not maintained.~~

## ~~Instagram bulk Unsend message automating~~
~~*v1.5*~~
~~*Pishang Ujeniya*~~

~~This python script automates un send message task for all messages sent on instagram dm.
The script uses OpenCV image processing for getting mask of chat messages and using pyautogui windows supported library
mimics mouse pointer action of deleting messages.~~

## ~~Requirements and Tested on:~~
- ~~Windows 10~~
- ~~Python 3.7.3~~
- ~~[Nox Player Android Emulator](https://www.bignox.com/) version 6.3.0~~
- ~~[Tesseract](https://github.com/tesseract-ocr/tesseract/releases) needed by [pytesseract](https://github.com/madmaze/pytesseract)~~
- ~~[Follow this guide for installing in Windows](https://github.com/UB-Mannheim/tesseract/wiki)~~
- ~~[Nox Player Android Emulator](https://www.bignox.com/) version 6.3.0~~
- ~~Screen resolution of 1920 x 1080~~
- ~~After starting Nox player change the screen mode to portrait and~~
~~from *Nox player* > *Advanced Settings* > *Resolution Settings* > click on *Restore Window Size*
so that the Nox Player screen sets to center of your screen~~
- ~~Open the chat DM and run the script and switch to chat screen and press Start on prompt.~~
- ~~Change the value of `LOOPER` variable to the large number to delete more messages.~~
