# Instagram Helper Script
> Instagram Scripts for various tasks automation


This JavaScript has helper methods to perform various tasks automation.

### How to delete all messages?


1. Open Chrome Browser
2. Open [Instagram.com](https://instagram.com)
3. Press `F12` (Developer Tools) or `Ctrl+Shift+I`
4. Open any chat and then see the link should be such as (https://www.instagram.com/direct/t/xxxx)
5. Note and copy the last long numerical digits from link to some notepad.
6. Those digits is your chat thread Id.
7. Now Copy the `InstagramHelper.js` file contents and paste it in `Console` tab
8. Run the following code

```javascript

var ig  = new InstagramHelper();
ig.getAllMessageIds("your_chat_thread_Id");

```
9. After that you will see **getting messages...** displayed in the console window.
10. As soon as it says **All Messages fetched, No More messages to fetch**, run the following code.

```javascript

ig.deleteAllMessages("your_chat_thread_Id");

```

11. It will start unsending deleting the messages.
12. Deleting messages is kept intentionally slow because Instagram has limit to delete number of messages in per second.
> If we delete fastly then Instagram servers detects it as bot and then unsending is not allowed with the session temporarily, until you logout and relogin. So to avoid getting detected, we have kept a delay in the code to delete messages with specific interval of time.

13. As and when it says **All Messages Deleted** it has deleted all the messages in the chat.

> It is very tedious and time consuming process, but efficient and better than doing it manually. One can simply open a new chrome browser window and follow the simple steps and minimise it.

> I am trying to keep this script updated to latest Instagram codes, so as to not have any issues further.

### Star it!
If it worked for you, star it.

### Upcoming features !!!

1. Get list of media sent, and unsend selected medias only. (such as video, audio, photos).
